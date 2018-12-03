---
title: 'synchronizationSchema: filterOperators'
description: Lista de todos los operadores compatibles con los filtros de ámbito.
ms.openlocfilehash: 968abf6584868b2b0b5e664c59f14eebc780f151
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086331"
---
# <a name="synchronizationschema-filteroperators"></a><span data-ttu-id="a3da4-103">synchronizationSchema: filterOperators</span><span class="sxs-lookup"><span data-stu-id="a3da4-103">synchronizationSchema: filterOperators</span></span>

> <span data-ttu-id="a3da4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a3da4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a3da4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a3da4-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a3da4-106">Lista de todos los operadores compatibles con los [filtros de ámbito](../resources/synchronization-filter.md).</span><span class="sxs-lookup"><span data-stu-id="a3da4-106">List all operators supported in the [scoping filters](../resources/synchronization-filter.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="a3da4-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="a3da4-107">Permissions</span></span>
<span data-ttu-id="a3da4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a3da4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a3da4-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a3da4-110">Permission type</span></span>                        | <span data-ttu-id="a3da4-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a3da4-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="a3da4-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a3da4-112">Delegated (work or school account)</span></span>     |<span data-ttu-id="a3da4-113">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a3da4-113">Directory.ReadWrite.All</span></span>  |
|<span data-ttu-id="a3da4-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a3da4-114">Delegated (personal Microsoft account)</span></span> |<span data-ttu-id="a3da4-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a3da4-115">Not supported.</span></span>|
|<span data-ttu-id="a3da4-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a3da4-116">Application</span></span>                            |<span data-ttu-id="a3da4-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a3da4-117">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="a3da4-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a3da4-118">HTTP Request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /servicePrincipals/{id}/synchronization/jobs/{jobId}/schema/filterOperators
GET /servicePrincipals/{id}/synchronization/templates/{templateId}/schema/filterOperators
GET /applications/{id}/synchronization/templates/{templateId}/schema/filterOperators
```

## <a name="request-headers"></a><span data-ttu-id="a3da4-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a3da4-119">Request headers</span></span>

| <span data-ttu-id="a3da4-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="a3da4-120">Name</span></span>           | <span data-ttu-id="a3da4-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="a3da4-121">Type</span></span>    | <span data-ttu-id="a3da4-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3da4-122">Description</span></span>|
|:---------------|:--------|:-----------|
| <span data-ttu-id="a3da4-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="a3da4-123">Authorization</span></span>  | <span data-ttu-id="a3da4-124">string</span><span class="sxs-lookup"><span data-stu-id="a3da4-124">string</span></span>  | <span data-ttu-id="a3da4-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a3da4-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a3da4-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a3da4-127">Request body</span></span>

<span data-ttu-id="a3da4-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a3da4-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a3da4-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a3da4-129">Response</span></span>

<span data-ttu-id="a3da4-130">Si tiene éxito, este método devuelve una `200, OK` código de respuesta y un objeto de colección [filterOperatorSchema](../resources/synchronization-filteroperatorschema.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a3da4-130">If successful, this method returns a `200, OK` response code and a [filterOperatorSchema](../resources/synchronization-filteroperatorschema.md) collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a3da4-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a3da4-131">Example</span></span>

##### <a name="request"></a><span data-ttu-id="a3da4-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a3da4-132">Request</span></span>
<span data-ttu-id="a3da4-133">El siguiente es un ejemplo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="a3da4-133">The following is an example of a request.</span></span>
<!-- {
  "blockType": "request",
  "name": "synchronizationschema_filteroperators"
}-->
```http
GET https://graph.microsoft.com/beta/servicePrincipals/{id}/synchronization/jobs/{jobId}/schema/filterOperators
```

##### <a name="response"></a><span data-ttu-id="a3da4-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a3da4-134">Response</span></span>
<span data-ttu-id="a3da4-135">El siguiente es un ejemplo de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="a3da4-135">The following is an example of a response.</span></span>

><span data-ttu-id="a3da4-136">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="a3da4-136">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="a3da4-137">Se devolverán todas las propiedades en una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a3da4-137">All the properties will be returned in an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.filterOperatorSchema",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
        {
            "name": "EQUALS",
            "arity": "Binary",
            "multivaluedComparisonType": "All",
            "supportedAttributeTypes": [
                "String",
                "Integer"
            ]
        }
    ]
}
```
<!--
Below is the full response, which had to be redacted above as Markdown Scanner tool trips over "type" values containing 
non-string type names like "Integer" or "Boolean"

{
    "value": [
        {
            "name": "EQUALS",
            "arity": "Binary",
            "multivaluedComparisonType": "All",
            "supportedAttributeTypes": [
                "Integer",
                "String"
            ]
        },
        {
            "name": "IS FALSE",
            "arity": "Unary",
            "multivaluedComparisonType": "All",
            "supportedAttributeTypes": [
                "Boolean"
            ]
        },
        {
            "name": "IS NOT NULL",
            "arity": "Unary",
            "multivaluedComparisonType": "All",
            "supportedAttributeTypes": [
                "Integer",
                "String",
                "Binary",
                "Boolean"
            ]
        },
        {
            "name": "IS NULL",
            "arity": "Unary",
            "multivaluedComparisonType": "All",
            "supportedAttributeTypes": [
                "Integer",
                "String",
                "Binary",
                "Boolean"
            ]
        },
        {
            "name": "IS TRUE",
            "arity": "Unary",
            "multivaluedComparisonType": "All",
            "supportedAttributeTypes": [
                "Boolean"
            ]
        },
        {
            "name": "NOT EQUALS",
            "arity": "Binary",
            "multivaluedComparisonType": "All",
            "supportedAttributeTypes": [
                "Integer",
                "String"
            ]
        },
        {
            "name": "NOT REGEX MATCH",
            "arity": "Binary",
            "multivaluedComparisonType": "All",
            "supportedAttributeTypes": [
                "Integer",
                "String"
            ]
        },
        {
            "name": "REGEX MATCH",
            "arity": "Binary",
            "multivaluedComparisonType": "All",
            "supportedAttributeTypes": [
                "Integer",
                "String"
            ]
        }
    ]
}
-->
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "synchronizationSchema: filterOperators",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->