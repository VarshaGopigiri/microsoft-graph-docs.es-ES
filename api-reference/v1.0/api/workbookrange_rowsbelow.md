# <a name="workbookrange-rowsbelow"></a><span data-ttu-id="c5a9f-101">workbookRange: rowsBelow</span><span class="sxs-lookup"><span data-stu-id="c5a9f-101">workbookRange: rowsBelow</span></span>

<span data-ttu-id="c5a9f-102">Obtiene un número determinado de filas a continuación de un intervalo dado.</span><span class="sxs-lookup"><span data-stu-id="c5a9f-102">Gets certain number of rows below a given range.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c5a9f-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c5a9f-103">Prerequisites</span></span>
<span data-ttu-id="c5a9f-104">Se requieren los siguientes **ámbitos** para ejecutar esta API: _Files.Read, Files.ReadWrite_</span><span class="sxs-lookup"><span data-stu-id="c5a9f-104">The following **scopes** are required to execute this API: _Files.Read, Files.ReadWrite_</span></span>
## <a name="http-request"></a><span data-ttu-id="c5a9f-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c5a9f-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/root/workbook/worksheets/{id}/range/rowsBelow(count=n)

```
## <a name="request-headers"></a><span data-ttu-id="c5a9f-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c5a9f-106">Request headers</span></span>
| <span data-ttu-id="c5a9f-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="c5a9f-107">Name</span></span>       | <span data-ttu-id="c5a9f-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5a9f-108">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="c5a9f-109">Authorization</span><span class="sxs-lookup"><span data-stu-id="c5a9f-109">Authorization</span></span>  | <span data-ttu-id="c5a9f-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c5a9f-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c5a9f-112">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="c5a9f-112">Workbook-Session-Id</span></span>  | <span data-ttu-id="c5a9f-p102">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="c5a9f-p102">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="parameters"></a><span data-ttu-id="c5a9f-115">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5a9f-115">Parameters</span></span>

| <span data-ttu-id="c5a9f-116">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c5a9f-116">Parameter</span></span>    | <span data-ttu-id="c5a9f-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="c5a9f-117">Type</span></span>   |<span data-ttu-id="c5a9f-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5a9f-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c5a9f-119">count</span><span class="sxs-lookup"><span data-stu-id="c5a9f-119">count</span></span>|<span data-ttu-id="c5a9f-120">Int32</span><span class="sxs-lookup"><span data-stu-id="c5a9f-120">Int32</span></span>|<span data-ttu-id="c5a9f-p103">El número de filas que se va a incluir en el intervalo resultante. En general, use un número positivo para crear un intervalo fuera del intervalo actual. También puede usar un número negativo para crear un intervalo dentro del intervalo actual. El valor predeterminado es 1</span><span class="sxs-lookup"><span data-stu-id="c5a9f-p103">The number of rows to include in the resulting range. In general, use a positive number to create a range outside the current range. You can also use a negative number to create a range within the current range. The default value is 1</span></span>|

## <a name="request-body"></a><span data-ttu-id="c5a9f-125">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="c5a9f-125">Request body</span></span>

## <a name="response"></a><span data-ttu-id="c5a9f-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c5a9f-126">Response</span></span>

<span data-ttu-id="c5a9f-127">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [workbookRange](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c5a9f-127">If successful, this method returns `200, OK` response code and [workbookRange](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c5a9f-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c5a9f-128">Example</span></span>
<span data-ttu-id="c5a9f-129">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="c5a9f-129">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="c5a9f-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c5a9f-130">Request</span></span>
<span data-ttu-id="c5a9f-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c5a9f-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "workbookrange_rowsBelow"
}-->
```http
POST https://graph.microsoft.com/v1.0/drive/root/workbook/worksheets/{id}/range/rowsBelow(count=2)
```

##### <a name="response"></a><span data-ttu-id="c5a9f-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c5a9f-132">Response</span></span>
<span data-ttu-id="c5a9f-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c5a9f-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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