# <a name="delete-attachment"></a><span data-ttu-id="3d789-101">Eliminar datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="3d789-101">Delete attachment</span></span>

<span data-ttu-id="3d789-102">Elimine datos adjuntos de un evento de calendario, mensaje de correo o publicación de grupo.</span><span class="sxs-lookup"><span data-stu-id="3d789-102">Delete an attachment from a calendar event, mail message, or group post.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3d789-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3d789-103">Prerequisites</span></span>
<span data-ttu-id="3d789-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="3d789-104">One of the following **scopes** is required to execute this API:</span></span>

* <span data-ttu-id="3d789-105">Si accede a datos adjuntos de mensajes: *Mail.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="3d789-105">If accessing attachments in Messages: *Mail.ReadWrite*</span></span>
* <span data-ttu-id="3d789-106">Si accede a datos adjuntos de eventos: *Calendars.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="3d789-106">If accessing attachments in Events: *Calendars.ReadWrite*</span></span>
* <span data-ttu-id="3d789-107">Si accede a datos adjuntos de publicaciones o eventos de grupo: *Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="3d789-107">If accessing attachments in Group Events or Posts: *Group.ReadWrite.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="3d789-108">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3d789-108">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="3d789-109">Datos adjuntos de un [event](../resources/event.md) en el [calendar](../resources/calendar.md) predeterminado del usuario o del grupo.</span><span class="sxs-lookup"><span data-stu-id="3d789-109">Attachments for an [event](../resources/event.md) in the user's or group's default [calendar](../resources/calendar.md).</span></span>
```http
DELETE /me/events/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/events/{id}/attachments/{id}
DELETE /groups/{id}/events/{id}/attachments/{id}

DELETE /me/calendar/{id}/events/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/calendar/events/{id}/attachments/{id}
DELETE /groups/{id}/calendar/events/{id}/attachments/{id}
```
<span data-ttu-id="3d789-110">Datos adjuntos de un [event](../resources/event.md) en un [calendar](../resources/calendar.md) perteneciente al [calendarGroup](../resources/calendargroup.md) predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="3d789-110">Attachments for an [event](../resources/event.md) in a [calendar](../resources/calendar.md) belonging to the user's default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
DELETE /me/calendars/{id}/events/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/calendars/{id}/events/{id}/attachments/{id}

DELETE /me/calendargroup/calendars/{id}/events/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/attachments/{id}
```
<span data-ttu-id="3d789-111">Datos adjuntos de un [event](../resources/event.md) en un [calendar](../resources/calendar.md) perteneciente al [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="3d789-111">Attachments for an [event](../resources/event.md) in a [calendar](../resources/calendar.md) belonging to a user's [calendarGroup](../resources/calendargroup.md).</span></span>
```http
DELETE /me/calendargroups/{id}/calendars/{id}/events/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/attachments/{id}
```
<span data-ttu-id="3d789-112">Datos adjuntos de un [message](../resources/message.md) en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="3d789-112">Attachments for a [message](../resources/message.md) in a user's mailbox.</span></span>
```http
DELETE /me/messages/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/messages/{id}/attachments/{id}
```
<span data-ttu-id="3d789-113">Datos adjuntos de un [message](../resources/message.md) contenido en una [mailFolder](../resources/mailfolder.md) de nivel superior en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="3d789-113">Attachments for a [message](../resources/message.md) contained in a top level [mailFolder](../resources/mailfolder.md) in a user's mailbox.</span></span>
```http
DELETE /me/mailFolders/{id}/messages/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/attachments/{id}
```
<span data-ttu-id="3d789-p101">Datos adjuntos de un [message](../resources/message.md) contenido en una carpeta secundaria de una [mailFolder](../resources/mailfolder.md) en el buzón de un usuario.  En el ejemplo, siguiente se muestra un nivel de anidamiento, pero un mensaje puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="3d789-p101">Attachments for a [message](../resources/message.md) contained in a child folder of a [mailFolder](../resources/mailfolder.md) in a user's mailbox.  The example below shows one level of nesting, but a message can be located in a child of a child and so on.</span></span>
```http
DELETE /me/mailFolders/{id}/childFolders/{id}/.../messages/{id}/attachments/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}/childFolders/{id}/messages/{id}/attachments/{id}
```
<span data-ttu-id="3d789-116">Datos adjuntos para un [post](../resources/post.md) de un [thread](../resources/conversationthread.md) perteneciente a una [conversation](../resources/conversation.md) de un grupo.</span><span class="sxs-lookup"><span data-stu-id="3d789-116">Attachments for a [post](../resources/post.md) in a [thread](../resources/conversationthread.md) belonging to a [conversation](../resources/conversation.md) of a group.</span></span>
```http
DELETE /groups/{id}/threads/{id}/posts/{id}/attachments/{id}
DELETE /groups/{id}/conversations/{id}/threads/{id}/posts/{id}/attachments/{id}
```
## <a name="request-headers"></a><span data-ttu-id="3d789-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3d789-117">Request headers</span></span>
| <span data-ttu-id="3d789-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="3d789-118">Name</span></span>       | <span data-ttu-id="3d789-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="3d789-119">Type</span></span> | <span data-ttu-id="3d789-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="3d789-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="3d789-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="3d789-121">Authorization</span></span>  | <span data-ttu-id="3d789-122">string</span><span class="sxs-lookup"><span data-stu-id="3d789-122">string</span></span>  | <span data-ttu-id="3d789-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3d789-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="3d789-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3d789-125">Request body</span></span>
<span data-ttu-id="3d789-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3d789-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3d789-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3d789-127">Response</span></span>

<span data-ttu-id="3d789-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3d789-p103">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3d789-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3d789-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3d789-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3d789-131">Request</span></span>
<span data-ttu-id="3d789-132">Este es un ejemplo de la solicitud para eliminar un archivo adjunto en un evento.</span><span class="sxs-lookup"><span data-stu-id="3d789-132">Here is an example of the request to delete an attachment on an event.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_attachment"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/events/{id}/attachments/{id}
```
##### <a name="response"></a><span data-ttu-id="3d789-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3d789-133">Response</span></span>
<span data-ttu-id="3d789-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3d789-134">Here is an example of the response.</span></span>
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
