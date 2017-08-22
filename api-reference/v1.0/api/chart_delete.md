# <a name="chart-delete"></a><span data-ttu-id="55c99-101">Chart: delete</span><span class="sxs-lookup"><span data-stu-id="55c99-101">Chart: delete</span></span>

<span data-ttu-id="55c99-102">Elimina el objeto chart.</span><span class="sxs-lookup"><span data-stu-id="55c99-102">Deletes the chart object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="55c99-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="55c99-103">Prerequisites</span></span>
<span data-ttu-id="55c99-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="55c99-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="55c99-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="55c99-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="55c99-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="55c99-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts(<name>)/delete

```
## <a name="request-headers"></a><span data-ttu-id="55c99-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="55c99-107">Request headers</span></span>
| <span data-ttu-id="55c99-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="55c99-108">Name</span></span>       | <span data-ttu-id="55c99-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="55c99-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="55c99-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="55c99-110">Authorization</span></span>  | <span data-ttu-id="55c99-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="55c99-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="55c99-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="55c99-113">Request body</span></span>

## <a name="response"></a><span data-ttu-id="55c99-114">Respuesta</span><span class="sxs-lookup"><span data-stu-id="55c99-114">Response</span></span>

<span data-ttu-id="55c99-p102">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="55c99-p102">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="55c99-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="55c99-117">Example</span></span>
<span data-ttu-id="55c99-118">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="55c99-118">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="55c99-119">Solicitud</span><span class="sxs-lookup"><span data-stu-id="55c99-119">Request</span></span>
<span data-ttu-id="55c99-120">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="55c99-120">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chart_delete"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/delete
```

##### <a name="response"></a><span data-ttu-id="55c99-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="55c99-121">Response</span></span>
<span data-ttu-id="55c99-122">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="55c99-122">Here is an example of the response.</span></span> 
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
  "description": "Chart: delete",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->