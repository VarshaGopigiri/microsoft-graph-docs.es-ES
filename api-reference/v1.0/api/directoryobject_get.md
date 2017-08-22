# <a name="get-directoryobject"></a><span data-ttu-id="c1dab-101">Obtener directoryObject</span><span class="sxs-lookup"><span data-stu-id="c1dab-101">Get directoryObject</span></span>

<span data-ttu-id="c1dab-102">Recupera las propiedades y relaciones del objeto directoryObject.</span><span class="sxs-lookup"><span data-stu-id="c1dab-102">Retrieve the properties and relationships of directoryObject object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c1dab-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c1dab-103">Prerequisites</span></span>
<span data-ttu-id="c1dab-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="c1dab-104">One of the following **scopes** is required to execute this API:</span></span> 
- <span data-ttu-id="c1dab-105">_Directory.Read.All_</span><span class="sxs-lookup"><span data-stu-id="c1dab-105">_Directory.Read.All_</span></span> 
- <span data-ttu-id="c1dab-106">_Directory.AccessAsUser.All_</span><span class="sxs-lookup"><span data-stu-id="c1dab-106">_Directory.AccessAsUser.All_</span></span>

> <span data-ttu-id="c1dab-107">Nota: Los ámbitos de permiso se muestran por orden de privilegio mínimo necesario.</span><span class="sxs-lookup"><span data-stu-id="c1dab-107">Note: Permission scopes are listed in least privilege required order.</span></span>

## <a name="http-request"></a><span data-ttu-id="c1dab-108">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c1dab-108">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /directoryObjects/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="c1dab-109">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c1dab-109">Optional query parameters</span></span>
<span data-ttu-id="c1dab-110">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c1dab-110">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="c1dab-111">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c1dab-111">Request headers</span></span>
| <span data-ttu-id="c1dab-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="c1dab-112">Name</span></span>       | <span data-ttu-id="c1dab-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="c1dab-113">Type</span></span> | <span data-ttu-id="c1dab-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1dab-114">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="c1dab-115">Authorization</span><span class="sxs-lookup"><span data-stu-id="c1dab-115">Authorization</span></span>  | <span data-ttu-id="c1dab-116">string</span><span class="sxs-lookup"><span data-stu-id="c1dab-116">string</span></span>  | <span data-ttu-id="c1dab-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c1dab-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c1dab-119">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c1dab-119">Request body</span></span>
<span data-ttu-id="c1dab-120">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c1dab-120">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c1dab-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c1dab-121">Response</span></span>

<span data-ttu-id="c1dab-122">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c1dab-122">If successful, this method returns a `200 OK` response code and [directoryObject](../resources/directoryobject.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c1dab-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c1dab-123">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c1dab-124">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c1dab-124">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_directoryobject"
}-->
```http
GET https://graph.microsoft.com/v1.0/directoryObjects/{id}
```
##### <a name="response"></a><span data-ttu-id="c1dab-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c1dab-125">Response</span></span>
<span data-ttu-id="c1dab-p102">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c1dab-p102">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get directoryObject",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
