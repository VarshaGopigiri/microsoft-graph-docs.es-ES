# <a name="workbookrange-columnsafter"></a><span data-ttu-id="bd01a-101">workbookRange: columnsAfter</span><span class="sxs-lookup"><span data-stu-id="bd01a-101">workbookRange: columnsAfter</span></span>

<span data-ttu-id="bd01a-102">Obtiene un número determinado de columnas a la derecha del rango especificado.</span><span class="sxs-lookup"><span data-stu-id="bd01a-102">Gets a certain number of columns to the right of the given range.</span></span>

## <a name="permissions"></a><span data-ttu-id="bd01a-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="bd01a-103">Permissions</span></span>
<span data-ttu-id="bd01a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="bd01a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="bd01a-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bd01a-106">Permission type</span></span>      | <span data-ttu-id="bd01a-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bd01a-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bd01a-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bd01a-108">Delegated (work or school account)</span></span> | <span data-ttu-id="bd01a-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="bd01a-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="bd01a-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bd01a-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bd01a-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bd01a-111">Not supported.</span></span>    |
|<span data-ttu-id="bd01a-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bd01a-112">Application</span></span> | <span data-ttu-id="bd01a-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bd01a-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="bd01a-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bd01a-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/root/workbook/worksheets/{id}/range/columnsAfter(count=n)

```

## <a name="function-parameters"></a><span data-ttu-id="bd01a-115">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="bd01a-115">Function parameters</span></span>

| <span data-ttu-id="bd01a-116">Parámetro</span><span class="sxs-lookup"><span data-stu-id="bd01a-116">Parameter</span></span>    | <span data-ttu-id="bd01a-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="bd01a-117">Type</span></span>   |<span data-ttu-id="bd01a-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="bd01a-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bd01a-119">count</span><span class="sxs-lookup"><span data-stu-id="bd01a-119">count</span></span>|<span data-ttu-id="bd01a-120">Int32</span><span class="sxs-lookup"><span data-stu-id="bd01a-120">Int32</span></span>|<span data-ttu-id="bd01a-121">Opcional.</span><span class="sxs-lookup"><span data-stu-id="bd01a-121">Optional.</span></span> <span data-ttu-id="bd01a-122">El número de columnas a incluir en el intervalo resultante.</span><span class="sxs-lookup"><span data-stu-id="bd01a-122">The number of columns to include in the resulting range.</span></span> <span data-ttu-id="bd01a-123">En general, use un número positivo para crear un intervalo fuera del intervalo actual.</span><span class="sxs-lookup"><span data-stu-id="bd01a-123">In general, use a positive number to create a range outside the current range.</span></span> <span data-ttu-id="bd01a-124">También puede utilizar un número negativo para crear un intervalo dentro del intervalo actual.</span><span class="sxs-lookup"><span data-stu-id="bd01a-124">You can also use a negative number to create a range within the current range.</span></span> <span data-ttu-id="bd01a-125">El valor predeterminado es 1</span><span class="sxs-lookup"><span data-stu-id="bd01a-125">The default value is 1.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="bd01a-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bd01a-126">Request headers</span></span>
| <span data-ttu-id="bd01a-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="bd01a-127">Name</span></span>       | <span data-ttu-id="bd01a-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="bd01a-128">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="bd01a-129">Autorización</span><span class="sxs-lookup"><span data-stu-id="bd01a-129">Authorization</span></span>  | <span data-ttu-id="bd01a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bd01a-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="bd01a-132">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="bd01a-132">Workbook-Session-Id</span></span>  | <span data-ttu-id="bd01a-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="bd01a-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="bd01a-135">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bd01a-135">Request body</span></span>
<span data-ttu-id="bd01a-136">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bd01a-136">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bd01a-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bd01a-137">Response</span></span>
<span data-ttu-id="bd01a-138">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [workbookRange](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bd01a-138">If successful, this method returns `200 OK` response code and [workbookRange](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bd01a-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bd01a-139">Example</span></span>
<span data-ttu-id="bd01a-140">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="bd01a-140">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="bd01a-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bd01a-141">Request</span></span>
<span data-ttu-id="bd01a-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bd01a-142">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "workbookrange_columnsafter",
  "idempotent": true
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/root/workbook/worksheets/{id}/range/columnsAfter(count=2)
```

##### <a name="response"></a><span data-ttu-id="bd01a-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bd01a-143">Response</span></span>
<span data-ttu-id="bd01a-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bd01a-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
