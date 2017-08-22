# <a name="list-groups"></a><span data-ttu-id="a125b-101">Enumerar grupos</span><span class="sxs-lookup"><span data-stu-id="a125b-101">List groups</span></span>

<span data-ttu-id="a125b-p101">Lista de todos los grupos disponibles en una organización, incluidos pero sin limitarse a ellos los grupos de Office 365. Se devuelven las [propiedades predeterminadas](../api/group_get.md#default-properties) de cada grupo.</span><span class="sxs-lookup"><span data-stu-id="a125b-p101">List all the groups available in an organization, including but not limited to Office 365 Groups. The [default properties](../api/group_get.md#default-properties) of each group are returned.</span></span>

<span data-ttu-id="a125b-104">Para enumerar únicamente grupos de Office 365 (también denominados grupos unificados), aplique un filtro en **groupTypes**:</span><span class="sxs-lookup"><span data-stu-id="a125b-104">To list only Office 365 Groups (aka unified groups), apply a filter on **groupTypes**:</span></span>
```
GET https://graph.microsoft.com/v1.0/groups?$filter=groupTypes/any(c:c+eq+'Unified')
```

<span data-ttu-id="a125b-105">Puede usar la opción de consulta de OData `$orderby` para ordenar grupos de una organización por el valor **displayName**, tal y como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a125b-105">You can use the OData query option `$orderby` to sort groups in an organization by the **displayName** values, as shown in the following example:</span></span>
```
GET https://graph.microsoft.com/v1.0/groups?$orderby=displayName
```


## <a name="prerequisites"></a><span data-ttu-id="a125b-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a125b-106">Prerequisites</span></span>
<span data-ttu-id="a125b-107">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Group.Read.All* o *Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="a125b-107">One of the following **scopes** is required to execute this API: *Group.Read.All* or *Group.ReadWrite.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="a125b-108">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a125b-108">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups
```
## <a name="optional-query-parameters"></a><span data-ttu-id="a125b-109">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a125b-109">Optional query parameters</span></span>
<span data-ttu-id="a125b-110">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a125b-110">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="a125b-111">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a125b-111">Request headers</span></span>
| <span data-ttu-id="a125b-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="a125b-112">Name</span></span>       | <span data-ttu-id="a125b-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="a125b-113">Type</span></span> | <span data-ttu-id="a125b-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a125b-114">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="a125b-115">Authorization</span><span class="sxs-lookup"><span data-stu-id="a125b-115">Authorization</span></span>  | <span data-ttu-id="a125b-116">string</span><span class="sxs-lookup"><span data-stu-id="a125b-116">string</span></span>  | <span data-ttu-id="a125b-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a125b-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a125b-119">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a125b-119">Request body</span></span>
<span data-ttu-id="a125b-120">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a125b-120">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a125b-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a125b-121">Response</span></span>

<span data-ttu-id="a125b-122">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [group](../resources/group.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a125b-122">If successful, this method returns a `200 OK` response code and collection of [group](../resources/group.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="a125b-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a125b-123">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a125b-124">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a125b-124">Request</span></span>
<span data-ttu-id="a125b-125">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a125b-125">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_groups"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups
```
##### <a name="response"></a><span data-ttu-id="a125b-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a125b-126">Response</span></span>
<span data-ttu-id="a125b-127">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a125b-127">Here is an example of the response.</span></span>

<span data-ttu-id="a125b-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Se devolverán las [propiedades predeterminadas](../api/group_get.md#default-properties) de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a125b-p103">Note: The response object shown here may be truncated for brevity. The [default properties](../api/group_get.md#default-properties) will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.group",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: xxx

 {
  "value": [
    {
      "id": "id-value",
      "description": "description-value",
      "displayName": "displayName-value",
      "groupTypes": [
        "groupTypes-value"
      ],
      "mail": "mail-value",
      "mailEnabled": true,
      "mailNickname": "mailNickname-value",
      "onPremisesLastSyncDateTime": "onPremisesLastSyncDateTime-value",
      "onPremisesSecurityIdentifier": "onPremisesSecurityIdentifier-value",
      "onPremisesSyncEnabled": true,
      "proxyAddresses": [
        "proxyAddresses-value"
      ],
      "securityEnabled": true,
      "visibility": "visibility-value"
    }
  ]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List groups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
