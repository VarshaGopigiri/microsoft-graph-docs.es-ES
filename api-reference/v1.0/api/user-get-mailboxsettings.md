---
title: Obtener configuración del buzón del usuario
description: 'Obtener mailboxSettings del usuario. Esto incluye la configuración de respuestas automáticas (informar a las personas automáticamente al '
localization_priority: Priority
author: dkershaw10
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 0e68d50cde270c20c76bce1e703ff07ff45c2107
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27914566"
---
# <a name="get-user-mailbox-settings"></a><span data-ttu-id="d2eb8-104">Obtener configuración del buzón del usuario</span><span class="sxs-lookup"><span data-stu-id="d2eb8-104">Get user mailbox settings</span></span>

<span data-ttu-id="d2eb8-p102">Obtenga el objeto [mailboxSettings](../resources/mailboxsettings.md) del usuario. Esto incluye la configuración de las respuestas automáticas (avisar a los usuarios de forma automática tras la recepción de su correo electrónico), la configuración regional (idioma y país o región), la zona horaria y el horario laboral.</span><span class="sxs-lookup"><span data-stu-id="d2eb8-p102">Get the user's [mailboxSettings](../resources/mailboxsettings.md). This includes settings for automatic replies (notify people automatically upon receipt of their email), locale (language and country/region), and time zone, and working hours.</span></span>

<span data-ttu-id="d2eb8-107">Puede ver toda la configuración del buzón u obtener una configuración específica.</span><span class="sxs-lookup"><span data-stu-id="d2eb8-107">You can view all mailbox settings, or, get specific settings.</span></span>

<span data-ttu-id="d2eb8-108">La zona horaria es una de las opciones preferidas que puede configurar un usuario para su buzón.</span><span class="sxs-lookup"><span data-stu-id="d2eb8-108">Time zone is one of the preferred settings a user can set up for the user's mailbox.</span></span> <span data-ttu-id="d2eb8-109">Los formatos de zona horaria válidos son el formato Windows y la [zona horaria de la autoridad de asignación de números de Internet (IANA)](https://www.iana.org/time-zones), también conocida como “zona horaria Olson”.</span><span class="sxs-lookup"><span data-stu-id="d2eb8-109">Valid time zone formats include the Windows time zone format and [Internet Assigned Numbers Authority (IANA) time zone](https://www.iana.org/time-zones) (also known as Olson time zone) format.</span></span> <span data-ttu-id="d2eb8-110">El formato Windows es el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d2eb8-110">The Windows format is the default.</span></span> 

<span data-ttu-id="d2eb8-111">Cuando se obtiene la zona horaria preferida de un usuario, esta se devuelve en el formato en el que se configuró.</span><span class="sxs-lookup"><span data-stu-id="d2eb8-111">When you get a user's preferred time zone, the time zone is returned in the format that it was set up.</span></span> <span data-ttu-id="d2eb8-112">Si quiere que esa zona horaria se muestre en un formato específico (Windows o IANA), puede [actualizar primero la zona horaria preferida en ese formato como opción de configuración del buzón](user-update-mailboxsettings.md).</span><span class="sxs-lookup"><span data-stu-id="d2eb8-112">If you want that time zone to be in a specific format (Windows or IANA), you can first [update the preferred time zone in that format as a mailbox setting](user-update-mailboxsettings.md).</span></span> <span data-ttu-id="d2eb8-113">Posteriormente, podrá obtener la zona horaria en ese formato.</span><span class="sxs-lookup"><span data-stu-id="d2eb8-113">Subsequently you will be able to get the time zone in that format.</span></span> <span data-ttu-id="d2eb8-114">Como alternativa, puede administrar la conversión de formato por separado en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d2eb8-114">Alternatively, you can manage the format conversion separately in your app.</span></span>

## <a name="permissions"></a><span data-ttu-id="d2eb8-115">Permisos</span><span class="sxs-lookup"><span data-stu-id="d2eb8-115">Permissions</span></span>
<span data-ttu-id="d2eb8-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d2eb8-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d2eb8-118">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d2eb8-118">Permission type</span></span>      | <span data-ttu-id="d2eb8-119">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d2eb8-119">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d2eb8-120">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d2eb8-120">Delegated (work or school account)</span></span> | <span data-ttu-id="d2eb8-121">MailboxSettings.Read, MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d2eb8-121">MailboxSettings.Read, MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="d2eb8-122">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d2eb8-122">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d2eb8-123">MailboxSettings.Read, MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d2eb8-123">MailboxSettings.Read, MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="d2eb8-124">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d2eb8-124">Application</span></span> | <span data-ttu-id="d2eb8-125">MailboxSettings.Read, MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d2eb8-125">MailboxSettings.Read, MailboxSettings.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="d2eb8-126">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d2eb8-126">HTTP request</span></span>
<span data-ttu-id="d2eb8-127">Para obtener todas las opciones de buzón de correo para un usuario:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="d2eb8-127">To get all mailbox settings for a user: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/mailboxSettings
GET /users/{id|userPrincipalName}/mailboxSettings
```

<span data-ttu-id="d2eb8-128">Para obtener la configuración específica - por ejemplo, sólo las respuestas automáticas configuración, configuración regional, zona horaria u horario laboral:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="d2eb8-128">To get specific settings - for example, only the automatic replies settings, locale, time zone, or working hours: <!-- { "blockType": "ignored" } --></span></span>
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
## <a name="optional-query-parameters"></a><span data-ttu-id="d2eb8-129">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="d2eb8-129">Optional query parameters</span></span>
<span data-ttu-id="d2eb8-130">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d2eb8-130">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="d2eb8-131">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d2eb8-131">Request headers</span></span>
| <span data-ttu-id="d2eb8-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="d2eb8-132">Name</span></span>       | <span data-ttu-id="d2eb8-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="d2eb8-133">Type</span></span> | <span data-ttu-id="d2eb8-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2eb8-134">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="d2eb8-135">Autorización</span><span class="sxs-lookup"><span data-stu-id="d2eb8-135">Authorization</span></span>  | <span data-ttu-id="d2eb8-136">string</span><span class="sxs-lookup"><span data-stu-id="d2eb8-136">string</span></span>  | <span data-ttu-id="d2eb8-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d2eb8-p106">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="d2eb8-139">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d2eb8-139">Request body</span></span>
<span data-ttu-id="d2eb8-140">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d2eb8-140">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d2eb8-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2eb8-141">Response</span></span>

<span data-ttu-id="d2eb8-142">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y uno de los siguientes objetos solicitados en el cuerpo de la respuesta:</span><span class="sxs-lookup"><span data-stu-id="d2eb8-142">If successful, this method returns a `200 OK` response code and one of the following requested objects in the response body:</span></span>

- <span data-ttu-id="d2eb8-143">Objeto [mailboxSettings](../resources/mailboxsettings.md)</span><span class="sxs-lookup"><span data-stu-id="d2eb8-143">[mailboxSettings](../resources/mailboxsettings.md) object</span></span>
- <span data-ttu-id="d2eb8-144">Objeto [automaticRepliesSetting](../resources/automaticrepliessetting.md)</span><span class="sxs-lookup"><span data-stu-id="d2eb8-144">[automaticRepliesSetting](../resources/automaticrepliessetting.md) object</span></span>
- <span data-ttu-id="d2eb8-145">Objeto [localeInfo](../resources/localeinfo.md)</span><span class="sxs-lookup"><span data-stu-id="d2eb8-145">[localeInfo](../resources/localeinfo.md) object</span></span>
- <span data-ttu-id="d2eb8-146">string (para **timeZone**)</span><span class="sxs-lookup"><span data-stu-id="d2eb8-146">string (for **timeZone**)</span></span>
- [<span data-ttu-id="d2eb8-147">workingHours</span><span class="sxs-lookup"><span data-stu-id="d2eb8-147">workingHours</span></span>](../resources/workinghours.md)

## <a name="example"></a><span data-ttu-id="d2eb8-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d2eb8-148">Example</span></span>
##### <a name="request-1"></a><span data-ttu-id="d2eb8-149">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="d2eb8-149">Request 1</span></span>
<span data-ttu-id="d2eb8-150">En el primer ejemplo se obtiene toda la configuración del buzón del usuario que ha iniciado sesión, que incluye la configuración de la zona horaria, las respuestas automáticas, la configuración regional (idioma y país o región) y el horario laboral.</span><span class="sxs-lookup"><span data-stu-id="d2eb8-150">The first example gets all the mailbox settings of the signed-in user's mailbox, which include settings for time zone, automatic replies, locale (language and country/region), and working hours.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_mailboxsettings_1"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/mailboxSettings
```
##### <a name="response-1"></a><span data-ttu-id="d2eb8-151">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="d2eb8-151">Response 1</span></span>
<span data-ttu-id="d2eb8-p107">La respuesta incluye toda la configuración del buzón. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d2eb8-p107">The response includes all the mailbox settings. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
        "startTime":"08:00:00.000",
        "endTime":"17:00:00.000",
        "timeZone":{
            "name":"Pacific Standard Time"
        }
    }
}
```

##### <a name="request-2"></a><span data-ttu-id="d2eb8-155">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="d2eb8-155">Request 2</span></span>
<span data-ttu-id="d2eb8-156">El segundo ejemplo obtiene específicamente la configuración de las respuestas automáticas del buzón del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="d2eb8-156">The second example gets specifically the automatic replies settings of the signed-in user's mailbox.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_mailboxsettings_2"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/mailboxSettings/automaticRepliesSetting
```
##### <a name="response-2"></a><span data-ttu-id="d2eb8-157">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="d2eb8-157">Response 2</span></span>
<span data-ttu-id="d2eb8-p108">La respuesta incluye solo la configuración de las respuestas automáticas. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d2eb8-p108">The response includes only the automatic replies settings. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.automaticRepliesSetting"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Me/mailboxSettings/automaticRepliesSetting",
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


##### <a name="request-3"></a><span data-ttu-id="d2eb8-161">Solicitud 3</span><span class="sxs-lookup"><span data-stu-id="d2eb8-161">Request 3</span></span>
<span data-ttu-id="d2eb8-162">En el tercer ejemplo se obtiene específicamente la configuración del horario laboral del buzón del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="d2eb8-162">The third example gets specifically the working hour settings of the signed-in user's mailbox.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_mailboxsettings_3"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/mailboxSettings/workingHours
```
##### <a name="response-3"></a><span data-ttu-id="d2eb8-163">Respuesta 3</span><span class="sxs-lookup"><span data-stu-id="d2eb8-163">Response 3</span></span>
<span data-ttu-id="d2eb8-164">La respuesta solo incluye la configuración del horario laboral.</span><span class="sxs-lookup"><span data-stu-id="d2eb8-164">The response includes only the working hours settings.</span></span> <span data-ttu-id="d2eb8-165">Observe que la jornada laboral del usuario se encuentra en una [zona horaria personalizada](../resources/customtimezone.md).</span><span class="sxs-lookup"><span data-stu-id="d2eb8-165">Notice that the user's work hours are in a [custom time zone](../resources/customtimezone.md).</span></span> <span data-ttu-id="d2eb8-166">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="d2eb8-166">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="d2eb8-167">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d2eb8-167">All of the properties will be returned from an actual call.</span></span>
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
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('94447c6e-ea4c-494c-a9ed-d905e366c5cb')/mailboxSettings/workingHours",
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
