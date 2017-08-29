# <a name="create-registereduser"></a><span data-ttu-id="7cf12-101">Create registeredUser</span><span class="sxs-lookup"><span data-stu-id="7cf12-101">Create registeredUser</span></span>

<span data-ttu-id="7cf12-102">Agrega un usuario registrado para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7cf12-102">Add a registered user for the device.</span></span>

## <a name="permissions"></a><span data-ttu-id="7cf12-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="7cf12-103">Permissions</span></span>
<span data-ttu-id="7cf12-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="7cf12-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="7cf12-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7cf12-106">Permission type</span></span>      | <span data-ttu-id="7cf12-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7cf12-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7cf12-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7cf12-108">Delegated (work or school account)</span></span> | <span data-ttu-id="7cf12-109">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="7cf12-109">Directory.ReadWrite.All or Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="7cf12-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7cf12-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7cf12-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7cf12-111">Not supported.</span></span>    |
|<span data-ttu-id="7cf12-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7cf12-112">Application</span></span> | <span data-ttu-id="7cf12-113">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7cf12-113">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="7cf12-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7cf12-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /devices/{id}/registeredUsers

```
## <a name="request-headers"></a><span data-ttu-id="7cf12-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7cf12-115">Request headers</span></span>
| <span data-ttu-id="7cf12-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="7cf12-116">Name</span></span>       | <span data-ttu-id="7cf12-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="7cf12-117">Type</span></span> | <span data-ttu-id="7cf12-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="7cf12-118">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="7cf12-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="7cf12-119">Authorization</span></span>  | <span data-ttu-id="7cf12-120">string</span><span class="sxs-lookup"><span data-stu-id="7cf12-120">string</span></span>  | <span data-ttu-id="7cf12-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7cf12-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="7cf12-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7cf12-123">Request body</span></span>
<span data-ttu-id="7cf12-124">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryObject](../resources/directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="7cf12-124">In the request body, supply a JSON representation of [directoryObject](../resources/directoryobject.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="7cf12-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7cf12-125">Response</span></span>

<span data-ttu-id="7cf12-126">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7cf12-126">If successful, this method returns `201, Created` response code and [directoryObject](../resources/directoryobject.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7cf12-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7cf12-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7cf12-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7cf12-128">Request</span></span>
<span data-ttu-id="7cf12-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7cf12-129">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_device"
}-->
```http
POST https://graph.microsoft.com/v1.0/devices/{id}/registeredUsers
Content-type: application/json
Content-length: 30

{
  "directoryObject": {
  }
}
```
<span data-ttu-id="7cf12-130">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryObject](../resources/directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="7cf12-130">In the request body, supply a JSON representation of [directoryObject](../resources/directoryobject.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="7cf12-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7cf12-131">Response</span></span>
<span data-ttu-id="7cf12-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7cf12-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 51

{
  "directoryObject": {
    "id": "id-value"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create registeredUser",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->