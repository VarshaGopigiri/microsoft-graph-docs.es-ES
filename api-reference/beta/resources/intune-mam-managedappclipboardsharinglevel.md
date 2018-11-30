---
title: tipo de enumeración managedAppClipboardSharingLevel
description: Representa el nivel al que Portapapeles del dispositivo pueden compartirse entre aplicaciones
ms.openlocfilehash: 71c4ab2d629fdfee3ded68612d7060a0fa069809
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090612"
---
# <a name="managedappclipboardsharinglevel-enum-type"></a><span data-ttu-id="ec021-103">tipo de enumeración managedAppClipboardSharingLevel</span><span class="sxs-lookup"><span data-stu-id="ec021-103">managedAppClipboardSharingLevel enum type</span></span>

> <span data-ttu-id="ec021-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ec021-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ec021-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ec021-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ec021-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ec021-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ec021-107">Representa el nivel al que Portapapeles del dispositivo pueden compartirse entre aplicaciones</span><span class="sxs-lookup"><span data-stu-id="ec021-107">Represents the level to which the device's clipboard may be shared between apps</span></span>
## <a name="members"></a><span data-ttu-id="ec021-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ec021-108">Members</span></span>
|<span data-ttu-id="ec021-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="ec021-109">Member</span></span>|<span data-ttu-id="ec021-110">Valor</span><span class="sxs-lookup"><span data-stu-id="ec021-110">Value</span></span>|<span data-ttu-id="ec021-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec021-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ec021-112">allApps</span><span class="sxs-lookup"><span data-stu-id="ec021-112">allApps</span></span>|<span data-ttu-id="ec021-113">0</span><span class="sxs-lookup"><span data-stu-id="ec021-113">0</span></span>|<span data-ttu-id="ec021-114">Se permite el uso compartido entre todas las aplicaciones, o no administradas</span><span class="sxs-lookup"><span data-stu-id="ec021-114">Sharing is allowed between all apps, managed or not</span></span>|
|<span data-ttu-id="ec021-115">managedAppsWithPasteIn</span><span class="sxs-lookup"><span data-stu-id="ec021-115">managedAppsWithPasteIn</span></span>|<span data-ttu-id="ec021-116">1</span><span class="sxs-lookup"><span data-stu-id="ec021-116">1</span></span>|<span data-ttu-id="ec021-117">Se permite el uso compartido entre todas las aplicaciones administradas con pegar en habilitado</span><span class="sxs-lookup"><span data-stu-id="ec021-117">Sharing is allowed between all managed apps with paste in enabled</span></span>|
|<span data-ttu-id="ec021-118">managedApps</span><span class="sxs-lookup"><span data-stu-id="ec021-118">managedApps</span></span>|<span data-ttu-id="ec021-119">2</span><span class="sxs-lookup"><span data-stu-id="ec021-119">2</span></span>|<span data-ttu-id="ec021-120">Se permite el uso compartido entre todas las aplicaciones administradas</span><span class="sxs-lookup"><span data-stu-id="ec021-120">Sharing is allowed between all managed apps</span></span>|
|<span data-ttu-id="ec021-121">bloqueado</span><span class="sxs-lookup"><span data-stu-id="ec021-121">blocked</span></span>|<span data-ttu-id="ec021-122">3</span><span class="sxs-lookup"><span data-stu-id="ec021-122">3</span></span>|<span data-ttu-id="ec021-123">Uso compartido entre aplicaciones está deshabilitado</span><span class="sxs-lookup"><span data-stu-id="ec021-123">Sharing between apps is disabled</span></span>|





