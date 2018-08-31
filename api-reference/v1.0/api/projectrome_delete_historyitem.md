# <a name="delete-a-historyitem"></a><span data-ttu-id="ef901-101">Eliminar un historyItem</span><span class="sxs-lookup"><span data-stu-id="ef901-101">Delete a historyItem</span></span>

<span data-ttu-id="ef901-102">Eliminar un elemento de historial existente para una actividad de usuario existente.</span><span class="sxs-lookup"><span data-stu-id="ef901-102">Delete an existing history item for an existing user activity.</span></span>

## <a name="permissions"></a><span data-ttu-id="ef901-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="ef901-103">Permissions</span></span>

<span data-ttu-id="ef901-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ef901-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="ef901-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ef901-106">Permission type</span></span>      | <span data-ttu-id="ef901-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ef901-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ef901-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ef901-108">Delegated (work or school account)</span></span> | <span data-ttu-id="ef901-109">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="ef901-109">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="ef901-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ef901-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ef901-111">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="ef901-111">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="ef901-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ef901-112">Application</span></span> | <span data-ttu-id="ef901-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ef901-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="ef901-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ef901-114">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /me/activities/{id}/historyItems/{id}
```

## <a name="request-headers"></a><span data-ttu-id="ef901-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ef901-115">Request headers</span></span>

|<span data-ttu-id="ef901-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="ef901-116">Name</span></span> | <span data-ttu-id="ef901-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="ef901-117">Type</span></span> | <span data-ttu-id="ef901-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef901-118">Description</span></span>|
|:----|:-----|:-----------|
|<span data-ttu-id="ef901-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="ef901-119">Authorization</span></span> | <span data-ttu-id="ef901-120">cadena</span><span class="sxs-lookup"><span data-stu-id="ef901-120">string</span></span> | <span data-ttu-id="ef901-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ef901-p102">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="ef901-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ef901-123">Request body</span></span>

<span data-ttu-id="ef901-124">Ningún cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ef901-124">No request body is required.</span></span>

## <a name="response"></a><span data-ttu-id="ef901-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ef901-125">Response</span></span>

<span data-ttu-id="ef901-126">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content` si se ha eliminado el elemento de historial.</span><span class="sxs-lookup"><span data-stu-id="ef901-126">If successful, this method returns the `204 No Content` response code if the history item was deleted.</span></span>

## <a name="example"></a><span data-ttu-id="ef901-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ef901-127">Example</span></span>

##### <a name="request"></a><span data-ttu-id="ef901-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ef901-128">Request</span></span>

<span data-ttu-id="ef901-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ef901-129">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_historyItem"
}-->

```http
PUT https://graph.microsoft.com/v1.0/me/activities/{activity-id}/historyItems/{item-id}
```

##### <a name="response"></a><span data-ttu-id="ef901-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ef901-130">Response</span></span>

<span data-ttu-id="ef901-131">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ef901-131">Here is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
} -->

```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2017-06-07 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete historyitem",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->