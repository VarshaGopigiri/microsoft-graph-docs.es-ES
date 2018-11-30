---
title: Actualizar synchronizationSchema
description: Actualizar el esquema de sincronización para un determinado trabajo o una plantilla. Este método reemplaza totalmente el esquema actual con el proporcionado en la solicitud. Para actualizar el esquema de una plantilla, realizar la llamada en el objeto application. Debe ser el propietario de la aplicación.
ms.openlocfilehash: 18ad164f0f1860ce954a9d4e1170f71e47f513b5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088678"
---
# <a name="update-synchronizationschema"></a><span data-ttu-id="24391-106">Actualizar synchronizationSchema</span><span class="sxs-lookup"><span data-stu-id="24391-106">Update synchronizationSchema</span></span>

> <span data-ttu-id="24391-107">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="24391-107">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="24391-108">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="24391-108">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="24391-109">Actualizar el esquema de sincronización para un determinado trabajo o una plantilla.</span><span class="sxs-lookup"><span data-stu-id="24391-109">Update the synchronization schema for a given job or template.</span></span> <span data-ttu-id="24391-110">Este método reemplaza totalmente el esquema actual con el proporcionado en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="24391-110">This method fully replaces the current schema with the one provided in the request.</span></span> <span data-ttu-id="24391-111">Para actualizar el esquema de una plantilla, realizar la llamada en el objeto application.</span><span class="sxs-lookup"><span data-stu-id="24391-111">To update the schema of a template, make the call on the application object.</span></span> <span data-ttu-id="24391-112">Debe ser el propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="24391-112">You must be the owner of the application.</span></span>

## <a name="permissions"></a><span data-ttu-id="24391-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="24391-113">Permissions</span></span>
<span data-ttu-id="24391-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="24391-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="24391-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="24391-116">Permission type</span></span>                        | <span data-ttu-id="24391-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="24391-117">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="24391-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="24391-118">Delegated (work or school account)</span></span>     |<span data-ttu-id="24391-119">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="24391-119">Directory.ReadWrite.All</span></span>  |
|<span data-ttu-id="24391-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="24391-120">Delegated (personal Microsoft account)</span></span> |<span data-ttu-id="24391-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="24391-121">Not supported.</span></span>|
|<span data-ttu-id="24391-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="24391-122">Application</span></span>                            |<span data-ttu-id="24391-123">No admitida.</span><span class="sxs-lookup"><span data-stu-id="24391-123">Not supported.</span></span>| 

## <a name="http-request"></a><span data-ttu-id="24391-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="24391-124">HTTP Request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PUT /servicePrincipals/{id}/synchronization/jobs/{jobId}/schema
PUT /applications/{id}/synchronization/templates/{templateId}/schema
```

## <a name="request-headers"></a><span data-ttu-id="24391-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="24391-125">Request headers</span></span>

| <span data-ttu-id="24391-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="24391-126">Name</span></span>           | <span data-ttu-id="24391-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="24391-127">Type</span></span>    | <span data-ttu-id="24391-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="24391-128">Description</span></span>|
|:---------------|:--------|:-----------|
| <span data-ttu-id="24391-129">Authorization</span><span class="sxs-lookup"><span data-stu-id="24391-129">Authorization</span></span>  | <span data-ttu-id="24391-130">string</span><span class="sxs-lookup"><span data-stu-id="24391-130">string</span></span>  | <span data-ttu-id="24391-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="24391-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="24391-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="24391-133">Request body</span></span>

<span data-ttu-id="24391-134">En el cuerpo de la solicitud, proporcione el objeto [synchronizationSchema](../resources/synchronization-synchronizationschema.md) que va a reemplazar el esquema existente con.</span><span class="sxs-lookup"><span data-stu-id="24391-134">In the request body, supply the [synchronizationSchema](../resources/synchronization-synchronizationschema.md) object to replace the existing schema with.</span></span>

## <a name="response"></a><span data-ttu-id="24391-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="24391-135">Response</span></span>

<span data-ttu-id="24391-136">Si se realiza correctamente, devuelve un `204 No Content` código de respuesta.</span><span class="sxs-lookup"><span data-stu-id="24391-136">If successful, returns a `204 No Content` response code.</span></span> <span data-ttu-id="24391-137">No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="24391-137">It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="24391-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="24391-138">Example</span></span>

##### <a name="request"></a><span data-ttu-id="24391-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="24391-139">Request</span></span>
<span data-ttu-id="24391-140">El siguiente es un ejemplo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="24391-140">The following is an example of a request.</span></span>

><span data-ttu-id="24391-141">**Nota:** El objeto de solicitud que se muestra aquí es más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="24391-141">**Note:** The request object shown here is shortened for readability.</span></span> <span data-ttu-id="24391-142">Proporcionar todas las propiedades en una llamada real.</span><span class="sxs-lookup"><span data-stu-id="24391-142">Supply all the properties in an actual call.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_synchronizationschema"
}-->
```http
PUT https://graph.microsoft.com/beta/servicePrincipals/{id}/synchronization/jobs/{jobId}/schema

{
    "directories": [
        {
            "name": "Azure Active Directory",
            "objects": [
                {
                    "name": "User",
                    "attributes": [
                        {
                            "name": "userPrincipalName",
                            "type": "string"
                        }
                    ]
                },
            ]
        },
        {
            "name": "Salesforce",
        }
    ],
    "synchronizationRules":[
        {
            "name": "USER_TO_USER",
            "sourceDirectoryName": "Azure Active Directory",
            "targetDirectoryName": "Salesforce",
            "objectMappings": [
                {
                    "sourceObjectName": "User",
                    "targetObjectName": "User",
                    "attributeMappings": [
                        {
                            "source": {},
                            "targetAttributeName": "userName"
                        },
                    ]
                },
            ]
        },
    ]
}

```

##### <a name="response"></a><span data-ttu-id="24391-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="24391-143">Response</span></span>
<span data-ttu-id="24391-144">El siguiente es un ejemplo de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="24391-144">The following is an example of a response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.synchronizationSchema"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update synchronizationschema",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->