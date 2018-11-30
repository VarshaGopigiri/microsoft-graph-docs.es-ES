---
title: Configurar la sincronización con los atributos de extensión de Active directory
description: 'Puede personalizar el esquema de sincronización para incluir los atributos de extensión de Active directory de Azure Active Directory (AD Azure). En este artículo se describe cómo usar un atributo de extensión de Active directory (**extension_9d98asdfl15980a_Nickname**) para rellenar el valor de User.CommunityNickname en la fuerza de ventas. En este escenario, debe conectar de Azure AD configurado para aprovisionar un número de atributos de extensión de Active directory de Windows Server Active Directory local a Azure AD. '
ms.openlocfilehash: fa29e405b235107cd6773444085e7b409441c90e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089788"
---
# <a name="configure-synchronization-with-directory-extension-attributes"></a><span data-ttu-id="2730e-105">Configurar la sincronización con los atributos de extensión de Active directory</span><span class="sxs-lookup"><span data-stu-id="2730e-105">Configure synchronization with directory extension attributes</span></span>

> <span data-ttu-id="2730e-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2730e-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2730e-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2730e-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2730e-108">Puede personalizar el esquema de sincronización para incluir los atributos de extensión de Active directory de Azure Active Directory (AD Azure).</span><span class="sxs-lookup"><span data-stu-id="2730e-108">You can customize your synchronization schema to include Azure Active Directory (Azure AD) directory extension attributes.</span></span> <span data-ttu-id="2730e-109">En este artículo se describe cómo usar un atributo de extensión de Active directory (**extension_9d98asdfl15980a_Nickname**) para rellenar el valor de User.CommunityNickname en la fuerza de ventas.</span><span class="sxs-lookup"><span data-stu-id="2730e-109">This article describes how to use a directory extension attribute (**extension_9d98asdfl15980a_Nickname**) to populate the value of User.CommunityNickname in Salesforce.</span></span> <span data-ttu-id="2730e-110">En este escenario, debe conectar de Azure AD configurado para aprovisionar un número de atributos de extensión de Active directory de Windows Server Active Directory local a Azure AD.</span><span class="sxs-lookup"><span data-stu-id="2730e-110">In this scenario, you have Azure AD Connect set up to provision a number of directory extension attributes from Windows Server Active Directory on-premises to Azure AD.</span></span> 

<span data-ttu-id="2730e-111">En este artículo se supone que ya se ha agregado una aplicación que admite la sincronización en su inquilino a través del [Portal de Azure](https://portal.azure.com), que conoce el nombre para mostrar de aplicación, y que tiene un símbolo (token) de autorización de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="2730e-111">This article assumes that you have already added an application that supports synchronization to your tenant through the [Azure Portal](https://portal.azure.com), that you know the application display name, and that you have an authorization token for Microsoft Graph.</span></span> <span data-ttu-id="2730e-112">Para obtener información acerca de cómo obtener el símbolo (token) de autorización, vea [tokens de acceso Get para llamar a Microsoft Graph](https://developer.microsoft.com/graph/docs/concepts/auth_overview).</span><span class="sxs-lookup"><span data-stu-id="2730e-112">For information about how to get the authorization token, see [Get access tokens to call Microsoft Graph](https://developer.microsoft.com/graph/docs/concepts/auth_overview).</span></span>

## <a name="find-the-service-principal-object-by-display-name"></a><span data-ttu-id="2730e-113">Busque el objeto de entidad de seguridad de servicio por nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="2730e-113">Find the service principal object by display name</span></span>

<span data-ttu-id="2730e-114">En el ejemplo siguiente se muestra cómo buscar un objeto de entidad de seguridad de servicio con el nombre para mostrar "Recinto fuerza de ventas".</span><span class="sxs-lookup"><span data-stu-id="2730e-114">The following example shows how to find a service principal object with the display name "Salesforce Sandbox".</span></span>

```http
GET https://graph.microsoft.com/beta/servicePrincipals?$select=id,appId,displayName&$filter=startswith(displayName, 'salesforce')
Authorization: Bearer {Token}
```

```json
{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#servicePrincipals(id,appId,displayName)",
    "value": [
    {
        "id": "167e33e9-f80e-490e-b4d8-698d4a80fb3e",
        "appId": "cd3ed3de-93ee-400b-8b19-b61ef44a0f29",
        "displayName": "Salesforce"
    },
    {
        "id": "8cbbb70b-7290-42da-83ee-89fa3517a977",
        "appId": "b0f2e3b1-fe31-4658-b216-44dcaeabb63a",
        "displayName": "salesforce 1"
    },
    {
        "id": "60443998-8cf7-4e61-b05c-a53b658cb5e1",
        "appId": "79079396-c301-405d-900f-e2e0c2439a90",
        "displayName": "Salesforce Sandbox"
    }
    ]
}
```

<span data-ttu-id="2730e-115">El `{servicePrincipalId}` es `60443998-8cf7-4e61-b05c-a53b658cb5e1`.</span><span class="sxs-lookup"><span data-stu-id="2730e-115">The `{servicePrincipalId}` is `60443998-8cf7-4e61-b05c-a53b658cb5e1`.</span></span>

## <a name="list-synchronization-jobs-in-the-context-of-the-service-principal"></a><span data-ttu-id="2730e-116">Lista de los trabajos de sincronización en el contexto de la entidad de seguridad de servicio</span><span class="sxs-lookup"><span data-stu-id="2730e-116">List synchronization jobs in the context of the service principal</span></span> 

<span data-ttu-id="2730e-117">En el ejemplo siguiente se muestra cómo obtener la `jobId` que necesita para que funcione con.</span><span class="sxs-lookup"><span data-stu-id="2730e-117">The following example shows you how to get the `jobId` that you need to work with.</span></span> <span data-ttu-id="2730e-118">Por lo general, la respuesta devuelve sólo un trabajo.</span><span class="sxs-lookup"><span data-stu-id="2730e-118">Generally, the response returns only one job.</span></span>

```http
GET https://graph.microsoft.com/beta/servicePrincipals/60443998-8cf7-4e61-b05c-a53b658cb5e1/synchronization/jobs
Authorization: Bearer {Token}
```

```json
{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#servicePrincipals('60443998-8cf7-4e61-b05c-a53b658cb5e1')/synchronization/jobs",
    "value": [
        {
            "id": "SfSandboxOutDelta.e4bbf44533ea4eabb17027f3a92e92aa",
            "templateId": "SfSandboxOutDelta",
            "schedule": {},
            "status": {}
    }
    ]
}
```

<span data-ttu-id="2730e-119">El `{jobId}` es `SfSandboxOutDelta.e4bbf44533ea4eabb17027f3a92e92aa`.</span><span class="sxs-lookup"><span data-stu-id="2730e-119">The `{jobId}` is `SfSandboxOutDelta.e4bbf44533ea4eabb17027f3a92e92aa`.</span></span>

## <a name="find-the-name-of-the-directory-extension-attribute-you-need"></a><span data-ttu-id="2730e-120">Busque el nombre del atributo de extensión del directorio que necesita</span><span class="sxs-lookup"><span data-stu-id="2730e-120">Find the name of the directory extension attribute you need</span></span>

<span data-ttu-id="2730e-121">Necesitará el nombre completo del atributo de extensión.</span><span class="sxs-lookup"><span data-stu-id="2730e-121">You'll need the full name of the extension attribute.</span></span> <span data-ttu-id="2730e-122">Si no conoce el nombre completo (que debe tener un aspecto similar a **extension_9d98asdfl15980a_Nickname**), vea la siguiente información acerca de los atributos de extensión de Active directory y cómo inspeccionarlos:</span><span class="sxs-lookup"><span data-stu-id="2730e-122">If you don't know the full name (which should look similar to **extension_9d98asdfl15980a_Nickname**), see the following information about directory extension attributes and how to inspect them:</span></span> 

* [<span data-ttu-id="2730e-123">Extender el esquema de Active directory de Azure AD con propiedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="2730e-123">Extending the Azure AD directory schema with custom properties</span></span>](https://azure.microsoft.com/en-us/resources/samples/active-directory-dotnet-graphapi-directoryextensions-web/)
* [<span data-ttu-id="2730e-124">Extensiones de esquema de Active Directory | Conceptos de API de gráfico</span><span class="sxs-lookup"><span data-stu-id="2730e-124">Directory schema extensions | Graph API concepts</span></span>](https://msdn.microsoft.com/library/azure/ad/graph/howto/azure-ad-graph-api-directory-schema-extensions)


## <a name="get-the-synchronization-schema"></a><span data-ttu-id="2730e-125">Obtener el esquema de sincronización</span><span class="sxs-lookup"><span data-stu-id="2730e-125">Get the synchronization schema</span></span>
<span data-ttu-id="2730e-126">En el ejemplo siguiente se muestra cómo obtener el esquema de sincronización.</span><span class="sxs-lookup"><span data-stu-id="2730e-126">The following example shows how to get the synchronization schema.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_synchronizationschema"
}-->
```http
GET https://graph.microsoft.com/beta/servicePrincipals/{servicePrincipalId}/synchronization/jobs/{jobId}/schema
Authorization: Bearer {Token}
```

><span data-ttu-id="2730e-127">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="2730e-127">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="2730e-128">Se devolverán todas las propiedades en una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2730e-128">All the properties will be returned in an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.synchronizationSchema"
} -->
```http
HTTP/1.1 200 OK

{
  "directories": [
        {
              "id": "66e4a8cc-1b7b-435e-95f8-f06cea133828",
              "name": "Azure Active Directory",
              "objects": [
                {
                    "attributes": [
                        {
                          "anchor": true,
                          "caseExact": false,
                          "defaultValue": null,
                          "metadata": [],
                          "multivalued": false,
                          "mutability": "ReadWrite",
                          "name": "objectId",
                          "required": false,
                          "referencedObjects": [],
                          "type": "String"
                        },
                        {
                          "anchor": false,
                          "caseExact": false,
                          "defaultValue": null,
                          "metadata": [],
                          "multivalued": false,
                          "mutability": "ReadWrite",
                          "name": "streetAddress",
                          "required": false,
                          "referencedObjects": [],
                          "type": "String"
                        }
                    ],
                    "name": "User"
                }
             ]
        },
        {
              "id": "8ffa6169-f354-4751-9b77-9c00765be92d",
              "name": "salesforce.com",
              "objects": []
        }
  ],
 "synchronizationRules": [
        {
          "editable": true,
          "id": "4c5ecfa1-a072-4460-b1c3-4adde3479854",
          "name": "USER_OUTBOUND_USER",
          "objectMappings": [
                {
                    "attributeMappings": [
                            {
                              "defaultValue": "True",
                              "exportMissingReferences": false,
                              "flowBehavior": "FlowWhenChanged",
                              "flowType": "Always",
                              "matchingPriority": 0,
                              "source": {
                                "expression": "Not([IsSoftDeleted])",
                                "name": "Not",
                                "parameters": [
                                  {
                                    "key": "source",
                                    "value": {
                                      "expression": "[IsSoftDeleted]",
                                      "name": "IsSoftDeleted",
                                      "parameters": [],
                                      "type": "Attribute"
                                    }
                                  }
                                ],
                                "type": "Function"
                              },
                              "targetAttributeName": "IsActive"
                            }
                     ],
                    "enabled": true,
                    "flowTypes": "Add, Update, Delete",
                    "name": "Synchronize Azure Active Directory Users to salesforce.com",
                    "scope": null,
                    "sourceObjectName": "User",
                    "targetObjectName": "User"
            }]
        }]
}
```

## <a name="add-a-definition-for-the-directory-extension-attribute-and-a-mapping-between-the-attributes"></a><span data-ttu-id="2730e-129">Agregue una definición para el atributo de extensión de Active directory y una asignación entre los atributos</span><span class="sxs-lookup"><span data-stu-id="2730e-129">Add a definition for the directory extension attribute, and a mapping between the attributes</span></span>

<span data-ttu-id="2730e-130">Use un editor de texto sin formato de su elección (por ejemplo, [el Bloc de notas ++](https://notepad-plus-plus.org/) o [En línea del Editor de JSON](https://www.jsoneditoronline.org/)) para:</span><span class="sxs-lookup"><span data-stu-id="2730e-130">Use a plain text editor of your choice (for example, [Notepad++](https://notepad-plus-plus.org/) or [JSON Editor Online](https://www.jsoneditoronline.org/)) to:</span></span>

1. <span data-ttu-id="2730e-131">Agregar una [definición de atributos](synchronization-attributedefinition.md) para el `extension_9d98asdfl15980a_Nickname` atributo.</span><span class="sxs-lookup"><span data-stu-id="2730e-131">Add an [attribute definition](synchronization-attributedefinition.md) for the `extension_9d98asdfl15980a_Nickname` attribute.</span></span> 

    - <span data-ttu-id="2730e-132">En directorios, busque el directorio con el nombre "Azure Active Directory" y, en la matriz del objeto, busque el con nombre un **usuario**.</span><span class="sxs-lookup"><span data-stu-id="2730e-132">Under directories, find the directory with the name "Azure Active Directory", and in the object's array, find the one named **User**.</span></span>
    - <span data-ttu-id="2730e-133">Agregue el atributo nuevo a la lista, especificando el nombre y tipo, tal como se muestra en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="2730e-133">Add the new attribute to the list, specifying the name and type, as shown in the following example.</span></span>

2. <span data-ttu-id="2730e-134">Agregar una [asignación de atributos](synchronization-attributemapping.md) entre extension_9d98asdfl15980a_Nickname y CommunityNickname.</span><span class="sxs-lookup"><span data-stu-id="2730e-134">Add an [attribute mapping](synchronization-attributemapping.md) between extension_9d98asdfl15980a_Nickname and CommunityNickname.</span></span>

    - <span data-ttu-id="2730e-135">En [synchronizationRules](synchronization-synchronizationrule.md), busque la regla que especifica Azure AD como directorio de origen y Salesforce.com como el directorio de destino (`"sourceDirectoryName": "Azure Active Directory",   "targetDirectoryName": "salesforce.com"`).</span><span class="sxs-lookup"><span data-stu-id="2730e-135">Under [synchronizationRules](synchronization-synchronizationrule.md), find the rule that specifies Azure AD as source directory, and Salesforce.com as the target directory (`"sourceDirectoryName": "Azure Active Directory",   "targetDirectoryName": "salesforce.com"`).</span></span>
    - <span data-ttu-id="2730e-136">En la [objectMappings](synchronization-objectmapping.md) de la regla, busque la asignación entre los usuarios (`"sourceObjectName": "User",   "targetObjectName": "User"`).</span><span class="sxs-lookup"><span data-stu-id="2730e-136">In the [objectMappings](synchronization-objectmapping.md) of the rule, find the mapping between users (`"sourceObjectName": "User",   "targetObjectName": "User"`).</span></span>
    - <span data-ttu-id="2730e-137">En la matriz [attributeMappings](synchronization-attributemapping.md) de la **objectMapping**, agregue una nueva entrada, tal como se muestra en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="2730e-137">In the [attributeMappings](synchronization-attributemapping.md) array of the **objectMapping**, add a new entry, as shown in the following example.</span></span>

    ```json
    {
        "directories": [
            {
                "id": "66e4a8cc-1b7b-435e-95f8-f06cea133828",
                "name": "Azure Active Directory",
                "objects": [
                    {
                        "attributes": [
                                ,{
                                "name": "extension_9d98asdfl15980a_Nickname",
                                "type": "String"
                                }
                        ],
                        "name":"User"
                    }]
            }
        ],
        "synchronizationRules": [
            {
            "editable": true,
            "id": "4c5ecfa1-a072-4460-b1c3-4adde3479854",
            "metadata": [..],
            "name": "USER_OUTBOUND_USER",
            "objectMappings": [
                {
                    "attributeMappings": [
                    ,{
                        "source": {
                            "name": "extension_9d98asdfl15980a_Nickname",
                            "type": "Attribute"
                        },
                        "targetAttributeName": "CommunityNickname"
                        }
                ],
                "name": "Synchronize Azure Active Directory Users to salesforce.com",
                    "scope": null,
                    "sourceObjectName": "User",
                    "targetObjectName": "User"
                }
            ],
            "priority": 1,
            "sourceDirectoryName": "Azure Active Directory",
            "targetDirectoryName": "salesforce.com"
            },
        ]
    }
    ```

## <a name="save-the-modified-synchronization-schema"></a><span data-ttu-id="2730e-138">Guarde el esquema de sincronización modificado</span><span class="sxs-lookup"><span data-stu-id="2730e-138">Save the modified synchronization schema</span></span>

<span data-ttu-id="2730e-139">Cuando se guarda el esquema de sincronización actualizado, asegúrese de que incluye todo el esquema, incluidos los elementos no modificados.</span><span class="sxs-lookup"><span data-stu-id="2730e-139">When you save the updated synchronization schema, make sure that you include the entire schema, including the unmodified parts.</span></span> <span data-ttu-id="2730e-140">Esta solicitud reemplazará el esquema existente con el que se proporciona.</span><span class="sxs-lookup"><span data-stu-id="2730e-140">This request will replace the existing schema with the one that you provide.</span></span>

```http
PUT https://graph.microsoft.com/beta/servicePrincipals/{servicePrincipalId}/synchronization/jobs/{jobId}/schema
Authorization: Bearer {Token}
{
    "directories": [],
    "synchronizationRules": []
}

HTTP/1.1 201 No Content
```

<span data-ttu-id="2730e-141">Si el esquema se ha guardado correctamente, en la siguiente iteración del trabajo de sincronización, se iniciará volver a procesar todas las cuentas en su Azure AD y las nuevas asignaciones se aplicará a todas las cuentas suministradas.</span><span class="sxs-lookup"><span data-stu-id="2730e-141">If the schema was saved successfully, on the next iteration of the synchronization job, it will start re-processing all the accounts in your Azure AD, and the new mappings will be applied to all provisioned accounts.</span></span>