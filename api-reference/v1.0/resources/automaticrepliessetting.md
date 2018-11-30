---
title: Tipo de recurso automaticRepliesSetting
description: 'Opciones de configuración para notificar automáticamente al remitente de un correo electrónico entrante con un mensaje desde la '
ms.openlocfilehash: 983f5062c5a7bacaccfdca4687705aed5aa7a604
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028605"
---
# <a name="automaticrepliessetting-resource-type"></a><span data-ttu-id="226ed-103">Tipo de recurso automaticRepliesSetting</span><span class="sxs-lookup"><span data-stu-id="226ed-103">automaticRepliesSetting resource type</span></span>

<span data-ttu-id="226ed-p101">Opciones de configuración para notificar de forma automática al remitente de un mensaje de correo entrante con un mensaje del usuario que ha iniciado sesión. Por ejemplo, una respuesta automática para notificar que el usuario que ha iniciado sesión no está disponible para responder a correos electrónicos.</span><span class="sxs-lookup"><span data-stu-id="226ed-p101">Configuration settings to automatically notify the sender of an incoming email with a message from the signed-in user. For example, an automatic reply to notify that the signed-in user is unavailable to respond to emails.</span></span> 


## <a name="properties"></a><span data-ttu-id="226ed-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="226ed-106">Properties</span></span>
| <span data-ttu-id="226ed-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="226ed-107">Property</span></span>     | <span data-ttu-id="226ed-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="226ed-108">Type</span></span>   |<span data-ttu-id="226ed-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="226ed-109">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="226ed-110">externalAudience</span><span class="sxs-lookup"><span data-stu-id="226ed-110">externalAudience</span></span>|<span data-ttu-id="226ed-111">externalAudienceScope</span><span class="sxs-lookup"><span data-stu-id="226ed-111">externalAudienceScope</span></span>| <span data-ttu-id="226ed-112">El conjunto de audiencia externo a la organización del usuario que ha iniciado sesión que va a recibir el **ExternalReplyMessage**, si el **estado** es `AlwaysEnabled` o `Scheduled`.</span><span class="sxs-lookup"><span data-stu-id="226ed-112">The set of audience external to the signed-in user's organization who will receive the **ExternalReplyMessage**, if **Status** is `AlwaysEnabled` or `Scheduled`.</span></span> <span data-ttu-id="226ed-113">Los valores posibles son: `none`, `contactsOnly`, `all`.</span><span class="sxs-lookup"><span data-stu-id="226ed-113">The possible values are: `none`, `contactsOnly`, `all`.</span></span>|
|<span data-ttu-id="226ed-114">externalReplyMessage</span><span class="sxs-lookup"><span data-stu-id="226ed-114">externalReplyMessage</span></span>|<span data-ttu-id="226ed-115">string</span><span class="sxs-lookup"><span data-stu-id="226ed-115">string</span></span>|<span data-ttu-id="226ed-116">La respuesta automática para enviar a la audiencia externa especificada, si **Status** es `AlwaysEnabled` o `Scheduled`.</span><span class="sxs-lookup"><span data-stu-id="226ed-116">The automatic reply to send to the specified external audience, if **Status** is `AlwaysEnabled` or `Scheduled`.</span></span>|
|<span data-ttu-id="226ed-117">internalReplyMessage</span><span class="sxs-lookup"><span data-stu-id="226ed-117">internalReplyMessage</span></span>|<span data-ttu-id="226ed-118">string</span><span class="sxs-lookup"><span data-stu-id="226ed-118">string</span></span>|<span data-ttu-id="226ed-119">La respuesta automática para enviar a la audiencia interna de la organización del usuario que ha iniciado sesión, si **Status** es `AlwaysEnabled` o `Scheduled`.</span><span class="sxs-lookup"><span data-stu-id="226ed-119">The automatic reply to send to the audience internal to the signed-in user's organization, if **Status** is `AlwaysEnabled` or `Scheduled`.</span></span> |
|<span data-ttu-id="226ed-120">scheduledEndDateTime</span><span class="sxs-lookup"><span data-stu-id="226ed-120">scheduledEndDateTime</span></span>|[<span data-ttu-id="226ed-121">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="226ed-121">dateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="226ed-122">La fecha y hora en que se establece la finalización de las respuestas automáticas, si **Status** se establece en `Scheduled`.</span><span class="sxs-lookup"><span data-stu-id="226ed-122">The date and time that automatic replies are set to end, if **Status** is set to `Scheduled`.</span></span> |
|<span data-ttu-id="226ed-123">scheduledStartDateTime</span><span class="sxs-lookup"><span data-stu-id="226ed-123">scheduledStartDateTime</span></span>|[<span data-ttu-id="226ed-124">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="226ed-124">dateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="226ed-125">La fecha y hora en que se establece el inicio de las respuestas automáticas, si **Status** se establece en `Scheduled`.</span><span class="sxs-lookup"><span data-stu-id="226ed-125">The date and time that automatic replies are set to begin, if **Status** is set to `Scheduled`.</span></span>|
|<span data-ttu-id="226ed-126">status</span><span class="sxs-lookup"><span data-stu-id="226ed-126">status</span></span>|<span data-ttu-id="226ed-127">automaticRepliesStatus</span><span class="sxs-lookup"><span data-stu-id="226ed-127">automaticRepliesStatus</span></span>|<span data-ttu-id="226ed-128">Estado de las configuraciones de las respuestas automáticas.</span><span class="sxs-lookup"><span data-stu-id="226ed-128">Configurations status for automatic replies.</span></span> <span data-ttu-id="226ed-129">Los valores posibles son: `disabled`, `alwaysEnabled`, `scheduled`.</span><span class="sxs-lookup"><span data-stu-id="226ed-129">The possible values are: `disabled`, `alwaysEnabled`, `scheduled`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="226ed-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="226ed-130">JSON representation</span></span>

<span data-ttu-id="226ed-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="226ed-131">Here is a JSON representation of the resource.</span></span>

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
