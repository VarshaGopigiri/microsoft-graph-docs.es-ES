# <a name="update-worksheet"></a><span data-ttu-id="e19d2-101">Update worksheet</span><span class="sxs-lookup"><span data-stu-id="e19d2-101">Update worksheet</span></span>

<span data-ttu-id="e19d2-102">Actualiza las propiedades del objeto worksheet.</span><span class="sxs-lookup"><span data-stu-id="e19d2-102">Update the properties of worksheet object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e19d2-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e19d2-103">Prerequisites</span></span>
<span data-ttu-id="e19d2-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="e19d2-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="e19d2-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e19d2-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="e19d2-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e19d2-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}
```
## <a name="optional-request-headers"></a><span data-ttu-id="e19d2-107">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="e19d2-107">Optional request headers</span></span>
| <span data-ttu-id="e19d2-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="e19d2-108">Name</span></span>       | <span data-ttu-id="e19d2-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e19d2-109">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="e19d2-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="e19d2-110">Authorization</span></span>  | <span data-ttu-id="e19d2-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e19d2-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="e19d2-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e19d2-113">Request body</span></span>
<span data-ttu-id="e19d2-p102">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="e19d2-p102">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="e19d2-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e19d2-117">Property</span></span>     | <span data-ttu-id="e19d2-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="e19d2-118">Type</span></span>   |<span data-ttu-id="e19d2-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="e19d2-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e19d2-120">name</span><span class="sxs-lookup"><span data-stu-id="e19d2-120">name</span></span>|<span data-ttu-id="e19d2-121">string</span><span class="sxs-lookup"><span data-stu-id="e19d2-121">string</span></span>|<span data-ttu-id="e19d2-122">Nombre para mostrar de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="e19d2-122">The display name of the worksheet.</span></span>|
|<span data-ttu-id="e19d2-123">position</span><span class="sxs-lookup"><span data-stu-id="e19d2-123">position</span></span>|<span data-ttu-id="e19d2-124">entero</span><span class="sxs-lookup"><span data-stu-id="e19d2-124">int</span></span>|<span data-ttu-id="e19d2-125">Posición de base cero de la hoja de cálculo dentro del libro.</span><span class="sxs-lookup"><span data-stu-id="e19d2-125">The zero-based position of the worksheet within the workbook.</span></span>|
|<span data-ttu-id="e19d2-126">visibility</span><span class="sxs-lookup"><span data-stu-id="e19d2-126">visibility</span></span>|<span data-ttu-id="e19d2-127">string</span><span class="sxs-lookup"><span data-stu-id="e19d2-127">string</span></span>|<span data-ttu-id="e19d2-p103">Visibilidad de la hoja de cálculo. Valores posibles: `Visible`, `Hidden`, `VeryHidden`.</span><span class="sxs-lookup"><span data-stu-id="e19d2-p103">The Visibility of the worksheet. Possible values are: `Visible`, `Hidden`, `VeryHidden`.</span></span>|

## <a name="response"></a><span data-ttu-id="e19d2-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e19d2-130">Response</span></span>

<span data-ttu-id="e19d2-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [Worksheet](../resources/worksheet.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e19d2-131">If successful, this method returns a `200 OK` response code and updated [Worksheet](../resources/worksheet.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e19d2-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e19d2-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e19d2-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e19d2-133">Request</span></span>
<span data-ttu-id="e19d2-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e19d2-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_worksheet"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}
Content-type: application/json
Content-length: 100

{
  "position": 99,
  "name": "name-value",
  "visibility": "visibility-value"
}
```
##### <a name="response"></a><span data-ttu-id="e19d2-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e19d2-135">Response</span></span>
<span data-ttu-id="e19d2-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e19d2-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.worksheet"
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
  "description": "Update worksheet",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->