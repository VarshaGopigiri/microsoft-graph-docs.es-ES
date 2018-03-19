# <a name="group-renew"></a><span data-ttu-id="f4133-101">group: renew</span><span class="sxs-lookup"><span data-stu-id="f4133-101">group: renew</span></span>

<span data-ttu-id="f4133-102">Renueva la expiración de un grupo.</span><span class="sxs-lookup"><span data-stu-id="f4133-102">Renews a group's expiration.</span></span> <span data-ttu-id="f4133-103">Cuando se renueva un grupo, la expiración del grupo se amplía por el número de días definidos en la directiva.</span><span class="sxs-lookup"><span data-stu-id="f4133-103">When a group is renewed, the group expiration is extended by the number of days defined in the policy.</span></span>

## <a name="permissions"></a><span data-ttu-id="f4133-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="f4133-104">Permissions</span></span>

<span data-ttu-id="f4133-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f4133-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>
 

|<span data-ttu-id="f4133-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f4133-107">Permission type</span></span>      | <span data-ttu-id="f4133-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f4133-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f4133-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f4133-109">Delegated (work or school account)</span></span> | <span data-ttu-id="f4133-110">Group.ReadWrite.All o Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f4133-110">Group.ReadWrite.All, Directory.ReadWrite.All</span></span>    |
|<span data-ttu-id="f4133-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f4133-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f4133-112">No admitido</span><span class="sxs-lookup"><span data-stu-id="f4133-112">Not supported</span></span> |
|<span data-ttu-id="f4133-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f4133-113">Application</span></span> | <span data-ttu-id="f4133-114">Group.ReadWrite.All o Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f4133-114">Group.ReadWrite.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="f4133-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f4133-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/<id>/renew
```

## <a name="request-headers"></a><span data-ttu-id="f4133-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f4133-116">Request headers</span></span>
| <span data-ttu-id="f4133-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="f4133-117">Name</span></span>       | <span data-ttu-id="f4133-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4133-118">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="f4133-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="f4133-119">Authorization</span></span>  | <span data-ttu-id="f4133-120">Bearer {token}</span><span class="sxs-lookup"><span data-stu-id="f4133-120">Bearer %token%</span></span> |


## <a name="request-body"></a><span data-ttu-id="f4133-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f4133-121">Request body</span></span>

<span data-ttu-id="f4133-122">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f4133-122">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f4133-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f4133-123">Response</span></span>

<span data-ttu-id="f4133-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f4133-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f4133-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f4133-126">Example</span></span>

##### <a name="request"></a><span data-ttu-id="f4133-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f4133-127">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "group_renew"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/<id>/renew
```

##### <a name="response"></a><span data-ttu-id="f4133-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f4133-128">Response</span></span>
<span data-ttu-id="f4133-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f4133-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Boolean"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "group: renew",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->