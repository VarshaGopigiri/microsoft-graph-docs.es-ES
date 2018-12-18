---
title: List alerts
description: Recuperar una lista de los objetos de alerta.
author: Preetikr
ms.openlocfilehash: 64589fa04d4b6b11fb2ec435f6531df2e2f58a8a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27324034"
---
# <a name="list-alerts"></a><span data-ttu-id="9918d-103">List alerts</span><span class="sxs-lookup"><span data-stu-id="9918d-103">List alerts</span></span>

<span data-ttu-id="9918d-104">Recuperar una lista de objetos de [alerta](../resources/alert.md) .</span><span class="sxs-lookup"><span data-stu-id="9918d-104">Retrieve a list of [alert](../resources/alert.md) objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="9918d-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="9918d-105">Permissions</span></span>

<span data-ttu-id="9918d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9918d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9918d-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9918d-108">Permission type</span></span>      | <span data-ttu-id="9918d-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9918d-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9918d-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9918d-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="9918d-111">SecurityEvents.Read.All, SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9918d-111">SecurityEvents.Read.All, SecurityEvents.ReadWrite.All</span></span>  |
|<span data-ttu-id="9918d-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9918d-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="9918d-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9918d-113">Not supported.</span></span>  |
|<span data-ttu-id="9918d-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9918d-114">Application</span></span> | <span data-ttu-id="9918d-115">SecurityEvents.Read.All, SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9918d-115">SecurityEvents.Read.All, SecurityEvents.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="9918d-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9918d-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /security/alerts
GET /security/alerts?$top=1
GET /security/alerts?$filter={property} eq '{property-value}'
GET /security/alerts?$filter={property} eq '{property-value}'&$top=5
GET /security/alerts?$filter={property} eq '{property-value}'&{property} eq '{property-value}'
```

## <a name="optional-query-parameters"></a><span data-ttu-id="9918d-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="9918d-117">Optional query parameters</span></span>

<span data-ttu-id="9918d-118">Este método admite los siguientes [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta:</span><span class="sxs-lookup"><span data-stu-id="9918d-118">This method supports the following [OData query parameters](/graph/query-parameters) to help customize the response:</span></span>

- `$count`
- `$filter`
- `$orderby`
- `$select`
- `$skip`
- <span data-ttu-id="9918d-119">`$top`devolverá los primeros resultados agregados de cada proveedor de API de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9918d-119">`$top` will return the aggregated top results from each security API provider.</span></span>  

<span data-ttu-id="9918d-120">Para devolver un conjunto de propiedades alternativo, utilice la OData `$select` parámetro para especificar el conjunto de propiedades de la **alerta** que desee de la consulta.</span><span class="sxs-lookup"><span data-stu-id="9918d-120">To return an alternative property set, use the OData `$select` query parameter to specify the set of **alert** properties that you want.</span></span>  <span data-ttu-id="9918d-121">Por ejemplo, para devolver el **assignedTo**, **categoría**y propiedades de **gravedad** , agregue lo siguiente a la consulta: `$select=assignedTo,category,severity`.</span><span class="sxs-lookup"><span data-stu-id="9918d-121">For example, to return the **assignedTo**, **category**, and **severity** properties, add the following to your query: `$select=assignedTo,category,severity`.</span></span>

> <span data-ttu-id="9918d-122">**Nota:** `$top` tiene un límite de 1000 alertas y una combinación de `$top`  +  `$skip` no puede superar los 6000 alertas.</span><span class="sxs-lookup"><span data-stu-id="9918d-122">**Note:** `$top` has a limit of 1000 alerts, and a combination of `$top` + `$skip` cannot exceed 6000 alerts.</span></span> <span data-ttu-id="9918d-123">Por ejemplo, `/security/alerts?$top=10&$skip=5990` devolverá un `200 OK` código de respuesta, pero `/security/alerts?$top=10&$skip=5991` devolverá un `400 Bad Request` código de respuesta.</span><span class="sxs-lookup"><span data-stu-id="9918d-123">For example, `/security/alerts?$top=10&$skip=5990` will return a `200 OK` response code, but `/security/alerts?$top=10&$skip=5991` will return a `400 Bad Request` response code.</span></span>  <span data-ttu-id="9918d-124">Para obtener más información, vea [respuestas de error de la API de seguridad de Microsoft Graph](../resources/security-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9918d-124">For more information, see [Microsoft Graph Security API error responses](../resources/security-error-codes.md).</span></span>

## <a name="request-headers"></a><span data-ttu-id="9918d-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9918d-125">Request headers</span></span>

| <span data-ttu-id="9918d-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="9918d-126">Name</span></span>      |<span data-ttu-id="9918d-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="9918d-127">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="9918d-128">Autorización</span><span class="sxs-lookup"><span data-stu-id="9918d-128">Authorization</span></span>  | <span data-ttu-id="9918d-p104">{código} del portador. Necesario.</span><span class="sxs-lookup"><span data-stu-id="9918d-p104">Bearer {code}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="9918d-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9918d-131">Request body</span></span>

<span data-ttu-id="9918d-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9918d-132">Do not supply a request body for this method.</span></span> <span data-ttu-id="9918d-133">Se pasará por alto el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9918d-133">The request body will be ignored.</span></span>

## <a name="response"></a><span data-ttu-id="9918d-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9918d-134">Response</span></span>

<span data-ttu-id="9918d-135">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de **alerta** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9918d-135">If successful, this method returns a `200 OK` response code and collection of **alert** objects in the response body.</span></span> <span data-ttu-id="9918d-136">Si se devuelve un código de estado que no sea 2xx o 404 desde un proveedor o un proveedor de tiempo de espera, la respuesta será un `206 Partial Content` código de estado con la respuesta del proveedor en un encabezado de advertencia.</span><span class="sxs-lookup"><span data-stu-id="9918d-136">If a status code other than 2xx or 404 is returned from a provider or if a provider times out, the response will be a `206 Partial Content` status code with the provider's response in a warning header.</span></span> <span data-ttu-id="9918d-137">Para obtener más información, vea [respuestas de error de la API de seguridad de Microsoft Graph](../resources/security-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9918d-137">For more information, see [Microsoft Graph Security API error responses](../resources/security-error-codes.md).</span></span>

## <a name="example"></a><span data-ttu-id="9918d-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9918d-138">Example</span></span>

### <a name="request"></a><span data-ttu-id="9918d-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9918d-139">Request</span></span>

<span data-ttu-id="9918d-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9918d-140">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_alerts"
}-->

```http
GET https://graph.microsoft.com/v1.0/security/alerts
```

### <a name="response"></a><span data-ttu-id="9918d-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9918d-141">Response</span></span>

<span data-ttu-id="9918d-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9918d-142">The following is an example of the response.</span></span>

><span data-ttu-id="9918d-p107">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9918d-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.alert",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "activityGroupName": "activityGroupName-value",
      "assignedTo": "assignedTo-value",
      "azureSubscriptionId": "azureSubscriptionId-value",
      "azureTenantId": "azureTenantId-value",
      "category": "category-value",
      "closedDateTime": "datetime-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List alerts",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
