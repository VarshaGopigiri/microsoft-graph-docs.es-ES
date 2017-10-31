# <a name="get-calendar"></a><span data-ttu-id="62120-101">Obtener calendario</span><span class="sxs-lookup"><span data-stu-id="62120-101">Get calendar</span></span>

<span data-ttu-id="62120-102">Obtiene las propiedades y relaciones de un objeto de [calendario](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="62120-102">Retrieve the properties and relationships of a calendar group object.</span></span> <span data-ttu-id="62120-103">El calendario puede ser de un [usuario](../resources/user.md) o el calendario predeterminado de un [grupo](../resources/group.md) de Office 365.</span><span class="sxs-lookup"><span data-stu-id="62120-103">The calendar can be one for a [user](../resources/user.md), or the default calendar of an Office 365 [group](../resources/group.md).</span></span>


### <a name="get-another-users-calendar"></a><span data-ttu-id="62120-104">Obtener el calendario de otro usuario</span><span class="sxs-lookup"><span data-stu-id="62120-104">Get another user's drive</span></span>

<span data-ttu-id="62120-105">Si dispone de permisos de la aplicación o si tiene los [permisos](#permissions) delegados apropiados de un usuario, es posible obtener el calendario de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="62120-105">If you have application permissions, or if you have the appropriate delegated [permissions](#permissions) from one user, it's possible to get a calendar of another user's.</span></span> <span data-ttu-id="62120-106">Esta sección se centra en escenarios que implican permisos delegados.</span><span class="sxs-lookup"><span data-stu-id="62120-106">This section focuses on scenarios that involve delegated permissions.</span></span>

<span data-ttu-id="62120-107">Por ejemplo, su aplicación ha adquirido permisos delegados del usuario John.</span><span class="sxs-lookup"><span data-stu-id="62120-107">For example, your app has acquired delegated permissions from the user, John.</span></span> <span data-ttu-id="62120-108">Suponga que otro usuario, Garth, ha compartido un calendario con John.</span><span class="sxs-lookup"><span data-stu-id="62120-108">Suppose another user, Garth, has shared a calendar with John.</span></span> <span data-ttu-id="62120-109">Puede obtener dicho calendario compartido especificando el identificador de usuario de Garth (o su nombre principal de usuario) en la consulta de ejemplo que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="62120-109">You can get that shared calendar by specifying Garth’s user ID (or user principal name) in the example query shown below.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /users/{Garth-id | Garth-userPrincipalName}/calendar
```

<span data-ttu-id="62120-110">Esta capacidad se aplica a todas las operaciones de calendario GET compatibles para un usuario individual, como se muestra en la sección [solicitud HTTP](#http-request) a continuación.</span><span class="sxs-lookup"><span data-stu-id="62120-110">This capability applies to all the supported GET calendar operations for an individual user, as listed in the [HTTP request](#http-request) section below.</span></span> <span data-ttu-id="62120-111">También se aplica si Garth ha delegado todo el buzón en John.</span><span class="sxs-lookup"><span data-stu-id="62120-111">It also applies if Garth has delegated his entire mailbox to John.</span></span>

<span data-ttu-id="62120-112">Si Garth no ha compartido su calendario con John ni ha delegado su buzón en John, especificar el identificador de usuario del Garth o el nombre principal de usuario en esas operaciones GET devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="62120-112">If Garth has not shared his calendar with John, nor has he delegated his mailbox to John, specifying Garth’s user ID or user principal name in those GET operations will return an error.</span></span> <span data-ttu-id="62120-113">En tales casos, especificar un identificador de usuario o un nombre principal de usuario solo funciona para obtener un calendario del usuario que ha iniciado sesión, y la consulta es equivalente a usar el método abreviado de /me:</span><span class="sxs-lookup"><span data-stu-id="62120-113">In such cases, specifying a user ID or user principal name only works for getting a calendar of the signed-in user’s, and the query is equivalent to using the /me shortcut:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/calendar
```

<span data-ttu-id="62120-114">Esta capacidad solo está disponible en las operaciones GET de:</span><span class="sxs-lookup"><span data-stu-id="62120-114">This capability is available in only GET operations of:</span></span>

- <span data-ttu-id="62120-115">Carpetas de contactos compartidas</span><span class="sxs-lookup"><span data-stu-id="62120-115">Shared contact folders</span></span>
- <span data-ttu-id="62120-116">Calendarios compartidos</span><span class="sxs-lookup"><span data-stu-id="62120-116">Shared calendars</span></span>
- <span data-ttu-id="62120-117">Contactos y eventos en carpetas compartidas</span><span class="sxs-lookup"><span data-stu-id="62120-117">Contacts and events in shared folders</span></span>
- <span data-ttu-id="62120-118">Los recursos anteriores en buzones delegados</span><span class="sxs-lookup"><span data-stu-id="62120-118">The above resources in delegated mailboxes</span></span>

<span data-ttu-id="62120-119">Esta capacidad no está disponible en otras operaciones de contactos, eventos y sus carpetas.</span><span class="sxs-lookup"><span data-stu-id="62120-119">This capability is not available in other operations for contacts, events, and their folders.</span></span>


## <a name="permissions"></a><span data-ttu-id="62120-120">Permisos</span><span class="sxs-lookup"><span data-stu-id="62120-120">Permissions</span></span>
<span data-ttu-id="62120-p106">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="62120-p106">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="62120-123">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="62120-123">Permission type</span></span>      | <span data-ttu-id="62120-124">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="62120-124">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="62120-125">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="62120-125">Delegated (work or school account)</span></span> | <span data-ttu-id="62120-126">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="62120-126">Calendars.Read</span></span>    |
|<span data-ttu-id="62120-127">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="62120-127">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="62120-128">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="62120-128">Calendars.Read</span></span>    |
|<span data-ttu-id="62120-129">Aplicación</span><span class="sxs-lookup"><span data-stu-id="62120-129">Application</span></span> | <span data-ttu-id="62120-130">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="62120-130">Calendars.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="62120-131">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="62120-131">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="62120-132">[calendar](../resources/calendar.md) predeterminado de un usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="62120-132">A user's or group's default [calendar](../resources/calendar.md).</span></span>
```http
GET /me/calendar
GET /users/{id | userPrincipalName}/calendar
GET /groups/{id}/calendar
```
<span data-ttu-id="62120-133">[calendar](../resources/calendar.md) de un usuario del [calendarGroup](../resources/calendargroup.md) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="62120-133">A user's [calendar](../resources/calendar.md) in the default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
GET /me/calendars/{id}
GET /users/{id | userPrincipalName}/calendars/{id}

GET /me/calendarGroup/calendars/{id}
GET /users/{id | userPrincipalName}/calendarGroup/calendars/{id}
```
<span data-ttu-id="62120-134">[calendar](../resources/calendar.md) de un usuario de un [calendarGroup](../resources/calendargroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="62120-134">A user's [calendar](../resources/calendar.md) in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
```http
GET /me/calendarGroups/{id}/calendars/{id}
GET /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="62120-135">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="62120-135">Optional query parameters</span></span>
<span data-ttu-id="62120-136">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="62120-136">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="62120-137">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="62120-137">Request headers</span></span>
| <span data-ttu-id="62120-138">Nombre</span><span class="sxs-lookup"><span data-stu-id="62120-138">Name</span></span>       | <span data-ttu-id="62120-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="62120-139">Type</span></span> | <span data-ttu-id="62120-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="62120-140">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="62120-141">Authorization</span><span class="sxs-lookup"><span data-stu-id="62120-141">Authorization</span></span>  | <span data-ttu-id="62120-142">string</span><span class="sxs-lookup"><span data-stu-id="62120-142">string</span></span>  | <span data-ttu-id="62120-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="62120-p107">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="62120-145">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="62120-145">Request body</span></span>
<span data-ttu-id="62120-146">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="62120-146">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="62120-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="62120-147">Response</span></span>

<span data-ttu-id="62120-148">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [calendar](../resources/calendar.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="62120-148">If successful, this method returns a `200 OK` response code and [calendar](../resources/calendar.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="62120-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="62120-149">Example</span></span>
##### <a name="request"></a><span data-ttu-id="62120-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="62120-150">Request</span></span>
<span data-ttu-id="62120-151">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="62120-151">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_calendar"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendar
```
##### <a name="response"></a><span data-ttu-id="62120-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="62120-152">Response</span></span>
<span data-ttu-id="62120-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="62120-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendar"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#me/calendars/$entity",
    "@odata.id": "https://graph.microsoft.com/v1.0/users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/calendars('AAMkAGI2TGuLAAA=')",
    "id": "AAMkAGI2TGuLAAA=",
    "name": "Calendar",
    "color": "auto",
    "changeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x0+w==",
    "canShare":true,
    "canViewPrivateItems":true,
    "canEdit":true,
    "owner":{
        "name":"Samantha Booth",
        "address":"samanthab@adatum.onmicrosoft.com"
    }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get calendar",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
