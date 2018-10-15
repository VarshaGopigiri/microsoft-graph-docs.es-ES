# <a name="list-tablecollection"></a><span data-ttu-id="6774d-101">Enumerar TableCollection</span><span class="sxs-lookup"><span data-stu-id="6774d-101">List TableCollection</span></span>

<span data-ttu-id="6774d-102">Recuperar una lista de objetos table.</span><span class="sxs-lookup"><span data-stu-id="6774d-102">Retrieve a list of table objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="6774d-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="6774d-103">Permissions</span></span>
<span data-ttu-id="6774d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6774d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6774d-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6774d-106">Permission type</span></span>      | <span data-ttu-id="6774d-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6774d-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6774d-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6774d-108">Delegated (work or school account)</span></span> | <span data-ttu-id="6774d-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6774d-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="6774d-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6774d-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6774d-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6774d-111">Not supported.</span></span>    |
|<span data-ttu-id="6774d-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6774d-112">Application</span></span> | <span data-ttu-id="6774d-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6774d-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="6774d-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6774d-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/tables
GET /workbook/worksheets/{id|name}/tables
```
## <a name="optional-query-parameters"></a><span data-ttu-id="6774d-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="6774d-115">Optional query parameters</span></span>
<span data-ttu-id="6774d-116">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6774d-116">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="6774d-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6774d-117">Request headers</span></span>
| <span data-ttu-id="6774d-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="6774d-118">Name</span></span>      |<span data-ttu-id="6774d-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="6774d-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="6774d-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="6774d-120">Authorization</span></span>  | <span data-ttu-id="6774d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6774d-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="6774d-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="6774d-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="6774d-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="6774d-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="6774d-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6774d-126">Request body</span></span>
<span data-ttu-id="6774d-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6774d-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6774d-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6774d-128">Response</span></span>

<span data-ttu-id="6774d-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [WorkbookTable](../resources/table.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6774d-129">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/table.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="6774d-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6774d-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6774d-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6774d-131">Request</span></span>
<span data-ttu-id="6774d-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6774d-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_tablecollection"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables
```
##### <a name="response"></a><span data-ttu-id="6774d-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6774d-133">Response</span></span>
<span data-ttu-id="6774d-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6774d-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookTable",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 158

{
  "value": [
    {
      "id": "99",
      "name": "name-value",
      "showHeaders": true,
      "showTotals": true,
      "style": "style-value"
    }
  ]
}
```
> <span data-ttu-id="6774d-137">**Nota**: Use los parámetros de consulta [$top](https://developer.microsoft.com/en-us/graph/docs/concepts/query_parameters#top) y [$skip](https://developer.microsoft.com/en-us/graph/docs/concepts/query_parameters#top) para examinar un gran número de tablas.</span><span class="sxs-lookup"><span data-stu-id="6774d-137">**Note:** Use the [$top](https://developer.microsoft.com/en-us/graph/docs/concepts/query_parameters#top) and [$skip](https://developer.microsoft.com/en-us/graph/docs/concepts/query_parameters#top) query parameters to page through large numbers of tables.</span></span>

<span data-ttu-id="6774d-138">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="6774d-138">Example:</span></span> 

`https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables?$top=5`
`https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables?$top=5&$skip=5`

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List TableCollection",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
