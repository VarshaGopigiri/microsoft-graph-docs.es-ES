# <a name="filter-apply"></a><span data-ttu-id="79b83-101">Filter: apply</span><span class="sxs-lookup"><span data-stu-id="79b83-101">Filter: apply</span></span>

<span data-ttu-id="79b83-102">Aplica los criterios de filtro especificados en la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="79b83-102">Apply the given filter criteria on the given column.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="79b83-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="79b83-103">Prerequisites</span></span>
<span data-ttu-id="79b83-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="79b83-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="79b83-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="79b83-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="79b83-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="79b83-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/columns/{id|name}/filter/apply
POST /workbook/worksheets/{id|name}/tables/{id|name}/columns/{id|name}/filter/apply

```
## <a name="request-headers"></a><span data-ttu-id="79b83-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="79b83-107">Request headers</span></span>
| <span data-ttu-id="79b83-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="79b83-108">Name</span></span>       | <span data-ttu-id="79b83-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="79b83-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="79b83-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="79b83-110">Authorization</span></span>  | <span data-ttu-id="79b83-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="79b83-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="79b83-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="79b83-113">Request body</span></span>
<span data-ttu-id="79b83-114">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="79b83-114">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="79b83-115">Parámetro</span><span class="sxs-lookup"><span data-stu-id="79b83-115">Parameter</span></span>    | <span data-ttu-id="79b83-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="79b83-116">Type</span></span>   |<span data-ttu-id="79b83-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="79b83-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="79b83-118">criterios</span><span class="sxs-lookup"><span data-stu-id="79b83-118">criteria</span></span>|<span data-ttu-id="79b83-119">FilterCriteria</span><span class="sxs-lookup"><span data-stu-id="79b83-119">FilterCriteria</span></span>|<span data-ttu-id="79b83-120">Criterios que se aplicarán.</span><span class="sxs-lookup"><span data-stu-id="79b83-120">The criteria to apply.</span></span>|

## <a name="response"></a><span data-ttu-id="79b83-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="79b83-121">Response</span></span>

<span data-ttu-id="79b83-p102">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="79b83-p102">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="79b83-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="79b83-124">Example</span></span>
<span data-ttu-id="79b83-125">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="79b83-125">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="79b83-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="79b83-126">Request</span></span>
<span data-ttu-id="79b83-127">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="79b83-127">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "filter_apply"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/columns/{id|name}/filter/apply
Content-type: application/json
Content-length: 321

{
  "criteria": {
    "criterion1": "criterion1-value",
    "criterion2": "criterion2-value",
    "color": "color-value",
    "operator": {
    },
    "icon": {
      "set": "set-value",
      "index": 99
    },
    "dynamicCriteria": "dynamicCriteria-value",
    "values": {
    },
    "filterOn": "filterOn-value"
  }
}
```

##### <a name="response"></a><span data-ttu-id="79b83-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="79b83-128">Response</span></span>
<span data-ttu-id="79b83-129">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="79b83-129">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.none"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Filter: apply",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->