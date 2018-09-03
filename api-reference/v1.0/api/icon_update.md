# <a name="update-icon"></a><span data-ttu-id="a40c8-101">Update icon</span><span class="sxs-lookup"><span data-stu-id="a40c8-101">Update icon</span></span>

<span data-ttu-id="a40c8-102">Actualiza las propiedades del objeto icon.</span><span class="sxs-lookup"><span data-stu-id="a40c8-102">Update the properties of icon object.</span></span>
## <a name="permissions"></a><span data-ttu-id="a40c8-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="a40c8-103">Permissions</span></span>
<span data-ttu-id="a40c8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a40c8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="a40c8-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a40c8-106">Permission type</span></span>      | <span data-ttu-id="a40c8-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a40c8-107">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="a40c8-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a40c8-108">Delegated (work or school account)</span></span> | <span data-ttu-id="a40c8-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a40c8-109">Files.ReadWrite</span></span>    | 
|<span data-ttu-id="a40c8-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a40c8-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a40c8-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a40c8-111">Not supported.</span></span>    | 
|<span data-ttu-id="a40c8-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a40c8-112">Application</span></span> | <span data-ttu-id="a40c8-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a40c8-113">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="a40c8-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a40c8-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/tables/{id|name}/sort/fields/icon
PATCH /workbook/worksheets/{id|name}/tables/{id|name}/sort/fields/icon
```
## <a name="optional-request-headers"></a><span data-ttu-id="a40c8-115">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="a40c8-115">Optional request headers</span></span>
| <span data-ttu-id="a40c8-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="a40c8-116">Name</span></span>       | <span data-ttu-id="a40c8-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="a40c8-117">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="a40c8-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="a40c8-118">Authorization</span></span>  | <span data-ttu-id="a40c8-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a40c8-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="a40c8-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a40c8-121">Request body</span></span>
<span data-ttu-id="a40c8-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="a40c8-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="a40c8-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a40c8-125">Property</span></span>     | <span data-ttu-id="a40c8-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="a40c8-126">Type</span></span>   |<span data-ttu-id="a40c8-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="a40c8-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a40c8-128">index</span><span class="sxs-lookup"><span data-stu-id="a40c8-128">index</span></span>|<span data-ttu-id="a40c8-129">entero</span><span class="sxs-lookup"><span data-stu-id="a40c8-129">int</span></span>|<span data-ttu-id="a40c8-130">Representa el índice del icono en el conjunto concreto.</span><span class="sxs-lookup"><span data-stu-id="a40c8-130">Represents the index of the icon in the given set.</span></span>|
|<span data-ttu-id="a40c8-131">set</span><span class="sxs-lookup"><span data-stu-id="a40c8-131">set</span></span>|<span data-ttu-id="a40c8-132">cadena</span><span class="sxs-lookup"><span data-stu-id="a40c8-132">string</span></span>|<span data-ttu-id="a40c8-133">Representa el conjunto del que el icono de forma parte.</span><span class="sxs-lookup"><span data-stu-id="a40c8-133">Represents the set that the icon is part of. Possible values are: , , , , , , , , , , , , , , , , , , , , .</span></span> <span data-ttu-id="a40c8-134">Los valores posibles son: `Invalid`, `ThreeArrows`, `ThreeArrowsGray`, `ThreeFlags`, `ThreeTrafficLights1`, `ThreeTrafficLights2`, `ThreeSigns`, `ThreeSymbols`, `ThreeSymbols2`, `FourArrows`, `FourArrowsGray`, `FourRedToBlack`, `FourRating`, `FourTrafficLights`, `FiveArrows`, `FiveArrowsGray`, `FiveRating`, `FiveQuarters`, `ThreeStars`, `ThreeTriangles` y `FiveBoxes`.</span><span class="sxs-lookup"><span data-stu-id="a40c8-134">The possible values are: `Invalid`, `ThreeArrows`, `ThreeArrowsGray`, `ThreeFlags`, `ThreeTrafficLights1`, `ThreeTrafficLights2`, `ThreeSigns`, `ThreeSymbols`, `ThreeSymbols2`, `FourArrows`, `FourArrowsGray`, `FourRedToBlack`, `FourRating`, `FourTrafficLights`, `FiveArrows`, `FiveArrowsGray`, `FiveRating`, `FiveQuarters`, `ThreeStars`, `ThreeTriangles`, `FiveBoxes`.</span></span>|

## <a name="response"></a><span data-ttu-id="a40c8-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a40c8-135">Response</span></span>

<span data-ttu-id="a40c8-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [Icon](../resources/icon.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a40c8-136">If successful, this method returns a `200 OK` response code and updated [Icon](../resources/icon.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="a40c8-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a40c8-137">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a40c8-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a40c8-138">Request</span></span>
<span data-ttu-id="a40c8-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a40c8-139">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_icon"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/sort/fields/icon
Content-type: application/json
Content-length: 39

{
  "set": "set-value",
  "index": 99
}
```
##### <a name="response"></a><span data-ttu-id="a40c8-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a40c8-140">Response</span></span>
<span data-ttu-id="a40c8-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a40c8-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookIcon"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 39

{
  "set": "set-value",
  "index": 99
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update icon",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->