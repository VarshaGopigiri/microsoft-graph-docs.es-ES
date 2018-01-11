# <a name="get-user-mailbox-settings"></a><span data-ttu-id="3e103-101">Obtener configuración del buzón del usuario</span><span class="sxs-lookup"><span data-stu-id="3e103-101">Get user mailbox settings</span></span>

<span data-ttu-id="3e103-p101">Obtener el objeto [mailboxSettings](../resources/mailboxsettings.md) del usuario. Esto incluye la configuración de las respuestas automáticas (avisar a los usuarios de forma automática tras la recepción de su correo electrónico), configuración regional (idioma y país o región) y zona horaria.</span><span class="sxs-lookup"><span data-stu-id="3e103-p101">Get the user's [mailboxSettings](../resources/mailboxsettings.md). This includes settings for automatic replies (notify people automatically upon receipt of their email), locale (language and country/region), and time zone.</span></span>

<span data-ttu-id="3e103-104">Puede ver toda la configuración del buzón u obtener una configuración específica.</span><span class="sxs-lookup"><span data-stu-id="3e103-104">You can view all mailbox settings, or, get specific settings.</span></span>

<span data-ttu-id="3e103-105">La zona horaria es una de las opciones preferidas que puede configurar un usuario para su buzón.</span><span class="sxs-lookup"><span data-stu-id="3e103-105">Time zone is one of the preferred settings a user can set up for the user's mailbox.</span></span> <span data-ttu-id="3e103-106">Los formatos de zona horaria válidos son el formato Windows y la [zona horaria de la autoridad de asignación de números de Internet (IANA)]((http://www.iana.org/time-zones)), también conocida como “zona horaria Olson”.</span><span class="sxs-lookup"><span data-stu-id="3e103-106">Valid time zone formats include the Windows time zone format and [Internet Assigned Numbers Authority (IANA) time zone]((http://www.iana.org/time-zones)) (also known as Olson time zone) format.</span></span> <span data-ttu-id="3e103-107">El formato Windows es el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3e103-107">The Windows format is the default.</span></span> 

<span data-ttu-id="3e103-108">Cuando se obtiene la zona horaria preferida de un usuario, esta se devuelve en el formato en el que se configuró.</span><span class="sxs-lookup"><span data-stu-id="3e103-108">When you get a user's preferred time zone, the time zone is returned in the format that it was set up.</span></span> <span data-ttu-id="3e103-109">Si quiere que esa zona horaria se muestre en un formato específico (Windows o IANA), puede [actualizar primero la zona horaria preferida en ese formato como opción de configuración del buzón](user_update_mailboxsettings.md).</span><span class="sxs-lookup"><span data-stu-id="3e103-109">If you want that time zone to be in a specific format (Windows or IANA), you can first [update the preferred time zone in that format as a mailbox setting](user_update_mailboxsettings.md).</span></span> <span data-ttu-id="3e103-110">Posteriormente, podrá obtener la zona horaria en ese formato.</span><span class="sxs-lookup"><span data-stu-id="3e103-110">Subsequently you will be able to get the time zone in that format.</span></span> <span data-ttu-id="3e103-111">Como alternativa, puede administrar la conversión de formato por separado en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3e103-111">Alternatively, you can manage the format conversion separately in your app.</span></span>

## <a name="permissions"></a><span data-ttu-id="3e103-112">Permisos</span><span class="sxs-lookup"><span data-stu-id="3e103-112">Permissions</span></span>
<span data-ttu-id="3e103-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="3e103-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="3e103-115">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3e103-115">Permission type</span></span>      | <span data-ttu-id="3e103-116">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3e103-116">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3e103-117">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3e103-117">Delegated (work or school account)</span></span> | <span data-ttu-id="3e103-118">MailboxSettings.Read, MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e103-118">MailboxSettings.Read, MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="3e103-119">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3e103-119">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3e103-120">MailboxSettings.Read, MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e103-120">MailboxSettings.Read, MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="3e103-121">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3e103-121">Application</span></span> | <span data-ttu-id="3e103-122">MailboxSettings.Read, MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e103-122">MailboxSettings.Read, MailboxSettings.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="3e103-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3e103-123">HTTP request</span></span>
<span data-ttu-id="3e103-124">Para obtener toda la configuración del buzón, que incluye la configuración de las respuestas automáticas:</span><span class="sxs-lookup"><span data-stu-id="3e103-124">To get all mailbox settings which include automatic replies settings:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailboxSettings
GET /users/{id|userPrincipalName}/mailboxSettings
```

<span data-ttu-id="3e103-125">Para obtener una configuración específica (por ejemplo, solo la configuración de las respuestas automáticas, la configuración regional o la zona horaria):</span><span class="sxs-lookup"><span data-stu-id="3e103-125">To get specific settings - for example, only the automatic replies settings, locale, or time zone:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailboxSettings/automaticRepliesSetting
GET /users/{id|userPrincipalName}/mailboxSettings/automaticRepliesSetting

GET /me/mailboxSettings/language
GET /users/{id|userPrincipalName}/mailboxSettings/language

GET /me/mailboxSettings/timeZone
GET /users/{id|userPrincipalName}/mailboxSettings/timeZone
```
## <a name="optional-query-parameters"></a><span data-ttu-id="3e103-126">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="3e103-126">Optional query parameters</span></span>
<span data-ttu-id="3e103-127">Este método admite los [parámetros de consulta de OData]((http://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters)) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3e103-127">This method supports the [OData Query Parameters]((http://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters)) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="3e103-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3e103-128">Request headers</span></span>
| <span data-ttu-id="3e103-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="3e103-129">Name</span></span>       | <span data-ttu-id="3e103-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="3e103-130">Type</span></span> | <span data-ttu-id="3e103-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="3e103-131">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="3e103-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="3e103-132">Authorization</span></span>  | <span data-ttu-id="3e103-133">string</span><span class="sxs-lookup"><span data-stu-id="3e103-133">string</span></span>  | <span data-ttu-id="3e103-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3e103-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="3e103-136">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3e103-136">Request body</span></span>
<span data-ttu-id="3e103-137">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3e103-137">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3e103-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3e103-138">Response</span></span>

<span data-ttu-id="3e103-139">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y uno de los siguientes objetos solicitados en el cuerpo de la respuesta:</span><span class="sxs-lookup"><span data-stu-id="3e103-139">If successful, this method returns a `200 OK` response code and one of the following requested objects in the response body:</span></span>

- <span data-ttu-id="3e103-140">Objeto [mailboxSettings](../resources/mailboxsettings.md)</span><span class="sxs-lookup"><span data-stu-id="3e103-140">[mailboxSettings](../resources/mailboxsettings.md) object</span></span>
- <span data-ttu-id="3e103-141">Objeto [automaticRepliesSetting](../resources/automaticRepliesSetting.md)</span><span class="sxs-lookup"><span data-stu-id="3e103-141">[automaticRepliesSetting](../resources/automaticRepliesSetting.md) object</span></span>
- <span data-ttu-id="3e103-142">Objeto [localeInfo](../resources/localeinfo.md)</span><span class="sxs-lookup"><span data-stu-id="3e103-142">[localeInfo](../resources/localeinfo.md) object</span></span>
- <span data-ttu-id="3e103-143">string (para **timeZone**)</span><span class="sxs-lookup"><span data-stu-id="3e103-143">string (for **timeZone**)</span></span>

## <a name="example"></a><span data-ttu-id="3e103-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3e103-144">Example</span></span>
##### <a name="request-1"></a><span data-ttu-id="3e103-145">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="3e103-145">Request 1</span></span>
<span data-ttu-id="3e103-146">El primer ejemplo obtiene toda la configuración del buzón del usuario que ha iniciado sesión, que incluye la configuración de idioma, la zona horaria y la configuración de las respuestas automáticas.</span><span class="sxs-lookup"><span data-stu-id="3e103-146">The first example gets all the mailbox settings of the signed-in user's mailbox, which include automatic replies settings, time zone, and language settings.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_mailboxsettings_1"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/mailboxSettings
```
##### <a name="response-1"></a><span data-ttu-id="3e103-147">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="3e103-147">Response 1</span></span>
<span data-ttu-id="3e103-p106">La respuesta incluye toda la configuración del buzón. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3e103-p106">The response includes all the mailbox settings. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
    }
}
```

##### <a name="request-2"></a><span data-ttu-id="3e103-151">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="3e103-151">Request 2</span></span>
<span data-ttu-id="3e103-152">El segundo ejemplo obtiene específicamente la configuración de las respuestas automáticas del buzón del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="3e103-152">The second example gets specifically the automatic replies settings of the signed-in user's mailbox.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_mailboxsettings_2"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/mailboxSettings/automaticRepliesSetting
```
##### <a name="response-2"></a><span data-ttu-id="3e103-153">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="3e103-153">Response 2</span></span>
<span data-ttu-id="3e103-p107">La respuesta incluye solo la configuración de las respuestas automáticas. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3e103-p107">The response includes only the automatic replies settings. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.automaticRepliesSetting"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/api/v1.0/$metadata#Me/mailboxSettings/automaticRepliesSetting",
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

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get mailbox settings",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->