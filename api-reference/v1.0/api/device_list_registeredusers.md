# <a name="list-registeredusers"></a><span data-ttu-id="56b23-101">List registeredUsers</span><span class="sxs-lookup"><span data-stu-id="56b23-101">List registeredUsers</span></span>

<span data-ttu-id="56b23-102">Recupera una lista de usuarios que son usuarios registrados del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56b23-102">Retrieve a list of users that are registered users of the device.</span></span>

<span data-ttu-id="56b23-103">En el caso de los dispositivos unidos a la nube y los dispositivos personales registrados, los usuarios registrados se establecen en el mismo valor que los propietarios registrados en el momento del registro.</span><span class="sxs-lookup"><span data-stu-id="56b23-103">For cloud joined devices and registered personal devices, registered users are set to the same value as registered owners at the time of registration.</span></span>

## <a name="permissions"></a><span data-ttu-id="56b23-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="56b23-104">Permissions</span></span>
<span data-ttu-id="56b23-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="56b23-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="56b23-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="56b23-107">Permission type</span></span>      | <span data-ttu-id="56b23-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="56b23-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="56b23-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="56b23-109">Delegated (work or school account)</span></span> | <span data-ttu-id="56b23-110">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="56b23-110">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="56b23-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="56b23-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="56b23-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="56b23-112">Not supported.</span></span>    |
|<span data-ttu-id="56b23-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="56b23-113">Application</span></span> | <span data-ttu-id="56b23-114">Device.ReadWrite.All y User.ReadBasic.All, Directory.Read.All o Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="56b23-114">Device.ReadWrite.All and User.ReadBasic.All or Directory.Read.All or Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="56b23-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="56b23-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /devices/{id}/registeredUsers
```
## <a name="optional-query-parameters"></a><span data-ttu-id="56b23-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="56b23-116">Optional query parameters</span></span>
<span data-ttu-id="56b23-117">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="56b23-117">This method supports the [OData Query Parameters](http://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="56b23-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="56b23-118">Request headers</span></span>
| <span data-ttu-id="56b23-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="56b23-119">Name</span></span>       | <span data-ttu-id="56b23-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="56b23-120">Type</span></span> | <span data-ttu-id="56b23-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="56b23-121">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="56b23-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="56b23-122">Authorization</span></span>  | <span data-ttu-id="56b23-123">string</span><span class="sxs-lookup"><span data-stu-id="56b23-123">string</span></span>  | <span data-ttu-id="56b23-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="56b23-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="56b23-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="56b23-126">Request body</span></span>
<span data-ttu-id="56b23-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="56b23-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="56b23-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="56b23-128">Response</span></span>

<span data-ttu-id="56b23-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="56b23-129">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="56b23-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="56b23-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="56b23-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="56b23-131">Request</span></span>
<span data-ttu-id="56b23-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="56b23-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_registeredusers"
}-->
```http
GET https://graph.microsoft.com/v1.0/devices/{id}/registeredUsers
```
##### <a name="response"></a><span data-ttu-id="56b23-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="56b23-133">Response</span></span>
<span data-ttu-id="56b23-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="56b23-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 55

{
  "value": [
    {
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List registeredUsers",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->