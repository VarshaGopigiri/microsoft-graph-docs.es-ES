# <a name="event-delta"></a><span data-ttu-id="38d37-101">event: delta</span><span class="sxs-lookup"><span data-stu-id="38d37-101">event: delta</span></span>

<span data-ttu-id="38d37-102">Obtenga un conjunto de eventos que se han agregado, eliminado o actualizado en una **calendarView** (un intervalo de eventos) del calendario principal del usuario.</span><span class="sxs-lookup"><span data-stu-id="38d37-102">Get a set of events that have been added, deleted, or updated in a **calendarView** (a range of events) of the user's primary calendar.</span></span>

<span data-ttu-id="38d37-p101">La llamada de una función **delta** para eventos funciona de forma similar a una solicitud `GET /calendarview` para un intervalo de fechas en el calendario principal del usuario, salvo que, al aplicar correctamente los [tokens de estado](../../../concepts/delta_query_overview.md) en al menos una de estas llamadas, pueda realizar una consulta para obtener los cambios incrementales en la vista del calendario. Esto permite mantener y sincronizar un almacén local de eventos de un usuario en el calendario principal, sin tener que capturar cada vez todos los eventos de ese calendario desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="38d37-p101">A **delta** function call for events is similar to a `GET /calendarview` request for a range of dates in the user's primary calendar, except that by appropriately applying [state tokens](../../../concepts/delta_query_overview.md) in one or more of these calls, you can query for incremental changes in that calender view. This allows you to maintain and synchronize a local store of a user's events in the primary calendar, without having to fetch all the events of that calendar from the server every time.</span></span>

## <a name="permissions"></a><span data-ttu-id="38d37-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="38d37-105">Permissions</span></span>
<span data-ttu-id="38d37-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="38d37-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="38d37-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="38d37-108">Permission type</span></span>      | <span data-ttu-id="38d37-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="38d37-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="38d37-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="38d37-110">Delegated (work or school account)</span></span> | <span data-ttu-id="38d37-111">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="38d37-111">Calendars.Read</span></span>    |
|<span data-ttu-id="38d37-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="38d37-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="38d37-113">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="38d37-113">Calendars.Read</span></span>    |
|<span data-ttu-id="38d37-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="38d37-114">Application</span></span> | <span data-ttu-id="38d37-115">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="38d37-115">Calendars.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="38d37-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="38d37-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendarView/delta?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id}/calendarView/delta?startDateTime={start_datetime}&endDateTime={end_datetime}

```

### <a name="query-parameters"></a><span data-ttu-id="38d37-117">Parámetros de consulta</span><span class="sxs-lookup"><span data-stu-id="38d37-117">Query parameters</span></span>

<span data-ttu-id="38d37-p103">El seguimiento de cambios en los eventos conlleva al menos una llamada de una función **delta**. Si usa cualquier parámetro de consulta (distinto de `$deltatoken` y `$skiptoken`), debe especificarlo en la solicitud **delta** inicial. Microsoft Graph codifica automáticamente cualquier parámetro especificado en la parte del token de la URL `nextLink` o `deltaLink` proporcionada en la respuesta. Solo debe especificar una vez por adelantado los parámetros de consulta deseados. En solicitudes posteriores, basta con copiar y aplicar la dirección URL `nextLink` o `deltaLink` de la respuesta anterior, dado que la dirección URL ya incluye los parámetros codificados deseados.</span><span class="sxs-lookup"><span data-stu-id="38d37-p103">Tracking changes in events incurs a round of one or more **delta** function calls. If you use any query parameter (other than `$deltatoken` and `$skiptoken`), you must specify it in the initial **delta** request. Microsoft Graph automatically encodes any specified parameters into the token portion of the `nextLink` or `deltaLink` URL provided in the response. You only need to specify any desired query parameters once upfront. In subsequent requests, simply copy and apply the `nextLink` or `deltaLink` URL from the previous response, as that URL already includes the encoded, desired parameters.</span></span>


| <span data-ttu-id="38d37-123">Parámetro de consulta</span><span class="sxs-lookup"><span data-stu-id="38d37-123">Query parameter</span></span>      | <span data-ttu-id="38d37-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="38d37-124">Type</span></span>   |<span data-ttu-id="38d37-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="38d37-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="38d37-126">startDateTime</span><span class="sxs-lookup"><span data-stu-id="38d37-126">startDateTime</span></span>|<span data-ttu-id="38d37-127">String</span><span class="sxs-lookup"><span data-stu-id="38d37-127">String</span></span>|<span data-ttu-id="38d37-p104">La fecha y hora de inicio del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T19:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="38d37-p104">The start date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T19:00:00.0000000".</span></span>|
|<span data-ttu-id="38d37-130">endDateTime</span><span class="sxs-lookup"><span data-stu-id="38d37-130">endDateTime</span></span>|<span data-ttu-id="38d37-131">String</span><span class="sxs-lookup"><span data-stu-id="38d37-131">String</span></span>|<span data-ttu-id="38d37-p105">La fecha y hora de finalización del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T20:00:00.0000000".</span><span class="sxs-lookup"><span data-stu-id="38d37-p105">The end date and time of the time range, represented in ISO 8601 format. For example, "2015-11-08T20:00:00.0000000".</span></span>|
| <span data-ttu-id="38d37-134">$deltatoken</span><span class="sxs-lookup"><span data-stu-id="38d37-134">$deltatoken</span></span> | <span data-ttu-id="38d37-135">string</span><span class="sxs-lookup"><span data-stu-id="38d37-135">string</span></span> | <span data-ttu-id="38d37-p106">[Token de estado](../../../concepts/delta_query_overview.md) que se devuelve en la dirección URL de `deltaLink` de la llamada de función **delta** anterior para la misma colección de usuarios. Indica el progreso de la ronda de seguimiento de cambios. Guarde y aplique toda la dirección URL `deltaLink`, incluido este token, en la primera solicitud de la siguiente ronda de seguimiento de la vista del calendario.</span><span class="sxs-lookup"><span data-stu-id="38d37-p106">A [state token](../../../concepts/delta_query_overview.md) returned in the `deltaLink` URL of the previous **delta** function call for the same calendar view, indicating the completion of that round of change tracking. Save and apply the entire `deltaLink` URL including this token in the first request of the next round of change tracking for that calendar view.</span></span>|
| <span data-ttu-id="38d37-138">$skiptoken</span><span class="sxs-lookup"><span data-stu-id="38d37-138">$skiptoken</span></span> | <span data-ttu-id="38d37-139">string</span><span class="sxs-lookup"><span data-stu-id="38d37-139">string</span></span> | <span data-ttu-id="38d37-140">[Token de estado](../../../concepts/delta_query_overview.md) que se devuelve en la dirección URL de `nextLink` de la llamada de función **delta**. Indica que debe realizarse el seguimiento de más cambios en la misma vista del calendario.</span><span class="sxs-lookup"><span data-stu-id="38d37-140">A [state token](../../../concepts/delta_query_overview.md) returned in the `nextLink` URL of the previous **delta** function call, indicating there are further changes to be tracked in the same calendar view.</span></span> |

<span data-ttu-id="38d37-p107">Al hacer una consulta delta en una vista del calendario, se espera obtener todas las propiedades que se obtendrían con normalidad de una solicitud `GET /calendarview`. `$select` no se admite en este caso.</span><span class="sxs-lookup"><span data-stu-id="38d37-p107">When you do a delta query on a calendar view, expect to get all the properties you'd normally get from a `GET /calendarview` request. `$select` is not supported in this case.</span></span> 


## <a name="request-headers"></a><span data-ttu-id="38d37-143">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="38d37-143">Request headers</span></span>
| <span data-ttu-id="38d37-144">Nombre</span><span class="sxs-lookup"><span data-stu-id="38d37-144">Name</span></span>       | <span data-ttu-id="38d37-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="38d37-145">Type</span></span> | <span data-ttu-id="38d37-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="38d37-146">Description</span></span> |
|:---------------|:----------|:----------|
| <span data-ttu-id="38d37-147">Authorization</span><span class="sxs-lookup"><span data-stu-id="38d37-147">Authorization</span></span>  | <span data-ttu-id="38d37-148">cadena</span><span class="sxs-lookup"><span data-stu-id="38d37-148">string</span></span>  | <span data-ttu-id="38d37-p108">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="38d37-p108">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="38d37-151">Content-Type</span><span class="sxs-lookup"><span data-stu-id="38d37-151">Content-Type</span></span>  | <span data-ttu-id="38d37-152">string</span><span class="sxs-lookup"><span data-stu-id="38d37-152">string</span></span>  | <span data-ttu-id="38d37-p109">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="38d37-p109">application/json. Required.</span></span> |
| <span data-ttu-id="38d37-155">Prefer</span><span class="sxs-lookup"><span data-stu-id="38d37-155">Prefer</span></span> | <span data-ttu-id="38d37-156">string</span><span class="sxs-lookup"><span data-stu-id="38d37-156">string</span></span>  | <span data-ttu-id="38d37-p110">odata.maxpagesize={x}. Opcional.</span><span class="sxs-lookup"><span data-stu-id="38d37-p110">odata.maxpagesize={x}. Optional.</span></span> |
| <span data-ttu-id="38d37-159">Prefer</span><span class="sxs-lookup"><span data-stu-id="38d37-159">Prefer</span></span> | <span data-ttu-id="38d37-160">string</span><span class="sxs-lookup"><span data-stu-id="38d37-160">string</span></span> | <span data-ttu-id="38d37-p111">{Zona horaria}. Opcional, se supone la hora UTC si no se encuentra.</span><span class="sxs-lookup"><span data-stu-id="38d37-p111">{Time zone}. Optional, UTC assumed if absent.</span></span>|

## <a name="response"></a><span data-ttu-id="38d37-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="38d37-163">Response</span></span>

<span data-ttu-id="38d37-164">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto de colección [event](../resources/event.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="38d37-164">If successful, this method returns a `200 OK` response code and [event](../resources/event.md) collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="38d37-165">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="38d37-165">Example</span></span>
##### <a name="request"></a><span data-ttu-id="38d37-166">Solicitud</span><span class="sxs-lookup"><span data-stu-id="38d37-166">Request</span></span>

<span data-ttu-id="38d37-167">En el ejemplo siguiente se muestra cómo realizar una llamada de función **delta** única y limitar el número máximo de eventos en el cuerpo de la respuesta a 2.</span><span class="sxs-lookup"><span data-stu-id="38d37-167">The following example shows how to make a single **delta** function call, and limit the maximum number of events in the response body to 2.</span></span>

<span data-ttu-id="38d37-168">Para realizar un seguimiento de la vista del calendario, debería realizar al menos una llamada de función **delta**, con unos [tokens de estado](../../../concepts/delta_query_overview.md) adecuados, para obtener el conjunto de cambios incrementales desde la última consulta delta.</span><span class="sxs-lookup"><span data-stu-id="38d37-168">To track changes in a calendar view, you would make one or more **delta** function calls, with appropriate [state tokens](../../../concepts/delta_query_overview.md), to get the set of incremental changes since the last delta query.</span></span> 

<!-- {
  "blockType": "request",
  "name": "event_delta"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendarView/delta?startdatetime={start_datetime}&enddatetime={end_datetime}

Prefer: odata.maxpagesize=2
```

##### <a name="response"></a><span data-ttu-id="38d37-169">Respuesta</span><span class="sxs-lookup"><span data-stu-id="38d37-169">Response</span></span>
<span data-ttu-id="38d37-p112">Si la solicitud es correcta, la respuesta debería incluir un token de estado, que puede ser un _skipToken_ (en un encabezado de respuesta _@odata.nextLink_) o un _deltaToken_ (en un encabezado de respuesta _@odata.deltaLink_). Respectivamente, indican si debe continuar con la ronda, o bien si ha terminado de obtener todos los cambios de la ronda.</span><span class="sxs-lookup"><span data-stu-id="38d37-p112">If the request is successful, the response would include a state token, which is either a _skipToken_ (in an _@odata.nextLink_ response header) or a _deltaToken_ (in an _@odata.deltaLink_ response header). Respectively, they indicate whether you should continue with the round or you have completed getting all the changes for that round.</span></span>

<span data-ttu-id="38d37-172">La respuesta siguiente muestra un _skipToken_ en un encabezado de respuesta de _@odata.nextLink_.</span><span class="sxs-lookup"><span data-stu-id="38d37-172">The response below shows a _skipToken_ in an _@odata.nextLink_ response header.</span></span>

<span data-ttu-id="38d37-p113">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="38d37-p113">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.event",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 359

{
  "@odata.nextLink":"https://graph.microsoft.com/v1.0/me/calendarView/delta?$skiptoken={_skipToken_}",
  "value": [
    {
      "originalStartTimeZone": "originalStartTimeZone-value",
      "originalEndTimeZone": "originalEndTimeZone-value",
      "responseStatus": {
        "response": "response-value",
        "time": "datetime-value"
      },
      "iCalUId": "iCalUId-value",
      "reminderMinutesBeforeStart": 99,
      "isReminderOn": true
    }
  ]
}
```

### <a name="see-also"></a><span data-ttu-id="38d37-175">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="38d37-175">See also</span></span>

- [<span data-ttu-id="38d37-176">Usar la consulta delta para realizar el seguimiento de los cambios en datos de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="38d37-176">Use delta query to track changes in Microsoft Graph data</span></span>](../../../concepts/delta_query_overview.md)
- [<span data-ttu-id="38d37-177">Obtener los cambios incrementales en los eventos en un calendario</span><span class="sxs-lookup"><span data-stu-id="38d37-177">Get incremental changes to events in a calendar</span></span>](../../../concepts/delta_query_events.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "event: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->