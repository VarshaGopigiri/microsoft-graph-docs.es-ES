# <a name="get-directoryobject"></a><span data-ttu-id="51852-101">Obtener directoryObject</span><span class="sxs-lookup"><span data-stu-id="51852-101">Get directoryObject</span></span>

<span data-ttu-id="51852-102">Recupera las propiedades y relaciones del objeto directoryObject.</span><span class="sxs-lookup"><span data-stu-id="51852-102">Retrieve the properties and relationships of directoryObject object.</span></span>
## <a name="permissions"></a><span data-ttu-id="51852-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="51852-103">Permissions</span></span>
<span data-ttu-id="51852-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="51852-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="51852-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="51852-106">Permission type</span></span>      | <span data-ttu-id="51852-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="51852-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="51852-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="51852-108">Delegated (work or school account)</span></span> | <span data-ttu-id="51852-109">Directory.Read.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="51852-109">Directory.Read.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="51852-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="51852-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="51852-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="51852-111">Not supported.</span></span>    |
|<span data-ttu-id="51852-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="51852-112">Application</span></span> | <span data-ttu-id="51852-113">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="51852-113">Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="51852-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="51852-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /directoryObjects/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="51852-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="51852-115">Optional query parameters</span></span>
<span data-ttu-id="51852-116">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="51852-116">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="51852-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="51852-117">Request headers</span></span>
| <span data-ttu-id="51852-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="51852-118">Name</span></span>       | <span data-ttu-id="51852-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="51852-119">Type</span></span> | <span data-ttu-id="51852-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="51852-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="51852-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="51852-121">Authorization</span></span>  | <span data-ttu-id="51852-122">string</span><span class="sxs-lookup"><span data-stu-id="51852-122">string</span></span>  | <span data-ttu-id="51852-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="51852-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="51852-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="51852-125">Request body</span></span>
<span data-ttu-id="51852-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="51852-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="51852-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="51852-127">Response</span></span>

<span data-ttu-id="51852-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="51852-128">If successful, this method returns a `200 OK` response code and [directoryObject](../resources/directoryobject.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="51852-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="51852-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="51852-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="51852-130">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_directoryobject"
}-->
```http
GET https://graph.microsoft.com/v1.0/directoryObjects/{id}
```
##### <a name="response"></a><span data-ttu-id="51852-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="51852-131">Response</span></span>
<span data-ttu-id="51852-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="51852-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
