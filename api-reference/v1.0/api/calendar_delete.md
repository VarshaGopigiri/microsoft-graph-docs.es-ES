# <a name="delete-calendar"></a><span data-ttu-id="ddd9d-101">Eliminar calendario</span><span class="sxs-lookup"><span data-stu-id="ddd9d-101">Delete calendar</span></span>

<span data-ttu-id="ddd9d-102">Elimina un calendario que no sea el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ddd9d-102">Delete a calendar other than the default calendar.</span></span>
## <a name="permissions"></a><span data-ttu-id="ddd9d-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="ddd9d-103">Permissions</span></span>
<span data-ttu-id="ddd9d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ddd9d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ddd9d-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ddd9d-106">Permission type</span></span>      | <span data-ttu-id="ddd9d-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ddd9d-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ddd9d-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ddd9d-108">Delegated (work or school account)</span></span> | <span data-ttu-id="ddd9d-109">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ddd9d-109">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="ddd9d-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ddd9d-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ddd9d-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ddd9d-111">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="ddd9d-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ddd9d-112">Application</span></span> | <span data-ttu-id="ddd9d-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ddd9d-113">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="ddd9d-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ddd9d-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="ddd9d-115">Un [calendar](../resources/calendar.md) de usuario que no sea el calendario predeterminado del [calendarGroup](../resources/calendargroup.md) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ddd9d-115">A user's [calendar](../resources/calendar.md) other than the default calendar in the default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
DELETE /me/calendars/{id}
DELETE /users/{id | userPrincipalName}/calendars/{id}

DELETE /me/calendarGroup/calendars/{id}
DELETE /users/{id | userPrincipalName}/calendarGroup/calendars/{id}
```
<span data-ttu-id="ddd9d-116">Un [calendar](../resources/calendar.md) que no sea el calendario predeterminado de un [calendarGroup](../resources/calendargroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="ddd9d-116">A [calendar](../resources/calendar.md) other than the default calendar, in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
```http
DELETE /me/calendarGroups/{id}/calendars/{id}
DELETE /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}
```
## <a name="request-headers"></a><span data-ttu-id="ddd9d-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ddd9d-117">Request headers</span></span>
| <span data-ttu-id="ddd9d-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="ddd9d-118">Name</span></span>           |  <span data-ttu-id="ddd9d-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="ddd9d-119">Type</span></span>    | <span data-ttu-id="ddd9d-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddd9d-120">Description</span></span>|
|:---------------|:---------|:----------|
| <span data-ttu-id="ddd9d-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="ddd9d-121">Authorization</span></span>  |  <span data-ttu-id="ddd9d-122">string</span><span class="sxs-lookup"><span data-stu-id="ddd9d-122">string</span></span>  | <span data-ttu-id="ddd9d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ddd9d-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ddd9d-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ddd9d-125">Request body</span></span>
<span data-ttu-id="ddd9d-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ddd9d-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ddd9d-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ddd9d-127">Response</span></span>

<span data-ttu-id="ddd9d-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ddd9d-p103">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ddd9d-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ddd9d-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ddd9d-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ddd9d-131">Request</span></span>
<span data-ttu-id="ddd9d-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ddd9d-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_calendar"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/calendar
```
##### <a name="response"></a><span data-ttu-id="ddd9d-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ddd9d-133">Response</span></span>
<span data-ttu-id="ddd9d-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ddd9d-134">Here is an example of the response.</span></span> 
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
  "description": "Delete calendar",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
