# <a name="get-directory-objects-from-a-list-of-ids"></a><span data-ttu-id="4f6fa-101">Obtener objetos de directorio a partir de una lista de identificadores</span><span class="sxs-lookup"><span data-stu-id="4f6fa-101">Get directory objects from a list of ids</span></span>

<span data-ttu-id="4f6fa-p101">Devuelve los objetos de directorio especificados en una lista de identificadores.  NOTA: Los objetos de directorio devueltos son los objetos completos que contienen **todas** sus propiedades. La opción de consulta `$select` no está disponible para esta operación.</span><span class="sxs-lookup"><span data-stu-id="4f6fa-p101">Returns the directory objects specified in a list of ids.  NOTE: The directory objects returned are the full objects containing **all** their properties. The `$select` query option is not available for this operation.</span></span>

<span data-ttu-id="4f6fa-105">Algunos usos comunes de esta función son:</span><span class="sxs-lookup"><span data-stu-id="4f6fa-105">Some common uses for this function are to:</span></span>

* <span data-ttu-id="4f6fa-106">Resolver identificadores devueltos por funciones (que devuelven colecciones de identificadores) como [getMemberObjects](directoryobject_getmemberobjects.md) o [getMemberGroups](directoryobject_getmembergroups.md) a sus objetos del directorio de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="4f6fa-106">Resolve ids returned by functions (that return collections of ids) such as [getMemberObjects](directoryobject_getmemberobjects.md) or [getMemberGroups](directoryobject_getmembergroups.md)  to their backing directory objects.</span></span>
* <span data-ttu-id="4f6fa-107">Resolver identificadores que conserva la aplicación en un almacén externo para sus objetos del directorio de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="4f6fa-107">Resolve ids persisted in an external store by the application to their backing directory objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="4f6fa-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="4f6fa-108">Permissions</span></span>

<span data-ttu-id="4f6fa-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="4f6fa-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="4f6fa-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4f6fa-111">Permission type</span></span>      | <span data-ttu-id="4f6fa-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4f6fa-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4f6fa-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4f6fa-113">Delegated (work or school account)</span></span> | <span data-ttu-id="4f6fa-114">Directory.Read.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="4f6fa-114">Directory.Read.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="4f6fa-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4f6fa-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4f6fa-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4f6fa-116">Not supported.</span></span>    |
|<span data-ttu-id="4f6fa-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4f6fa-117">Application</span></span> | <span data-ttu-id="4f6fa-118">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="4f6fa-118">Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="4f6fa-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4f6fa-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /directoryObjects/getById
```

## <a name="request-headers"></a><span data-ttu-id="4f6fa-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4f6fa-120">Request headers</span></span>

| <span data-ttu-id="4f6fa-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="4f6fa-121">Name</span></span>       | <span data-ttu-id="4f6fa-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="4f6fa-122">Type</span></span> | <span data-ttu-id="4f6fa-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f6fa-123">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="4f6fa-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="4f6fa-124">Authorization</span></span>  | <span data-ttu-id="4f6fa-125">string</span><span class="sxs-lookup"><span data-stu-id="4f6fa-125">string</span></span>  | <span data-ttu-id="4f6fa-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4f6fa-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="4f6fa-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="4f6fa-128">Content-Type</span></span>  | <span data-ttu-id="4f6fa-129">application/json</span><span class="sxs-lookup"><span data-stu-id="4f6fa-129">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="4f6fa-130">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="4f6fa-130">Request body</span></span>

<span data-ttu-id="4f6fa-131">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="4f6fa-131">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="4f6fa-132">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4f6fa-132">Parameter</span></span>   | <span data-ttu-id="4f6fa-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="4f6fa-133">Type</span></span> |<span data-ttu-id="4f6fa-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f6fa-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4f6fa-135">ids</span><span class="sxs-lookup"><span data-stu-id="4f6fa-135">ids</span></span>|<span data-ttu-id="4f6fa-136">Colección string</span><span class="sxs-lookup"><span data-stu-id="4f6fa-136">String collection</span></span>| <span data-ttu-id="4f6fa-p104">Una colección de identificadores para devolverles objetos. Se pueden especificar hasta 1000 identificadores.</span><span class="sxs-lookup"><span data-stu-id="4f6fa-p104">A collection of ids for which to return objects. You can specify up to 1000 ids.</span></span> |
|<span data-ttu-id="4f6fa-139">types</span><span class="sxs-lookup"><span data-stu-id="4f6fa-139">types</span></span>|<span data-ttu-id="4f6fa-140">Colección string</span><span class="sxs-lookup"><span data-stu-id="4f6fa-140">String collection</span></span>| <span data-ttu-id="4f6fa-p105">Una colección de tipos de recursos que especifica el conjunto de colecciones de recursos en el que debe buscarse. Si no se especifica, el valor predeterminado es [directoryObject](../resources/directoryobject.md), que contiene todos los tipos de recursos definidos en el directorio. Cualquier objeto que derive de `directoryObject` puede especificarse en la colección; por ejemplo: [user](../resources/user.md), [group](../resources/group.md), [device](../resources/device.md), etc. Los valores no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4f6fa-p105">A collection of resource types that specifies the set of resource collections to search. If not specified, the default is [directoryObject](../resources/directoryobject.md), which contains all of the resource types defined in the directory. Any object that derives from `directoryObject` may be specified in the collection; for example: [user](../resources/user.md), [group](../resources/group.md), [device](../resources/device.md), and so on. The values are not case sensitive.</span></span>|

## <a name="response"></a><span data-ttu-id="4f6fa-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4f6fa-145">Response</span></span>

<span data-ttu-id="4f6fa-146">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4f6fa-146">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4f6fa-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4f6fa-147">Example</span></span>

##### <a name="request"></a><span data-ttu-id="4f6fa-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4f6fa-148">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "directoryobject_getById"
}-->

```http
POST https://graph.microsoft.com/v1.0/directoryObjects/getByIds
Content-type: application/json

{
    "ids":["84b80893-8749-40a3-97b7-68513b600544","5d6059b6-368d-45f8-91e1-8e07d485f1d0"],
    "types":["user"]
}
```

##### <a name="response"></a><span data-ttu-id="4f6fa-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4f6fa-149">Response</span></span>

<span data-ttu-id="4f6fa-p106">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4f6fa-p106">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#directoryObjects",
    "value": [
      {
        "@odata.type": "#microsoft.graph.user",
        "id": "84b80893-8749-40a3-97b7-68513b600544",
        "accountEnabled": true,
        "displayName": "Trevor Jones"
      },
      {
        "@odata.type": "#microsoft.graph.user",
        "id": "84b80893-8749-40a3-97b7-68513b600544",
        "accountEnabled": true,
        "displayName": "Billy Smith"
      }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryObject: getById",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
