# <a name="list-names"></a><span data-ttu-id="1ece8-101">Incluir en una lista los nombres</span><span class="sxs-lookup"><span data-stu-id="1ece8-101">List names</span></span>

<span data-ttu-id="1ece8-102">Recupere una lista del elemento con nombre asociada a la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="1ece8-102">Retrieve a list of named item associated with the worksheet.</span></span> 
## <a name="prerequisites"></a><span data-ttu-id="1ece8-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1ece8-103">Prerequisites</span></span>
<span data-ttu-id="1ece8-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="1ece8-104">One of the following **scopes** is required to execute this API:</span></span>

  * <span data-ttu-id="1ece8-105">Files.Read</span><span class="sxs-lookup"><span data-stu-id="1ece8-105">Files.Read</span></span>
  * <span data-ttu-id="1ece8-106">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1ece8-106">Files.ReadWrite</span></span>
  * <span data-ttu-id="1ece8-107">Sites.Read.All</span><span class="sxs-lookup"><span data-stu-id="1ece8-107">Sites.Read.All</span></span>

## <a name="http-request"></a><span data-ttu-id="1ece8-108">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1ece8-108">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets({id|name})/names
```
## <a name="optional-query-parameters"></a><span data-ttu-id="1ece8-109">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1ece8-109">Optional query parameters</span></span>
<span data-ttu-id="1ece8-110">Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1ece8-110">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="1ece8-111">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1ece8-111">Request headers</span></span>
| <span data-ttu-id="1ece8-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="1ece8-112">Name</span></span>      |<span data-ttu-id="1ece8-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ece8-113">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="1ece8-114">Authorization</span><span class="sxs-lookup"><span data-stu-id="1ece8-114">Authorization</span></span>  | <span data-ttu-id="1ece8-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1ece8-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="1ece8-117">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1ece8-117">Request body</span></span>
<span data-ttu-id="1ece8-118">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1ece8-118">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1ece8-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1ece8-119">Response</span></span>

<span data-ttu-id="1ece8-120">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [NamedItem](../resources/nameditem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1ece8-120">If successful, this method returns a `200 OK` response code and collection of [NamedItem](../resources/nameditem.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="1ece8-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1ece8-121">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1ece8-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1ece8-122">Request</span></span>
<span data-ttu-id="1ece8-123">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1ece8-123">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_tables"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/names
```
##### <a name="response"></a><span data-ttu-id="1ece8-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1ece8-124">Response</span></span>
<span data-ttu-id="1ece8-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1ece8-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.namedItem",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 158

{
  "value": [
    {
      "name": "myrange",
      "scope": "worksheet"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List tables",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
