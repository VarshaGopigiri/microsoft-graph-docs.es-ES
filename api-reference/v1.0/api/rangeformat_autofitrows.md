# <a name="rangeformat-autofitrows"></a><span data-ttu-id="b33be-101">RangeFormat: autofitRows</span><span class="sxs-lookup"><span data-stu-id="b33be-101">RangeFormat: autofitRows</span></span>

<span data-ttu-id="b33be-102">Cambia el alto de las filas del rango actual para obtener el ajuste perfecto (según los datos actuales de las columnas).</span><span class="sxs-lookup"><span data-stu-id="b33be-102">Changes the height of the rows of the current range to achieve the best fit, based on the current data in the columns.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b33be-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b33be-103">Prerequisites</span></span>
<span data-ttu-id="b33be-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="b33be-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="b33be-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b33be-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="b33be-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b33be-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names(<name>)/range/format/autofitRows
POST /workbook/worksheets/{id|name}/range(<address>)/format/autofitRows
POST /workbook/tables/{id|name}/columns/{id|name}/range/format/autofitRows

```
## <a name="request-headers"></a><span data-ttu-id="b33be-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b33be-107">Request headers</span></span>
| <span data-ttu-id="b33be-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="b33be-108">Name</span></span>       | <span data-ttu-id="b33be-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b33be-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="b33be-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="b33be-110">Authorization</span></span>  | <span data-ttu-id="b33be-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b33be-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="b33be-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b33be-113">Request body</span></span>

## <a name="response"></a><span data-ttu-id="b33be-114">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b33be-114">Response</span></span>

<span data-ttu-id="b33be-p102">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b33be-p102">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b33be-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b33be-117">Example</span></span>
<span data-ttu-id="b33be-118">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="b33be-118">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="b33be-119">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b33be-119">Request</span></span>
<span data-ttu-id="b33be-120">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b33be-120">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "rangeformat_autofitrows"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/format/autofitRows
```

##### <a name="response"></a><span data-ttu-id="b33be-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b33be-121">Response</span></span>
<span data-ttu-id="b33be-122">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b33be-122">Here is an example of the response.</span></span> 
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
  "description": "RangeFormat: autofitRows",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->