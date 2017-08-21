# <a name="create-chartpoints"></a><span data-ttu-id="64e8b-101">Create ChartPoints</span><span class="sxs-lookup"><span data-stu-id="64e8b-101">Create ChartPoints</span></span>

<span data-ttu-id="64e8b-102">Use esta API para crear un objeto ChartPoints.</span><span class="sxs-lookup"><span data-stu-id="64e8b-102">Use this API to create a new ChartPoints.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="64e8b-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="64e8b-103">Prerequisites</span></span>
<span data-ttu-id="64e8b-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="64e8b-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="64e8b-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="64e8b-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="64e8b-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="64e8b-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts(<name>)/series(<undefined>)/points

```
## <a name="request-headers"></a><span data-ttu-id="64e8b-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="64e8b-107">Request headers</span></span>
| <span data-ttu-id="64e8b-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="64e8b-108">Name</span></span>       | <span data-ttu-id="64e8b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="64e8b-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="64e8b-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="64e8b-110">Authorization</span></span>  | <span data-ttu-id="64e8b-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="64e8b-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="64e8b-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="64e8b-113">Request body</span></span>
<span data-ttu-id="64e8b-114">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [ChartPoints](../resources/chartpoint.md).</span><span class="sxs-lookup"><span data-stu-id="64e8b-114">In the request body, supply a JSON representation of [ChartPoints](../resources/chartpoint.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="64e8b-115">Respuesta</span><span class="sxs-lookup"><span data-stu-id="64e8b-115">Response</span></span>

<span data-ttu-id="64e8b-116">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [ChartPoints](../resources/chartpoint.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="64e8b-116">If successful, this method returns `201, Created` response code and [ChartPoints](../resources/chartpoint.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="64e8b-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="64e8b-117">Example</span></span>
##### <a name="request"></a><span data-ttu-id="64e8b-118">Solicitud</span><span class="sxs-lookup"><span data-stu-id="64e8b-118">Request</span></span>
<span data-ttu-id="64e8b-119">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="64e8b-119">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_chartpoints_from_chartseries"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/series(<undefined>)/points
Content-type: application/json
Content-length: 3

{
}
```
<span data-ttu-id="64e8b-120">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [ChartPoints](../resources/chartpoint.md).</span><span class="sxs-lookup"><span data-stu-id="64e8b-120">In the request body, supply a JSON representation of [ChartPoints](../resources/chartpoint.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="64e8b-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="64e8b-121">Response</span></span>
<span data-ttu-id="64e8b-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="64e8b-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartPoint"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 3

{
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create ChartPoints",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->