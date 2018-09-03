# <a name="workbookrange-rowsabove"></a><span data-ttu-id="d2af8-101">workbookRange: rowsAbove</span><span class="sxs-lookup"><span data-stu-id="d2af8-101">workbookRange: rowsAbove</span></span>

<span data-ttu-id="d2af8-102">Obtiene un número determinado de filas encima de un rango dado.</span><span class="sxs-lookup"><span data-stu-id="d2af8-102">Gets a certain number of rows above a given range.</span></span>

## <a name="permissions"></a><span data-ttu-id="d2af8-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="d2af8-103">Permissions</span></span>
<span data-ttu-id="d2af8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d2af8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d2af8-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d2af8-106">Permission type</span></span>      | <span data-ttu-id="d2af8-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d2af8-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d2af8-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d2af8-108">Delegated (work or school account)</span></span> | <span data-ttu-id="d2af8-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d2af8-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="d2af8-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d2af8-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d2af8-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d2af8-111">Not supported.</span></span>    |
|<span data-ttu-id="d2af8-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d2af8-112">Application</span></span> | <span data-ttu-id="d2af8-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d2af8-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="d2af8-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d2af8-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/root/workbook/worksheets/{id}/range/rowsAbove(count=n)

```

## <a name="function-parameters"></a><span data-ttu-id="d2af8-115">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="d2af8-115">Function parameters</span></span>

| <span data-ttu-id="d2af8-116">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d2af8-116">Parameter</span></span>    | <span data-ttu-id="d2af8-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="d2af8-117">Type</span></span>   |<span data-ttu-id="d2af8-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2af8-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d2af8-119">count</span><span class="sxs-lookup"><span data-stu-id="d2af8-119">count</span></span>|<span data-ttu-id="d2af8-120">Int32</span><span class="sxs-lookup"><span data-stu-id="d2af8-120">Int32</span></span>|<span data-ttu-id="d2af8-p102">Opcional. El número de filas que se va a incluir en el intervalo resultante. En general, use un número positivo para crear un intervalo fuera del intervalo actual. También puede usar un número negativo para crear un intervalo dentro del intervalo actual. El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="d2af8-p102">Optional. The number of rows to include in the resulting range. In general, use a positive number to create a range outside the current range. You can also use a negative number to create a range within the current range. The default value is 1.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="d2af8-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d2af8-126">Request headers</span></span>
| <span data-ttu-id="d2af8-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="d2af8-127">Name</span></span>       | <span data-ttu-id="d2af8-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2af8-128">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="d2af8-129">Autorización</span><span class="sxs-lookup"><span data-stu-id="d2af8-129">Authorization</span></span>  | <span data-ttu-id="d2af8-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d2af8-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d2af8-132">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="d2af8-132">Workbook-Session-Id</span></span>  | <span data-ttu-id="d2af8-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="d2af8-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="d2af8-135">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d2af8-135">Request body</span></span>
<span data-ttu-id="d2af8-136">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d2af8-136">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d2af8-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2af8-137">Response</span></span>
<span data-ttu-id="d2af8-138">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [workbookRange](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d2af8-138">If successful, this method returns `200 OK` response code and [workbookRange](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d2af8-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d2af8-139">Example</span></span>
<span data-ttu-id="d2af8-140">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="d2af8-140">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="d2af8-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d2af8-141">Request</span></span>
<span data-ttu-id="d2af8-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d2af8-142">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "workbookrange_rowsAbove",
  "idempotent": true
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/root/workbook/worksheets/{id}/range/rowsAbove(count=2)
```

##### <a name="response"></a><span data-ttu-id="d2af8-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2af8-143">Response</span></span>
<span data-ttu-id="d2af8-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d2af8-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

<span data-ttu-id="d2af8-147">Si se llama sin el parámetro opcional `count`, esta función devuelve la única fila por encima del intervalo.</span><span class="sxs-lookup"><span data-stu-id="d2af8-147">If called without the optional `count` parameter, this function returns the single row above the range.</span></span>

##### <a name="request"></a><span data-ttu-id="d2af8-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d2af8-148">Request</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "workbookrange_rowsAbove_nocount",
  "idempotent": true
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/root/workbook/worksheets/{id}/range/rowsAbove
```

##### <a name="response"></a><span data-ttu-id="d2af8-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2af8-149">Response</span></span>
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