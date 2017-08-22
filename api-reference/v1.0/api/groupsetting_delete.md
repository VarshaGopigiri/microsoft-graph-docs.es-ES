# <a name="delete-a-group-setting"></a><span data-ttu-id="c2955-101">Eliminar una configuración de grupo</span><span class="sxs-lookup"><span data-stu-id="c2955-101">Delete a group setting</span></span>

<span data-ttu-id="c2955-102">Elimina una configuración de grupo.</span><span class="sxs-lookup"><span data-stu-id="c2955-102">Delete a group setting.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c2955-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c2955-103">Prerequisites</span></span>

<span data-ttu-id="c2955-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Directory.ReadWrite.All* o *Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="c2955-104">One of the following **scopes** is required to execute this API: *Directory.ReadWrite.All* or *Directory.AccessAsUser.All*</span></span>

> <span data-ttu-id="c2955-105">Nota: Solo los administradores de inquilinos tienen permiso para realizar operaciones de creación, actualización y eliminación.</span><span class="sxs-lookup"><span data-stu-id="c2955-105">Note: Only tenant admins have permissions to perform create, update, and delete operations.</span></span>

## <a name="http-request"></a><span data-ttu-id="c2955-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c2955-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groupSettings/{id}
DELETE /groups/{id}/settings/{id}

```

## <a name="request-headers"></a><span data-ttu-id="c2955-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c2955-107">Request headers</span></span>

| <span data-ttu-id="c2955-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="c2955-108">Name</span></span> | <span data-ttu-id="c2955-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2955-109">Description</span></span> |
|:---------------|:----------|
| <span data-ttu-id="c2955-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="c2955-110">Authorization</span></span>  | <span data-ttu-id="c2955-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c2955-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c2955-113">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c2955-113">Content-Type</span></span>  | <span data-ttu-id="c2955-114">application/json</span><span class="sxs-lookup"><span data-stu-id="c2955-114">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="c2955-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c2955-115">Request body</span></span>
<span data-ttu-id="c2955-116">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c2955-116">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c2955-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2955-117">Response</span></span>

<span data-ttu-id="c2955-p102">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c2955-p102">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c2955-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c2955-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c2955-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c2955-121">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_groupsetting"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groupSettings/{id}
```
##### <a name="response"></a><span data-ttu-id="c2955-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2955-122">Response</span></span>
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
  "description": "Delete groupSetting",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->