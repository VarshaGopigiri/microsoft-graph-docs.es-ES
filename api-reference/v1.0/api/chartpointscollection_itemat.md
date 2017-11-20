# <a name="chartpointscollection-itemat"></a><span data-ttu-id="78334-101">ChartPointsCollection: ItemAt</span><span class="sxs-lookup"><span data-stu-id="78334-101">ChartPointsCollection: ItemAt</span></span>

<span data-ttu-id="78334-102">Recuperar un punto en función de su posición dentro de la serie.</span><span class="sxs-lookup"><span data-stu-id="78334-102">Retrieve a point based on its position within the series.</span></span>
## <a name="permissions"></a><span data-ttu-id="78334-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="78334-103">Permissions</span></span>
<span data-ttu-id="78334-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="78334-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="78334-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="78334-106">Permission type</span></span>      | <span data-ttu-id="78334-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="78334-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="78334-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="78334-108">Delegated (work or school account)</span></span> | <span data-ttu-id="78334-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="78334-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="78334-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="78334-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="78334-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="78334-111">Not supported.</span></span>    |
|<span data-ttu-id="78334-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="78334-112">Application</span></span> | <span data-ttu-id="78334-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="78334-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="78334-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="78334-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts(<name>)/series(<undefined>)/points/ItemAt

```
## <a name="request-headers"></a><span data-ttu-id="78334-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="78334-115">Request headers</span></span>
| <span data-ttu-id="78334-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="78334-116">Name</span></span>       | <span data-ttu-id="78334-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="78334-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="78334-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="78334-118">Authorization</span></span>  | <span data-ttu-id="78334-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="78334-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="78334-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="78334-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="78334-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="78334-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="78334-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="78334-124">Request body</span></span>
<span data-ttu-id="78334-125">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="78334-125">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="78334-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="78334-126">Parameter</span></span>    | <span data-ttu-id="78334-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="78334-127">Type</span></span>   |<span data-ttu-id="78334-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="78334-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="78334-129">index</span><span class="sxs-lookup"><span data-stu-id="78334-129">index</span></span>|<span data-ttu-id="78334-130">number</span><span class="sxs-lookup"><span data-stu-id="78334-130">number</span></span>|<span data-ttu-id="78334-p104">Valor de índice del objeto que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="78334-p104">Index value of the object to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="78334-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="78334-133">Response</span></span>

<span data-ttu-id="78334-134">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [ChartPoint](../resources/chartpoint.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="78334-134">If successful, this method returns `200 OK` response code and [ChartPoint](../resources/chartpoint.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="78334-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="78334-135">Example</span></span>
<span data-ttu-id="78334-136">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="78334-136">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="78334-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="78334-137">Request</span></span>
<span data-ttu-id="78334-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="78334-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chartpointscollection_itemat"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/series(<undefined>)/points/ItemAt
Content-type: application/json
Content-length: 20

{
  "index": {
  }
}
```

##### <a name="response"></a><span data-ttu-id="78334-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="78334-139">Response</span></span>
<span data-ttu-id="78334-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="78334-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartPoint"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 20

{
  "value": {
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartPointsCollection: ItemAt",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->