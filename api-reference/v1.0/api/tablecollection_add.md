# <a name="tablecollection-add"></a><span data-ttu-id="74464-101">TableCollection: add</span><span class="sxs-lookup"><span data-stu-id="74464-101">TableCollection: add</span></span>

<span data-ttu-id="74464-p101">Crea una tabla nueva. La dirección de origen del rango determina la hoja de cálculo en la que se agregará la tabla. Si no se puede agregar la tabla (por ejemplo, porque la dirección no es válida o porque la tabla se superpondría con otra tabla), se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="74464-p101">Create a new table. The range source address determines the worksheet under which the table will be added. If the table cannot be added (e.g., because the address is invalid, or the table would overlap with another table), an error will be thrown.</span></span>

## <a name="error-handling"></a><span data-ttu-id="74464-105">Control de errores</span><span class="sxs-lookup"><span data-stu-id="74464-105">Error Handling</span></span>

<span data-ttu-id="74464-106">En ocasiones, esta solicitud puede recibir el error HTTP 504.</span><span class="sxs-lookup"><span data-stu-id="74464-106">This request might occasionally receive a 504 HTTP error.</span></span> <span data-ttu-id="74464-107">La respuesta adecuada a este error es repetir la solicitud.</span><span class="sxs-lookup"><span data-stu-id="74464-107">The appropriate response to this error is to repeat the request.</span></span>

## <a name="permissions"></a><span data-ttu-id="74464-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="74464-108">Permissions</span></span>
<span data-ttu-id="74464-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="74464-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="74464-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="74464-111">Permission type</span></span>      | <span data-ttu-id="74464-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="74464-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="74464-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="74464-113">Delegated (work or school account)</span></span> | <span data-ttu-id="74464-114">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="74464-114">Files.ReadWrite</span></span>    |
|<span data-ttu-id="74464-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="74464-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="74464-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="74464-116">Not supported.</span></span>    |
|<span data-ttu-id="74464-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="74464-117">Application</span></span> | <span data-ttu-id="74464-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="74464-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="74464-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="74464-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/add
POST /workbook/worksheets/{id|name}/tables/add

```
## <a name="request-headers"></a><span data-ttu-id="74464-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="74464-120">Request headers</span></span>
| <span data-ttu-id="74464-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="74464-121">Name</span></span>       | <span data-ttu-id="74464-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="74464-122">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="74464-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="74464-123">Authorization</span></span>  | <span data-ttu-id="74464-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="74464-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="74464-126">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="74464-126">Workbook-Session-Id</span></span>  | <span data-ttu-id="74464-p105">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="74464-p105">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="74464-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="74464-129">Request body</span></span>
<span data-ttu-id="74464-130">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="74464-130">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="74464-131">Parámetro</span><span class="sxs-lookup"><span data-stu-id="74464-131">Parameter</span></span>    | <span data-ttu-id="74464-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="74464-132">Type</span></span>   |<span data-ttu-id="74464-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="74464-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="74464-134">address</span><span class="sxs-lookup"><span data-stu-id="74464-134">address</span></span>|<span data-ttu-id="74464-135">cadena</span><span class="sxs-lookup"><span data-stu-id="74464-135">string</span></span>|<span data-ttu-id="74464-p106">Dirección o nombre del objeto de intervalo que representa el origen de datos. Si la dirección no contiene un nombre de hoja, se usa la hoja activa en ese momento.</span><span class="sxs-lookup"><span data-stu-id="74464-p106">Address or name of the range object representing the data source. If the address does not contain a sheet name, the currently-active sheet is used.</span></span>|
|<span data-ttu-id="74464-138">hasHeaders</span><span class="sxs-lookup"><span data-stu-id="74464-138">hasHeaders</span></span>|<span data-ttu-id="74464-139">booleano</span><span class="sxs-lookup"><span data-stu-id="74464-139">boolean</span></span>|<span data-ttu-id="74464-p107">Valor booleano que indica si los datos que se están importando tienen etiquetas de columna. Si el origen no contiene encabezados (es decir, cuando esta propiedad se establece en false), Excel generará automáticamente el encabezado desplazando los datos una fila hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="74464-p107">Boolean value that indicates whether the data being imported has column labels. If the source does not contain headers (i.e,. when this property set to false), Excel will automatically generate header shifting the data down by one row.</span></span>|

## <a name="response"></a><span data-ttu-id="74464-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="74464-143">Response</span></span>

<span data-ttu-id="74464-144">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [WorkbookTable](../resources/table.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="74464-144">If successful, this method returns `200 OK` response code and [groupSetting](../resources/table.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="74464-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="74464-145">Example</span></span>
<span data-ttu-id="74464-146">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="74464-146">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="74464-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="74464-147">Request</span></span>
<span data-ttu-id="74464-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="74464-148">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="74464-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="74464-149">Response</span></span>
<span data-ttu-id="74464-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="74464-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookTable"
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
