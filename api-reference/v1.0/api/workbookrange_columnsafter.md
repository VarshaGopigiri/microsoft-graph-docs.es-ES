# <a name="workbookrange-columnsafter"></a><span data-ttu-id="15e27-101">workbookRange: columnsAfter</span><span class="sxs-lookup"><span data-stu-id="15e27-101">workbookRange: columnsAfter</span></span>

<span data-ttu-id="15e27-102">Obtiene un número determinado de columnas a la derecha del rango especificado.</span><span class="sxs-lookup"><span data-stu-id="15e27-102">Gets a certain number of columns to the right of the given range.</span></span>

## <a name="permissions"></a><span data-ttu-id="15e27-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="15e27-103">Permissions</span></span>
<span data-ttu-id="15e27-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="15e27-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="15e27-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="15e27-106">Permission type</span></span>      | <span data-ttu-id="15e27-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="15e27-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="15e27-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="15e27-108">Delegated (work or school account)</span></span> | <span data-ttu-id="15e27-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="15e27-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="15e27-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="15e27-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="15e27-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="15e27-111">Not supported.</span></span>    |
|<span data-ttu-id="15e27-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="15e27-112">Application</span></span> | <span data-ttu-id="15e27-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="15e27-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="15e27-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="15e27-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/root/workbook/worksheets/{id}/range/columnsAfter(count=n)

```
## <a name="request-headers"></a><span data-ttu-id="15e27-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="15e27-115">Request headers</span></span>
| <span data-ttu-id="15e27-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="15e27-116">Name</span></span>       | <span data-ttu-id="15e27-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="15e27-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="15e27-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="15e27-118">Authorization</span></span>  | <span data-ttu-id="15e27-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="15e27-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="15e27-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="15e27-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="15e27-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="15e27-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="parameters"></a><span data-ttu-id="15e27-124">Parámetros</span><span class="sxs-lookup"><span data-stu-id="15e27-124">Parameters</span></span>

| <span data-ttu-id="15e27-125">Parámetro</span><span class="sxs-lookup"><span data-stu-id="15e27-125">Parameter</span></span>    | <span data-ttu-id="15e27-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="15e27-126">Type</span></span>   |<span data-ttu-id="15e27-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="15e27-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="15e27-128">count</span><span class="sxs-lookup"><span data-stu-id="15e27-128">count</span></span>|<span data-ttu-id="15e27-129">Int32</span><span class="sxs-lookup"><span data-stu-id="15e27-129">Int32</span></span>|<span data-ttu-id="15e27-130">Opcional.</span><span class="sxs-lookup"><span data-stu-id="15e27-130">Optional.</span></span> <span data-ttu-id="15e27-131">El número de columnas a incluir en el intervalo resultante.</span><span class="sxs-lookup"><span data-stu-id="15e27-131">The number of columns to include in the resulting range.</span></span> <span data-ttu-id="15e27-132">En general, use un número positivo para crear un intervalo fuera del intervalo actual.</span><span class="sxs-lookup"><span data-stu-id="15e27-132">In general, use a positive number to create a range outside the current range.</span></span> <span data-ttu-id="15e27-133">También puede utilizar un número negativo para crear un intervalo dentro del intervalo actual.</span><span class="sxs-lookup"><span data-stu-id="15e27-133">You can also use a negative number to create a range within the current range.</span></span> <span data-ttu-id="15e27-134">El valor predeterminado es 1</span><span class="sxs-lookup"><span data-stu-id="15e27-134">The default value is 1.</span></span>|

## <a name="request-body"></a><span data-ttu-id="15e27-135">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="15e27-135">Request body</span></span>

### <a name="response"></a><span data-ttu-id="15e27-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="15e27-136">Response</span></span>
<span data-ttu-id="15e27-137">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [workbookRange](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="15e27-137">If successful, this method returns `200 OK` response code and [workbookRange](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="15e27-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="15e27-138">Example</span></span>
<span data-ttu-id="15e27-139">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="15e27-139">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="15e27-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="15e27-140">Request</span></span>
<span data-ttu-id="15e27-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="15e27-141">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "workbookrange_columnsafter",
  "idempotent": true
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/root/workbook/worksheets/{id}/range/columnsAfter(count=2)
```

##### <a name="response"></a><span data-ttu-id="15e27-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="15e27-142">Response</span></span>
<span data-ttu-id="15e27-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="15e27-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
