# <a name="get-icon"></a><span data-ttu-id="2c9c4-101">Get Icon</span><span class="sxs-lookup"><span data-stu-id="2c9c4-101">Get Icon</span></span>

<span data-ttu-id="2c9c4-102">Recupera las propiedades y relaciones del objeto icon.</span><span class="sxs-lookup"><span data-stu-id="2c9c4-102">Retrieve the properties and relationships of icon object.</span></span>
## <a name="permissions"></a><span data-ttu-id="2c9c4-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="2c9c4-103">Permissions</span></span>
<span data-ttu-id="2c9c4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="2c9c4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="2c9c4-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2c9c4-106">Permission type</span></span>      | <span data-ttu-id="2c9c4-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2c9c4-107">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="2c9c4-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2c9c4-108">Delegated (work or school account)</span></span> | <span data-ttu-id="2c9c4-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2c9c4-109">Files.ReadWrite</span></span>    | 
|<span data-ttu-id="2c9c4-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2c9c4-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2c9c4-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2c9c4-111">Not supported.</span></span>    | 
|<span data-ttu-id="2c9c4-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2c9c4-112">Application</span></span> | <span data-ttu-id="2c9c4-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2c9c4-113">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="2c9c4-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2c9c4-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/tables/{id|name}/sort/fields/icon
GET /workbook/worksheets/{id|name}/tables/{id|name}/sort/fields/icon
```
## <a name="optional-query-parameters"></a><span data-ttu-id="2c9c4-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="2c9c4-115">Optional query parameters</span></span>
<span data-ttu-id="2c9c4-116">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2c9c4-116">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="2c9c4-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2c9c4-117">Request headers</span></span>
| <span data-ttu-id="2c9c4-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="2c9c4-118">Name</span></span>      |<span data-ttu-id="2c9c4-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c9c4-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="2c9c4-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="2c9c4-120">Authorization</span></span>  | <span data-ttu-id="2c9c4-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2c9c4-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="2c9c4-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2c9c4-123">Request body</span></span>
<span data-ttu-id="2c9c4-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2c9c4-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2c9c4-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2c9c4-125">Response</span></span>

<span data-ttu-id="2c9c4-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [Icon](../resources/icon.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2c9c4-126">If successful, this method returns a `200 OK` response code and [Icon](../resources/icon.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="2c9c4-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2c9c4-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2c9c4-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2c9c4-128">Request</span></span>
<span data-ttu-id="2c9c4-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2c9c4-129">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_icon"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/sort/fields/icon
```
##### <a name="response"></a><span data-ttu-id="2c9c4-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2c9c4-130">Response</span></span>
<span data-ttu-id="2c9c4-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2c9c4-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookIcon"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 39

{
  "set": "set-value",
  "index": 99
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get Icon",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->