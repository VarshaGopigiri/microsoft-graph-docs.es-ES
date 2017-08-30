# <a name="workbookrange-resizedrange"></a><span data-ttu-id="2615d-101">workbookRange: resizedRange</span><span class="sxs-lookup"><span data-stu-id="2615d-101">workbookRange: resizedRange</span></span>
<span data-ttu-id="2615d-102">Obtiene un objeto de rango similar al objeto actual, pero con su esquina inferior derecha expandida (o contraída) mediante un número de filas y columnas.</span><span class="sxs-lookup"><span data-stu-id="2615d-102">Gets a range object similar to the current range object, but with its bottom-right corner expanded (or contracted) by some number of rows and columns.</span></span>

## <a name="permissions"></a><span data-ttu-id="2615d-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="2615d-103">Permissions</span></span>
<span data-ttu-id="2615d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="2615d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="2615d-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2615d-106">Permission type</span></span>      | <span data-ttu-id="2615d-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2615d-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2615d-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2615d-108">Delegated (work or school account)</span></span> | <span data-ttu-id="2615d-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2615d-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="2615d-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2615d-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2615d-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2615d-111">Not supported.</span></span>    |
|<span data-ttu-id="2615d-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2615d-112">Application</span></span> | <span data-ttu-id="2615d-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2615d-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="2615d-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2615d-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/root/workbook/worksheets/{id}/range/resizedRange(deltaRows={n}, deltaColumns={n})

```
## <a name="request-headers"></a><span data-ttu-id="2615d-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2615d-115">Request headers</span></span>
| <span data-ttu-id="2615d-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="2615d-116">Name</span></span>       | <span data-ttu-id="2615d-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="2615d-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="2615d-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="2615d-118">Authorization</span></span>  | <span data-ttu-id="2615d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2615d-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="2615d-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="2615d-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="2615d-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="2615d-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="parameters"></a><span data-ttu-id="2615d-124">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2615d-124">Parameters</span></span>

| <span data-ttu-id="2615d-125">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2615d-125">Parameter</span></span>    | <span data-ttu-id="2615d-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="2615d-126">Type</span></span>   |<span data-ttu-id="2615d-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="2615d-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2615d-128">deltarows</span><span class="sxs-lookup"><span data-stu-id="2615d-128">deltarows</span></span>|<span data-ttu-id="2615d-129">Int32</span><span class="sxs-lookup"><span data-stu-id="2615d-129">Int32</span></span>|<span data-ttu-id="2615d-p104">El número de filas en el que se va a expandir la esquina inferior derecha, con respecto al intervalo actual. Use un número positivo para expandir el intervalo, o un número negativo para reducirlo.</span><span class="sxs-lookup"><span data-stu-id="2615d-p104">The number of rows by which to expand the bottom-right corner, relative to the current range. Use a positive number to expand the range, or a negative number to decrease it</span></span>|
|<span data-ttu-id="2615d-132">deltaColumns</span><span class="sxs-lookup"><span data-stu-id="2615d-132">deltaColumns</span></span>|<span data-ttu-id="2615d-133">Int32</span><span class="sxs-lookup"><span data-stu-id="2615d-133">Int32</span></span>|<span data-ttu-id="2615d-p105">El número de columnas en el que se va a expandir la esquina inferior derecha, con respecto al intervalo actual. Use un número positivo para expandir el intervalo, o un número negativo para reducirlo.</span><span class="sxs-lookup"><span data-stu-id="2615d-p105">The number of columnsby which to expand the bottom-right corner, relative to the current range. Use a positive number to expand the range, or a negative number to decrease it.</span></span>|

## <a name="request-body"></a><span data-ttu-id="2615d-136">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2615d-136">Request body</span></span>
<span data-ttu-id="2615d-137">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="2615d-137">In the request URL, provide following query parameters with values.</span></span>

| <span data-ttu-id="2615d-138">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2615d-138">Parameter</span></span>    | <span data-ttu-id="2615d-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="2615d-139">Type</span></span>   |<span data-ttu-id="2615d-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="2615d-140">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2615d-141">deltaRows</span><span class="sxs-lookup"><span data-stu-id="2615d-141">deltaRows</span></span>|<span data-ttu-id="2615d-142">Int32</span><span class="sxs-lookup"><span data-stu-id="2615d-142">Int32</span></span>||
|<span data-ttu-id="2615d-143">deltaColumns</span><span class="sxs-lookup"><span data-stu-id="2615d-143">deltaColumns</span></span>|<span data-ttu-id="2615d-144">Int32</span><span class="sxs-lookup"><span data-stu-id="2615d-144">Int32</span></span>||

### <a name="response"></a><span data-ttu-id="2615d-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2615d-145">Response</span></span>
<span data-ttu-id="2615d-146">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [workbookRange](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2615d-146">If successful, this method returns `200, OK` response code and [workbookRange](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2615d-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2615d-147">Example</span></span>
<span data-ttu-id="2615d-148">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="2615d-148">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="2615d-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2615d-149">Request</span></span>
<span data-ttu-id="2615d-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2615d-150">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "workbookrange_resizedrange"
}-->
```http
POST https://graph.microsoft.com/v1.0/drive/root/workbook/worksheets/{id}/range/resizedRange(deltarows={n}, deltaColumns={n})
```

##### <a name="response"></a><span data-ttu-id="2615d-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2615d-151">Response</span></span>
<span data-ttu-id="2615d-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2615d-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.range"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 157

{
  "address": "address-value",
  "addressLocal": "addressLocal-value",
  "cellCount": 99,
  "columnCount": 99,
  "columnHidden": true,
  "columnIndex": 99
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "workbookRange: resizedRange",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
