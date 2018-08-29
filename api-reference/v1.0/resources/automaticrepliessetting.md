# <a name="automaticrepliessetting-resource-type"></a><span data-ttu-id="2480b-101">Tipo de recurso automaticRepliesSetting</span><span class="sxs-lookup"><span data-stu-id="2480b-101">automaticRepliesSetting resource type</span></span>

<span data-ttu-id="2480b-p101">Opciones de configuración para notificar de forma automática al remitente de un mensaje de correo entrante con un mensaje del usuario que ha iniciado sesión. Por ejemplo, una respuesta automática para notificar que el usuario que ha iniciado sesión no está disponible para responder a correos electrónicos.</span><span class="sxs-lookup"><span data-stu-id="2480b-p101">Configuration settings to automatically notify the sender of an incoming email with a message from the signed-in user. For example, an automatic reply to notify that the signed-in user is unavailable to respond to emails.</span></span> 


## <a name="properties"></a><span data-ttu-id="2480b-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2480b-104">Properties</span></span>
| <span data-ttu-id="2480b-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2480b-105">Property</span></span>     | <span data-ttu-id="2480b-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="2480b-106">Type</span></span>   |<span data-ttu-id="2480b-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="2480b-107">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2480b-108">externalAudience</span><span class="sxs-lookup"><span data-stu-id="2480b-108">externalAudience</span></span>|<span data-ttu-id="2480b-109">externalAudienceScope</span><span class="sxs-lookup"><span data-stu-id="2480b-109">ExternalAudienceScope</span></span>| <span data-ttu-id="2480b-110">El conjunto de audiencia externa a la organización del usuario que ha iniciado sesión que recibirá el **ExternalReplyMessage**, si **Status** es `AlwaysEnabled` o `Scheduled`.</span><span class="sxs-lookup"><span data-stu-id="2480b-110">The set of audience external to the signed-in user's organization who will receive the **ExternalReplyMessage**, if **Status** is `AlwaysEnabled` or . Possible values are: , , `Scheduled`.</span></span> <span data-ttu-id="2480b-111">Los valores posibles son: `none`, `contactsOnly` y `all`.</span><span class="sxs-lookup"><span data-stu-id="2480b-111">The possible values are `none`, `contactsOnly`, `all`, , , , , , , , , or .</span></span>|
|<span data-ttu-id="2480b-112">externalReplyMessage</span><span class="sxs-lookup"><span data-stu-id="2480b-112">externalReplyMessage</span></span>|<span data-ttu-id="2480b-113">cadena</span><span class="sxs-lookup"><span data-stu-id="2480b-113">string</span></span>|<span data-ttu-id="2480b-114">La respuesta automática para enviar a la audiencia externa especificada, si **Status** es `AlwaysEnabled` o `Scheduled`.</span><span class="sxs-lookup"><span data-stu-id="2480b-114">The automatic reply to send to the specified external audience, if **Status** is `AlwaysEnabled` or `Scheduled`.</span></span>|
|<span data-ttu-id="2480b-115">internalReplyMessage</span><span class="sxs-lookup"><span data-stu-id="2480b-115">internalReplyMessage</span></span>|<span data-ttu-id="2480b-116">cadena</span><span class="sxs-lookup"><span data-stu-id="2480b-116">string</span></span>|<span data-ttu-id="2480b-117">La respuesta automática para enviar a la audiencia interna de la organización del usuario que ha iniciado sesión, si **Status** es `AlwaysEnabled` o `Scheduled`.</span><span class="sxs-lookup"><span data-stu-id="2480b-117">The automatic reply to send to the audience internal to the signed-in user's organization, if **Status** is `AlwaysEnabled` or `Scheduled`.</span></span> |
|<span data-ttu-id="2480b-118">scheduledEndDateTime</span><span class="sxs-lookup"><span data-stu-id="2480b-118">scheduledEndDateTime</span></span>|[<span data-ttu-id="2480b-119">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="2480b-119">dateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="2480b-120">La fecha y hora en que se establece la finalización de las respuestas automáticas, si **Status** se establece en `Scheduled`.</span><span class="sxs-lookup"><span data-stu-id="2480b-120">The date and time that automatic replies are set to end, if **Status** is set to `Scheduled`.</span></span> |
|<span data-ttu-id="2480b-121">scheduledStartDateTime</span><span class="sxs-lookup"><span data-stu-id="2480b-121">scheduledStartDateTime</span></span>|[<span data-ttu-id="2480b-122">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="2480b-122">dateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="2480b-123">La fecha y hora en que se establece el inicio de las respuestas automáticas, si **Status** se establece en `Scheduled`.</span><span class="sxs-lookup"><span data-stu-id="2480b-123">The date and time that automatic replies are set to begin, if **Status** is set to `Scheduled`.</span></span>|
|<span data-ttu-id="2480b-124">status</span><span class="sxs-lookup"><span data-stu-id="2480b-124">status</span></span>|<span data-ttu-id="2480b-125">automaticRepliesStatus</span><span class="sxs-lookup"><span data-stu-id="2480b-125">AutomaticRepliesStatus</span></span>|<span data-ttu-id="2480b-126">Estado de las configuraciones de las respuestas automáticas.</span><span class="sxs-lookup"><span data-stu-id="2480b-126">Configurations status for automatic replies. Possible values are: , , .</span></span> <span data-ttu-id="2480b-127">Los valores posibles son: `disabled`, `alwaysEnabled` y `scheduled`.</span><span class="sxs-lookup"><span data-stu-id="2480b-127">The possible values are `disabled`, `alwaysEnabled`, `scheduled`, , , , , , , , , or .</span></span>|

## <a name="json-representation"></a><span data-ttu-id="2480b-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2480b-128">JSON representation</span></span>

<span data-ttu-id="2480b-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2480b-129">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.automaticRepliesSetting"
}-->

```json
{
  "externalAudience": "String",
  "externalReplyMessage": "string",
  "internalReplyMessage": "string",
  "scheduledEndDateTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "scheduledStartDateTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "status": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "automaticRepliesSetting resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
