# <a name="get-user-mailbox-settings"></a><span data-ttu-id="b5ead-101">Obtener configuración del buzón del usuario</span><span class="sxs-lookup"><span data-stu-id="b5ead-101">Get user mailbox settings</span></span>

<span data-ttu-id="b5ead-p101">Obtener el objeto [mailboxSettings](../resources/mailboxsettings.md) del usuario. Esto incluye la configuración de las respuestas automáticas (avisar a los usuarios de forma automática tras la recepción de su correo electrónico), configuración regional (idioma y país o región) y zona horaria.</span><span class="sxs-lookup"><span data-stu-id="b5ead-p101">Get the user's [mailboxSettings](../resources/mailboxsettings.md). This includes settings for automatic replies (notify people automatically upon receipt of their email), locale (language and country/region), and time zone.</span></span>

<span data-ttu-id="b5ead-104">Puede ver toda la configuración del buzón u obtener una configuración específica.</span><span class="sxs-lookup"><span data-stu-id="b5ead-104">You can view all mailbox settings, or, get specific settings.</span></span>

## <a name="permissions"></a><span data-ttu-id="b5ead-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="b5ead-105">Permissions</span></span>
<span data-ttu-id="b5ead-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="b5ead-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b5ead-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b5ead-108">Permission type</span></span>      | <span data-ttu-id="b5ead-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b5ead-109">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="b5ead-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b5ead-110">Delegated (work or school account)</span></span> | <span data-ttu-id="b5ead-111">MailboxSettings.Read, MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b5ead-111">MailboxSettings.Read, MailboxSettings.ReadWrite</span></span>    | 
|<span data-ttu-id="b5ead-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b5ead-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b5ead-113">MailboxSettings.Read, MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b5ead-113">MailboxSettings.Read, MailboxSettings.ReadWrite</span></span>    | 
|<span data-ttu-id="b5ead-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b5ead-114">Application</span></span> | <span data-ttu-id="b5ead-115">MailboxSettings.Read, MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b5ead-115">MailboxSettings.Read, MailboxSettings.ReadWrite</span></span> | 

## <a name="http-request"></a><span data-ttu-id="b5ead-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b5ead-116">HTTP request</span></span>
<span data-ttu-id="b5ead-117">Para obtener toda la configuración del buzón, que incluye la configuración de las respuestas automáticas:</span><span class="sxs-lookup"><span data-stu-id="b5ead-117">To get all mailbox settings which include automatic replies settings:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailboxSettings
GET /users/{id|userPrincipalName}/mailboxSettings
```

<span data-ttu-id="b5ead-118">Para obtener una configuración específica (por ejemplo, solo la configuración de las respuestas automáticas, la configuración regional o la zona horaria):</span><span class="sxs-lookup"><span data-stu-id="b5ead-118">To get specific settings - for example, only the automatic replies settings, locale, or time zone:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailboxSettings/automaticRepliesSetting
GET /users/{id|userPrincipalName}/mailboxSettings/automaticRepliesSetting

GET /me/mailboxSettings/language
GET /users/{id|userPrincipalName}/mailboxSettings/language

GET /me/mailboxSettings/timeZone
GET /users/{id|userPrincipalName}/mailboxSettings/timeZone
```
## <a name="optional-query-parameters"></a><span data-ttu-id="b5ead-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b5ead-119">Optional query parameters</span></span>
<span data-ttu-id="b5ead-120">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b5ead-120">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="b5ead-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b5ead-121">Request headers</span></span>
| <span data-ttu-id="b5ead-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="b5ead-122">Name</span></span>       | <span data-ttu-id="b5ead-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="b5ead-123">Type</span></span> | <span data-ttu-id="b5ead-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5ead-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="b5ead-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="b5ead-125">Authorization</span></span>  | <span data-ttu-id="b5ead-126">string</span><span class="sxs-lookup"><span data-stu-id="b5ead-126">string</span></span>  | <span data-ttu-id="b5ead-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b5ead-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b5ead-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b5ead-129">Request body</span></span>
<span data-ttu-id="b5ead-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b5ead-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b5ead-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b5ead-131">Response</span></span>

<span data-ttu-id="b5ead-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y uno de los siguientes objetos solicitados en el cuerpo de la respuesta:</span><span class="sxs-lookup"><span data-stu-id="b5ead-132">If successful, this method returns a `200 OK` response code and one of the following requested objects in the response body:</span></span>

- <span data-ttu-id="b5ead-133">Objeto [mailboxSettings](../resources/mailboxsettings.md)</span><span class="sxs-lookup"><span data-stu-id="b5ead-133">[mailboxSettings](../resources/mailboxsettings.md) object</span></span>
- <span data-ttu-id="b5ead-134">Objeto [automaticRepliesSetting](../resources/automaticRepliesSetting.md)</span><span class="sxs-lookup"><span data-stu-id="b5ead-134">[automaticRepliesSetting](../resources/automaticRepliesSetting.md) object</span></span>
- <span data-ttu-id="b5ead-135">Objeto [localeInfo](../resources/localeinfo.md)</span><span class="sxs-lookup"><span data-stu-id="b5ead-135">[localeInfo](../resources/localeinfo.md) object</span></span>
- <span data-ttu-id="b5ead-136">string (para **timeZone**)</span><span class="sxs-lookup"><span data-stu-id="b5ead-136">string (for **timeZone**)</span></span>

## <a name="example"></a><span data-ttu-id="b5ead-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b5ead-137">Example</span></span>
##### <a name="request-1"></a><span data-ttu-id="b5ead-138">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="b5ead-138">Request 1</span></span>
<span data-ttu-id="b5ead-139">El primer ejemplo obtiene toda la configuración del buzón del usuario que ha iniciado sesión, que incluye la configuración de idioma, la zona horaria y la configuración de las respuestas automáticas.</span><span class="sxs-lookup"><span data-stu-id="b5ead-139">The first example gets all the mailbox settings of the signed-in user's mailbox, which include automatic replies settings, time zone, and language settings.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_mailboxsettings_1"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/mailboxSettings
```
##### <a name="response-1"></a><span data-ttu-id="b5ead-140">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="b5ead-140">Response 1</span></span>
<span data-ttu-id="b5ead-p104">La respuesta incluye toda la configuración del buzón. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b5ead-p104">The response includes all the mailbox settings. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

##### <a name="request-2"></a><span data-ttu-id="b5ead-144">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="b5ead-144">Request 2</span></span>
<span data-ttu-id="b5ead-145">El segundo ejemplo obtiene específicamente la configuración de las respuestas automáticas del buzón del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="b5ead-145">The second example gets specifically the automatic replies settings of the signed-in user's mailbox.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_mailboxsettings_2"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/mailboxSettings/automaticRepliesSetting
```
##### <a name="response-2"></a><span data-ttu-id="b5ead-146">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="b5ead-146">Response 2</span></span>
<span data-ttu-id="b5ead-p105">La respuesta incluye solo la configuración de las respuestas automáticas. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b5ead-p105">The response includes only the automatic replies settings. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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