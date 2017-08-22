# <a name="worksheetcollection-add"></a><span data-ttu-id="5a3f3-101">WorksheetCollection: add</span><span class="sxs-lookup"><span data-stu-id="5a3f3-101">WorksheetCollection: add</span></span>

<span data-ttu-id="5a3f3-p101">Agrega una nueva hoja al libro. La hoja de cálculo se agregará al final de las hojas de cálculo existentes. Si desea activar la hoja de cálculo recién agregada, llame en ella a ".activate().</span><span class="sxs-lookup"><span data-stu-id="5a3f3-p101">Adds a new worksheet to the workbook. The worksheet will be added at the end of existing worksheets. If you wish to activate the newly added worksheet, call ".activate() on it.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5a3f3-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5a3f3-105">Prerequisites</span></span>
<span data-ttu-id="5a3f3-106">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="5a3f3-106">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="5a3f3-107">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5a3f3-107">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="5a3f3-108">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5a3f3-108">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/

```
## <a name="request-headers"></a><span data-ttu-id="5a3f3-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5a3f3-109">Request headers</span></span>
| <span data-ttu-id="5a3f3-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="5a3f3-110">Name</span></span>       | <span data-ttu-id="5a3f3-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5a3f3-111">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="5a3f3-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="5a3f3-112">Authorization</span></span>  | <span data-ttu-id="5a3f3-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5a3f3-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="5a3f3-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5a3f3-115">Request body</span></span>
<span data-ttu-id="5a3f3-116">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="5a3f3-116">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="5a3f3-117">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5a3f3-117">Parameter</span></span>    | <span data-ttu-id="5a3f3-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="5a3f3-118">Type</span></span>   |<span data-ttu-id="5a3f3-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="5a3f3-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5a3f3-120">name</span><span class="sxs-lookup"><span data-stu-id="5a3f3-120">name</span></span>|<span data-ttu-id="5a3f3-121">string</span><span class="sxs-lookup"><span data-stu-id="5a3f3-121">string</span></span>|<span data-ttu-id="5a3f3-p103">Opcional. Nombre de la hoja de cálculo que se va a agregar. Si se especifica, el nombre debe ser único. Si no se especifica, Excel determina el nombre de la nueva hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="5a3f3-p103">Optional. The name of the worksheet to be added. If specified, name should be unqiue. If not specified, Excel determines the name of the new worksheet.</span></span>|

## <a name="response"></a><span data-ttu-id="5a3f3-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5a3f3-126">Response</span></span>

<span data-ttu-id="5a3f3-127">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [Worksheet](../resources/worksheet.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5a3f3-127">If successful, this method returns `200, OK` response code and [Worksheet](../resources/worksheet.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5a3f3-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5a3f3-128">Example</span></span>
<span data-ttu-id="5a3f3-129">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="5a3f3-129">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="5a3f3-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5a3f3-130">Request</span></span>
<span data-ttu-id="5a3f3-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5a3f3-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "worksheetcollection_add"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/add
Content-type: application/json
Content-length: 26

{
  "name": "name-value"
}
```

##### <a name="response"></a><span data-ttu-id="5a3f3-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5a3f3-132">Response</span></span>
<span data-ttu-id="5a3f3-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5a3f3-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.worksheet"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 100

{
  "id": "id-value",
  "position": 99,
  "name": "name-value",
  "visibility": "visibility-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "WorksheetCollection: add",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->