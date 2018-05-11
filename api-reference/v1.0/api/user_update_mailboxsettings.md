# <a name="update-user-mailbox-settings"></a><span data-ttu-id="1ccc7-101">Actualizar la configuración del buzón del usuario</span><span class="sxs-lookup"><span data-stu-id="1ccc7-101">Update user mailbox settings</span></span>

<span data-ttu-id="1ccc7-p101">Actualice uno o varios valores de configuración del buzón del usuario. Esto incluye la configuración de las [respuestas automáticas](../resources/automaticrepliessetting.md) (avisar a los usuarios de forma automática tras la recepción de su correo electrónico), la [configuración regional](../resources/localeinfo.md) (idioma y país o región), la zona horaria y el [horario laboral](../resources/workinghours.md).</span><span class="sxs-lookup"><span data-stu-id="1ccc7-p101">Update one or more settings for the user's mailbox. This includes settings for automatic replies (notify people automatically upon receipt of their email), locale, or time zone.</span></span>

<span data-ttu-id="1ccc7-104">Puede habilitar, configurar o deshabilitar uno o varios de estos valores como parte de [mailboxSettings](../resources/mailboxsettings.md).</span><span class="sxs-lookup"><span data-stu-id="1ccc7-104">You can enable, configure, or disable one or more of these settings as part of [mailboxSettings](../resources/mailboxsettings.md).</span></span>

<span data-ttu-id="1ccc7-105">**Nota**: No puede crear ni eliminar ninguna configuración del buzón.</span><span class="sxs-lookup"><span data-stu-id="1ccc7-105">**Note** You cannot create or delete any mailbox settings.</span></span>

<span data-ttu-id="1ccc7-106">Al actualizar la zona horaria preferida de un usuario, puede especificarla en el formato Windows o en la [zona horaria de la autoridad de asignación de números de Internet (IANA)](http://www.iana.org/time-zones), también conocida como “zona horaria Olson”.</span><span class="sxs-lookup"><span data-stu-id="1ccc7-106">When you update the preferred time zone for a user, you can specify it in the Windows or  [Internet Assigned Numbers Authority (IANA) time zone](http://www.iana.org/time-zones) (also known as Olson time zone) format.</span></span>

## <a name="permissions"></a><span data-ttu-id="1ccc7-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="1ccc7-107">Permissions</span></span>
<span data-ttu-id="1ccc7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="1ccc7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="1ccc7-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1ccc7-110">Permission type</span></span>      | <span data-ttu-id="1ccc7-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1ccc7-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1ccc7-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1ccc7-112">Delegated (work or school account)</span></span> | <span data-ttu-id="1ccc7-113">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1ccc7-113">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="1ccc7-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1ccc7-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1ccc7-115">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1ccc7-115">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="1ccc7-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1ccc7-116">Application</span></span> | <span data-ttu-id="1ccc7-117">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1ccc7-117">MailboxSettings.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="1ccc7-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1ccc7-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/mailboxSettings
PATCH /users/{id|userPrincipalName}/mailboxSettings
```
## <a name="optional-query-parameters"></a><span data-ttu-id="1ccc7-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1ccc7-119">Optional query parameters</span></span>
<span data-ttu-id="1ccc7-120">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1ccc7-120">This method supports the [OData Query Parameters](http://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="1ccc7-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1ccc7-121">Request headers</span></span>
| <span data-ttu-id="1ccc7-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="1ccc7-122">Name</span></span>       | <span data-ttu-id="1ccc7-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="1ccc7-123">Type</span></span> | <span data-ttu-id="1ccc7-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ccc7-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="1ccc7-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="1ccc7-125">Authorization</span></span>  | <span data-ttu-id="1ccc7-126">string</span><span class="sxs-lookup"><span data-stu-id="1ccc7-126">string</span></span>  | <span data-ttu-id="1ccc7-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1ccc7-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="1ccc7-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1ccc7-129">Request body</span></span>
<span data-ttu-id="1ccc7-p104">En el cuerpo de la solicitud, proporcione los valores de las propiedades relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado. Las siguientes propiedades son modificables o actualizables:</span><span class="sxs-lookup"><span data-stu-id="1ccc7-p104">In the request body, supply the values for the relevant properties that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed. The following are the writable/updatable properties:</span></span>

| <span data-ttu-id="1ccc7-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1ccc7-134">Property</span></span>     | <span data-ttu-id="1ccc7-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="1ccc7-135">Type</span></span>   |<span data-ttu-id="1ccc7-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ccc7-136">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1ccc7-137">automaticRepliesSetting</span><span class="sxs-lookup"><span data-stu-id="1ccc7-137">automaticRepliesSetting</span></span>|[<span data-ttu-id="1ccc7-138">automaticRepliesSetting</span><span class="sxs-lookup"><span data-stu-id="1ccc7-138">automaticRepliesSetting</span></span>](../resources/automaticrepliessetting.md)|<span data-ttu-id="1ccc7-139">Opciones de configuración para notificar de forma automática al remitente de un mensaje de correo entrante con un mensaje del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="1ccc7-139">Configuration settings to automatically notify the sender of an incoming email with a message from the signed-in user.</span></span>|
|<span data-ttu-id="1ccc7-140">language</span><span class="sxs-lookup"><span data-stu-id="1ccc7-140">language</span></span>|[<span data-ttu-id="1ccc7-141">localeInfo</span><span class="sxs-lookup"><span data-stu-id="1ccc7-141">localeInfo</span></span>](../resources/localeinfo.md)|<span data-ttu-id="1ccc7-142">Representación de la configuración regional del usuario, como el idioma preferido y el país o región.</span><span class="sxs-lookup"><span data-stu-id="1ccc7-142">The locale information for the user, including the preferred language and country/region.</span></span>|
|<span data-ttu-id="1ccc7-143">timeZone</span><span class="sxs-lookup"><span data-stu-id="1ccc7-143">timeZone</span></span>|<span data-ttu-id="1ccc7-144">string</span><span class="sxs-lookup"><span data-stu-id="1ccc7-144">string</span></span>|<span data-ttu-id="1ccc7-145">La zona horaria predeterminada del buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="1ccc7-145">The default time zone for the user's mailbox.</span></span>|
|<span data-ttu-id="1ccc7-146">workingHours</span><span class="sxs-lookup"><span data-stu-id="1ccc7-146">workingHours</span></span>|[<span data-ttu-id="1ccc7-147">workingHours</span><span class="sxs-lookup"><span data-stu-id="1ccc7-147">workingHours</span></span>](../resources/workinghours.md)|<span data-ttu-id="1ccc7-148">Horas, días de la semana y zona horaria en la que trabaja el usuario.</span><span class="sxs-lookup"><span data-stu-id="1ccc7-148">The hours, days of a week, and time zone that the user works.</span></span>|

## <a name="response"></a><span data-ttu-id="1ccc7-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1ccc7-149">Response</span></span>

<span data-ttu-id="1ccc7-150">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [mailboxSettings](../resources/mailboxSettings.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1ccc7-150">If successful, this method returns a `200 OK` response code and [mailboxSettings](../resources/mailboxSettings.md) object in the response body.</span></span>


## <a name="errors"></a><span data-ttu-id="1ccc7-151">Errores</span><span class="sxs-lookup"><span data-stu-id="1ccc7-151">Errors</span></span>

<span data-ttu-id="1ccc7-152">Si se configura el horario laboral con valores incorrectos, pueden devolverse los errores siguientes.</span><span class="sxs-lookup"><span data-stu-id="1ccc7-152">Setting working hours with inappropriate values may return the following errors.</span></span>

| <span data-ttu-id="1ccc7-153">Escenario</span><span class="sxs-lookup"><span data-stu-id="1ccc7-153">Scenario</span></span>   | <span data-ttu-id="1ccc7-154">Código de estado HTTP</span><span class="sxs-lookup"><span data-stu-id="1ccc7-154">HTTP Status Code</span></span> | <span data-ttu-id="1ccc7-155">Código de error</span><span class="sxs-lookup"><span data-stu-id="1ccc7-155">Error code</span></span> | <span data-ttu-id="1ccc7-156">Mensaje de error</span><span class="sxs-lookup"><span data-stu-id="1ccc7-156">Error message</span></span> |
|:-----------|:------|:----------|:----------|
| <span data-ttu-id="1ccc7-157">**startTime** o **endTime** no válidos</span><span class="sxs-lookup"><span data-stu-id="1ccc7-157">Invalid **startTime** or **endTime**</span></span> | <span data-ttu-id="1ccc7-158">400</span><span class="sxs-lookup"><span data-stu-id="1ccc7-158">400</span></span> | <span data-ttu-id="1ccc7-159">RequestBodyRead</span><span class="sxs-lookup"><span data-stu-id="1ccc7-159">RequestBodyRead</span></span> | <span data-ttu-id="1ccc7-160">No se puede convertir el literal "08" al tipo esperado "Edm.TimeOfDay".</span><span class="sxs-lookup"><span data-stu-id="1ccc7-160">Cannot convert the literal '08' to the expected type 'Edm.TimeOfDay'.</span></span>|
| <span data-ttu-id="1ccc7-161">La hora de inicio es posterior a la hora de finalización</span><span class="sxs-lookup"><span data-stu-id="1ccc7-161">Start time is greater than end time</span></span> | <span data-ttu-id="1ccc7-162">400</span><span class="sxs-lookup"><span data-stu-id="1ccc7-162">400</span></span> | <span data-ttu-id="1ccc7-163">ErrorInvalidTimeSettings</span><span class="sxs-lookup"><span data-stu-id="1ccc7-163">ErrorInvalidTimeSettings</span></span> | <span data-ttu-id="1ccc7-164">La hora de inicio debe ser anterior a la hora de finalización.</span><span class="sxs-lookup"><span data-stu-id="1ccc7-164">Start Time should occur before End Time.</span></span> |
| <span data-ttu-id="1ccc7-165">Día no válido en **daysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="1ccc7-165">Invalid day in **daysOfWeek**</span></span> | <span data-ttu-id="1ccc7-166">400</span><span class="sxs-lookup"><span data-stu-id="1ccc7-166">400</span></span> | <span data-ttu-id="1ccc7-167">InvalidArguments</span><span class="sxs-lookup"><span data-stu-id="1ccc7-167">InvalidArguments</span></span> | <span data-ttu-id="1ccc7-168">No se encuentra el valor solicitado "RandomDay".</span><span class="sxs-lookup"><span data-stu-id="1ccc7-168">Requested value 'RandomDay' was not found.</span></span>|
| <span data-ttu-id="1ccc7-169">**timeZone** no válido</span><span class="sxs-lookup"><span data-stu-id="1ccc7-169">Invalid **timeZone**</span></span> | <span data-ttu-id="1ccc7-170">400</span><span class="sxs-lookup"><span data-stu-id="1ccc7-170">400</span></span> | <span data-ttu-id="1ccc7-171">InvalidTimeZone</span><span class="sxs-lookup"><span data-stu-id="1ccc7-171">InvalidTimeZone</span></span> | <span data-ttu-id="1ccc7-172">La configuración de zona horaria proporcionada no es válida.</span><span class="sxs-lookup"><span data-stu-id="1ccc7-172">Time Zone settings provided are invalid.</span></span>|


## <a name="example"></a><span data-ttu-id="1ccc7-173">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1ccc7-173">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1ccc7-174">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1ccc7-174">Request</span></span>
<span data-ttu-id="1ccc7-175">En el primer ejemplo se habilitan las respuestas automáticas para un intervalo de fechas; para ello, se establecen las siguientes propiedades de la propiedad **automaticRepliesSetting**: **status**, **scheduledStartDateTime** y **scheduledEndDateTime**.</span><span class="sxs-lookup"><span data-stu-id="1ccc7-175">The following example enables automatic replies for a date range, by setting the following properties of the **automaticRepliesSetting** property: **status**, **scheduledStartDateTime** and **scheduledEndDateTime**.</span></span>

<!-- {
  "blockType": "request",
  "name": "update_mailboxsettings"
}-->
```http
PATCH https://graph.microsoft.com/api/v1.0/me/mailboxSettings
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/api/v1.0/$metadata#Me/mailboxSettings",
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
##### <a name="response"></a><span data-ttu-id="1ccc7-176">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1ccc7-176">Response</span></span>
<span data-ttu-id="1ccc7-177">La respuesta incluye la configuración actualizada de las respuestas automáticas.</span><span class="sxs-lookup"><span data-stu-id="1ccc7-177">The response includes the updated settings for automatic replies.</span></span> <span data-ttu-id="1ccc7-178">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="1ccc7-178">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="1ccc7-179">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1ccc7-179">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailboxSettings"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/api/v1.0/$metadata#Me/mailboxSettings",
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


##### <a name="request-2"></a><span data-ttu-id="1ccc7-180">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="1ccc7-180">Request 2</span></span>
<span data-ttu-id="1ccc7-181">En el segundo ejemplo se personaliza la zona horaria del horario laboral del usuario que ha iniciado sesión; para ello, se establece la propiedad **timeZone** en una [zona horaria personalizada](../resources/customtimezone.md).</span><span class="sxs-lookup"><span data-stu-id="1ccc7-181">The second example customizes the time zone for the working hours of the signed-in user, by setting the **timeZone** property to a [custom time zone](../resources/customtimezone.md).</span></span>

<!-- {
  "blockType": "ignored",
  "name": "update_mailboxsettings_2"
}-->
```http
PATCH https://graph.microsoft.com/api/v1.0/me/mailboxSettings
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
##### <a name="response-2"></a><span data-ttu-id="1ccc7-182">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="1ccc7-182">Response 2</span></span>
<span data-ttu-id="1ccc7-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1ccc7-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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