# <a name="update-worksheet"></a><span data-ttu-id="11a5d-101">Update worksheet</span><span class="sxs-lookup"><span data-stu-id="11a5d-101">Update worksheet</span></span>

<span data-ttu-id="11a5d-102">Actualizar las propiedades del objeto worksheet.</span><span class="sxs-lookup"><span data-stu-id="11a5d-102">Update the properties of worksheet object.</span></span>
## <a name="permissions"></a><span data-ttu-id="11a5d-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="11a5d-103">Permissions</span></span>
<span data-ttu-id="11a5d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="11a5d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="11a5d-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="11a5d-106">Permission type</span></span>      | <span data-ttu-id="11a5d-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="11a5d-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="11a5d-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="11a5d-108">Delegated (work or school account)</span></span> | <span data-ttu-id="11a5d-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="11a5d-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="11a5d-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="11a5d-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="11a5d-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="11a5d-111">Not supported.</span></span>    |
|<span data-ttu-id="11a5d-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="11a5d-112">Application</span></span> | <span data-ttu-id="11a5d-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="11a5d-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="11a5d-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="11a5d-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}
```
## <a name="optional-request-headers"></a><span data-ttu-id="11a5d-115">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="11a5d-115">Optional request headers</span></span>
| <span data-ttu-id="11a5d-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="11a5d-116">Name</span></span>       | <span data-ttu-id="11a5d-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="11a5d-117">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="11a5d-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="11a5d-118">Authorization</span></span>  | <span data-ttu-id="11a5d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="11a5d-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="11a5d-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="11a5d-121">Request body</span></span>
<span data-ttu-id="11a5d-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="11a5d-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="11a5d-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="11a5d-125">Property</span></span>     | <span data-ttu-id="11a5d-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="11a5d-126">Type</span></span>   |<span data-ttu-id="11a5d-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="11a5d-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="11a5d-128">name</span><span class="sxs-lookup"><span data-stu-id="11a5d-128">name</span></span>|<span data-ttu-id="11a5d-129">string</span><span class="sxs-lookup"><span data-stu-id="11a5d-129">string</span></span>|<span data-ttu-id="11a5d-130">Nombre para mostrar de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="11a5d-130">The display name of the worksheet.</span></span>|
|<span data-ttu-id="11a5d-131">position</span><span class="sxs-lookup"><span data-stu-id="11a5d-131">position</span></span>|<span data-ttu-id="11a5d-132">entero</span><span class="sxs-lookup"><span data-stu-id="11a5d-132">int</span></span>|<span data-ttu-id="11a5d-133">Posición de base cero de la hoja de cálculo dentro del libro.</span><span class="sxs-lookup"><span data-stu-id="11a5d-133">The zero-based position of the worksheet within the workbook.</span></span>|
|<span data-ttu-id="11a5d-134">visibility</span><span class="sxs-lookup"><span data-stu-id="11a5d-134">visibility</span></span>|<span data-ttu-id="11a5d-135">string</span><span class="sxs-lookup"><span data-stu-id="11a5d-135">string</span></span>|<span data-ttu-id="11a5d-p104">Visibilidad de la hoja de cálculo. Valores posibles: `Visible`, `Hidden`, `VeryHidden`.</span><span class="sxs-lookup"><span data-stu-id="11a5d-p104">The Visibility of the worksheet. Possible values are: `Visible`, `Hidden`, `VeryHidden`.</span></span>|

## <a name="response"></a><span data-ttu-id="11a5d-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="11a5d-138">Response</span></span>

<span data-ttu-id="11a5d-139">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [Worksheet](../resources/worksheet.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="11a5d-139">If successful, this method returns a `200 OK` response code and updated [Worksheet](../resources/worksheet.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="11a5d-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="11a5d-140">Example</span></span>
##### <a name="request"></a><span data-ttu-id="11a5d-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="11a5d-141">Request</span></span>
<span data-ttu-id="11a5d-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="11a5d-142">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="11a5d-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="11a5d-143">Response</span></span>
<span data-ttu-id="11a5d-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="11a5d-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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