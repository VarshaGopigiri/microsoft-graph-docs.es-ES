# <a name="workbookrange-resizedrange"></a><span data-ttu-id="08893-101">workbookRange: resizedRange</span><span class="sxs-lookup"><span data-stu-id="08893-101">workbookRange: resizedRange</span></span>
<span data-ttu-id="08893-102">Obtiene un objeto de rango similar al objeto actual, pero con su esquina inferior derecha expandida (o contraída) mediante un número de filas y columnas.</span><span class="sxs-lookup"><span data-stu-id="08893-102">Gets a range object similar to the current range object, but with its bottom-right corner expanded (or contracted) by some number of rows and columns.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="08893-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="08893-103">Prerequisites</span></span>
<span data-ttu-id="08893-104">Se requieren los siguientes **ámbitos** para ejecutar esta API: _Files.Read, Files.ReadWrite_</span><span class="sxs-lookup"><span data-stu-id="08893-104">The following **scopes** are required to execute this API: _Files.Read, Files.ReadWrite_</span></span>
## <a name="http-request"></a><span data-ttu-id="08893-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="08893-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/root/workbook/worksheets/{id}/range/resizedRange(deltaRows={n}, deltaColumns={n})

```
## <a name="request-headers"></a><span data-ttu-id="08893-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="08893-106">Request headers</span></span>
| <span data-ttu-id="08893-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="08893-107">Name</span></span>       | <span data-ttu-id="08893-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="08893-108">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="08893-109">Authorization</span><span class="sxs-lookup"><span data-stu-id="08893-109">Authorization</span></span>  | <span data-ttu-id="08893-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="08893-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="08893-112">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="08893-112">Workbook-Session-Id</span></span>  | <span data-ttu-id="08893-p102">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="08893-p102">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="parameters"></a><span data-ttu-id="08893-115">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08893-115">Parameters</span></span>

| <span data-ttu-id="08893-116">Parámetro</span><span class="sxs-lookup"><span data-stu-id="08893-116">Parameter</span></span>    | <span data-ttu-id="08893-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="08893-117">Type</span></span>   |<span data-ttu-id="08893-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="08893-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="08893-119">deltarows</span><span class="sxs-lookup"><span data-stu-id="08893-119">deltarows</span></span>|<span data-ttu-id="08893-120">Int32</span><span class="sxs-lookup"><span data-stu-id="08893-120">Int32</span></span>|<span data-ttu-id="08893-p103">El número de filas en el que se va a expandir la esquina inferior derecha, con respecto al intervalo actual. Use un número positivo para expandir el intervalo, o un número negativo para reducirlo.</span><span class="sxs-lookup"><span data-stu-id="08893-p103">The number of rows by which to expand the bottom-right corner, relative to the current range. Use a positive number to expand the range, or a negative number to decrease it</span></span>|
|<span data-ttu-id="08893-123">deltaColumns</span><span class="sxs-lookup"><span data-stu-id="08893-123">deltaColumns</span></span>|<span data-ttu-id="08893-124">Int32</span><span class="sxs-lookup"><span data-stu-id="08893-124">Int32</span></span>|<span data-ttu-id="08893-p104">El número de columnas en el que se va a expandir la esquina inferior derecha, con respecto al intervalo actual. Use un número positivo para expandir el intervalo, o un número negativo para reducirlo.</span><span class="sxs-lookup"><span data-stu-id="08893-p104">The number of columnsby which to expand the bottom-right corner, relative to the current range. Use a positive number to expand the range, or a negative number to decrease it.</span></span>|

## <a name="request-body"></a><span data-ttu-id="08893-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="08893-127">Request body</span></span>
<span data-ttu-id="08893-128">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="08893-128">In the request URL, provide following query parameters with values.</span></span>

| <span data-ttu-id="08893-129">Parámetro</span><span class="sxs-lookup"><span data-stu-id="08893-129">Parameter</span></span>    | <span data-ttu-id="08893-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="08893-130">Type</span></span>   |<span data-ttu-id="08893-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="08893-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="08893-132">deltaRows</span><span class="sxs-lookup"><span data-stu-id="08893-132">deltaRows</span></span>|<span data-ttu-id="08893-133">Int32</span><span class="sxs-lookup"><span data-stu-id="08893-133">Int32</span></span>||
|<span data-ttu-id="08893-134">deltaColumns</span><span class="sxs-lookup"><span data-stu-id="08893-134">deltaColumns</span></span>|<span data-ttu-id="08893-135">Int32</span><span class="sxs-lookup"><span data-stu-id="08893-135">Int32</span></span>||

## <a name="response"></a><span data-ttu-id="08893-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="08893-136">Response</span></span>

<span data-ttu-id="08893-137">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [workbookRange](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="08893-137">If successful, this method returns `200, OK` response code and [workbookRange](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="08893-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="08893-138">Example</span></span>
<span data-ttu-id="08893-139">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="08893-139">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="08893-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="08893-140">Request</span></span>
<span data-ttu-id="08893-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="08893-141">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "workbookrange_resizedrange"
}-->
```http
POST https://graph.microsoft.com/v1.0/drive/root/workbook/worksheets/{id}/range/resizedRange(deltarows={n}, deltaColumns={n})
```

##### <a name="response"></a><span data-ttu-id="08893-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="08893-142">Response</span></span>
<span data-ttu-id="08893-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="08893-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
