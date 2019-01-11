---
title: Obtener configuración del buzón del usuario
description: 'Obtener mailboxSettings del usuario. Esto incluye la configuración de respuestas automáticas (informar a las personas automáticamente al '
localization_priority: Normal
ms.openlocfilehash: 2d1e2ce16d82e89e701bbe90386c28b76d1607c0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27880181"
---
# <a name="get-user-mailbox-settings"></a><span data-ttu-id="4bac9-104">Obtener configuración del buzón del usuario</span><span class="sxs-lookup"><span data-stu-id="4bac9-104">Get user mailbox settings</span></span>

> <span data-ttu-id="4bac9-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4bac9-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4bac9-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4bac9-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4bac9-107">Obtenga del usuario [mailboxSettings](../resources/mailboxsettings.md).</span><span class="sxs-lookup"><span data-stu-id="4bac9-107">Get the user's [mailboxSettings](../resources/mailboxsettings.md).</span></span> <span data-ttu-id="4bac9-108">Esto incluye la configuración de respuestas automáticas (informar a las personas automáticamente tras la recepción de su correo electrónico), configuración regional (idioma y país o región), zona horaria y horario laboral.</span><span class="sxs-lookup"><span data-stu-id="4bac9-108">This includes settings for automatic replies (notify people automatically upon receipt of their email), locale (language and country/region), time zone, and working hours.</span></span>

<span data-ttu-id="4bac9-109">Puede ver toda la configuración del buzón u obtener una configuración específica.</span><span class="sxs-lookup"><span data-stu-id="4bac9-109">You can view all mailbox settings, or, get specific settings.</span></span>

<span data-ttu-id="4bac9-110">La zona horaria es una de las opciones preferidas que puede configurar un usuario para su buzón.</span><span class="sxs-lookup"><span data-stu-id="4bac9-110">Time zone is one of the preferred settings a user can set up for the user's mailbox.</span></span> <span data-ttu-id="4bac9-111">El usuario lo elige desde la [admite zonas horarias](outlookuser-supportedtimezones.md) que un administrador ha configurado para el servidor de buzón de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="4bac9-111">The user chooses it from the [supported time zones](outlookuser-supportedtimezones.md) that an administrator has set up for the user's mailbox server.</span></span> <span data-ttu-id="4bac9-112">El administrador configura las zonas horarias en el formato de la [zona horaria de autoridad de números asignados de Internet (IANA)](https://www.iana.org/time-zones) (también conocido como zona horaria de Olson) o el formato de la zona horaria de Windows.</span><span class="sxs-lookup"><span data-stu-id="4bac9-112">The administrator sets up time zones in the Windows time zone format or  [Internet Assigned Numbers Authority (IANA) time zone](https://www.iana.org/time-zones) (also known as Olson time zone) format.</span></span> <span data-ttu-id="4bac9-113">El formato Windows es el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4bac9-113">The Windows format is the default.</span></span> 

<span data-ttu-id="4bac9-114">Cuando se obtiene la zona horaria preferida de un usuario, esta se devuelve en el formato en el que se configuró.</span><span class="sxs-lookup"><span data-stu-id="4bac9-114">When you get a user's preferred time zone, the time zone is returned in the format that it was set up.</span></span> <span data-ttu-id="4bac9-115">Si quiere que esa zona horaria se muestre en un formato específico (Windows o IANA), puede [actualizar primero la zona horaria preferida en ese formato como opción de configuración del buzón](user-update-mailboxsettings.md).</span><span class="sxs-lookup"><span data-stu-id="4bac9-115">If you want that time zone to be in a specific format (Windows or IANA), you can first [update the preferred time zone in that format as a mailbox setting](user-update-mailboxsettings.md).</span></span> <span data-ttu-id="4bac9-116">Posteriormente, podrá obtener la zona horaria en ese formato.</span><span class="sxs-lookup"><span data-stu-id="4bac9-116">Subsequently you will be able to get the time zone in that format.</span></span> <span data-ttu-id="4bac9-117">Como alternativa, puede administrar la conversión de formato por separado en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4bac9-117">Alternatively, you can manage the format conversion separately in your app.</span></span>

## <a name="permissions"></a><span data-ttu-id="4bac9-118">Permisos</span><span class="sxs-lookup"><span data-stu-id="4bac9-118">Permissions</span></span>
<span data-ttu-id="4bac9-p106">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4bac9-p106">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4bac9-121">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4bac9-121">Permission type</span></span>      | <span data-ttu-id="4bac9-122">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4bac9-122">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4bac9-123">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4bac9-123">Delegated (work or school account)</span></span> | <span data-ttu-id="4bac9-124">MailboxSettings.Read, MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4bac9-124">MailboxSettings.Read, MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="4bac9-125">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4bac9-125">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4bac9-126">MailboxSettings.Read, MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4bac9-126">MailboxSettings.Read, MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="4bac9-127">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4bac9-127">Application</span></span> | <span data-ttu-id="4bac9-128">MailboxSettings.Read, MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4bac9-128">MailboxSettings.Read, MailboxSettings.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="4bac9-129">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4bac9-129">HTTP request</span></span>
<span data-ttu-id="4bac9-130">Para obtener todas las opciones de buzón de correo para un usuario:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="4bac9-130">To get all the mailbox settings for a user: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/mailboxSettings
GET /users/{id|userPrincipalName}/mailboxSettings
```

<span data-ttu-id="4bac9-131">Para obtener la configuración específica - sólo la configuración de respuestas automáticas, configuración regional, zona horaria u horario laboral:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="4bac9-131">To get specific settings - only the automatic replies settings, locale, time zone, or working hours: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/mailboxSettings/automaticRepliesSetting
GET /users/{id|userPrincipalName}/mailboxSettings/automaticRepliesSetting

GET /me/mailboxSettings/language
GET /users/{id|userPrincipalName}/mailboxSettings/language

GET /me/mailboxSettings/timeZone
GET /users/{id|userPrincipalName}/mailboxSettings/timeZone

GET /me/mailboxSettings/workingHours
GET /users/{id|userPrincipalName}/mailboxSettings/workingHours
```
## <a name="optional-query-parameters"></a><span data-ttu-id="4bac9-132">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="4bac9-132">Optional query parameters</span></span>
<span data-ttu-id="4bac9-133">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4bac9-133">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="4bac9-134">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4bac9-134">Request headers</span></span>
| <span data-ttu-id="4bac9-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="4bac9-135">Name</span></span>       | <span data-ttu-id="4bac9-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="4bac9-136">Type</span></span> | <span data-ttu-id="4bac9-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="4bac9-137">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="4bac9-138">Autorización</span><span class="sxs-lookup"><span data-stu-id="4bac9-138">Authorization</span></span>  | <span data-ttu-id="4bac9-139">string</span><span class="sxs-lookup"><span data-stu-id="4bac9-139">string</span></span>  | <span data-ttu-id="4bac9-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4bac9-p107">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4bac9-142">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4bac9-142">Request body</span></span>
<span data-ttu-id="4bac9-143">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4bac9-143">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4bac9-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4bac9-144">Response</span></span>

<span data-ttu-id="4bac9-145">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y uno de los siguientes objetos solicitados en el cuerpo de la respuesta:</span><span class="sxs-lookup"><span data-stu-id="4bac9-145">If successful, this method returns a `200 OK` response code and one of the following requested objects in the response body:</span></span>

- <span data-ttu-id="4bac9-146">Objeto [mailboxSettings](../resources/mailboxsettings.md)</span><span class="sxs-lookup"><span data-stu-id="4bac9-146">[mailboxSettings](../resources/mailboxsettings.md) object</span></span>
- <span data-ttu-id="4bac9-147">Objeto [automaticRepliesSetting](../resources/automaticrepliessetting.md)</span><span class="sxs-lookup"><span data-stu-id="4bac9-147">[automaticRepliesSetting](../resources/automaticrepliessetting.md) object</span></span>
- <span data-ttu-id="4bac9-148">Objeto [localeInfo](../resources/localeinfo.md)</span><span class="sxs-lookup"><span data-stu-id="4bac9-148">[localeInfo](../resources/localeinfo.md) object</span></span>
- <span data-ttu-id="4bac9-149">string (para **timeZone**)</span><span class="sxs-lookup"><span data-stu-id="4bac9-149">string (for **timeZone**)</span></span>
- [<span data-ttu-id="4bac9-150">workingHours</span><span class="sxs-lookup"><span data-stu-id="4bac9-150">workingHours</span></span>](../resources/workinghours.md)

## <a name="example"></a><span data-ttu-id="4bac9-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4bac9-151">Example</span></span>
##### <a name="request-1"></a><span data-ttu-id="4bac9-152">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="4bac9-152">Request 1</span></span>
<span data-ttu-id="4bac9-153">En el primer ejemplo se obtiene toda la configuración del buzón del usuario que ha iniciado sesión, que incluye la configuración de la zona horaria, las respuestas automáticas, la configuración regional (idioma y país o región) y el horario laboral.</span><span class="sxs-lookup"><span data-stu-id="4bac9-153">The first example gets all the mailbox settings of the signed-in user's mailbox, which include settings for time zone, automatic replies, locale (language and country/region), and working hours.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_mailboxsettings_1"
}-->
```http
GET https://graph.microsoft.com/beta/me/mailboxSettings
```
##### <a name="response-1"></a><span data-ttu-id="4bac9-154">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="4bac9-154">Response 1</span></span>
<span data-ttu-id="4bac9-155">La respuesta incluye todas las opciones de buzón de correo del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="4bac9-155">The response includes all the mailbox settings of the signed-in user.</span></span> <span data-ttu-id="4bac9-156">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="4bac9-156">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="4bac9-157">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4bac9-157">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailboxSettings"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#Me/mailboxSettings",
    "automaticRepliesSetting": {
        "status": "Scheduled",
        "externalAudience": "All",
        "scheduledStartDateTime": {
            "dateTime": "2016-03-14T07:00:00.0000000",
            "timeZone": "UTC"
        },
        "scheduledEndDateTime": {
            "dateTime": "2016-03-28T07:00:00.0000000",
            "timeZone": "UTC"
        },
        "internalReplyMessage": "<html>\n<body>\n<p>I'm at our company's worldwide reunion and will respond to your message as soon as I return.<br>\n</p></body>\n</html>\n",
        "externalReplyMessage": "<html>\n<body>\n<p>I'm at the Contoso worldwide reunion and will respond to your message as soon as I return.<br>\n</p></body>\n</html>\n"
    },
    "timeZone":"UTC",
    "language":{
      "locale":"en-US",
      "displayName":"English (United States)"
    },
    "workingHours":{
        "daysOfWeek":[
            "monday",
            "tuesday",
            "wednesday",
            "thursday",
            "friday"
        ],
        "startTime":"08:00:00.0000000",
        "endTime":"17:00:00.0000000",
        "timeZone":{
            "name":"Pacific Standard Time"
        }
    }
}
```

##### <a name="request-2"></a><span data-ttu-id="4bac9-158">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="4bac9-158">Request 2</span></span>
<span data-ttu-id="4bac9-159">El segundo ejemplo obtiene específicamente la configuración de las respuestas automáticas del buzón del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="4bac9-159">The second example gets specifically the automatic replies settings of the signed-in user's mailbox.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_mailboxsettings_2"
}-->
```http
GET https://graph.microsoft.com/beta/me/mailboxSettings/automaticRepliesSetting
```
##### <a name="response-2"></a><span data-ttu-id="4bac9-160">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="4bac9-160">Response 2</span></span>
<span data-ttu-id="4bac9-p109">La respuesta incluye solo la configuración de las respuestas automáticas. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4bac9-p109">The response includes only the automatic replies settings. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.automaticRepliesSetting"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#Me/mailboxSettings/automaticRepliesSetting",
    "status": "alwaysEnabled",
    "externalAudience": "None",
    "scheduledStartDateTime": {
        "dateTime": "2016-03-19T02:00:00.0000000",
        "timeZone": "UTC"
    },
    "scheduledEndDateTime": {
        "dateTime": "2016-03-20T02:00:00.0000000",
        "timeZone": "UTC"
    },
    "internalReplyMessage": "<html>\n<body>\n<p>I'm at our company's worldwide reunion and will respond to your message as soon as I return.<br>\n</p></body>\n</html>\n",
    "externalReplyMessage": "<html>\n<body>\n<p>I'm at the Contoso worldwide reunion and will respond to your message as soon as I return.<br>\n</p></body>\n</html>\n"
}
```


##### <a name="request-3"></a><span data-ttu-id="4bac9-164">Solicitud 3</span><span class="sxs-lookup"><span data-stu-id="4bac9-164">Request 3</span></span>
<span data-ttu-id="4bac9-165">En el tercer ejemplo se obtiene específicamente la configuración del horario laboral del buzón del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="4bac9-165">The third example gets specifically the working hour settings of the signed-in user's mailbox.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_mailboxsettings_3"
}-->
```http
GET https://graph.microsoft.com/beta/me/mailboxSettings/workingHours
```
##### <a name="response-3"></a><span data-ttu-id="4bac9-166">Respuesta 3</span><span class="sxs-lookup"><span data-stu-id="4bac9-166">Response 3</span></span>
<span data-ttu-id="4bac9-167">La respuesta solo incluye la configuración del horario laboral.</span><span class="sxs-lookup"><span data-stu-id="4bac9-167">The response includes only the working hours settings.</span></span> <span data-ttu-id="4bac9-168">Observe que la jornada laboral del usuario se encuentra en una [zona horaria personalizada](../resources/customtimezone.md).</span><span class="sxs-lookup"><span data-stu-id="4bac9-168">Notice that the user's work hours are in a [custom time zone](../resources/customtimezone.md).</span></span> <span data-ttu-id="4bac9-169">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="4bac9-169">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="4bac9-170">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4bac9-170">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_mailboxsettings_3",
  "truncated": true,
  "@odata.type": "microsoft.graph.workingHours"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#users('94447c6e-ea4c-494c-a9ed-d905e366c5cb')/mailboxSettings/workingHours",
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
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get mailbox settings",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
