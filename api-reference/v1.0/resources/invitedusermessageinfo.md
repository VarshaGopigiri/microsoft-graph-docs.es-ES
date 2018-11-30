---
title: Configurar el mensaje de invitación
description: El objeto invitedUserMessageInfo le permite configurar el mensaje de invitación.
ms.openlocfilehash: c8258d2b90d1aa5f5081b271ccc70fcb7408b132
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031804"
---
# <a name="configuring-the-invitation-message"></a><span data-ttu-id="948fd-103">Configurar el mensaje de invitación</span><span class="sxs-lookup"><span data-stu-id="948fd-103">Configuring the invitation message</span></span>

<span data-ttu-id="948fd-104">El objeto invitedUserMessageInfo le permite configurar el mensaje de [invitación](invitation.md).</span><span class="sxs-lookup"><span data-stu-id="948fd-104">The invitedUserMessageInfo object allows you to configure the [invitation](invitation.md) message.</span></span>


## <a name="properties"></a><span data-ttu-id="948fd-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="948fd-105">Properties</span></span>
| <span data-ttu-id="948fd-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="948fd-106">Property</span></span>     | <span data-ttu-id="948fd-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="948fd-107">Type</span></span>   |<span data-ttu-id="948fd-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="948fd-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="948fd-109">ccRecipients</span><span class="sxs-lookup"><span data-stu-id="948fd-109">ccRecipients</span></span>|<span data-ttu-id="948fd-110">Colección [Recipient](recipient.md)</span><span class="sxs-lookup"><span data-stu-id="948fd-110">[Recipient](recipient.md) collection</span></span>|<span data-ttu-id="948fd-p101">Destinatarios adicionales a los que se debe enviar el mensaje de invitación. Actualmente se admite solo 1 destinatario adicional.</span><span class="sxs-lookup"><span data-stu-id="948fd-p101">Additional recipients the invitation message should be sent to. Currently only 1 additional recipient is supported.</span></span>|
|<span data-ttu-id="948fd-113">customizedMessageBody</span><span class="sxs-lookup"><span data-stu-id="948fd-113">customizedMessageBody</span></span>|<span data-ttu-id="948fd-114">String</span><span class="sxs-lookup"><span data-stu-id="948fd-114">String</span></span>|<span data-ttu-id="948fd-115">Cuerpo del mensaje personalizado que quiere enviar si no quiere el mensaje predeterminado.</span><span class="sxs-lookup"><span data-stu-id="948fd-115">Customized message body you want to send if you don't want the default message.</span></span>|
|<span data-ttu-id="948fd-116">messageLanguage</span><span class="sxs-lookup"><span data-stu-id="948fd-116">messageLanguage</span></span>|<span data-ttu-id="948fd-117">String</span><span class="sxs-lookup"><span data-stu-id="948fd-117">String</span></span>|<span data-ttu-id="948fd-p102">El idioma en el que quiere enviar el mensaje predeterminado. Si se especifica el customizedMessageBody, esta propiedad se omite y el mensaje se envía con el customizedMessageBody. El formato de idioma debe estar en ISO 639. El valor predeterminado es en-US.</span><span class="sxs-lookup"><span data-stu-id="948fd-p102">The language you want to send the default message in. If the customizedMessageBody is specified, this property is ignored, and the message is sent using the customizedMessageBody. The language format should be in ISO 639. The default is en-US.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="948fd-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="948fd-122">JSON representation</span></span>
<span data-ttu-id="948fd-123">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="948fd-123">Here is a JSON representation of the resource</span></span>

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
