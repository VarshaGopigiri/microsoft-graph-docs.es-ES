# <a name="delete-directoryobject"></a><span data-ttu-id="f8206-101">Delete directoryObject</span><span class="sxs-lookup"><span data-stu-id="f8206-101">Delete directoryObject</span></span>

<span data-ttu-id="f8206-102">Elimina un directoryObject.</span><span class="sxs-lookup"><span data-stu-id="f8206-102">Deletes a directoryObject.</span></span>

## <a name="permissions"></a><span data-ttu-id="f8206-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="f8206-103">Permissions</span></span>
<span data-ttu-id="f8206-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f8206-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="f8206-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f8206-106">Permission type</span></span>      | <span data-ttu-id="f8206-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f8206-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f8206-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f8206-108">Delegated (work or school account)</span></span> | <span data-ttu-id="f8206-109">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="f8206-109">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="f8206-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f8206-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f8206-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f8206-111">Not supported.</span></span>    |
|<span data-ttu-id="f8206-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f8206-112">Application</span></span> | <span data-ttu-id="f8206-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f8206-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f8206-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f8206-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /directoryObjects/{id}

```
## <a name="request-headers"></a><span data-ttu-id="f8206-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f8206-115">Request headers</span></span>
| <span data-ttu-id="f8206-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="f8206-116">Name</span></span>       | <span data-ttu-id="f8206-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="f8206-117">Type</span></span> | <span data-ttu-id="f8206-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8206-118">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="f8206-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="f8206-119">Authorization</span></span>  | <span data-ttu-id="f8206-120">string</span><span class="sxs-lookup"><span data-stu-id="f8206-120">string</span></span>  | <span data-ttu-id="f8206-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f8206-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f8206-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f8206-123">Request body</span></span>
<span data-ttu-id="f8206-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f8206-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f8206-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f8206-125">Response</span></span>

<span data-ttu-id="f8206-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f8206-p103">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f8206-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f8206-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f8206-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f8206-129">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_directoryobject"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/directoryObject/{id}
```
##### <a name="response"></a><span data-ttu-id="f8206-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f8206-130">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete directoryObject",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->