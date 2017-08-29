# <a name="update-user-mailbox-settings"></a><span data-ttu-id="21439-101">Actualizar la configuración del buzón del usuario</span><span class="sxs-lookup"><span data-stu-id="21439-101">Update user mailbox settings</span></span>

<span data-ttu-id="21439-p101">Actualice uno o varios valores de configuración del buzón del usuario. Esto incluye la configuración de las respuestas automáticas (avisar a los usuarios de forma automática tras la recepción de su correo electrónico), configuración regional y zona horaria.</span><span class="sxs-lookup"><span data-stu-id="21439-p101">Update one or more settings for the user's mailbox. This includes settings for automatic replies (notify people automatically upon receipt of their email), locale, or time zone.</span></span>

<span data-ttu-id="21439-104">Puede habilitar, configurar o deshabilitar uno o varios de estos valores como parte de [mailboxSettings](../resources/mailboxsettings.md).</span><span class="sxs-lookup"><span data-stu-id="21439-104">You can enable, configure, or disable one or more of these settings as part of [mailboxSettings](../resources/mailboxsettings.md).</span></span>

<span data-ttu-id="21439-105">**Nota** No puede crear ni eliminar ninguna configuración del buzón.</span><span class="sxs-lookup"><span data-stu-id="21439-105">**Note** You cannot create or delete any mailbox settings.</span></span>

## <a name="permissions"></a><span data-ttu-id="21439-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="21439-106">Permissions</span></span>
<span data-ttu-id="21439-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="21439-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="21439-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="21439-109">Permission type</span></span>      | <span data-ttu-id="21439-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="21439-110">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="21439-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="21439-111">Delegated (work or school account)</span></span> | <span data-ttu-id="21439-112">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="21439-112">MailboxSettings.ReadWrite</span></span>    | 
|<span data-ttu-id="21439-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="21439-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="21439-114">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="21439-114">MailboxSettings.ReadWrite</span></span>    | 
|<span data-ttu-id="21439-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="21439-115">Application</span></span> | <span data-ttu-id="21439-116">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="21439-116">MailboxSettings.ReadWrite</span></span> | 

## <a name="http-request"></a><span data-ttu-id="21439-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="21439-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/mailboxSettings
PATCH /users/{id|userPrincipalName}/mailboxSettings
```
## <a name="optional-query-parameters"></a><span data-ttu-id="21439-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="21439-118">Optional query parameters</span></span>
<span data-ttu-id="21439-119">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="21439-119">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="21439-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="21439-120">Request headers</span></span>
| <span data-ttu-id="21439-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="21439-121">Name</span></span>       | <span data-ttu-id="21439-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="21439-122">Type</span></span> | <span data-ttu-id="21439-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="21439-123">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="21439-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="21439-124">Authorization</span></span>  | <span data-ttu-id="21439-125">string</span><span class="sxs-lookup"><span data-stu-id="21439-125">string</span></span>  | <span data-ttu-id="21439-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="21439-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="21439-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="21439-128">Request body</span></span>
<span data-ttu-id="21439-p104">En el cuerpo de la solicitud, proporcione los valores de las propiedades relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado. Las siguientes propiedades son modificables o actualizables:</span><span class="sxs-lookup"><span data-stu-id="21439-p104">In the request body, supply the values for the relevant properties that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed. The following are the writable/updatable properties:</span></span>

| <span data-ttu-id="21439-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="21439-133">Property</span></span>     | <span data-ttu-id="21439-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="21439-134">Type</span></span>   |<span data-ttu-id="21439-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="21439-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="21439-136">automaticRepliesSetting</span><span class="sxs-lookup"><span data-stu-id="21439-136">automaticRepliesSetting</span></span>|[<span data-ttu-id="21439-137">automaticRepliesSetting</span><span class="sxs-lookup"><span data-stu-id="21439-137">automaticRepliesSetting</span></span>](../resources/automaticrepliessetting.md)|<span data-ttu-id="21439-138">Opciones de configuración para notificar de forma automática al remitente de un mensaje de correo entrante con un mensaje del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="21439-138">Configuration settings to automatically notify the sender of an incoming email with a message from the signed-in user.</span></span>|
|<span data-ttu-id="21439-139">language</span><span class="sxs-lookup"><span data-stu-id="21439-139">language</span></span>|[<span data-ttu-id="21439-140">localeInfo</span><span class="sxs-lookup"><span data-stu-id="21439-140">localeInfo</span></span>](../resources/localeinfo.md)|<span data-ttu-id="21439-141">Representación de la configuración regional del usuario, como el idioma preferido y el país o región.</span><span class="sxs-lookup"><span data-stu-id="21439-141">The locale information for the user, including the preferred language and country/region.</span></span>|
|<span data-ttu-id="21439-142">timeZone</span><span class="sxs-lookup"><span data-stu-id="21439-142">timeZone</span></span>|<span data-ttu-id="21439-143">string</span><span class="sxs-lookup"><span data-stu-id="21439-143">string</span></span>|<span data-ttu-id="21439-144">La zona horaria predeterminada del buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="21439-144">The default time zone for the user's mailbox.</span></span>|

## <a name="response"></a><span data-ttu-id="21439-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="21439-145">Response</span></span>

<span data-ttu-id="21439-146">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [mailboxSettings](../resources/mailboxSettings.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="21439-146">If successful, this method returns a `200 OK` response code and [mailboxSettings](../resources/mailboxSettings.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="21439-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="21439-147">Example</span></span>
##### <a name="request"></a><span data-ttu-id="21439-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="21439-148">Request</span></span>
<span data-ttu-id="21439-149">En el ejemplo siguiente, se habilitan las respuestas automáticas para un intervalo de fechas; para ello, se establecen las siguientes propiedades de la propiedad **automaticRepliesSetting**: **status**, **scheduledStartDateTime** y **scheduledEndDateTime**.</span><span class="sxs-lookup"><span data-stu-id="21439-149">The following example enables automatic replies for a date range, by setting the following properties of the **automaticRepliesSetting** property: **status**, **scheduledStartDateTime** and **scheduledEndDateTime**.</span></span>

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
##### <a name="response"></a><span data-ttu-id="21439-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="21439-150">Response</span></span>
<span data-ttu-id="21439-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="21439-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
        "externalAudience": "none",
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
    },
    "timeZone":"UTC",
    "language":{
      "locale":"en-US",
      "displayName":"English (United States)"
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