# <a name="list-registeredowners"></a><span data-ttu-id="79e02-101">List registeredOwners</span><span class="sxs-lookup"><span data-stu-id="79e02-101">List registeredOwners</span></span>

<span data-ttu-id="79e02-102">Recupera una lista de usuarios que son propietarios registrados del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="79e02-102">Retrieve a list of users that are registered owners of the device.</span></span> <span data-ttu-id="79e02-103">El usuario registrado es el usuario que ha unido el dispositivo a la nube o que ha registrado su dispositivo personal.</span><span class="sxs-lookup"><span data-stu-id="79e02-103">A registered owner is the user that cloud joined the device or registered their personal device.</span></span> <span data-ttu-id="79e02-104">El propietario registrado se establece en el momento del registro.</span><span class="sxs-lookup"><span data-stu-id="79e02-104">The registered owner is set at the time of registration.</span></span> <span data-ttu-id="79e02-105">Actualmente, solo puede haber un propietario.</span><span class="sxs-lookup"><span data-stu-id="79e02-105">Currently, there can be only one owner.</span></span>

## <a name="permissions"></a><span data-ttu-id="79e02-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="79e02-106">Permissions</span></span>
<span data-ttu-id="79e02-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="79e02-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="79e02-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="79e02-109">Permission type</span></span>      | <span data-ttu-id="79e02-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="79e02-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="79e02-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="79e02-111">Delegated (work or school account)</span></span> | <span data-ttu-id="79e02-112">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="79e02-112">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="79e02-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="79e02-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="79e02-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="79e02-114">Not supported.</span></span>    |
|<span data-ttu-id="79e02-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="79e02-115">Application</span></span> | <span data-ttu-id="79e02-116">Device.ReadWrite.All y User.ReadBasic.All, Directory.Read.All o Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="79e02-116">Device.ReadWrite.All and User.ReadBasic.All or Directory.Read.All or Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="79e02-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="79e02-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /devices/{id}/registeredOwners
```
## <a name="optional-query-parameters"></a><span data-ttu-id="79e02-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="79e02-118">Optional query parameters</span></span>
<span data-ttu-id="79e02-119">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="79e02-119">This method supports the [OData Query Parameters](http://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="79e02-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="79e02-120">Request headers</span></span>
| <span data-ttu-id="79e02-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="79e02-121">Name</span></span>       | <span data-ttu-id="79e02-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="79e02-122">Type</span></span> | <span data-ttu-id="79e02-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="79e02-123">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="79e02-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="79e02-124">Authorization</span></span>  | <span data-ttu-id="79e02-125">string</span><span class="sxs-lookup"><span data-stu-id="79e02-125">string</span></span>  | <span data-ttu-id="79e02-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="79e02-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="79e02-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="79e02-128">Request body</span></span>
<span data-ttu-id="79e02-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="79e02-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="79e02-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="79e02-130">Response</span></span>

<span data-ttu-id="79e02-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="79e02-131">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="79e02-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="79e02-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="79e02-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="79e02-133">Request</span></span>
<span data-ttu-id="79e02-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="79e02-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_registeredowners"
}-->
```http
GET https://graph.microsoft.com/v1.0/devices/{id}/registeredOwners
```
##### <a name="response"></a><span data-ttu-id="79e02-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="79e02-135">Response</span></span>
<span data-ttu-id="79e02-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="79e02-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "List registeredOwners",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->