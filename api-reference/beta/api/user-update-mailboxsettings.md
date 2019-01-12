---
title: Actualizar la configuración del buzón del usuario
description: Actualice uno o varios valores de configuración del buzón del usuario. Esto incluye la configuración de las respuestas automáticas (avisar a los usuarios de forma automática tras la recepción de su correo electrónico), la configuración regional (idioma y país o región), la zona horaria y el horario laboral.
localization_priority: Normal
author: dkershaw10
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 96896d7b5440887f023b4817195af2f55beb6752
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27938128"
---
# <a name="update-user-mailbox-settings"></a><span data-ttu-id="e425d-104">Actualizar la configuración del buzón del usuario</span><span class="sxs-lookup"><span data-stu-id="e425d-104">Update user mailbox settings</span></span>

> <span data-ttu-id="e425d-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e425d-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e425d-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e425d-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e425d-p103">Actualice uno o varios valores de configuración del buzón del usuario. Esto incluye la configuración de las [respuestas automáticas](../resources/automaticrepliessetting.md) (avisar a los usuarios de forma automática tras la recepción de su correo electrónico), la [configuración regional](../resources/localeinfo.md) (idioma y país o región), la zona horaria y el [horario laboral](../resources/workinghours.md).</span><span class="sxs-lookup"><span data-stu-id="e425d-p103">Update one or more settings for the user's mailbox. This includes settings for [automatic replies](../resources/automaticrepliessetting.md) (notify people automatically upon receipt of their email), [locale](../resources/localeinfo.md) (language and country/region), time zone, and [working hours](../resources/workinghours.md).</span></span>

<span data-ttu-id="e425d-109">Puede habilitar, configurar o deshabilitar uno o varios de estos valores como parte de [mailboxSettings](../resources/mailboxsettings.md).</span><span class="sxs-lookup"><span data-stu-id="e425d-109">You can enable, configure, or disable one or more of these settings as part of [mailboxSettings](../resources/mailboxsettings.md).</span></span>

<span data-ttu-id="e425d-110">**Nota**: No puede crear ni eliminar ninguna configuración del buzón.</span><span class="sxs-lookup"><span data-stu-id="e425d-110">**Note** You cannot create or delete any mailbox settings.</span></span>

<span data-ttu-id="e425d-111">Al actualizar la zona horaria preferida de un usuario, puede especificarla en el formato Windows o en la [zona horaria de la autoridad de asignación de números de Internet (IANA)](https://www.iana.org/time-zones), también conocida como “zona horaria Olson”.</span><span class="sxs-lookup"><span data-stu-id="e425d-111">When you update the preferred time zone for a user, you can specify it in the Windows or  [Internet Assigned Numbers Authority (IANA) time zone](https://www.iana.org/time-zones) (also known as Olson time zone) format.</span></span> <span data-ttu-id="e425d-112">Se puede personalizar también aún más la zona horaria tal como se muestra en [el ejemplo 2](#request-2) a continuación.</span><span class="sxs-lookup"><span data-stu-id="e425d-112">You can also further customize the time zone as shown in [example 2](#request-2) below.</span></span>

## <a name="permissions"></a><span data-ttu-id="e425d-113">Permisos</span><span class="sxs-lookup"><span data-stu-id="e425d-113">Permissions</span></span>
<span data-ttu-id="e425d-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e425d-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e425d-116">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e425d-116">Permission type</span></span>      | <span data-ttu-id="e425d-117">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e425d-117">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e425d-118">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e425d-118">Delegated (work or school account)</span></span> | <span data-ttu-id="e425d-119">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e425d-119">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="e425d-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e425d-120">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e425d-121">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e425d-121">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="e425d-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e425d-122">Application</span></span> | <span data-ttu-id="e425d-123">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e425d-123">MailboxSettings.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="e425d-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e425d-124">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/mailboxSettings
PATCH /users/{id|userPrincipalName}/mailboxSettings
```
## <a name="optional-query-parameters"></a><span data-ttu-id="e425d-125">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e425d-125">Optional query parameters</span></span>
<span data-ttu-id="e425d-126">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e425d-126">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="e425d-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e425d-127">Request headers</span></span>
| <span data-ttu-id="e425d-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="e425d-128">Name</span></span>       | <span data-ttu-id="e425d-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="e425d-129">Type</span></span> | <span data-ttu-id="e425d-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="e425d-130">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="e425d-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="e425d-131">Authorization</span></span>  | <span data-ttu-id="e425d-132">string</span><span class="sxs-lookup"><span data-stu-id="e425d-132">string</span></span>  | <span data-ttu-id="e425d-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e425d-p106">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e425d-135">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e425d-135">Request body</span></span>
<span data-ttu-id="e425d-p107">En el cuerpo de la solicitud, proporcione los valores de las propiedades relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado. Las siguientes propiedades son modificables o actualizables:</span><span class="sxs-lookup"><span data-stu-id="e425d-p107">In the request body, supply the values for the relevant properties that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed. The following are the writable/updatable properties:</span></span>

| <span data-ttu-id="e425d-140">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e425d-140">Property</span></span>     | <span data-ttu-id="e425d-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="e425d-141">Type</span></span>   |<span data-ttu-id="e425d-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="e425d-142">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e425d-143">automaticRepliesSetting</span><span class="sxs-lookup"><span data-stu-id="e425d-143">automaticRepliesSetting</span></span>|[<span data-ttu-id="e425d-144">automaticRepliesSetting</span><span class="sxs-lookup"><span data-stu-id="e425d-144">automaticRepliesSetting</span></span>](../resources/automaticrepliessetting.md)|<span data-ttu-id="e425d-145">Opciones de configuración para notificar de forma automática al remitente de un mensaje de correo entrante con un mensaje del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="e425d-145">Configuration settings to automatically notify the sender of an incoming email with a message from the signed-in user.</span></span> <span data-ttu-id="e425d-146">Puede establecer tales notificaciones para sólo un intervalo de fechas futuras.</span><span class="sxs-lookup"><span data-stu-id="e425d-146">You can set such notifications for only a future date range.</span></span>|
|<span data-ttu-id="e425d-147">language</span><span class="sxs-lookup"><span data-stu-id="e425d-147">language</span></span>|[<span data-ttu-id="e425d-148">localeInfo</span><span class="sxs-lookup"><span data-stu-id="e425d-148">localeInfo</span></span>](../resources/localeinfo.md)|<span data-ttu-id="e425d-149">Representación de la configuración regional del usuario, como el idioma preferido y el país o región.</span><span class="sxs-lookup"><span data-stu-id="e425d-149">The locale information for the user, including the preferred language and country/region.</span></span>|
|<span data-ttu-id="e425d-150">timeZone</span><span class="sxs-lookup"><span data-stu-id="e425d-150">timeZone</span></span>|<span data-ttu-id="e425d-151">string</span><span class="sxs-lookup"><span data-stu-id="e425d-151">string</span></span>|<span data-ttu-id="e425d-152">La zona horaria predeterminada del buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="e425d-152">The default time zone for the user's mailbox.</span></span>|
|<span data-ttu-id="e425d-153">workingHours</span><span class="sxs-lookup"><span data-stu-id="e425d-153">workingHours</span></span>|[<span data-ttu-id="e425d-154">workingHours</span><span class="sxs-lookup"><span data-stu-id="e425d-154">workingHours</span></span>](../resources/workinghours.md)|<span data-ttu-id="e425d-155">Horas, días de la semana y zona horaria en la que trabaja el usuario.</span><span class="sxs-lookup"><span data-stu-id="e425d-155">The hours, days of a week, and time zone that the user works.</span></span>|

## <a name="response"></a><span data-ttu-id="e425d-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e425d-156">Response</span></span>

<span data-ttu-id="e425d-157">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [mailboxSettings](../resources/mailboxsettings.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e425d-157">If successful, this method returns a `200 OK` response code and [mailboxSettings](../resources/mailboxsettings.md) object in the response body.</span></span>

## <a name="errors"></a><span data-ttu-id="e425d-158">Errores</span><span class="sxs-lookup"><span data-stu-id="e425d-158">Errors</span></span>

<span data-ttu-id="e425d-159">Si se configura el horario laboral con valores incorrectos, pueden devolverse los errores siguientes.</span><span class="sxs-lookup"><span data-stu-id="e425d-159">Setting working hours with inappropriate values may return the following errors.</span></span>

| <span data-ttu-id="e425d-160">Escenario</span><span class="sxs-lookup"><span data-stu-id="e425d-160">Scenario</span></span>   | <span data-ttu-id="e425d-161">Código de estado HTTP</span><span class="sxs-lookup"><span data-stu-id="e425d-161">HTTP status code</span></span> | <span data-ttu-id="e425d-162">Código de error</span><span class="sxs-lookup"><span data-stu-id="e425d-162">Error code</span></span> | <span data-ttu-id="e425d-163">Mensaje de error</span><span class="sxs-lookup"><span data-stu-id="e425d-163">Error message</span></span> |
|:-----------|:------|:----------|:----------|
| <span data-ttu-id="e425d-164">**startTime** o **endTime** no válidos</span><span class="sxs-lookup"><span data-stu-id="e425d-164">Invalid **startTime** or **endTime**</span></span> | <span data-ttu-id="e425d-165">400</span><span class="sxs-lookup"><span data-stu-id="e425d-165">400</span></span> | <span data-ttu-id="e425d-166">RequestBodyRead</span><span class="sxs-lookup"><span data-stu-id="e425d-166">RequestBodyRead</span></span> | <span data-ttu-id="e425d-167">No se puede convertir el literal "08" al tipo esperado "Edm.TimeOfDay".</span><span class="sxs-lookup"><span data-stu-id="e425d-167">Cannot convert the literal '08' to the expected type 'Edm.TimeOfDay'.</span></span>|
| <span data-ttu-id="e425d-168">La hora de inicio es posterior a la hora de finalización</span><span class="sxs-lookup"><span data-stu-id="e425d-168">Start time is greater than end time</span></span> | <span data-ttu-id="e425d-169">400</span><span class="sxs-lookup"><span data-stu-id="e425d-169">400</span></span> | <span data-ttu-id="e425d-170">ErrorInvalidTimeSettings</span><span class="sxs-lookup"><span data-stu-id="e425d-170">ErrorInvalidTimeSettings</span></span> | <span data-ttu-id="e425d-171">La hora de inicio debe ser anterior a la hora de finalización.</span><span class="sxs-lookup"><span data-stu-id="e425d-171">Start Time should occur before End Time.</span></span> |
| <span data-ttu-id="e425d-172">Día no válido en **daysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="e425d-172">Invalid day in **daysOfWeek**</span></span> | <span data-ttu-id="e425d-173">400</span><span class="sxs-lookup"><span data-stu-id="e425d-173">400</span></span> | <span data-ttu-id="e425d-174">InvalidArguments</span><span class="sxs-lookup"><span data-stu-id="e425d-174">InvalidArguments</span></span> | <span data-ttu-id="e425d-175">No se encuentra el valor solicitado "RandomDay".</span><span class="sxs-lookup"><span data-stu-id="e425d-175">Requested value 'RandomDay' was not found.</span></span>|
| <span data-ttu-id="e425d-176">**timeZone** no válido</span><span class="sxs-lookup"><span data-stu-id="e425d-176">Invalid **timeZone**</span></span> | <span data-ttu-id="e425d-177">400</span><span class="sxs-lookup"><span data-stu-id="e425d-177">400</span></span> | <span data-ttu-id="e425d-178">InvalidTimeZone</span><span class="sxs-lookup"><span data-stu-id="e425d-178">InvalidTimeZone</span></span> | <span data-ttu-id="e425d-179">La configuración de zona horaria proporcionada no es válida.</span><span class="sxs-lookup"><span data-stu-id="e425d-179">Time Zone settings provided are invalid.</span></span>|


## <a name="example"></a><span data-ttu-id="e425d-180">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e425d-180">Example</span></span>
##### <a name="request-1"></a><span data-ttu-id="e425d-181">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="e425d-181">Request 1</span></span>
<span data-ttu-id="e425d-182">En el primer ejemplo se habilitan las respuestas automáticas para un intervalo de fechas; para ello, se establecen las siguientes propiedades de la propiedad **automaticRepliesSetting**: **status**, **scheduledStartDateTime** y **scheduledEndDateTime**.</span><span class="sxs-lookup"><span data-stu-id="e425d-182">The first example enables automatic replies for a date range, by setting the following properties of the **automaticRepliesSetting** property: **status**, **scheduledStartDateTime** and **scheduledEndDateTime**.</span></span>

<!-- {
  "blockType": "request",
  "name": "update_mailboxsettings_1"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/mailboxSettings
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#Me/mailboxSettings",
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
##### <a name="response-1"></a><span data-ttu-id="e425d-183">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="e425d-183">Response 1</span></span>
<span data-ttu-id="e425d-184">La respuesta incluye la configuración actualizada de las respuestas automáticas.</span><span class="sxs-lookup"><span data-stu-id="e425d-184">The response includes the updated settings for automatic replies.</span></span> <span data-ttu-id="e425d-185">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="e425d-185">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="e425d-186">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e425d-186">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "name": "update_mailboxsettings_1",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailboxSettings"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#Me/mailboxSettings",
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


##### <a name="request-2"></a><span data-ttu-id="e425d-187">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="e425d-187">Request 2</span></span>
<span data-ttu-id="e425d-188">En el segundo ejemplo se personaliza la zona horaria del horario laboral del usuario que ha iniciado sesión; para ello, se establece la propiedad **timeZone** en una [zona horaria personalizada](../resources/customtimezone.md).</span><span class="sxs-lookup"><span data-stu-id="e425d-188">The second example customizes the time zone for the working hours of the signed-in user, by setting the **timeZone** property to a [custom time zone](../resources/customtimezone.md).</span></span>

<!-- {
  "blockType": "ignored",
  "name": "update_mailboxsettings_2"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/mailboxSettings
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
##### <a name="response-2"></a><span data-ttu-id="e425d-189">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="e425d-189">Response 2</span></span>
<span data-ttu-id="e425d-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e425d-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#users('94447c6e-ea4c-494c-a9ed-d905e366c5cb')/mailboxSettings",
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
