---
title: tipo de enumeración managedAppClipboardSharingLevel
description: Representa el nivel al que Portapapeles del dispositivo pueden compartirse entre aplicaciones
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: 349f0ee08b8e3bff4e627c58318e2c21fa00847c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27946787"
---
# <a name="managedappclipboardsharinglevel-enum-type"></a><span data-ttu-id="4e182-103">tipo de enumeración managedAppClipboardSharingLevel</span><span class="sxs-lookup"><span data-stu-id="4e182-103">managedAppClipboardSharingLevel enum type</span></span>

> <span data-ttu-id="4e182-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4e182-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4e182-105">Representa el nivel al que Portapapeles del dispositivo pueden compartirse entre aplicaciones</span><span class="sxs-lookup"><span data-stu-id="4e182-105">Represents the level to which the device's clipboard may be shared between apps</span></span>
## <a name="members"></a><span data-ttu-id="4e182-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="4e182-106">Members</span></span>
|<span data-ttu-id="4e182-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="4e182-107">Member</span></span>|<span data-ttu-id="4e182-108">Valor</span><span class="sxs-lookup"><span data-stu-id="4e182-108">Value</span></span>|<span data-ttu-id="4e182-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e182-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4e182-110">allApps</span><span class="sxs-lookup"><span data-stu-id="4e182-110">allApps</span></span>|<span data-ttu-id="4e182-111">0</span><span class="sxs-lookup"><span data-stu-id="4e182-111">0</span></span>|<span data-ttu-id="4e182-112">Se permite el uso compartido entre todas las aplicaciones, o no administradas</span><span class="sxs-lookup"><span data-stu-id="4e182-112">Sharing is allowed between all apps, managed or not</span></span>|
|<span data-ttu-id="4e182-113">managedAppsWithPasteIn</span><span class="sxs-lookup"><span data-stu-id="4e182-113">managedAppsWithPasteIn</span></span>|<span data-ttu-id="4e182-114">1</span><span class="sxs-lookup"><span data-stu-id="4e182-114">1</span></span>|<span data-ttu-id="4e182-115">Se permite el uso compartido entre todas las aplicaciones administradas con pegar en habilitado</span><span class="sxs-lookup"><span data-stu-id="4e182-115">Sharing is allowed between all managed apps with paste in enabled</span></span>|
|<span data-ttu-id="4e182-116">managedApps</span><span class="sxs-lookup"><span data-stu-id="4e182-116">managedApps</span></span>|<span data-ttu-id="4e182-117">2</span><span class="sxs-lookup"><span data-stu-id="4e182-117">2</span></span>|<span data-ttu-id="4e182-118">Se permite el uso compartido entre todas las aplicaciones administradas</span><span class="sxs-lookup"><span data-stu-id="4e182-118">Sharing is allowed between all managed apps</span></span>|
|<span data-ttu-id="4e182-119">bloqueado</span><span class="sxs-lookup"><span data-stu-id="4e182-119">blocked</span></span>|<span data-ttu-id="4e182-120">3</span><span class="sxs-lookup"><span data-stu-id="4e182-120">3</span></span>|<span data-ttu-id="4e182-121">Uso compartido entre aplicaciones está deshabilitado</span><span class="sxs-lookup"><span data-stu-id="4e182-121">Sharing between apps is disabled</span></span>|



