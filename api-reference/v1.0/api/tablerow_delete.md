# <a name="tablerow-delete"></a><span data-ttu-id="cd998-101">TableRow: delete</span><span class="sxs-lookup"><span data-stu-id="cd998-101">TableRow: delete</span></span>

<span data-ttu-id="cd998-102">Elimina la fila de la tabla.</span><span class="sxs-lookup"><span data-stu-id="cd998-102">Deletes the row from the table.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cd998-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cd998-103">Prerequisites</span></span>
<span data-ttu-id="cd998-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="cd998-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="cd998-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cd998-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="cd998-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cd998-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/rows(<index>)/delete
POST /workbook/worksheets/{id|name}/tables/{id|name}/rows(<index>)/delete

```
## <a name="request-headers"></a><span data-ttu-id="cd998-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cd998-107">Request headers</span></span>
| <span data-ttu-id="cd998-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="cd998-108">Name</span></span>       | <span data-ttu-id="cd998-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd998-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="cd998-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="cd998-110">Authorization</span></span>  | <span data-ttu-id="cd998-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cd998-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="cd998-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cd998-113">Request body</span></span>

## <a name="response"></a><span data-ttu-id="cd998-114">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cd998-114">Response</span></span>

<span data-ttu-id="cd998-p102">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cd998-p102">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cd998-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd998-117">Example</span></span>
<span data-ttu-id="cd998-118">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="cd998-118">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="cd998-119">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cd998-119">Request</span></span>
<span data-ttu-id="cd998-120">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cd998-120">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablerow_delete"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/rows(<index>)/delete
```

##### <a name="response"></a><span data-ttu-id="cd998-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cd998-121">Response</span></span>
<span data-ttu-id="cd998-122">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cd998-122">Here is an example of the response.</span></span> 
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
  "description": "TableRow: delete",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->