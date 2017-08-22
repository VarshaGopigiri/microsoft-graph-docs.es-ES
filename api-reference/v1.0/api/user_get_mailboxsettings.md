# <a name="get-user-mailbox-settings"></a><span data-ttu-id="ef33d-101">Obtener configuración del buzón del usuario</span><span class="sxs-lookup"><span data-stu-id="ef33d-101">Get user mailbox settings</span></span>

<span data-ttu-id="ef33d-p101">Obtener el objeto [mailboxSettings](../resources/mailboxsettings.md) del usuario. Esto incluye la configuración de las respuestas automáticas (avisar a los usuarios de forma automática tras la recepción de su correo electrónico), configuración regional (idioma y país o región) y zona horaria.</span><span class="sxs-lookup"><span data-stu-id="ef33d-p101">Get the user's [mailboxSettings](../resources/mailboxsettings.md). This includes settings for automatic replies (notify people automatically upon receipt of their email), locale (language and country/region), and time zone.</span></span>

<span data-ttu-id="ef33d-104">Puede ver toda la configuración del buzón u obtener una configuración específica.</span><span class="sxs-lookup"><span data-stu-id="ef33d-104">You can view all mailbox settings, or, get specific settings.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ef33d-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ef33d-105">Prerequisites</span></span>
<span data-ttu-id="ef33d-106">Se requiere el siguiente **ámbito** para ejecutar esta API: *MailboxSettings.Read*</span><span class="sxs-lookup"><span data-stu-id="ef33d-106">The following **scope** is required to execute this API: *MailboxSettings.Read*</span></span>  

## <a name="http-request"></a><span data-ttu-id="ef33d-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ef33d-107">HTTP request</span></span>
<span data-ttu-id="ef33d-108">Para obtener toda la configuración del buzón, que incluye la configuración de las respuestas automáticas:</span><span class="sxs-lookup"><span data-stu-id="ef33d-108">To get all mailbox settings which include automatic replies settings:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailboxSettings
GET /users/{id|userPrincipalName}/mailboxSettings
```

<span data-ttu-id="ef33d-109">Para obtener una configuración específica (por ejemplo, solo la configuración de las respuestas automáticas, la configuración regional o la zona horaria):</span><span class="sxs-lookup"><span data-stu-id="ef33d-109">To get specific settings - for example, only the automatic replies settings, locale, or time zone:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailboxSettings/automaticRepliesSetting
GET /users/{id|userPrincipalName}/mailboxSettings/automaticRepliesSetting

GET /me/mailboxSettings/language
GET /users/{id|userPrincipalName}/mailboxSettings/language

GET /me/mailboxSettings/timeZone
GET /users/{id|userPrincipalName}/mailboxSettings/timeZone
```
## <a name="optional-query-parameters"></a><span data-ttu-id="ef33d-110">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ef33d-110">Optional query parameters</span></span>
<span data-ttu-id="ef33d-111">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ef33d-111">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="ef33d-112">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ef33d-112">Request headers</span></span>
| <span data-ttu-id="ef33d-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="ef33d-113">Name</span></span>       | <span data-ttu-id="ef33d-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="ef33d-114">Type</span></span> | <span data-ttu-id="ef33d-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef33d-115">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="ef33d-116">Authorization</span><span class="sxs-lookup"><span data-stu-id="ef33d-116">Authorization</span></span>  | <span data-ttu-id="ef33d-117">string</span><span class="sxs-lookup"><span data-stu-id="ef33d-117">string</span></span>  | <span data-ttu-id="ef33d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ef33d-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ef33d-120">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ef33d-120">Request body</span></span>
<span data-ttu-id="ef33d-121">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ef33d-121">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ef33d-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ef33d-122">Response</span></span>

<span data-ttu-id="ef33d-123">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y uno de los siguientes objetos solicitados en el cuerpo de la respuesta:</span><span class="sxs-lookup"><span data-stu-id="ef33d-123">If successful, this method returns a `200 OK` response code and one of the following requested objects in the response body:</span></span>

- <span data-ttu-id="ef33d-124">Objeto [mailboxSettings](../resources/mailboxsettings.md)</span><span class="sxs-lookup"><span data-stu-id="ef33d-124">[mailboxSettings](../resources/mailboxsettings.md) object</span></span>
- <span data-ttu-id="ef33d-125">Objeto [automaticRepliesSetting](../resources/automaticRepliesSetting.md)</span><span class="sxs-lookup"><span data-stu-id="ef33d-125">[automaticRepliesSetting](../resources/automaticRepliesSetting.md) object</span></span>
- <span data-ttu-id="ef33d-126">Objeto [localeInfo](../resources/localeinfo.md)</span><span class="sxs-lookup"><span data-stu-id="ef33d-126">[localeInfo](../resources/localeinfo.md) object</span></span>
- <span data-ttu-id="ef33d-127">string (para **timeZone**)</span><span class="sxs-lookup"><span data-stu-id="ef33d-127">string (for **timeZone**)</span></span>

## <a name="example"></a><span data-ttu-id="ef33d-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ef33d-128">Example</span></span>
##### <a name="request-1"></a><span data-ttu-id="ef33d-129">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="ef33d-129">Request 1</span></span>
<span data-ttu-id="ef33d-130">El primer ejemplo obtiene toda la configuración del buzón del usuario que ha iniciado sesión, que incluye la configuración de idioma, la zona horaria y la configuración de las respuestas automáticas.</span><span class="sxs-lookup"><span data-stu-id="ef33d-130">The first example gets all the mailbox settings of the signed-in user's mailbox, which include automatic replies settings, time zone, and language settings.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_mailboxsettings_1"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/mailboxSettings
```
##### <a name="response-1"></a><span data-ttu-id="ef33d-131">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="ef33d-131">Response 1</span></span>
<span data-ttu-id="ef33d-p103">La respuesta incluye toda la configuración del buzón. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ef33d-p103">The response includes all the mailbox settings. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

##### <a name="request-2"></a><span data-ttu-id="ef33d-135">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="ef33d-135">Request 2</span></span>
<span data-ttu-id="ef33d-136">El segundo ejemplo obtiene específicamente la configuración de las respuestas automáticas del buzón del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="ef33d-136">The second example gets specifically the automatic replies settings of the signed-in user's mailbox.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_mailboxsettings_2"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/mailboxSettings/automaticRepliesSetting
```
##### <a name="response-2"></a><span data-ttu-id="ef33d-137">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="ef33d-137">Response 2</span></span>
<span data-ttu-id="ef33d-p104">La respuesta incluye solo la configuración de las respuestas automáticas. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ef33d-p104">The response includes only the automatic replies settings. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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