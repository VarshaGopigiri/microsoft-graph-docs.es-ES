---
title: Obtener synchronizationSchema
description: Recuperar el esquema para un trabajo de sincronización determinado o una plantilla.
localization_priority: Normal
ms.openlocfilehash: 768a35940593231bbc4fbd4c3f5498c7eb3243fd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27863472"
---
# <a name="get-synchronizationschema"></a><span data-ttu-id="3e3a7-103">Obtener synchronizationSchema</span><span class="sxs-lookup"><span data-stu-id="3e3a7-103">Get synchronizationSchema</span></span>

> <span data-ttu-id="3e3a7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3e3a7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3e3a7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3e3a7-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3e3a7-106">Recuperar el esquema para un trabajo de sincronización determinado o una plantilla.</span><span class="sxs-lookup"><span data-stu-id="3e3a7-106">Retrieve the schema for a given synchronization job or template.</span></span>

## <a name="permissions"></a><span data-ttu-id="3e3a7-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="3e3a7-107">Permissions</span></span>
<span data-ttu-id="3e3a7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3e3a7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3e3a7-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3e3a7-110">Permission type</span></span>                        | <span data-ttu-id="3e3a7-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3e3a7-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="3e3a7-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3e3a7-112">Delegated (work or school account)</span></span>     |<span data-ttu-id="3e3a7-113">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3e3a7-113">Directory.ReadWrite.All</span></span>  |
|<span data-ttu-id="3e3a7-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3e3a7-114">Delegated (personal Microsoft account)</span></span> |<span data-ttu-id="3e3a7-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3e3a7-115">Not supported.</span></span> |
|<span data-ttu-id="3e3a7-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3e3a7-116">Application</span></span>                            |<span data-ttu-id="3e3a7-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3e3a7-117">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="3e3a7-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3e3a7-118">HTTP Request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /servicePrincipals/{id}/synchronization/jobs/{jobId}/schema
GET /servicePrincipals/{id}/synchronization/templates/{templateId}/schema
GET /applications/{id}/synchronization/templates/{templateId}/schema
```

## <a name="request-headers"></a><span data-ttu-id="3e3a7-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3e3a7-119">Request headers</span></span>

| <span data-ttu-id="3e3a7-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="3e3a7-120">Name</span></span>           | <span data-ttu-id="3e3a7-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="3e3a7-121">Type</span></span>    | <span data-ttu-id="3e3a7-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="3e3a7-122">Description</span></span>|
|:---------------|:--------|:-----------|
| <span data-ttu-id="3e3a7-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="3e3a7-123">Authorization</span></span>  | <span data-ttu-id="3e3a7-124">string</span><span class="sxs-lookup"><span data-stu-id="3e3a7-124">string</span></span>  | <span data-ttu-id="3e3a7-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3e3a7-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="3e3a7-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3e3a7-127">Request body</span></span>

<span data-ttu-id="3e3a7-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3e3a7-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3e3a7-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3e3a7-129">Response</span></span>

<span data-ttu-id="3e3a7-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [synchronizationSchema](../resources/synchronization-synchronizationschema.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3e3a7-130">If successful, this method returns a `200 OK` response code and a [synchronizationSchema](../resources/synchronization-synchronizationschema.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3e3a7-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3e3a7-131">Example</span></span>

##### <a name="request"></a><span data-ttu-id="3e3a7-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3e3a7-132">Request</span></span>
<span data-ttu-id="3e3a7-133">El siguiente es un ejemplo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="3e3a7-133">The following is an example of a request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_synchronizationschema"
}-->
```http
GET https://graph.microsoft.com/beta/servicePrincipals/{id}/synchronization/jobs/{jobId}/schema
```

##### <a name="response"></a><span data-ttu-id="3e3a7-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3e3a7-134">Response</span></span>
<span data-ttu-id="3e3a7-135">El siguiente es un ejemplo de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="3e3a7-135">The following is an example of a response.</span></span>

><span data-ttu-id="3e3a7-136">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="3e3a7-136">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="3e3a7-137">Se devolverán todas las propiedades en una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3e3a7-137">All the properties will be returned in an actual call.</span></span>
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
                }
            ]
        },
        {
            "name": "Salesforce",
            "objects": [{}]
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
                        {}
                    ]
                },
                {}
            ]
        },
        {}
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get synchronizationSchema",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
