---
title: Tipo de recurso mailboxSettings
description: Configuración del buzón principal del usuario que inició sesión.
localization_priority: Normal
ms.openlocfilehash: 83bb3fffce2c4d61c92b9110c88d05fbba86893a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27887727"
---
# <a name="mailboxsettings-resource-type"></a><span data-ttu-id="9240e-103">Tipo de recurso mailboxSettings</span><span class="sxs-lookup"><span data-stu-id="9240e-103">mailboxSettings resource type</span></span>

> <span data-ttu-id="9240e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9240e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9240e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9240e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9240e-106">Configuración del buzón principal del usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="9240e-106">Settings for the primary mailbox of the signed-in user.</span></span>


## <a name="properties"></a><span data-ttu-id="9240e-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9240e-107">Properties</span></span>
| <span data-ttu-id="9240e-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9240e-108">Property</span></span>     | <span data-ttu-id="9240e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="9240e-109">Type</span></span>   |<span data-ttu-id="9240e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9240e-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9240e-111">archiveFolder</span><span class="sxs-lookup"><span data-stu-id="9240e-111">archiveFolder</span></span>|<span data-ttu-id="9240e-112">string</span><span class="sxs-lookup"><span data-stu-id="9240e-112">string</span></span>|<span data-ttu-id="9240e-113">Identificador de una carpeta de archivo del usuario.</span><span class="sxs-lookup"><span data-stu-id="9240e-113">Folder ID of an archive folder for the user.</span></span>|
|<span data-ttu-id="9240e-114">automaticRepliesSetting</span><span class="sxs-lookup"><span data-stu-id="9240e-114">automaticRepliesSetting</span></span>|[<span data-ttu-id="9240e-115">automaticRepliesSetting</span><span class="sxs-lookup"><span data-stu-id="9240e-115">automaticRepliesSetting</span></span>](automaticrepliessetting.md)|<span data-ttu-id="9240e-116">Opciones de configuración para notificar de forma automática al remitente de un mensaje de correo entrante con un mensaje del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="9240e-116">Configuration settings to automatically notify the sender of an incoming email with a message from the signed-in user.</span></span>|
|<span data-ttu-id="9240e-117">language</span><span class="sxs-lookup"><span data-stu-id="9240e-117">language</span></span>|[<span data-ttu-id="9240e-118">localeInfo</span><span class="sxs-lookup"><span data-stu-id="9240e-118">localeInfo</span></span>](localeinfo.md)|<span data-ttu-id="9240e-119">Representación de la configuración regional del usuario, como el idioma preferido y el país o región.</span><span class="sxs-lookup"><span data-stu-id="9240e-119">The locale information for the user, including the preferred language and country/region.</span></span>|
|<span data-ttu-id="9240e-120">timeZone</span><span class="sxs-lookup"><span data-stu-id="9240e-120">timeZone</span></span>|<span data-ttu-id="9240e-121">string</span><span class="sxs-lookup"><span data-stu-id="9240e-121">string</span></span>|<span data-ttu-id="9240e-122">La zona horaria predeterminada del buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="9240e-122">The default time zone for the user's mailbox.</span></span>|
|<span data-ttu-id="9240e-123">workingHours</span><span class="sxs-lookup"><span data-stu-id="9240e-123">workingHours</span></span>|[<span data-ttu-id="9240e-124">workingHours</span><span class="sxs-lookup"><span data-stu-id="9240e-124">workingHours</span></span>](workinghours.md)|<span data-ttu-id="9240e-125">Días de la semana y horas de la zona horaria específica en la que trabaja el usuario.</span><span class="sxs-lookup"><span data-stu-id="9240e-125">The days of the week and hours in a specific time zone that the user works.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="9240e-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9240e-126">JSON representation</span></span>

<span data-ttu-id="9240e-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9240e-127">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "archiveFolder"
  ],
  "@odata.type": "microsoft.graph.mailboxSettings"
}-->

```json
{
  "archiveFolder": "string",
  "automaticRepliesSetting": {"@odata.type": "microsoft.graph.automaticRepliesSetting"},
  "language": {"@odata.type": "microsoft.graph.localeInfo"},
  "timeZone": "string",
  "workingHours": {"@odata.type": "microsoft.graph.workingHours"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mailboxSettings resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
