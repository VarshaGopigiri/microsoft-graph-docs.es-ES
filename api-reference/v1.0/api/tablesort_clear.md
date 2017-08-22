# <a name="tablesort-clear"></a><span data-ttu-id="ec694-101">TableSort: clear</span><span class="sxs-lookup"><span data-stu-id="ec694-101">TableSort: clear</span></span>

<span data-ttu-id="ec694-p101">Borra la ordenación que se aplica actualmente en la tabla. Aunque esto no modifica la ordenación de la tabla, borra el estado de los botones de encabezado.</span><span class="sxs-lookup"><span data-stu-id="ec694-p101">Clears the sorting that is currently on the table. While this doesn't modify the table's ordering, it clears the state of the header buttons.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ec694-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ec694-104">Prerequisites</span></span>
<span data-ttu-id="ec694-105">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="ec694-105">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="ec694-106">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ec694-106">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="ec694-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ec694-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/sort/clear
POST /workbook/worksheets/{id|name}/tables/{id|name}/sort/clear

```
## <a name="request-headers"></a><span data-ttu-id="ec694-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ec694-108">Request headers</span></span>
| <span data-ttu-id="ec694-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="ec694-109">Name</span></span>       | <span data-ttu-id="ec694-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec694-110">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="ec694-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="ec694-111">Authorization</span></span>  | <span data-ttu-id="ec694-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ec694-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="ec694-114">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ec694-114">Request body</span></span>

## <a name="response"></a><span data-ttu-id="ec694-115">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ec694-115">Response</span></span>

<span data-ttu-id="ec694-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ec694-p103">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ec694-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ec694-118">Example</span></span>
<span data-ttu-id="ec694-119">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="ec694-119">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="ec694-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ec694-120">Request</span></span>
<span data-ttu-id="ec694-121">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ec694-121">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablesort_clear"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/sort/clear
```

##### <a name="response"></a><span data-ttu-id="ec694-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ec694-122">Response</span></span>
<span data-ttu-id="ec694-123">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ec694-123">Here is an example of the response.</span></span> 
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
  "description": "TableSort: clear",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->