---
title: Configurar la sincronización con los atributos de destino personalizado
description: Puede personalizar el esquema de sincronización para incluir los atributos personalizados que se definen en el directorio de destino. En este artículo se describe cómo personalizar una suscripción a la fuerza de ventas mediante la adición de un nuevo campo denominado `officeCode`. Configurar la sincronización de Azure Active Directory (AD Azure) a la fuerza de ventas, y para cada usuario, rellenará la `officeCode` campo fuerza de ventas con el valor de la `extensionAttribute10` campo en Azure AD.
ms.openlocfilehash: e043fa5e458a56312871567bb14598f9232e97eb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086308"
---
# <a name="configure-synchronization-with-custom-target-attributes"></a>Configurar la sincronización con los atributos de destino personalizado

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Puede personalizar el esquema de sincronización para incluir los atributos personalizados que se definen en el directorio de destino. En este artículo se describe cómo personalizar una suscripción a la fuerza de ventas mediante la adición de un nuevo campo denominado `officeCode`. Configurar la sincronización de Azure Active Directory (AD Azure) a la fuerza de ventas, y para cada usuario, rellenará la `officeCode` campo fuerza de ventas con el valor de la `extensionAttribute10` campo en Azure AD.

En este artículo se supone que ya se ha agregado una aplicación que admite la sincronización en su inquilino a través del [Portal de Azure](https://portal.azure.com), que conoce el nombre para mostrar de aplicación, y que tiene un símbolo (token) de autorización de Microsoft Graph. Para obtener información acerca de cómo obtener el símbolo (token) de autorización, vea [tokens de acceso Get para llamar a Microsoft Graph](https://developer.microsoft.com/graph/docs/concepts/auth_overview).

## <a name="find-the-service-principal-object-by-display-name"></a>Busque el objeto de entidad de seguridad de servicio por nombre para mostrar

En el ejemplo siguiente se muestra cómo buscar un objeto de entidad de seguridad de servicio con el nombre para mostrar fuerza de ventas.

```http
GET https://graph.microsoft.com/beta/servicePrincipals?$select=id,appId,displayName&$filter=startswith(displayName, 'salesforce')
Authorization: Bearer {Token}

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

El `{servicePrincipalId}` es `167e33e9-f80e-490e-b4d8-698d4a80fb3e`.


## <a name="list-synchronization-jobs-in-the-context-of-the-service-principal"></a>Lista de los trabajos de sincronización en el contexto de la entidad de seguridad de servicio 

En el ejemplo siguiente se muestra cómo obtener la `jobId` que necesita para que funcione con. Por lo general, la respuesta devuelve sólo un trabajo.

```http
GET https://graph.microsoft.com/beta/servicePrincipals/60443998-8cf7-4e61-b05c-a53b658cb5e1/synchronization/jobs
Authorization: Bearer {Token}

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

El `{jobId}` es `SfSandboxOutDelta.e4bbf44533ea4eabb17027f3a92e92aa`.


## <a name="get-the-synchronization-schema"></a>Obtener el esquema de sincronización
En el ejemplo siguiente se muestra cómo obtener el esquema de sincronización.

<!-- {
  "blockType": "request",
  "name": "get_synchronizationschema"
}-->
```http
GET https://graph.microsoft.com/beta/servicePrincipals/{servicePrincipalId}/synchronization/jobs/{jobId}/schema
Authorization: Bearer {Token}
```

>**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades en una llamada real.

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

## <a name="add-a-definition-for-the-officecode-attribute-and-a-mapping-between-attributes"></a>Agregue una definición para el atributo officeCode y una asignación entre atributos

Use un editor de texto sin formato de su elección (por ejemplo, [el Bloc de notas ++](https://notepad-plus-plus.org/) o [En línea del Editor de JSON](https://www.jsoneditoronline.org/)) para:

1. Agregar una [definición de atributos](synchronization-attributedefinition.md) para el `officeCode` atributo. 

    - En directorios, busque el directorio con el nombre salesforce.com y en la matriz del objeto, busque el un con nombre de **usuario**.
    - Agregue el atributo nuevo a la lista, especificando el nombre y tipo, tal como se muestra en el siguiente ejemplo.

2. Agregar una [asignación de atributos](synchronization-attributemapping.md) entre `officeCode` y `extensionAttribute10`.

    - En [synchronizationRules](synchronization-synchronizationrule.md), busque la regla que especifica Azure AD como el directorio de origen y Salesforce.com como el directorio de destino (`"sourceDirectoryName": "Azure Active Directory",   "targetDirectoryName": "salesforce.com"`).
    - En la [objectMappings](synchronization-objectmapping.md) de la regla, busque la asignación entre los usuarios (`"sourceObjectName": "User",   "targetObjectName": "User"`).
    - En la matriz [attributeMappings](synchronization-attributemapping.md) de la **objectMapping**, agregue una nueva entrada, tal como se muestra en el siguiente ejemplo.

```json
{  
    "directories": [
    {
        "id": "8ffa6169-f354-4751-9b77-9c00765be92d",
            "name": "salesforce.com",
            "objects": [
            {
                "attributes": [
                        {
                            "name": "officeCode",
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
        "name": "USER_OUTBOUND_USER",
        "objectMappings": [
            {
            "attributeMappings": [
                {
                    "source": {
                            "name": "extensionAttribute10",
                            "type": "Attribute"
                        },
                    "targetAttributeName": "officeCode"
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
    }
    ]
}
```

## <a name="save-the-modified-synchronization-schema"></a>Guarde el esquema de sincronización modificado

Cuando se guarda el esquema de sincronización actualizado, asegúrese de que incluye todo el esquema, incluidos los elementos no modificados. Esta solicitud reemplazará el esquema existente con el que se proporciona.

```http
PUT https://graph.microsoft.com/beta/servicePrincipals/{servicePrincipalId}/synchronization/jobs/{jobId}/schema
Authorization: Bearer {Token}
{
    "directories": [..],
    "synchronizationRules": [..]
}

HTTP/1.1 201 No Content
```

Si el esquema se ha guardado correctamente, en la siguiente iteración del trabajo de sincronización, se iniciará volver a procesar todas las cuentas en su Azure AD y las nuevas asignaciones se aplicará a todas las cuentas suministradas.
