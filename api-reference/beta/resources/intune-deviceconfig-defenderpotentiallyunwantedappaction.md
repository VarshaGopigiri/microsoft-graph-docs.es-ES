---
title: tipo de enumeración defenderPotentiallyUnwantedAppAction
description: Acción de Defender tomar detectado potencialmente no deseados aplicación (PUA).
ms.openlocfilehash: c786906046d6a35c026da95246016537e4325aab
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085203"
---
# <a name="defenderpotentiallyunwantedappaction-enum-type"></a><span data-ttu-id="a2403-103">tipo de enumeración defenderPotentiallyUnwantedAppAction</span><span class="sxs-lookup"><span data-stu-id="a2403-103">defenderPotentiallyUnwantedAppAction enum type</span></span>

> <span data-ttu-id="a2403-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a2403-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a2403-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a2403-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a2403-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a2403-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a2403-107">Acción de Defender tomar detectado potencialmente no deseados aplicación (PUA).</span><span class="sxs-lookup"><span data-stu-id="a2403-107">Defender’s action to take on detected Potentially Unwanted Application (PUA).</span></span>
## <a name="members"></a><span data-ttu-id="a2403-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a2403-108">Members</span></span>
|<span data-ttu-id="a2403-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="a2403-109">Member</span></span>|<span data-ttu-id="a2403-110">Valor</span><span class="sxs-lookup"><span data-stu-id="a2403-110">Value</span></span>|<span data-ttu-id="a2403-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2403-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a2403-112">deviceDefault</span><span class="sxs-lookup"><span data-stu-id="a2403-112">deviceDefault</span></span>|<span data-ttu-id="a2403-113">0</span><span class="sxs-lookup"><span data-stu-id="a2403-113">0</span></span>|<span data-ttu-id="a2403-114">Protección de PUA está desactivada.</span><span class="sxs-lookup"><span data-stu-id="a2403-114">PUA Protection is off.</span></span> <span data-ttu-id="a2403-115">Defender no protegerá contra aplicaciones potencialmente no deseadas.</span><span class="sxs-lookup"><span data-stu-id="a2403-115">Defender will not protect against potentially unwanted applications.</span></span>|
|<span data-ttu-id="a2403-116">bloque</span><span class="sxs-lookup"><span data-stu-id="a2403-116">block</span></span>|<span data-ttu-id="a2403-117">1</span><span class="sxs-lookup"><span data-stu-id="a2403-117">1</span></span>|<span data-ttu-id="a2403-118">Protección de PUA está activada.</span><span class="sxs-lookup"><span data-stu-id="a2403-118">PUA Protection is on.</span></span> <span data-ttu-id="a2403-119">Elementos detectados están bloqueados.</span><span class="sxs-lookup"><span data-stu-id="a2403-119">Detected items are blocked.</span></span> <span data-ttu-id="a2403-120">Se muestran en el historial de junto con otras amenazas.</span><span class="sxs-lookup"><span data-stu-id="a2403-120">They will show in history along with other threats.</span></span>|
|<span data-ttu-id="a2403-121">auditoría</span><span class="sxs-lookup"><span data-stu-id="a2403-121">audit</span></span>|<span data-ttu-id="a2403-122">2</span><span class="sxs-lookup"><span data-stu-id="a2403-122">2</span></span>|<span data-ttu-id="a2403-123">Modo de auditoría.</span><span class="sxs-lookup"><span data-stu-id="a2403-123">Audit mode.</span></span> <span data-ttu-id="a2403-124">Defender se detecta aplicaciones potencialmente no deseadas, pero no tomar ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="a2403-124">Defender will detect potentially unwanted applications, but take no actions.</span></span> <span data-ttu-id="a2403-125">Puede revisar información acerca de las aplicaciones Defender habría tomado acción contra buscando creados por Defender en el evento Visor de eventos.</span><span class="sxs-lookup"><span data-stu-id="a2403-125">You can review information about applications Defender would have taken action against by searching for events created by Defender in the Event Viewer.</span></span>|





