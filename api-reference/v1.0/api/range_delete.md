# <a name="range-delete"></a><span data-ttu-id="e34c1-101">Range: delete</span><span class="sxs-lookup"><span data-stu-id="e34c1-101">Range: delete</span></span>

<span data-ttu-id="e34c1-102">Elimina las celdas asociadas al rango.</span><span class="sxs-lookup"><span data-stu-id="e34c1-102">Deletes the cells associated with the range.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e34c1-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e34c1-103">Prerequisites</span></span>
<span data-ttu-id="e34c1-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="e34c1-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="e34c1-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e34c1-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="e34c1-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e34c1-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names(<name>)/range/delete
POST /workbook/worksheets/{id|name}/range(<address>)/delete
POST /workbook/tables/{id|name}/columns/{id|name}/range/delete

```
## <a name="request-headers"></a><span data-ttu-id="e34c1-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e34c1-107">Request headers</span></span>
| <span data-ttu-id="e34c1-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="e34c1-108">Name</span></span>       | <span data-ttu-id="e34c1-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e34c1-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="e34c1-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="e34c1-110">Authorization</span></span>  | <span data-ttu-id="e34c1-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e34c1-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="e34c1-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e34c1-113">Request body</span></span>
<span data-ttu-id="e34c1-114">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="e34c1-114">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="e34c1-115">Parámetro</span><span class="sxs-lookup"><span data-stu-id="e34c1-115">Parameter</span></span>    | <span data-ttu-id="e34c1-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="e34c1-116">Type</span></span>   |<span data-ttu-id="e34c1-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="e34c1-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e34c1-118">Shift</span><span class="sxs-lookup"><span data-stu-id="e34c1-118">shift</span></span>|<span data-ttu-id="e34c1-119">string</span><span class="sxs-lookup"><span data-stu-id="e34c1-119">string</span></span>|<span data-ttu-id="e34c1-p102">Especifica hacia dónde se desplazarán las celdas.  Valores posibles: `Up`, `Left`.</span><span class="sxs-lookup"><span data-stu-id="e34c1-p102">Specifies which way to shift the cells.  Possible values are: `Up`, `Left`.</span></span>|

## <a name="response"></a><span data-ttu-id="e34c1-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e34c1-122">Response</span></span>

<span data-ttu-id="e34c1-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e34c1-p103">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e34c1-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e34c1-125">Example</span></span>
<span data-ttu-id="e34c1-126">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="e34c1-126">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="e34c1-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e34c1-127">Request</span></span>
<span data-ttu-id="e34c1-128">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e34c1-128">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_delete"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/delete
Content-type: application/json
Content-length: 28

{
  "shift": "shift-value"
}
```

##### <a name="response"></a><span data-ttu-id="e34c1-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e34c1-129">Response</span></span>
<span data-ttu-id="e34c1-130">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e34c1-130">Here is an example of the response.</span></span> 
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
  "description": "Range: delete",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->