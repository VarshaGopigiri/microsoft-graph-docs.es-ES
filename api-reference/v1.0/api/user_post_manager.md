# <a name="assign-a-manager"></a><span data-ttu-id="2eb84-101">Assign a manager</span><span class="sxs-lookup"><span data-stu-id="2eb84-101">Assign a manager</span></span>

<span data-ttu-id="2eb84-102">Use esta API para asignar un administrador de usuarios.</span><span class="sxs-lookup"><span data-stu-id="2eb84-102">Use this API to assign a user's manager.</span></span>
> <span data-ttu-id="2eb84-103">Nota: No puede asignar subordinados directos; en lugar de ello, use esta API.</span><span class="sxs-lookup"><span data-stu-id="2eb84-103">Note: You cannot assign direct reports - instead use this API.</span></span>

## <a name="permissions"></a><span data-ttu-id="2eb84-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="2eb84-104">Permissions</span></span>
<span data-ttu-id="2eb84-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="2eb84-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="2eb84-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2eb84-107">Permission type</span></span>      | <span data-ttu-id="2eb84-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2eb84-108">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="2eb84-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2eb84-109">Delegated (work or school account)</span></span> | <span data-ttu-id="2eb84-110">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="2eb84-110">Directory.ReadWrite.All or Directory.AccessAsUser.All</span></span>    | 
|<span data-ttu-id="2eb84-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2eb84-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2eb84-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2eb84-112">Not supported.</span></span>    | 
|<span data-ttu-id="2eb84-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2eb84-113">Application</span></span> | <span data-ttu-id="2eb84-114">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2eb84-114">Directory.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="2eb84-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2eb84-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PUT /users/{id}/manager/$ref
```
## <a name="request-headers"></a><span data-ttu-id="2eb84-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2eb84-116">Request headers</span></span>
| <span data-ttu-id="2eb84-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="2eb84-117">Name</span></span>       | <span data-ttu-id="2eb84-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="2eb84-118">Type</span></span> | <span data-ttu-id="2eb84-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="2eb84-119">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="2eb84-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="2eb84-120">Authorization</span></span>  | <span data-ttu-id="2eb84-121">string</span><span class="sxs-lookup"><span data-stu-id="2eb84-121">string</span></span>  | <span data-ttu-id="2eb84-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2eb84-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="2eb84-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2eb84-124">Request body</span></span>
<span data-ttu-id="2eb84-125">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryObject](../resources/directoryobject.md) o [user](../resources/user.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="2eb84-125">In the request body, supply a JSON representation of [directoryObject](../resources/directoryobject.md) or [user](../resources/user.md) object to be added.</span></span>

## <a name="response"></a><span data-ttu-id="2eb84-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2eb84-126">Response</span></span>

<span data-ttu-id="2eb84-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2eb84-p103">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2eb84-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2eb84-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2eb84-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2eb84-130">Request</span></span>
<span data-ttu-id="2eb84-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2eb84-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_group"
}-->
```http
PUT https://graph.microsoft.com/v1.0/users/{id}/manager/$ref
Content-type: application/json
Content-length: xxx

{
  "@odata.id": "https://graph.microsoft.com/v1.0/users/{id}"
}
```
<span data-ttu-id="2eb84-132">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [user](../resources/user.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="2eb84-132">In the request body, supply a JSON representation of [user](../resources/user.md) object to be added.</span></span>
##### <a name="response"></a><span data-ttu-id="2eb84-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2eb84-133">Response</span></span>
<span data-ttu-id="2eb84-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2eb84-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create member",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
