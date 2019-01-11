---
title: Configurar el mensaje de invitación
description: El objeto invitedUserMessageInfo le permite configurar el mensaje de invitación.
localization_priority: Normal
ms.openlocfilehash: f8a6dd118f1774320e3fe8327d284dac1141fc55
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27874126"
---
# <a name="configuring-the-invitation-message"></a><span data-ttu-id="d2e37-103">Configurar el mensaje de invitación</span><span class="sxs-lookup"><span data-stu-id="d2e37-103">Configuring the invitation message</span></span>

> <span data-ttu-id="d2e37-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d2e37-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d2e37-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d2e37-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d2e37-106">El objeto invitedUserMessageInfo le permite configurar el mensaje de [invitación](invitation.md).</span><span class="sxs-lookup"><span data-stu-id="d2e37-106">The invitedUserMessageInfo object allows you to configure the [invitation](invitation.md) message.</span></span>


## <a name="properties"></a><span data-ttu-id="d2e37-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d2e37-107">Properties</span></span>
| <span data-ttu-id="d2e37-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d2e37-108">Property</span></span>     | <span data-ttu-id="d2e37-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="d2e37-109">Type</span></span>   |<span data-ttu-id="d2e37-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2e37-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d2e37-111">ccRecipients</span><span class="sxs-lookup"><span data-stu-id="d2e37-111">ccRecipients</span></span>|[<span data-ttu-id="d2e37-112">Destinatarios</span><span class="sxs-lookup"><span data-stu-id="d2e37-112">Recipients</span></span>](recipient.md)|<span data-ttu-id="d2e37-p102">Destinatarios adicionales a los que se debe enviar el mensaje de invitación. Actualmente se admite solo 1 destinatario adicional.</span><span class="sxs-lookup"><span data-stu-id="d2e37-p102">Additional recipients the invitation message should be sent to. Currently only 1 additional recipient is supported.</span></span>|
|<span data-ttu-id="d2e37-115">customizedMessageBody</span><span class="sxs-lookup"><span data-stu-id="d2e37-115">customizedMessageBody</span></span>|<span data-ttu-id="d2e37-116">String</span><span class="sxs-lookup"><span data-stu-id="d2e37-116">String</span></span>|<span data-ttu-id="d2e37-117">Cuerpo del mensaje personalizado que quiere enviar si no quiere el mensaje predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d2e37-117">Customized message body you want to send if you don't want the default message.</span></span>|
|<span data-ttu-id="d2e37-118">messageLanguage</span><span class="sxs-lookup"><span data-stu-id="d2e37-118">messageLanguage</span></span>|<span data-ttu-id="d2e37-119">String</span><span class="sxs-lookup"><span data-stu-id="d2e37-119">String</span></span>|<span data-ttu-id="d2e37-p103">El idioma en el que quiere enviar el mensaje predeterminado. Si se especifica el customizedMessageBody, esta propiedad se omite y el mensaje se envía con el customizedMessageBody. El formato de idioma debe estar en ISO 639. El valor predeterminado es en-US.</span><span class="sxs-lookup"><span data-stu-id="d2e37-p103">The language you want to send the default message in. If the customizedMessageBody is specified, this property is ignored, and the message is sent using the customizedMessageBody. The language format should be in ISO 639. The default is en-US.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d2e37-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d2e37-124">JSON representation</span></span>
<span data-ttu-id="d2e37-125">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d2e37-125">Here is a JSON representation of the resource</span></span>

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
