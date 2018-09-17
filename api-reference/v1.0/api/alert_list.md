# <a name="list-alerts"></a><span data-ttu-id="06674-101">Alertas de lista</span><span class="sxs-lookup"><span data-stu-id="06674-101">List alerts</span></span>

<span data-ttu-id="06674-102">Recuperar una lista de objetos de [alerta](../resources/alert.md).</span><span class="sxs-lookup"><span data-stu-id="06674-102">Retrieve a list of nameditem objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="06674-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="06674-103">Permissions</span></span>

<span data-ttu-id="06674-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="06674-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="06674-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="06674-106">Permission type</span></span>      | <span data-ttu-id="06674-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="06674-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="06674-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="06674-108">Delegated (work or school account)</span></span> |  <span data-ttu-id="06674-109">SecurityEvents.Read.All, SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="06674-109">SecurityEvents.Read.All, SecurityEvents.ReadWrite.All</span></span>  |
|<span data-ttu-id="06674-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="06674-110">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="06674-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="06674-111">Not supported.</span></span>  |
|<span data-ttu-id="06674-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="06674-112">Application</span></span> | <span data-ttu-id="06674-113">SecurityEvents.Read.All, SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="06674-113">SecurityEvents.Read.All, SecurityEvents.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="06674-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="06674-114">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /security/alerts
GET /security/alerts?$top=1
GET /security/alerts?$filter={property} eq '{property-value}'
GET /security/alerts?$filter={property} eq '{property-value}'&$top=5
GET /security/alerts?$filter={property} eq '{property-value}'&{property} eq '{property-value}'
```

## <a name="optional-query-parameters"></a><span data-ttu-id="06674-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="06674-115">Optional query parameters</span></span>

<span data-ttu-id="06674-116">Este método admite los siguientes [parámetros de consulta de OData](../../../concepts/query_parameters.md) a modo de ayuda para personalizar la respuesta:</span><span class="sxs-lookup"><span data-stu-id="06674-116">This method supports the following [OData Query Parameters](../../../concepts/query_parameters.md) to help customize the response.</span></span>

- `$count`
- `$filter`
- `$orderby`
- `$select`
- `$skip`
- <span data-ttu-id="06674-117">`$top` devolverá los primeros resultados agregados para cada proveedor API de seguridad.</span><span class="sxs-lookup"><span data-stu-id="06674-117">`$top` will return the aggregated top results from each security API provider.</span></span>  

<span data-ttu-id="06674-118">Para usar un conjunto de propiedades alternativo, utilice el parámetro de consulta`$select` para especificar el conjunto de propiedades de **alerta** que quiere.</span><span class="sxs-lookup"><span data-stu-id="06674-118">To return an alternative property set, use the OData `$select` query parameter to specify the set of **alert** properties that you want.</span></span>  <span data-ttu-id="06674-119">Por ejemplo, para devolver las propiedades **assignedTo**, **category**, y **severity** añada lo siguiente a su consulta: `$select=assignedTo,category,severity`.</span><span class="sxs-lookup"><span data-stu-id="06674-119">For example, to return the **assignedTo**, **category**, and **severity** properties, add the following to your query: `$select=assignedTo,category,severity`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="06674-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="06674-120">Request headers</span></span>

| <span data-ttu-id="06674-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="06674-121">Name</span></span>      |<span data-ttu-id="06674-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="06674-122">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="06674-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="06674-123">Authorization</span></span>  | <span data-ttu-id="06674-p103">{código} del portador. Necesario.</span><span class="sxs-lookup"><span data-stu-id="06674-p103">Bearer {code}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="06674-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="06674-126">Request body</span></span>

<span data-ttu-id="06674-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="06674-127">Do not supply a request body for this method.</span></span> <span data-ttu-id="06674-128">Se pasará por alto el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="06674-128">The request body will be ignored.</span></span>

## <a name="response"></a><span data-ttu-id="06674-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="06674-129">Response</span></span>

<span data-ttu-id="06674-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos **alerta** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="06674-130">If successful, this method returns a `200 OK` response code and collection of **Attachment** objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="06674-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="06674-131">Example</span></span>

### <a name="request"></a><span data-ttu-id="06674-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="06674-132">Request</span></span>

<span data-ttu-id="06674-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="06674-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_alerts"
}-->

```http
GET https://graph.microsoft.com/v1.0/security/alerts
```

### <a name="response"></a><span data-ttu-id="06674-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="06674-134">Response</span></span>

<span data-ttu-id="06674-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="06674-135">The following is an example of the response.</span></span>

><span data-ttu-id="06674-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="06674-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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
