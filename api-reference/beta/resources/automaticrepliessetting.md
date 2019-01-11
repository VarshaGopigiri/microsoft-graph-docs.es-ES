---
title: Tipo de recurso automaticRepliesSetting
description: 'Opciones de configuración para notificar automáticamente al remitente de un correo electrónico entrante con un mensaje desde la '
localization_priority: Normal
ms.openlocfilehash: 0160197a4fafe10b7f78be9124da3b6260bfcee6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27820660"
---
# <a name="automaticrepliessetting-resource-type"></a><span data-ttu-id="52ff7-103">Tipo de recurso automaticRepliesSetting</span><span class="sxs-lookup"><span data-stu-id="52ff7-103">automaticRepliesSetting resource type</span></span>

> <span data-ttu-id="52ff7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="52ff7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="52ff7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="52ff7-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="52ff7-p102">Opciones de configuración para notificar de forma automática al remitente de un mensaje de correo entrante con un mensaje del usuario que ha iniciado sesión. Por ejemplo, una respuesta automática para notificar que el usuario que ha iniciado sesión no está disponible para responder a correos electrónicos.</span><span class="sxs-lookup"><span data-stu-id="52ff7-p102">Configuration settings to automatically notify the sender of an incoming email with a message from the signed-in user. For example, an automatic reply to notify that the signed-in user is unavailable to respond to emails.</span></span> 


## <a name="properties"></a><span data-ttu-id="52ff7-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="52ff7-108">Properties</span></span>
| <span data-ttu-id="52ff7-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="52ff7-109">Property</span></span>     | <span data-ttu-id="52ff7-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="52ff7-110">Type</span></span>   |<span data-ttu-id="52ff7-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="52ff7-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="52ff7-112">externalAudience</span><span class="sxs-lookup"><span data-stu-id="52ff7-112">externalAudience</span></span>|<span data-ttu-id="52ff7-113">String</span><span class="sxs-lookup"><span data-stu-id="52ff7-113">String</span></span>| <span data-ttu-id="52ff7-p103">El conjunto de audiencia externa a la organización del usuario que ha iniciado sesión que recibirá el **ExternalReplyMessage**, si **Status** es `AlwaysEnabled` o `Scheduled`. Los valores posibles son: `none`, `contactsOnly`, `all`.</span><span class="sxs-lookup"><span data-stu-id="52ff7-p103">The set of audience external to the signed-in user's organization who will receive the **ExternalReplyMessage**, if **Status** is `AlwaysEnabled` or `Scheduled`. Possible values are: `none`, `contactsOnly`, `all`.</span></span>|
|<span data-ttu-id="52ff7-116">externalReplyMessage</span><span class="sxs-lookup"><span data-stu-id="52ff7-116">externalReplyMessage</span></span>|<span data-ttu-id="52ff7-117">string</span><span class="sxs-lookup"><span data-stu-id="52ff7-117">string</span></span>|<span data-ttu-id="52ff7-118">La respuesta automática para enviar a la audiencia externa especificada, si **Status** es `AlwaysEnabled` o `Scheduled`.</span><span class="sxs-lookup"><span data-stu-id="52ff7-118">The automatic reply to send to the specified external audience, if **Status** is `AlwaysEnabled` or `Scheduled`.</span></span>|
|<span data-ttu-id="52ff7-119">internalReplyMessage</span><span class="sxs-lookup"><span data-stu-id="52ff7-119">internalReplyMessage</span></span>|<span data-ttu-id="52ff7-120">string</span><span class="sxs-lookup"><span data-stu-id="52ff7-120">string</span></span>|<span data-ttu-id="52ff7-121">La respuesta automática para enviar a la audiencia interna de la organización del usuario que ha iniciado sesión, si **Status** es `AlwaysEnabled` o `Scheduled`.</span><span class="sxs-lookup"><span data-stu-id="52ff7-121">The automatic reply to send to the audience internal to the signed-in user's organization, if **Status** is `AlwaysEnabled` or `Scheduled`.</span></span> |
|<span data-ttu-id="52ff7-122">scheduledEndDateTime</span><span class="sxs-lookup"><span data-stu-id="52ff7-122">scheduledEndDateTime</span></span>|[<span data-ttu-id="52ff7-123">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="52ff7-123">dateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="52ff7-124">La fecha y hora en que se establece la finalización de las respuestas automáticas, si **Status** se establece en `Scheduled`.</span><span class="sxs-lookup"><span data-stu-id="52ff7-124">The date and time that automatic replies are set to end, if **Status** is set to `Scheduled`.</span></span> |
|<span data-ttu-id="52ff7-125">scheduledStartDateTime</span><span class="sxs-lookup"><span data-stu-id="52ff7-125">scheduledStartDateTime</span></span>|[<span data-ttu-id="52ff7-126">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="52ff7-126">dateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="52ff7-127">La fecha y hora en que se establece el inicio de las respuestas automáticas, si **Status** se establece en `Scheduled`.</span><span class="sxs-lookup"><span data-stu-id="52ff7-127">The date and time that automatic replies are set to begin, if **Status** is set to `Scheduled`.</span></span>|
|<span data-ttu-id="52ff7-128">status</span><span class="sxs-lookup"><span data-stu-id="52ff7-128">status</span></span>|<span data-ttu-id="52ff7-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="52ff7-129">String</span></span>|<span data-ttu-id="52ff7-p104">Estado de las configuraciones para las respuestas automáticas. Los valores posibles son: `disabled`, `alwaysEnabled`, `scheduled`.</span><span class="sxs-lookup"><span data-stu-id="52ff7-p104">Configurations status for automatic replies. Possible values are: `disabled`, `alwaysEnabled`, `scheduled`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="52ff7-132">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="52ff7-132">JSON representation</span></span>

<span data-ttu-id="52ff7-133">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="52ff7-133">Here is a JSON representation of the resource.</span></span>

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
