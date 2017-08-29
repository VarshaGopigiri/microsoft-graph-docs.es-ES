# <a name="configuring-the-invitation-message"></a><span data-ttu-id="70a18-101">Configurar el mensaje de invitación</span><span class="sxs-lookup"><span data-stu-id="70a18-101">Configuring the invitation message</span></span>

<span data-ttu-id="70a18-102">El objeto invitedUserMessageInfo le permite configurar el mensaje de [invitación](invitation.md).</span><span class="sxs-lookup"><span data-stu-id="70a18-102">The invitedUserMessageInfo object allows you to configure the [invitation](invitation.md) message.</span></span>


## <a name="properties"></a><span data-ttu-id="70a18-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="70a18-103">Properties</span></span>
| <span data-ttu-id="70a18-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="70a18-104">Property</span></span>     | <span data-ttu-id="70a18-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="70a18-105">Type</span></span>   |<span data-ttu-id="70a18-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="70a18-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="70a18-107">ccRecipients</span><span class="sxs-lookup"><span data-stu-id="70a18-107">ccRecipients</span></span>|[<span data-ttu-id="70a18-108">Recipient</span><span class="sxs-lookup"><span data-stu-id="70a18-108">Recipient</span></span>](recipient.md)|<span data-ttu-id="70a18-p101">Destinatarios adicionales a los que se debe enviar el mensaje de invitación. Actualmente se admite solo 1 destinatario adicional.</span><span class="sxs-lookup"><span data-stu-id="70a18-p101">Additional recipients the invitation message should be sent to. Currently only 1 additional recipient is supported.</span></span>|
|<span data-ttu-id="70a18-111">customizedMessageBody</span><span class="sxs-lookup"><span data-stu-id="70a18-111">customizedMessageBody</span></span>|<span data-ttu-id="70a18-112">String</span><span class="sxs-lookup"><span data-stu-id="70a18-112">String</span></span>|<span data-ttu-id="70a18-113">Cuerpo del mensaje personalizado que quiere enviar si no quiere el mensaje predeterminado.</span><span class="sxs-lookup"><span data-stu-id="70a18-113">Customized message body you want to send if you don't want the default message.</span></span>|
|<span data-ttu-id="70a18-114">messageLanguage</span><span class="sxs-lookup"><span data-stu-id="70a18-114">messageLanguage</span></span>|<span data-ttu-id="70a18-115">String</span><span class="sxs-lookup"><span data-stu-id="70a18-115">String</span></span>|<span data-ttu-id="70a18-p102">El idioma en el que quiere enviar el mensaje predeterminado. Si se especifica el customizedMessageBody, esta propiedad se omite y el mensaje se envía con el customizedMessageBody. El formato de idioma debe estar en ISO 639. El valor predeterminado es en-US.</span><span class="sxs-lookup"><span data-stu-id="70a18-p102">The language you want to send the default message in. If the customizedMessageBody is specified, this property is ignored, and the message is sent using the customizedMessageBody. The language format should be in ISO 639. The default is en-US.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="70a18-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="70a18-120">JSON representation</span></span>
<span data-ttu-id="70a18-121">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="70a18-121">Here is a JSON representation of the resource</span></span>

<!-- {"blockType": "resource", "@odata.type": "microsoft.graph.invitedUserMessageInfo"} -->
```json
{
  "ccRecipients": [ {"@odata.type": "microsoft.graph.recipient"} ],
  "customizedMessageBody": "string",
  "messageLanguage": "string"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2016-22-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "invitedUserMessageInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
