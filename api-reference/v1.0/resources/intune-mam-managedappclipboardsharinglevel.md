---
title: tipo de enumeración managedAppClipboardSharingLevel
description: Representa el nivel al que Portapapeles del dispositivo pueden compartirse entre aplicaciones
localization_priority: Normal
ms.openlocfilehash: 16d6e9154b3d6e683d9ddce0efd70a40c01c8994
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27814318"
---
# <a name="managedappclipboardsharinglevel-enum-type"></a><span data-ttu-id="c67e9-103">tipo de enumeración managedAppClipboardSharingLevel</span><span class="sxs-lookup"><span data-stu-id="c67e9-103">managedAppClipboardSharingLevel enum type</span></span>

> <span data-ttu-id="c67e9-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c67e9-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c67e9-105">Representa el nivel al que Portapapeles del dispositivo pueden compartirse entre aplicaciones</span><span class="sxs-lookup"><span data-stu-id="c67e9-105">Represents the level to which the device's clipboard may be shared between apps</span></span>
## <a name="members"></a><span data-ttu-id="c67e9-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="c67e9-106">Members</span></span>
|<span data-ttu-id="c67e9-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="c67e9-107">Member</span></span>|<span data-ttu-id="c67e9-108">Valor</span><span class="sxs-lookup"><span data-stu-id="c67e9-108">Value</span></span>|<span data-ttu-id="c67e9-109">Description</span><span class="sxs-lookup"><span data-stu-id="c67e9-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c67e9-110">allApps</span><span class="sxs-lookup"><span data-stu-id="c67e9-110">allApps</span></span>|<span data-ttu-id="c67e9-111">0</span><span class="sxs-lookup"><span data-stu-id="c67e9-111">0</span></span>|<span data-ttu-id="c67e9-112">Se permite el uso compartido entre todas las aplicaciones, o no administradas</span><span class="sxs-lookup"><span data-stu-id="c67e9-112">Sharing is allowed between all apps, managed or not</span></span>|
|<span data-ttu-id="c67e9-113">managedAppsWithPasteIn</span><span class="sxs-lookup"><span data-stu-id="c67e9-113">managedAppsWithPasteIn</span></span>|<span data-ttu-id="c67e9-114">1</span><span class="sxs-lookup"><span data-stu-id="c67e9-114">1</span></span>|<span data-ttu-id="c67e9-115">Se permite el uso compartido entre todas las aplicaciones administradas con pegar en habilitado</span><span class="sxs-lookup"><span data-stu-id="c67e9-115">Sharing is allowed between all managed apps with paste in enabled</span></span>|
|<span data-ttu-id="c67e9-116">managedApps</span><span class="sxs-lookup"><span data-stu-id="c67e9-116">managedApps</span></span>|<span data-ttu-id="c67e9-117">2</span><span class="sxs-lookup"><span data-stu-id="c67e9-117">2</span></span>|<span data-ttu-id="c67e9-118">Se permite el uso compartido entre todas las aplicaciones administradas</span><span class="sxs-lookup"><span data-stu-id="c67e9-118">Sharing is allowed between all managed apps</span></span>|
|<span data-ttu-id="c67e9-119">bloqueado</span><span class="sxs-lookup"><span data-stu-id="c67e9-119">blocked</span></span>|<span data-ttu-id="c67e9-120">3</span><span class="sxs-lookup"><span data-stu-id="c67e9-120">3</span></span>|<span data-ttu-id="c67e9-121">Uso compartido entre aplicaciones está deshabilitado</span><span class="sxs-lookup"><span data-stu-id="c67e9-121">Sharing between apps is disabled</span></span>|



