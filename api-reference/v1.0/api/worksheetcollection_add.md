# <a name="worksheetcollection-add"></a><span data-ttu-id="bbf19-101">WorksheetCollection: add</span><span class="sxs-lookup"><span data-stu-id="bbf19-101">WorksheetCollection: add</span></span>

<span data-ttu-id="bbf19-p101">Agrega una nueva hoja al libro. La hoja de cálculo se agregará al final de las hojas de cálculo existentes. Si desea activar la hoja de cálculo recién agregada, llame en ella a ".activate().</span><span class="sxs-lookup"><span data-stu-id="bbf19-p101">Adds a new worksheet to the workbook. The worksheet will be added at the end of existing worksheets. If you wish to activate the newly added worksheet, call ".activate() on it.</span></span>
## <a name="permissions"></a><span data-ttu-id="bbf19-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="bbf19-105">Permissions</span></span>
<span data-ttu-id="bbf19-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="bbf19-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="bbf19-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bbf19-108">Permission type</span></span>      | <span data-ttu-id="bbf19-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bbf19-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bbf19-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bbf19-110">Delegated (work or school account)</span></span> | <span data-ttu-id="bbf19-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="bbf19-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="bbf19-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bbf19-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bbf19-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bbf19-113">Not supported.</span></span>    |
|<span data-ttu-id="bbf19-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bbf19-114">Application</span></span> | <span data-ttu-id="bbf19-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bbf19-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="bbf19-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bbf19-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/

```
## <a name="request-headers"></a><span data-ttu-id="bbf19-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bbf19-117">Request headers</span></span>
| <span data-ttu-id="bbf19-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="bbf19-118">Name</span></span>       | <span data-ttu-id="bbf19-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="bbf19-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="bbf19-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="bbf19-120">Authorization</span></span>  | <span data-ttu-id="bbf19-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bbf19-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="bbf19-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="bbf19-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="bbf19-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="bbf19-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="bbf19-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bbf19-126">Request body</span></span>
<span data-ttu-id="bbf19-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="bbf19-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="bbf19-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="bbf19-128">Parameter</span></span>    | <span data-ttu-id="bbf19-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="bbf19-129">Type</span></span>   |<span data-ttu-id="bbf19-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="bbf19-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bbf19-131">name</span><span class="sxs-lookup"><span data-stu-id="bbf19-131">name</span></span>|<span data-ttu-id="bbf19-132">cadena</span><span class="sxs-lookup"><span data-stu-id="bbf19-132">string</span></span>|<span data-ttu-id="bbf19-p105">Opcional. Nombre de la hoja de cálculo que se va a agregar. Si se especifica, el nombre debe ser único. Si no se especifica, Excel determina el nombre de la nueva hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="bbf19-p105">Optional. The name of the worksheet to be added. If specified, name should be unqiue. If not specified, Excel determines the name of the new worksheet.</span></span>|

## <a name="response"></a><span data-ttu-id="bbf19-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bbf19-137">Response</span></span>

<span data-ttu-id="bbf19-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [WorkbookWorksheet](../resources/worksheet.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bbf19-138">If successful, this method returns `200 OK` response code and [groupSetting](../resources/worksheet.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bbf19-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bbf19-139">Example</span></span>
<span data-ttu-id="bbf19-140">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="bbf19-140">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="bbf19-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bbf19-141">Request</span></span>
<span data-ttu-id="bbf19-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bbf19-142">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="bbf19-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bbf19-143">Response</span></span>
<span data-ttu-id="bbf19-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bbf19-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookWorksheet"
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