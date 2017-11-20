# <a name="list-names"></a><span data-ttu-id="4a355-101">Incluir en una lista los nombres</span><span class="sxs-lookup"><span data-stu-id="4a355-101">List names</span></span>

<span data-ttu-id="4a355-102">Recuperar una lista del elemento con nombre asociada a la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="4a355-102">Retrieve a list of named item associated with the worksheet.</span></span> 
## <a name="permissions"></a><span data-ttu-id="4a355-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="4a355-103">Permissions</span></span>
<span data-ttu-id="4a355-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="4a355-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="4a355-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4a355-106">Permission type</span></span>      | <span data-ttu-id="4a355-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4a355-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4a355-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4a355-108">Delegated (work or school account)</span></span> | <span data-ttu-id="4a355-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4a355-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="4a355-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4a355-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4a355-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4a355-111">Not supported.</span></span>    |
|<span data-ttu-id="4a355-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4a355-112">Application</span></span> | <span data-ttu-id="4a355-113">Sites.Read.All</span><span class="sxs-lookup"><span data-stu-id="4a355-113">Sites.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="4a355-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4a355-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets({id|name})/names
```
## <a name="optional-query-parameters"></a><span data-ttu-id="4a355-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="4a355-115">Optional query parameters</span></span>
<span data-ttu-id="4a355-116">Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4a355-116">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="4a355-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4a355-117">Request headers</span></span>
| <span data-ttu-id="4a355-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="4a355-118">Name</span></span>      |<span data-ttu-id="4a355-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a355-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="4a355-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="4a355-120">Authorization</span></span>  | <span data-ttu-id="4a355-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4a355-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="4a355-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="4a355-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="4a355-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="4a355-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="4a355-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4a355-126">Request body</span></span>
<span data-ttu-id="4a355-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4a355-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4a355-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4a355-128">Response</span></span>

<span data-ttu-id="4a355-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [NamedItem](../resources/nameditem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4a355-129">If successful, this method returns a `200 OK` response code and collection of [NamedItem](../resources/nameditem.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="4a355-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4a355-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4a355-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4a355-131">Request</span></span>
<span data-ttu-id="4a355-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4a355-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_tables"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/names
```
##### <a name="response"></a><span data-ttu-id="4a355-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4a355-133">Response</span></span>
<span data-ttu-id="4a355-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4a355-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
