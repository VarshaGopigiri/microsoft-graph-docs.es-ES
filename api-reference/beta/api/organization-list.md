---
title: List organization
description: Recupera una lista de objetos organization.
localization_priority: Normal
ms.openlocfilehash: 7087ea0ef7e3885334b33d53416d5e4b6fc750a7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27882799"
---
# <a name="list-organization"></a><span data-ttu-id="06458-103">List organization</span><span class="sxs-lookup"><span data-stu-id="06458-103">List organization</span></span>

> <span data-ttu-id="06458-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="06458-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="06458-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="06458-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="06458-106">Recupera una lista de objetos organization.</span><span class="sxs-lookup"><span data-stu-id="06458-106">Retrieve a list of organization objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="06458-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="06458-107">Permissions</span></span>
<span data-ttu-id="06458-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="06458-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="06458-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="06458-110">Permission type</span></span>      | <span data-ttu-id="06458-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="06458-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="06458-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="06458-112">Delegated (work or school account)</span></span> | <span data-ttu-id="06458-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="06458-113">Not supported.</span></span>    |
|<span data-ttu-id="06458-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="06458-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="06458-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="06458-115">Not supported.</span></span>    |
|<span data-ttu-id="06458-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="06458-116">Application</span></span> | <span data-ttu-id="06458-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="06458-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="06458-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="06458-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /organization
```
## <a name="optional-query-parameters"></a><span data-ttu-id="06458-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="06458-119">Optional query parameters</span></span>
<span data-ttu-id="06458-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="06458-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="06458-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="06458-121">Request headers</span></span>
| <span data-ttu-id="06458-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="06458-122">Name</span></span>       | <span data-ttu-id="06458-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="06458-123">Type</span></span> | <span data-ttu-id="06458-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="06458-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="06458-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="06458-125">Authorization</span></span>  | <span data-ttu-id="06458-126">string</span><span class="sxs-lookup"><span data-stu-id="06458-126">string</span></span>  | <span data-ttu-id="06458-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="06458-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="06458-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="06458-129">Request body</span></span>
<span data-ttu-id="06458-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="06458-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="06458-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="06458-131">Response</span></span>

<span data-ttu-id="06458-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [organization](../resources/organization.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="06458-132">If successful, this method returns a `200 OK` response code and collection of [organization](../resources/organization.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="06458-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="06458-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="06458-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="06458-134">Request</span></span>
<span data-ttu-id="06458-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="06458-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_organization"
}-->
```http
GET https://graph.microsoft.com/beta/organization
```
##### <a name="response"></a><span data-ttu-id="06458-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="06458-136">Response</span></span>
<span data-ttu-id="06458-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="06458-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.organization",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 500

{
  "value": [
    {
      "assignedPlans": [
        {
          "assignedDateTime": "2016-10-19T10:37:00Z",
          "capabilityStatus": "capabilityStatus-value",
          "service": "service-value",
          "servicePlanId": "servicePlanId-value"
        }
      ],
      "businessPhones": [
        "businessPhones-value"
      ],
      "city": "city-value",
      "country": "country-value",
      "countryLetterCode": "countryLetterCode-value",
      "displayName": "displayName-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List organization",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
