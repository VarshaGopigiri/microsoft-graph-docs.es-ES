---
title: List alerts
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: cd41c3c896c4c97d2090c2a43561c04510c771f9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084098"
---
# <a name="list-alerts"></a><span data-ttu-id="3ad09-104">List alerts</span><span class="sxs-lookup"><span data-stu-id="3ad09-104">List alerts</span></span>

 > <span data-ttu-id="3ad09-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3ad09-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3ad09-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3ad09-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3ad09-107">Recuperar una lista de objetos de [alerta](../resources/alert.md) .</span><span class="sxs-lookup"><span data-stu-id="3ad09-107">Retrieve a list of [alert](../resources/alert.md) objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="3ad09-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="3ad09-108">Permissions</span></span>

<span data-ttu-id="3ad09-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3ad09-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3ad09-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3ad09-111">Permission type</span></span>      | <span data-ttu-id="3ad09-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3ad09-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3ad09-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3ad09-113">Delegated (work or school account)</span></span> |  <span data-ttu-id="3ad09-114">SecurityEvents.Read.All, SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3ad09-114">SecurityEvents.Read.All, SecurityEvents.ReadWrite.All</span></span>  |
|<span data-ttu-id="3ad09-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3ad09-115">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="3ad09-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3ad09-116">Not supported.</span></span>  |
|<span data-ttu-id="3ad09-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3ad09-117">Application</span></span> | <span data-ttu-id="3ad09-118">SecurityEvents.Read.All, SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3ad09-118">SecurityEvents.Read.All, SecurityEvents.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="3ad09-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3ad09-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /security/alerts
GET /security/alerts?$top=1
GET /security/alerts?$filter={property} eq '{property-value}'
GET /security/alerts?$filter={property} eq '{property-value}'&$top=5
GET /security/alerts?$filter={property} eq '{property-value}'&{property} eq '{property-value}'
```

## <a name="optional-query-parameters"></a><span data-ttu-id="3ad09-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="3ad09-120">Optional query parameters</span></span>

<span data-ttu-id="3ad09-121">Este método admite los siguientes [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta:</span><span class="sxs-lookup"><span data-stu-id="3ad09-121">This method supports the following [OData query parameters](/graph/query-parameters) to help customize the response:</span></span>

- `$count`
- `$filter`
- `$orderby`
- `$select`
- `$skip`
- <span data-ttu-id="3ad09-122">`$top`devolverá los primeros resultados agregados de cada proveedor de API de seguridad.</span><span class="sxs-lookup"><span data-stu-id="3ad09-122">`$top` will return the aggregated top results from each security API provider.</span></span>  

<span data-ttu-id="3ad09-123">Para devolver un conjunto de propiedades alternativo, utilice la OData `$select` parámetro para especificar el conjunto de propiedades de la **alerta** que desee de la consulta.</span><span class="sxs-lookup"><span data-stu-id="3ad09-123">To return an alternative property set, use the OData `$select` query parameter to specify the set of **alert** properties that you want.</span></span>  <span data-ttu-id="3ad09-124">Por ejemplo, para devolver el **assignedTo**, **categoría**y propiedades de **gravedad** , agregue lo siguiente a la consulta: `$select=assignedTo,category,severity`.</span><span class="sxs-lookup"><span data-stu-id="3ad09-124">For example, to return the **assignedTo**, **category**, and **severity** properties, add the following to your query: `$select=assignedTo,category,severity`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="3ad09-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3ad09-125">Request headers</span></span>

| <span data-ttu-id="3ad09-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="3ad09-126">Name</span></span>      |<span data-ttu-id="3ad09-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ad09-127">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="3ad09-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="3ad09-128">Authorization</span></span>  | <span data-ttu-id="3ad09-p105">{código} del portador. Necesario.</span><span class="sxs-lookup"><span data-stu-id="3ad09-p105">Bearer {code}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="3ad09-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3ad09-131">Request body</span></span>

<span data-ttu-id="3ad09-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3ad09-132">Do not supply a request body for this method.</span></span> <span data-ttu-id="3ad09-133">Se pasará por alto el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3ad09-133">The request body will be ignored.</span></span>

## <a name="response"></a><span data-ttu-id="3ad09-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3ad09-134">Response</span></span>

<span data-ttu-id="3ad09-135">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de **alerta** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3ad09-135">If successful, this method returns a `200 OK` response code and collection of **alert** objects in the response body.</span></span> <span data-ttu-id="3ad09-136">Si se devuelve un código de estado que no sea 2xx o 404 desde un proveedor o un proveedor de tiempo de espera, la respuesta será un `206 Partial Content` código de estado con la respuesta de proveedores en un encabezado de advertencia.</span><span class="sxs-lookup"><span data-stu-id="3ad09-136">If a status code other than 2xx or 404 is returned from a provider or if a provider times out, the response will be a `206 Partial Content` status code with the providers response in a warning header.</span></span> <span data-ttu-id="3ad09-137">Para obtener más información, vea [respuestas de error de la API de seguridad de Microsoft Graph](../resources/security-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3ad09-137">For more information, see [Microsoft Graph Security API error responses](../resources/security-error-codes.md).</span></span>

## <a name="example"></a><span data-ttu-id="3ad09-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3ad09-138">Example</span></span>

### <a name="request"></a><span data-ttu-id="3ad09-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3ad09-139">Request</span></span>

<span data-ttu-id="3ad09-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3ad09-140">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_alerts"
}-->

```http
GET https://graph.microsoft.com/beta/security/alerts
```

### <a name="response"></a><span data-ttu-id="3ad09-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3ad09-141">Response</span></span>

<span data-ttu-id="3ad09-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3ad09-142">The following is an example of the response.</span></span> 

><span data-ttu-id="3ad09-p108">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3ad09-p108">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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
