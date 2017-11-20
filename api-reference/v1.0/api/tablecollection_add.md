# <a name="tablecollection-add"></a><span data-ttu-id="1ef27-101">TableCollection: add</span><span class="sxs-lookup"><span data-stu-id="1ef27-101">TableCollection: add</span></span>

<span data-ttu-id="1ef27-p101">Crea una tabla. La dirección de origen del rango determina la hoja de cálculo en la que se agregará la tabla. Si no se puede agregar la tabla (por ejemplo, porque la dirección no es válida o porque la tabla se superpondría con otra tabla), se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="1ef27-p101">Create a new table. The range source address determines the worksheet under which the table will be added. If the table cannot be added (e.g., because the address is invalid, or the table would overlap with another table), an error will be thrown.</span></span>
## <a name="permissions"></a><span data-ttu-id="1ef27-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="1ef27-105">Permissions</span></span>
<span data-ttu-id="1ef27-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="1ef27-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="1ef27-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1ef27-108">Permission type</span></span>      | <span data-ttu-id="1ef27-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1ef27-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1ef27-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1ef27-110">Delegated (work or school account)</span></span> | <span data-ttu-id="1ef27-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1ef27-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="1ef27-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1ef27-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1ef27-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1ef27-113">Not supported.</span></span>    |
|<span data-ttu-id="1ef27-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1ef27-114">Application</span></span> | <span data-ttu-id="1ef27-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1ef27-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="1ef27-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1ef27-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/add
POST /workbook/worksheets/{id|name}/tables/add

```
## <a name="request-headers"></a><span data-ttu-id="1ef27-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1ef27-117">Request headers</span></span>
| <span data-ttu-id="1ef27-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="1ef27-118">Name</span></span>       | <span data-ttu-id="1ef27-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ef27-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="1ef27-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="1ef27-120">Authorization</span></span>  | <span data-ttu-id="1ef27-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1ef27-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="1ef27-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="1ef27-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="1ef27-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="1ef27-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="1ef27-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1ef27-126">Request body</span></span>
<span data-ttu-id="1ef27-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="1ef27-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="1ef27-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="1ef27-128">Parameter</span></span>    | <span data-ttu-id="1ef27-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="1ef27-129">Type</span></span>   |<span data-ttu-id="1ef27-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ef27-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1ef27-131">address</span><span class="sxs-lookup"><span data-stu-id="1ef27-131">address</span></span>|<span data-ttu-id="1ef27-132">string</span><span class="sxs-lookup"><span data-stu-id="1ef27-132">string</span></span>|<span data-ttu-id="1ef27-p105">Dirección o nombre del objeto de intervalo que representa el origen de datos. Si la dirección no contiene un nombre de hoja, se usa la hoja activa en ese momento.</span><span class="sxs-lookup"><span data-stu-id="1ef27-p105">Address or name of the range object representing the data source. If the address does not contain a sheet name, the currently-active sheet is used.</span></span>|
|<span data-ttu-id="1ef27-135">hasHeaders</span><span class="sxs-lookup"><span data-stu-id="1ef27-135">hasHeaders</span></span>|<span data-ttu-id="1ef27-136">boolean</span><span class="sxs-lookup"><span data-stu-id="1ef27-136">boolean</span></span>|<span data-ttu-id="1ef27-p106">Valor booleano que indica si los datos que se están importando tienen etiquetas de columna. Si el origen no contiene encabezados (es decir, cuando esta propiedad se establece en false), Excel generará automáticamente el encabezado desplazando los datos una fila hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="1ef27-p106">Boolean value that indicates whether the data being imported has column labels. If the source does not contain headers (i.e,. when this property set to false), Excel will automatically generate header shifting the data down by one row.</span></span>|

## <a name="response"></a><span data-ttu-id="1ef27-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1ef27-140">Response</span></span>

<span data-ttu-id="1ef27-141">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [Table](../resources/table.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1ef27-141">If successful, this method returns `200 OK` response code and [Table](../resources/table.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1ef27-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1ef27-142">Example</span></span>
<span data-ttu-id="1ef27-143">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="1ef27-143">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="1ef27-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1ef27-144">Request</span></span>
<span data-ttu-id="1ef27-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1ef27-145">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="1ef27-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1ef27-146">Response</span></span>
<span data-ttu-id="1ef27-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1ef27-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
