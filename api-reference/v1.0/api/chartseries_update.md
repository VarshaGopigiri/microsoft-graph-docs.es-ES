# <a name="update-chartseries"></a><span data-ttu-id="9eec7-101">Actualizar chartseries</span><span class="sxs-lookup"><span data-stu-id="9eec7-101">Update chartseries</span></span>

<span data-ttu-id="9eec7-102">Actualizar las propiedades del objeto chartserie.</span><span class="sxs-lookup"><span data-stu-id="9eec7-102">Update the properties of chartseries object.</span></span>
## <a name="permissions"></a><span data-ttu-id="9eec7-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="9eec7-103">Permissions</span></span>
<span data-ttu-id="9eec7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9eec7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9eec7-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9eec7-106">Permission type</span></span>      | <span data-ttu-id="9eec7-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9eec7-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9eec7-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9eec7-108">Delegated (work or school account)</span></span> | <span data-ttu-id="9eec7-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9eec7-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="9eec7-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9eec7-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9eec7-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9eec7-111">Not supported.</span></span>    |
|<span data-ttu-id="9eec7-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9eec7-112">Application</span></span> | <span data-ttu-id="9eec7-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9eec7-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="9eec7-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9eec7-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts(<name>)/series(<undefined>)
```
## <a name="optional-request-headers"></a><span data-ttu-id="9eec7-115">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="9eec7-115">Optional request headers</span></span>
| <span data-ttu-id="9eec7-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="9eec7-116">Name</span></span>       | <span data-ttu-id="9eec7-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="9eec7-117">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="9eec7-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="9eec7-118">Authorization</span></span>  | <span data-ttu-id="9eec7-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9eec7-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9eec7-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9eec7-121">Request body</span></span>
<span data-ttu-id="9eec7-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="9eec7-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="9eec7-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9eec7-125">Property</span></span>     | <span data-ttu-id="9eec7-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="9eec7-126">Type</span></span>   |<span data-ttu-id="9eec7-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="9eec7-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9eec7-128">name</span><span class="sxs-lookup"><span data-stu-id="9eec7-128">name</span></span>|<span data-ttu-id="9eec7-129">string</span><span class="sxs-lookup"><span data-stu-id="9eec7-129">string</span></span>|<span data-ttu-id="9eec7-130">Representa el nombre de una serie de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="9eec7-130">Represents the name of a series in a chart.</span></span>|

## <a name="response"></a><span data-ttu-id="9eec7-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9eec7-131">Response</span></span>

<span data-ttu-id="9eec7-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [ChartSeries](../resources/chartseries.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9eec7-132">If successful, this method returns a `200 OK` response code and updated [ChartSeries](../resources/chartseries.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="9eec7-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9eec7-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9eec7-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9eec7-134">Request</span></span>
<span data-ttu-id="9eec7-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9eec7-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chartseries"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/series(<undefined>)
Content-type: application/json
Content-length: 26

{
  "name": "name-value"
}
```
##### <a name="response"></a><span data-ttu-id="9eec7-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9eec7-136">Response</span></span>
<span data-ttu-id="9eec7-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9eec7-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartSeries"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 26

{
  "name": "name-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update chartseries",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->