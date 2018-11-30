---
title: tipo de enumeración managedAppClipboardSharingLevel
description: Representa el nivel al que Portapapeles del dispositivo pueden compartirse entre aplicaciones
ms.openlocfilehash: 7cf7b4a2f6ea6dc129a21167a2d75ba215ff29fd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032621"
---
# <a name="managedappclipboardsharinglevel-enum-type"></a><span data-ttu-id="2883b-103">tipo de enumeración managedAppClipboardSharingLevel</span><span class="sxs-lookup"><span data-stu-id="2883b-103">managedAppClipboardSharingLevel enum type</span></span>

> <span data-ttu-id="2883b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2883b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2883b-105">Representa el nivel al que Portapapeles del dispositivo pueden compartirse entre aplicaciones</span><span class="sxs-lookup"><span data-stu-id="2883b-105">Represents the level to which the device's clipboard may be shared between apps</span></span>
## <a name="members"></a><span data-ttu-id="2883b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="2883b-106">Members</span></span>
|<span data-ttu-id="2883b-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="2883b-107">Member</span></span>|<span data-ttu-id="2883b-108">Valor</span><span class="sxs-lookup"><span data-stu-id="2883b-108">Value</span></span>|<span data-ttu-id="2883b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="2883b-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2883b-110">allApps</span><span class="sxs-lookup"><span data-stu-id="2883b-110">allApps</span></span>|<span data-ttu-id="2883b-111">0</span><span class="sxs-lookup"><span data-stu-id="2883b-111">0</span></span>|<span data-ttu-id="2883b-112">Se permite el uso compartido entre todas las aplicaciones, o no administradas</span><span class="sxs-lookup"><span data-stu-id="2883b-112">Sharing is allowed between all apps, managed or not</span></span>|
|<span data-ttu-id="2883b-113">managedAppsWithPasteIn</span><span class="sxs-lookup"><span data-stu-id="2883b-113">managedAppsWithPasteIn</span></span>|<span data-ttu-id="2883b-114">1</span><span class="sxs-lookup"><span data-stu-id="2883b-114">1</span></span>|<span data-ttu-id="2883b-115">Se permite el uso compartido entre todas las aplicaciones administradas con pegar en habilitado</span><span class="sxs-lookup"><span data-stu-id="2883b-115">Sharing is allowed between all managed apps with paste in enabled</span></span>|
|<span data-ttu-id="2883b-116">managedApps</span><span class="sxs-lookup"><span data-stu-id="2883b-116">managedApps</span></span>|<span data-ttu-id="2883b-117">2</span><span class="sxs-lookup"><span data-stu-id="2883b-117">2</span></span>|<span data-ttu-id="2883b-118">Se permite el uso compartido entre todas las aplicaciones administradas</span><span class="sxs-lookup"><span data-stu-id="2883b-118">Sharing is allowed between all managed apps</span></span>|
|<span data-ttu-id="2883b-119">bloqueado</span><span class="sxs-lookup"><span data-stu-id="2883b-119">blocked</span></span>|<span data-ttu-id="2883b-120">3</span><span class="sxs-lookup"><span data-stu-id="2883b-120">3</span></span>|<span data-ttu-id="2883b-121">Uso compartido entre aplicaciones está deshabilitado</span><span class="sxs-lookup"><span data-stu-id="2883b-121">Sharing between apps is disabled</span></span>|



