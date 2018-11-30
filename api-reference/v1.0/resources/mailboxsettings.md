---
title: Tipo de recurso mailboxSettings
description: Configuración del buzón principal del usuario que inició sesión.
ms.openlocfilehash: b8fb2c1f11f849a4633d6be4f4519b85b33923ea
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031800"
---
# <a name="mailboxsettings-resource-type"></a><span data-ttu-id="55493-103">Tipo de recurso mailboxSettings</span><span class="sxs-lookup"><span data-stu-id="55493-103">mailboxSettings resource type</span></span>

<span data-ttu-id="55493-104">Configuración del buzón principal del usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="55493-104">Settings for the primary mailbox of the signed-in user.</span></span>


## <a name="properties"></a><span data-ttu-id="55493-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="55493-105">Properties</span></span>
| <span data-ttu-id="55493-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="55493-106">Property</span></span>     | <span data-ttu-id="55493-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="55493-107">Type</span></span>   |<span data-ttu-id="55493-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="55493-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="55493-109">archiveFolder</span><span class="sxs-lookup"><span data-stu-id="55493-109">archiveFolder</span></span>|<span data-ttu-id="55493-110">string</span><span class="sxs-lookup"><span data-stu-id="55493-110">string</span></span>|<span data-ttu-id="55493-111">Identificador de una carpeta de archivo del usuario.</span><span class="sxs-lookup"><span data-stu-id="55493-111">Folder ID of an archive folder for the user.</span></span>|
|<span data-ttu-id="55493-112">automaticRepliesSetting</span><span class="sxs-lookup"><span data-stu-id="55493-112">automaticRepliesSetting</span></span>|[<span data-ttu-id="55493-113">automaticRepliesSetting</span><span class="sxs-lookup"><span data-stu-id="55493-113">automaticRepliesSetting</span></span>](automaticrepliessetting.md)|<span data-ttu-id="55493-114">Opciones de configuración para notificar de forma automática al remitente de un mensaje de correo entrante con un mensaje del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="55493-114">Configuration settings to automatically notify the sender of an incoming email with a message from the signed-in user.</span></span>|
|<span data-ttu-id="55493-115">language</span><span class="sxs-lookup"><span data-stu-id="55493-115">language</span></span>|[<span data-ttu-id="55493-116">localeInfo</span><span class="sxs-lookup"><span data-stu-id="55493-116">localeInfo</span></span>](localeinfo.md)|<span data-ttu-id="55493-117">Representación de la configuración regional del usuario, como el idioma preferido y el país o región.</span><span class="sxs-lookup"><span data-stu-id="55493-117">The locale information for the user, including the preferred language and country/region.</span></span>|
|<span data-ttu-id="55493-118">timeZone</span><span class="sxs-lookup"><span data-stu-id="55493-118">timeZone</span></span>|<span data-ttu-id="55493-119">string</span><span class="sxs-lookup"><span data-stu-id="55493-119">string</span></span>|<span data-ttu-id="55493-120">La zona horaria predeterminada del buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="55493-120">The default time zone for the user's mailbox.</span></span>|
|<span data-ttu-id="55493-121">workingHours</span><span class="sxs-lookup"><span data-stu-id="55493-121">workingHours</span></span>|[<span data-ttu-id="55493-122">workingHours</span><span class="sxs-lookup"><span data-stu-id="55493-122">workingHours</span></span>](workinghours.md)|<span data-ttu-id="55493-123">Días de la semana y horas de la zona horaria específica en la que trabaja el usuario.</span><span class="sxs-lookup"><span data-stu-id="55493-123">The days of the week and hours in a specific time zone that the user works.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="55493-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="55493-124">JSON representation</span></span>

<span data-ttu-id="55493-125">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="55493-125">Here is a JSON representation of the resource.</span></span>

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