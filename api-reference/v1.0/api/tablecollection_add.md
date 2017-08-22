# <a name="tablecollection-add"></a><span data-ttu-id="d9d5b-101">TableCollection: add</span><span class="sxs-lookup"><span data-stu-id="d9d5b-101">TableCollection: add</span></span>

<span data-ttu-id="d9d5b-p101">Crea una tabla. La dirección de origen del rango determina la hoja de cálculo en la que se agregará la tabla. Si no se puede agregar la tabla (por ejemplo, porque la dirección no es válida o porque la tabla se superpondría con otra tabla), se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="d9d5b-p101">Create a new table. The range source address determines the worksheet under which the table will be added. If the table cannot be added (e.g., because the address is invalid, or the table would overlap with another table), an error will be thrown.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d9d5b-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d9d5b-105">Prerequisites</span></span>
<span data-ttu-id="d9d5b-106">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="d9d5b-106">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="d9d5b-107">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d9d5b-107">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="d9d5b-108">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d9d5b-108">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/add
POST /workbook/worksheets/{id|name}/tables/add

```
## <a name="request-headers"></a><span data-ttu-id="d9d5b-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d9d5b-109">Request headers</span></span>
| <span data-ttu-id="d9d5b-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="d9d5b-110">Name</span></span>       | <span data-ttu-id="d9d5b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9d5b-111">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="d9d5b-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="d9d5b-112">Authorization</span></span>  | <span data-ttu-id="d9d5b-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d9d5b-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="d9d5b-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d9d5b-115">Request body</span></span>
<span data-ttu-id="d9d5b-116">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="d9d5b-116">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="d9d5b-117">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d9d5b-117">Parameter</span></span>    | <span data-ttu-id="d9d5b-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="d9d5b-118">Type</span></span>   |<span data-ttu-id="d9d5b-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9d5b-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d9d5b-120">address</span><span class="sxs-lookup"><span data-stu-id="d9d5b-120">address</span></span>|<span data-ttu-id="d9d5b-121">string</span><span class="sxs-lookup"><span data-stu-id="d9d5b-121">string</span></span>|<span data-ttu-id="d9d5b-p103">Dirección o nombre del objeto de intervalo que representa el origen de datos. Si la dirección no contiene un nombre de hoja, se usa la hoja activa en ese momento.</span><span class="sxs-lookup"><span data-stu-id="d9d5b-p103">Address or name of the range object representing the data source. If the address does not contain a sheet name, the currently-active sheet is used.</span></span>|
|<span data-ttu-id="d9d5b-124">hasHeaders</span><span class="sxs-lookup"><span data-stu-id="d9d5b-124">hasHeaders</span></span>|<span data-ttu-id="d9d5b-125">boolean</span><span class="sxs-lookup"><span data-stu-id="d9d5b-125">boolean</span></span>|<span data-ttu-id="d9d5b-p104">Valor booleano que indica si los datos que se están importando tienen etiquetas de columna. Si el origen no contiene encabezados (es decir, cuando esta propiedad se establece en false), Excel generará automáticamente el encabezado desplazando los datos una fila hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="d9d5b-p104">Boolean value that indicates whether the data being imported has column labels. If the source does not contain headers (i.e,. when this property set to false), Excel will automatically generate header shifting the data down by one row.</span></span>|

## <a name="response"></a><span data-ttu-id="d9d5b-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d9d5b-129">Response</span></span>

<span data-ttu-id="d9d5b-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200, OK` y el objeto [Table](../resources/table.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d9d5b-130">If successful, this method returns `200, OK` response code and [Table](../resources/table.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d9d5b-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d9d5b-131">Example</span></span>
<span data-ttu-id="d9d5b-132">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="d9d5b-132">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="d9d5b-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d9d5b-133">Request</span></span>
<span data-ttu-id="d9d5b-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d9d5b-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablecollection_add"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/add
Content-type: application/json
Content-length: 54

{
  "address": "Sheet1!A1:D5",
  "hasHeaders": true
}
```

##### <a name="response"></a><span data-ttu-id="d9d5b-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d9d5b-135">Response</span></span>
<span data-ttu-id="d9d5b-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d9d5b-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.table"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 109

{
  "id": "99",
  "name": "name-value",
  "showHeaders": true,
  "showTotals": true,
  "style": "style-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "TableCollection: add",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
