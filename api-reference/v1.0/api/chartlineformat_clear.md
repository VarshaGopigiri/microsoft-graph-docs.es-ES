# <a name="chartlineformat-clear"></a><span data-ttu-id="6621d-101">ChartLineFormat: clear</span><span class="sxs-lookup"><span data-stu-id="6621d-101">ChartLineFormat: clear</span></span>

<span data-ttu-id="6621d-102">Borra el formato de línea de un elemento de gráfico.</span><span class="sxs-lookup"><span data-stu-id="6621d-102">Clear the line format of a chart element.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6621d-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6621d-103">Prerequisites</span></span>
<span data-ttu-id="6621d-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="6621d-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="6621d-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6621d-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="6621d-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6621d-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts(<name>)/axes/seriesaxis/format/line/clear
POST /workbook/worksheets/{id|name}/charts(<name>)/axes/categoryaxis/format/line/clear
POST /workbook/worksheets/{id|name}/charts(<name>)/axes/seriesaxis/majorgridlines/format/line/clear

```
## <a name="request-headers"></a><span data-ttu-id="6621d-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6621d-107">Request headers</span></span>
| <span data-ttu-id="6621d-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="6621d-108">Name</span></span>       | <span data-ttu-id="6621d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="6621d-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="6621d-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="6621d-110">Authorization</span></span>  | <span data-ttu-id="6621d-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6621d-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="6621d-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6621d-113">Request body</span></span>

## <a name="response"></a><span data-ttu-id="6621d-114">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6621d-114">Response</span></span>

<span data-ttu-id="6621d-p102">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6621d-p102">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6621d-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6621d-117">Example</span></span>
<span data-ttu-id="6621d-118">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="6621d-118">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="6621d-119">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6621d-119">Request</span></span>
<span data-ttu-id="6621d-120">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6621d-120">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chartlineformat_clear"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/axes/seriesaxis/format/line/clear
```

##### <a name="response"></a><span data-ttu-id="6621d-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6621d-121">Response</span></span>
<span data-ttu-id="6621d-122">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6621d-122">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.none"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartLineFormat: clear",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->