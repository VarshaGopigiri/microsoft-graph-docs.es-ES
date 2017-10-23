# <a name="delete-attachment"></a><span data-ttu-id="335f4-101">Eliminar datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="335f4-101">Delete attachment</span></span>

<span data-ttu-id="335f4-102">Elimina datos adjuntos de un evento de calendario, mensaje de correo o publicación de grupo.</span><span class="sxs-lookup"><span data-stu-id="335f4-102">Delete an attachment from a calendar event, mail message, or group post.</span></span>
## <a name="permissions"></a><span data-ttu-id="335f4-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="335f4-103">Permissions</span></span>
<span data-ttu-id="335f4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="335f4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

* <span data-ttu-id="335f4-106">Si accede a datos adjuntos en Mensajes: Mail.ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="335f4-106">If accessing attachments in Messages: Mail.ReadWrite.</span></span>
* <span data-ttu-id="335f4-107">Si accede a datos adjuntos en Eventos: Calendars.ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="335f4-107">If accessing attachments in Events: Calendars.ReadWrite.</span></span>
* <span data-ttu-id="335f4-108">Si accede a datos adjuntos en Publicaciones o Eventos de grupo: Group.ReadWrite.All.</span><span class="sxs-lookup"><span data-stu-id="335f4-108">If accessing attachments in Group Events or Posts: Group.ReadWrite.All.</span></span>

## <a name="http-request"></a><span data-ttu-id="335f4-109">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="335f4-109">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="335f4-110">Datos adjuntos de un [event](../resources/event.md) en el [calendar](../resources/calendar.md) predeterminado del usuario o del grupo.</span><span class="sxs-lookup"><span data-stu-id="335f4-110">Attachments for an [event](../resources/event.md) in the user's or group's default [calendar](../resources/calendar.md).</span></span>
```http
DELETE /me/events/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/events/{id}/attachments/{id}
DELETE /groups/{id}/events/{id}/attachments/{id}

DELETE /me/calendar/{id}/events/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/calendar/events/{id}/attachments/{id}
DELETE /groups/{id}/calendar/events/{id}/attachments/{id}
```
<span data-ttu-id="335f4-111">Datos adjuntos de un [event](../resources/event.md) en un [calendar](../resources/calendar.md) perteneciente al [calendarGroup](../resources/calendargroup.md) predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="335f4-111">Attachments for an [event](../resources/event.md) in a [calendar](../resources/calendar.md) belonging to the user's default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
DELETE /me/calendars/{id}/events/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/calendars/{id}/events/{id}/attachments/{id}

DELETE /me/calendargroup/calendars/{id}/events/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/attachments/{id}
```
<span data-ttu-id="335f4-112">Datos adjuntos de un [event](../resources/event.md) en un [calendar](../resources/calendar.md) perteneciente al [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="335f4-112">Attachments for an [event](../resources/event.md) in a [calendar](../resources/calendar.md) belonging to a user's [calendarGroup](../resources/calendargroup.md).</span></span>
```http
DELETE /me/calendargroups/{id}/calendars/{id}/events/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/attachments/{id}
```
<span data-ttu-id="335f4-113">Datos adjuntos de un [message](../resources/message.md) en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="335f4-113">Attachments for a [message](../resources/message.md) in a user's mailbox.</span></span>
```http
DELETE /me/messages/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/messages/{id}/attachments/{id}
```
<span data-ttu-id="335f4-114">Datos adjuntos de un [message](../resources/message.md) contenido en una [mailFolder](../resources/mailfolder.md) de nivel superior en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="335f4-114">Attachments for a [message](../resources/message.md) contained in a top level [mailFolder](../resources/mailfolder.md) in a user's mailbox.</span></span>
```http
DELETE /me/mailFolders/{id}/messages/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/attachments/{id}
```
<span data-ttu-id="335f4-p102">Datos adjuntos de un [message](../resources/message.md) contenido en una carpeta secundaria de una [mailFolder](../resources/mailfolder.md) en el buzón de un usuario.  En el ejemplo, siguiente se muestra un nivel de anidamiento, pero un mensaje puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="335f4-p102">Attachments for a [message](../resources/message.md) contained in a child folder of a [mailFolder](../resources/mailfolder.md) in a user's mailbox.  The example below shows one level of nesting, but a message can be located in a child of a child and so on.</span></span>
```http
DELETE /me/mailFolders/{id}/childFolders/{id}/.../messages/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}/childFolders/{id}/messages/{id}/attachments/{id}
```
<span data-ttu-id="335f4-117">Datos adjuntos para un [post](../resources/post.md) de un [thread](../resources/conversationthread.md) perteneciente a una [conversation](../resources/conversation.md) de un grupo.</span><span class="sxs-lookup"><span data-stu-id="335f4-117">Attachments for a [post](../resources/post.md) in a [thread](../resources/conversationthread.md) belonging to a [conversation](../resources/conversation.md) of a group.</span></span>
```http
DELETE /groups/{id}/threads/{id}/posts/{id}/attachments/{id}
DELETE /groups/{id}/conversations/{id}/threads/{id}/posts/{id}/attachments/{id}
```
## <a name="request-headers"></a><span data-ttu-id="335f4-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="335f4-118">Request headers</span></span>
| <span data-ttu-id="335f4-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="335f4-119">Name</span></span>       | <span data-ttu-id="335f4-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="335f4-120">Type</span></span> | <span data-ttu-id="335f4-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="335f4-121">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="335f4-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="335f4-122">Authorization</span></span>  | <span data-ttu-id="335f4-123">string</span><span class="sxs-lookup"><span data-stu-id="335f4-123">string</span></span>  | <span data-ttu-id="335f4-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="335f4-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="335f4-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="335f4-126">Request body</span></span>
<span data-ttu-id="335f4-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="335f4-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="335f4-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="335f4-128">Response</span></span>

<span data-ttu-id="335f4-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="335f4-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="335f4-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="335f4-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="335f4-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="335f4-132">Request</span></span>
<span data-ttu-id="335f4-133">Este es un ejemplo de la solicitud para eliminar un archivo adjunto en un evento.</span><span class="sxs-lookup"><span data-stu-id="335f4-133">Here is an example of the request to delete an attachment on an event.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_attachment"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/events/{id}/attachments/{id}
```
##### <a name="response"></a><span data-ttu-id="335f4-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="335f4-134">Response</span></span>
<span data-ttu-id="335f4-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="335f4-135">Here is an example of the response.</span></span>
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
  "description": "Delete attachment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
