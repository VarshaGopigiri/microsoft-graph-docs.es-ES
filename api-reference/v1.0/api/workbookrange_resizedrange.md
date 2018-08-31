# <a name="workbookrange-resizedrange"></a><span data-ttu-id="107ac-101">workbookRange: resizedRange</span><span class="sxs-lookup"><span data-stu-id="107ac-101">workbookRange: resizedRange</span></span>
<span data-ttu-id="107ac-102">Obtiene un objeto de rango similar al objeto actual, pero con su esquina inferior derecha expandida (o contraída) mediante un número de filas y columnas.</span><span class="sxs-lookup"><span data-stu-id="107ac-102">Gets a range object similar to the current range object, but with its bottom-right corner expanded (or contracted) by some number of rows and columns.</span></span>

## <a name="permissions"></a><span data-ttu-id="107ac-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="107ac-103">Permissions</span></span>
<span data-ttu-id="107ac-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="107ac-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="107ac-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="107ac-106">Permission type</span></span>      | <span data-ttu-id="107ac-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="107ac-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="107ac-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="107ac-108">Delegated (work or school account)</span></span> | <span data-ttu-id="107ac-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="107ac-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="107ac-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="107ac-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="107ac-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="107ac-111">Not supported.</span></span>    |
|<span data-ttu-id="107ac-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="107ac-112">Application</span></span> | <span data-ttu-id="107ac-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="107ac-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="107ac-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="107ac-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/root/workbook/worksheets/{id}/range/resizedRange(deltaRows={n}, deltaColumns={n})

```
## <a name="request-headers"></a><span data-ttu-id="107ac-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="107ac-115">Request headers</span></span>
| <span data-ttu-id="107ac-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="107ac-116">Name</span></span>       | <span data-ttu-id="107ac-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="107ac-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="107ac-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="107ac-118">Authorization</span></span>  | <span data-ttu-id="107ac-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="107ac-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="107ac-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="107ac-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="107ac-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="107ac-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="parameters"></a><span data-ttu-id="107ac-124">Parámetros</span><span class="sxs-lookup"><span data-stu-id="107ac-124">Parameters</span></span>

| <span data-ttu-id="107ac-125">Parámetro</span><span class="sxs-lookup"><span data-stu-id="107ac-125">Parameter</span></span>    | <span data-ttu-id="107ac-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="107ac-126">Type</span></span>   |<span data-ttu-id="107ac-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="107ac-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="107ac-128">deltaRows</span><span class="sxs-lookup"><span data-stu-id="107ac-128">deltaRows</span></span>|<span data-ttu-id="107ac-129">Int32</span><span class="sxs-lookup"><span data-stu-id="107ac-129">Int32</span></span>|<span data-ttu-id="107ac-p104">El número de filas en el que se va a expandir la esquina inferior derecha, con respecto al intervalo actual. Use un número positivo para expandir el intervalo, o un número negativo para reducirlo.</span><span class="sxs-lookup"><span data-stu-id="107ac-p104">The number of rows by which to expand the bottom-right corner, relative to the current range. Use a positive number to expand the range, or a negative number to decrease it</span></span>|
|<span data-ttu-id="107ac-132">deltaColumns</span><span class="sxs-lookup"><span data-stu-id="107ac-132">deltaColumns</span></span>|<span data-ttu-id="107ac-133">Int32</span><span class="sxs-lookup"><span data-stu-id="107ac-133">Int32</span></span>|<span data-ttu-id="107ac-134">El número de columnas que se usará expandir la esquina inferior derecha, en relación con el intervalo actual.</span><span class="sxs-lookup"><span data-stu-id="107ac-134">The number of rows by which to expand the bottom-right corner, relative to the current range. Use a positive number to expand the range, or a negative number to decrease it</span></span> <span data-ttu-id="107ac-135">Use un número positivo para expandir el intervalo o un número negativo para reducirlo.</span><span class="sxs-lookup"><span data-stu-id="107ac-135">The number of columnsby which to expand the bottom-right corner, relative to the current range. Use a positive number to expand the range, or a negative number to decrease it.</span></span>|

### <a name="response"></a><span data-ttu-id="107ac-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="107ac-136">Response</span></span>
<span data-ttu-id="107ac-137">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [workbookRange](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="107ac-137">If successful, this method returns `200 OK` response code and [workbookRange](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="107ac-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="107ac-138">Example</span></span>
<span data-ttu-id="107ac-139">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="107ac-139">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="107ac-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="107ac-140">Request</span></span>
<span data-ttu-id="107ac-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="107ac-141">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "workbookrange_resizedrange",
  "idempotent": true
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/root/workbook/worksheets/{id}/range/resizedRange(deltaRows={n}, deltaColumns={n})
```

##### <a name="response"></a><span data-ttu-id="107ac-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="107ac-142">Response</span></span>
<span data-ttu-id="107ac-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="107ac-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRange"
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
