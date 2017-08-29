# <a name="delete-entity"></a><span data-ttu-id="08705-101">Delete entity</span><span class="sxs-lookup"><span data-stu-id="08705-101">Delete entity</span></span>

<span data-ttu-id="08705-102">Elimina la entidad.</span><span class="sxs-lookup"><span data-stu-id="08705-102">Delete entity.</span></span>
## <a name="permissions"></a><span data-ttu-id="08705-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="08705-103">Permissions</span></span>
<span data-ttu-id="08705-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="08705-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="08705-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="08705-106">Permission type</span></span>      | <span data-ttu-id="08705-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="08705-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="08705-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="08705-108">Delegated (work or school account)</span></span> | <span data-ttu-id="08705-109">No admitida.</span><span class="sxs-lookup"><span data-stu-id="08705-109">Not supported.</span></span>    |
|<span data-ttu-id="08705-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="08705-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="08705-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="08705-111">Not supported.</span></span>    |
|<span data-ttu-id="08705-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="08705-112">Application</span></span> | <span data-ttu-id="08705-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="08705-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="08705-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="08705-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http


```
## <a name="request-headers"></a><span data-ttu-id="08705-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="08705-115">Request headers</span></span>
| <span data-ttu-id="08705-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="08705-116">Name</span></span>       | <span data-ttu-id="08705-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="08705-117">Type</span></span> | <span data-ttu-id="08705-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="08705-118">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="08705-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="08705-119">Authorization</span></span>  | <span data-ttu-id="08705-120">string</span><span class="sxs-lookup"><span data-stu-id="08705-120">string</span></span>  | <span data-ttu-id="08705-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="08705-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="08705-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="08705-123">Request body</span></span>
<span data-ttu-id="08705-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="08705-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="08705-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="08705-125">Response</span></span>

<span data-ttu-id="08705-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="08705-p103">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="08705-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="08705-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="08705-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="08705-129">Request</span></span>
<span data-ttu-id="08705-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="08705-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "delete_entity"
}-->
```http

```
##### <a name="response"></a><span data-ttu-id="08705-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="08705-131">Response</span></span>
<span data-ttu-id="08705-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="08705-132">Here is an example of the response.</span></span>
<!-- {
  "blockType": "ignored",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete entity",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
