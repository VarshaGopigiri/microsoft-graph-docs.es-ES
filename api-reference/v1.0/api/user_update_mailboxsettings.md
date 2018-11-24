# <a name="update-user-mailbox-settings"></a><span data-ttu-id="c8093-101">Actualizar la configuración del buzón del usuario</span><span class="sxs-lookup"><span data-stu-id="c8093-101">Update user mailbox settings</span></span>

<span data-ttu-id="c8093-p101">Actualice uno o varios valores de configuración del buzón del usuario. Esto incluye la configuración de las [respuestas automáticas](../resources/automaticrepliessetting.md) (avisar a los usuarios de forma automática tras la recepción de su correo electrónico), la [configuración regional](../resources/localeinfo.md) (idioma y país o región), la zona horaria y el [horario laboral](../resources/workinghours.md).</span><span class="sxs-lookup"><span data-stu-id="c8093-p101">Update one or more settings for the user's mailbox. This includes settings for [automatic replies](../resources/automaticrepliessetting.md) (notify people automatically upon receipt of their email), [locale](../resources/localeinfo.md) (language and country/region), time zone, and [working hours](../resources/workinghours.md).</span></span>

<span data-ttu-id="c8093-104">Puede habilitar, configurar o deshabilitar uno o varios de estos valores como parte de [mailboxSettings](../resources/mailboxsettings.md).</span><span class="sxs-lookup"><span data-stu-id="c8093-104">You can enable, configure, or disable one or more of these settings as part of [mailboxSettings](../resources/mailboxsettings.md).</span></span>

<span data-ttu-id="c8093-105">**Nota**: No puede crear ni eliminar ninguna configuración del buzón.</span><span class="sxs-lookup"><span data-stu-id="c8093-105">**Note** You cannot create or delete any mailbox settings.</span></span>

<span data-ttu-id="c8093-106">Al actualizar la zona horaria preferida de un usuario, puede especificarla en el formato Windows o en la [zona horaria de la autoridad de asignación de números de Internet (IANA)](https://www.iana.org/time-zones), también conocida como “zona horaria Olson”.</span><span class="sxs-lookup"><span data-stu-id="c8093-106">When you update the preferred time zone for a user, you can specify it in the Windows or  [Internet Assigned Numbers Authority (IANA) time zone](https://www.iana.org/time-zones) (also known as Olson time zone) format.</span></span>

## <a name="permissions"></a><span data-ttu-id="c8093-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="c8093-107">Permissions</span></span>
<span data-ttu-id="c8093-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c8093-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="c8093-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c8093-110">Permission type</span></span>      | <span data-ttu-id="c8093-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c8093-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c8093-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c8093-112">Delegated (work or school account)</span></span> | <span data-ttu-id="c8093-113">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c8093-113">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="c8093-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c8093-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c8093-115">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c8093-115">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="c8093-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c8093-116">Application</span></span> | <span data-ttu-id="c8093-117">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c8093-117">MailboxSettings.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="c8093-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c8093-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/mailboxSettings
PATCH /users/{id|userPrincipalName}/mailboxSettings
```
## <a name="optional-query-parameters"></a><span data-ttu-id="c8093-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c8093-119">Optional query parameters</span></span>
<span data-ttu-id="c8093-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c8093-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="c8093-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c8093-121">Request headers</span></span>
| <span data-ttu-id="c8093-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="c8093-122">Name</span></span>       | <span data-ttu-id="c8093-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="c8093-123">Type</span></span> | <span data-ttu-id="c8093-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8093-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="c8093-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="c8093-125">Authorization</span></span>  | <span data-ttu-id="c8093-126">string</span><span class="sxs-lookup"><span data-stu-id="c8093-126">string</span></span>  | <span data-ttu-id="c8093-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c8093-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c8093-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c8093-129">Request body</span></span>
<span data-ttu-id="c8093-p104">En el cuerpo de la solicitud, proporcione los valores de las propiedades relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado. Las siguientes propiedades son modificables o actualizables:</span><span class="sxs-lookup"><span data-stu-id="c8093-p104">In the request body, supply the values for the relevant properties that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed. The following are the writable/updatable properties:</span></span>

| <span data-ttu-id="c8093-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c8093-134">Property</span></span>     | <span data-ttu-id="c8093-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="c8093-135">Type</span></span>   |<span data-ttu-id="c8093-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8093-136">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c8093-137">automaticRepliesSetting</span><span class="sxs-lookup"><span data-stu-id="c8093-137">automaticRepliesSetting</span></span>|[<span data-ttu-id="c8093-138">automaticRepliesSetting</span><span class="sxs-lookup"><span data-stu-id="c8093-138">automaticRepliesSetting</span></span>](../resources/automaticrepliessetting.md)|<span data-ttu-id="c8093-139">Opciones de configuración para notificar de forma automática al remitente de un mensaje de correo entrante con un mensaje del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="c8093-139">Configuration settings to automatically notify the sender of an incoming email with a message from the signed-in user.</span></span> <span data-ttu-id="c8093-140">Puede establecer tales notificaciones para sólo un intervalo de fechas futuras.</span><span class="sxs-lookup"><span data-stu-id="c8093-140">You can set such notifications for only a future date range.</span></span>|
|<span data-ttu-id="c8093-141">language</span><span class="sxs-lookup"><span data-stu-id="c8093-141">language</span></span>|[<span data-ttu-id="c8093-142">localeInfo</span><span class="sxs-lookup"><span data-stu-id="c8093-142">localeInfo</span></span>](../resources/localeinfo.md)|<span data-ttu-id="c8093-143">Representación de la configuración regional del usuario, como el idioma preferido y el país o región.</span><span class="sxs-lookup"><span data-stu-id="c8093-143">The locale information for the user, including the preferred language and country/region.</span></span>|
|<span data-ttu-id="c8093-144">timeZone</span><span class="sxs-lookup"><span data-stu-id="c8093-144">timeZone</span></span>|<span data-ttu-id="c8093-145">string</span><span class="sxs-lookup"><span data-stu-id="c8093-145">string</span></span>|<span data-ttu-id="c8093-146">La zona horaria predeterminada del buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="c8093-146">The default time zone for the user's mailbox.</span></span>|
|<span data-ttu-id="c8093-147">workingHours</span><span class="sxs-lookup"><span data-stu-id="c8093-147">workingHours</span></span>|[<span data-ttu-id="c8093-148">workingHours</span><span class="sxs-lookup"><span data-stu-id="c8093-148">workingHours</span></span>](../resources/workinghours.md)|<span data-ttu-id="c8093-149">Horas, días de la semana y zona horaria en la que trabaja el usuario.</span><span class="sxs-lookup"><span data-stu-id="c8093-149">The hours, days of a week, and time zone that the user works.</span></span>|

## <a name="response"></a><span data-ttu-id="c8093-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c8093-150">Response</span></span>

<span data-ttu-id="c8093-151">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [mailboxSettings](../resources/mailboxSettings.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c8093-151">If successful, this method returns a `200 OK` response code and [mailboxSettings](../resources/mailboxSettings.md) object in the response body.</span></span>


## <a name="errors"></a><span data-ttu-id="c8093-152">Errores</span><span class="sxs-lookup"><span data-stu-id="c8093-152">Errors</span></span>

<span data-ttu-id="c8093-153">Si se configura el horario laboral con valores incorrectos, pueden devolverse los errores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c8093-153">Setting working hours with inappropriate values may return the following errors.</span></span>

| <span data-ttu-id="c8093-154">Escenario</span><span class="sxs-lookup"><span data-stu-id="c8093-154">Scenario</span></span>   | <span data-ttu-id="c8093-155">Código de estado HTTP</span><span class="sxs-lookup"><span data-stu-id="c8093-155">HTTP status code</span></span> | <span data-ttu-id="c8093-156">Código de error</span><span class="sxs-lookup"><span data-stu-id="c8093-156">Error code</span></span> | <span data-ttu-id="c8093-157">Mensaje de error</span><span class="sxs-lookup"><span data-stu-id="c8093-157">Error message</span></span> |
|:-----------|:------|:----------|:----------|
| <span data-ttu-id="c8093-158">**startTime** o **endTime** no válidos</span><span class="sxs-lookup"><span data-stu-id="c8093-158">Invalid **startTime** or **endTime**</span></span> | <span data-ttu-id="c8093-159">400</span><span class="sxs-lookup"><span data-stu-id="c8093-159">400</span></span> | <span data-ttu-id="c8093-160">RequestBodyRead</span><span class="sxs-lookup"><span data-stu-id="c8093-160">RequestBodyRead</span></span> | <span data-ttu-id="c8093-161">No se puede convertir el literal "08" al tipo esperado "Edm.TimeOfDay".</span><span class="sxs-lookup"><span data-stu-id="c8093-161">Cannot convert the literal '08' to the expected type 'Edm.TimeOfDay'.</span></span>|
| <span data-ttu-id="c8093-162">La hora de inicio es posterior a la hora de finalización</span><span class="sxs-lookup"><span data-stu-id="c8093-162">Start time is greater than end time</span></span> | <span data-ttu-id="c8093-163">400</span><span class="sxs-lookup"><span data-stu-id="c8093-163">400</span></span> | <span data-ttu-id="c8093-164">ErrorInvalidTimeSettings</span><span class="sxs-lookup"><span data-stu-id="c8093-164">ErrorInvalidTimeSettings</span></span> | <span data-ttu-id="c8093-165">La hora de inicio debe ser anterior a la hora de finalización.</span><span class="sxs-lookup"><span data-stu-id="c8093-165">Start Time should occur before End Time.</span></span> |
| <span data-ttu-id="c8093-166">Día no válido en **daysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="c8093-166">Invalid day in **daysOfWeek**</span></span> | <span data-ttu-id="c8093-167">400</span><span class="sxs-lookup"><span data-stu-id="c8093-167">400</span></span> | <span data-ttu-id="c8093-168">InvalidArguments</span><span class="sxs-lookup"><span data-stu-id="c8093-168">InvalidArguments</span></span> | <span data-ttu-id="c8093-169">No se encuentra el valor solicitado "RandomDay".</span><span class="sxs-lookup"><span data-stu-id="c8093-169">Requested value 'RandomDay' was not found.</span></span>|
| <span data-ttu-id="c8093-170">**timeZone** no válido</span><span class="sxs-lookup"><span data-stu-id="c8093-170">Invalid **timeZone**</span></span> | <span data-ttu-id="c8093-171">400</span><span class="sxs-lookup"><span data-stu-id="c8093-171">400</span></span> | <span data-ttu-id="c8093-172">InvalidTimeZone</span><span class="sxs-lookup"><span data-stu-id="c8093-172">InvalidTimeZone</span></span> | <span data-ttu-id="c8093-173">La configuración de zona horaria proporcionada no es válida.</span><span class="sxs-lookup"><span data-stu-id="c8093-173">Time Zone settings provided are invalid.</span></span>|


## <a name="example"></a><span data-ttu-id="c8093-174">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c8093-174">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c8093-175">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c8093-175">Request</span></span>
<span data-ttu-id="c8093-176">En el primer ejemplo se habilitan las respuestas automáticas para un intervalo de fechas; para ello, se establecen las siguientes propiedades de la propiedad **automaticRepliesSetting**: **status**, **scheduledStartDateTime** y **scheduledEndDateTime**.</span><span class="sxs-lookup"><span data-stu-id="c8093-176">The first example enables automatic replies for a date range, by setting the following properties of the **automaticRepliesSetting** property: **status**, **scheduledStartDateTime** and **scheduledEndDateTime**.</span></span>

<!-- {
  "blockType": "request",
  "name": "update_mailboxsettings"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/mailboxSettings
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Me/mailboxSettings",
    "automaticRepliesSetting": {
        "status": "Scheduled",
        "scheduledStartDateTime": {
          "dateTime": "2016-03-20T18:00:00.0000000",
          "timeZone": "UTC"
        },
        "scheduledEndDateTime": {
          "dateTime": "2016-03-28T18:00:00.0000000",
          "timeZone": "UTC"
        }
    }
}
```
##### <a name="response"></a><span data-ttu-id="c8093-177">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c8093-177">Response</span></span>
<span data-ttu-id="c8093-178">La respuesta incluye la configuración actualizada de las respuestas automáticas.</span><span class="sxs-lookup"><span data-stu-id="c8093-178">The response includes the updated settings for automatic replies.</span></span> <span data-ttu-id="c8093-179">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="c8093-179">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="c8093-180">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c8093-180">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailboxSettings"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Me/mailboxSettings",
    "automaticRepliesSetting": {
        "status": "scheduled",
        "externalAudience": "all",
        "scheduledStartDateTime": {
            "dateTime": "2016-03-20T02:00:00.0000000",
            "timeZone": "UTC"
        },
        "scheduledEndDateTime": {
            "dateTime": "2016-03-28T02:00:00.0000000",
            "timeZone": "UTC"
        },
    "internalReplyMessage": "<html>\n<body>\n<p>I'm at our company's worldwide reunion and will respond to your message as soon as I return.<br>\n</p></body>\n</html>\n",
    "externalReplyMessage": "<html>\n<body>\n<p>I'm at the Contoso worldwide reunion and will respond to your message as soon as I return.<br>\n</p></body>\n</html>\n"
    }
}
```


##### <a name="request-2"></a><span data-ttu-id="c8093-181">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="c8093-181">Request 2</span></span>
<span data-ttu-id="c8093-182">En el segundo ejemplo se personaliza la zona horaria del horario laboral del usuario que ha iniciado sesión; para ello, se establece la propiedad **timeZone** en una [zona horaria personalizada](../resources/customtimezone.md).</span><span class="sxs-lookup"><span data-stu-id="c8093-182">The second example customizes the time zone for the working hours of the signed-in user, by setting the **timeZone** property to a [custom time zone](../resources/customtimezone.md).</span></span>

<!-- {
  "blockType": "ignored",
  "name": "update_mailboxsettings_2"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/mailboxSettings
Content-Type: application/json

{
  "workingHours": {
      "endTime" : "18:30:00.0000000", 
      "daysOfWeek": [ 
          "Monday", 
          "Tuesday", 
          "Wednesday", 
          "Thursday", 
          "Friday", 
          "Saturday" 
      ], 
      "timeZone" : { 
         "@odata.type": "#microsoft.graph.customTimeZone", 
         "bias":-300, 
         "name": "Customized Time Zone",
         "standardOffset":{   
           "time":"02:00:00.0000000", 
           "dayOccurrence":2, 
           "dayOfWeek":"Sunday", 
           "month":10, 
           "year":0 
         }, 
         "daylightOffset":{   
           "daylightBias":100, 
           "time":"02:00:00.0000000", 
           "dayOccurrence":4, 
           "dayOfWeek":"Sunday", 
           "month":5, 
           "year":0 
         } 
      } 
  }
} 
```
##### <a name="response-2"></a><span data-ttu-id="c8093-183">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="c8093-183">Response 2</span></span>
<span data-ttu-id="c8093-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c8093-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "update_mailboxsettings_2",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailboxSettings"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('94447c6e-ea4c-494c-a9ed-d905e366c5cb')/mailboxSettings",
    "workingHours":{
        "daysOfWeek":[
            "monday",
            "tuesday",
            "wednesday",
            "thursday",
            "friday",
            "saturday"
        ],
        "startTime":"09:00:00.0000000",
        "endTime":"18:30:00.0000000",
        "timeZone":{
            "@odata.type":"#microsoft.graph.customTimeZone",
            "bias":-200,
            "name":"Customized Time Zone",
            "standardOffset":{
                "time":"02:00:00.0000000",
                "dayOccurrence":4,
                "dayOfWeek":"sunday",
                "month":5,
                "year":0
            },
            "daylightOffset":{
                "daylightBias":-100,
                "time":"02:00:00.0000000",
                "dayOccurrence":2,
                "dayOfWeek":"sunday",
                "month":10,
                "year":0
            }
        }
    }
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update mailbox settings",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->