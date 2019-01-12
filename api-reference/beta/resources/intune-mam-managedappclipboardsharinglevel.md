---
title: tipo de enumeración managedAppClipboardSharingLevel
description: Representa el nivel al que Portapapeles del dispositivo pueden compartirse entre aplicaciones
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: 41983b9bb30880768fff0ee02883c32fcb5305a6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27968422"
---
# <a name="managedappclipboardsharinglevel-enum-type"></a><span data-ttu-id="094f0-103">tipo de enumeración managedAppClipboardSharingLevel</span><span class="sxs-lookup"><span data-stu-id="094f0-103">managedAppClipboardSharingLevel enum type</span></span>

> <span data-ttu-id="094f0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="094f0-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="094f0-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="094f0-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="094f0-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="094f0-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="094f0-107">Representa el nivel al que Portapapeles del dispositivo pueden compartirse entre aplicaciones</span><span class="sxs-lookup"><span data-stu-id="094f0-107">Represents the level to which the device's clipboard may be shared between apps</span></span>
## <a name="members"></a><span data-ttu-id="094f0-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="094f0-108">Members</span></span>
|<span data-ttu-id="094f0-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="094f0-109">Member</span></span>|<span data-ttu-id="094f0-110">Valor</span><span class="sxs-lookup"><span data-stu-id="094f0-110">Value</span></span>|<span data-ttu-id="094f0-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="094f0-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="094f0-112">allApps</span><span class="sxs-lookup"><span data-stu-id="094f0-112">allApps</span></span>|<span data-ttu-id="094f0-113">0</span><span class="sxs-lookup"><span data-stu-id="094f0-113">0</span></span>|<span data-ttu-id="094f0-114">Se permite el uso compartido entre todas las aplicaciones, o no administradas</span><span class="sxs-lookup"><span data-stu-id="094f0-114">Sharing is allowed between all apps, managed or not</span></span>|
|<span data-ttu-id="094f0-115">managedAppsWithPasteIn</span><span class="sxs-lookup"><span data-stu-id="094f0-115">managedAppsWithPasteIn</span></span>|<span data-ttu-id="094f0-116">1</span><span class="sxs-lookup"><span data-stu-id="094f0-116">1</span></span>|<span data-ttu-id="094f0-117">Se permite el uso compartido entre todas las aplicaciones administradas con pegar en habilitado</span><span class="sxs-lookup"><span data-stu-id="094f0-117">Sharing is allowed between all managed apps with paste in enabled</span></span>|
|<span data-ttu-id="094f0-118">managedApps</span><span class="sxs-lookup"><span data-stu-id="094f0-118">managedApps</span></span>|<span data-ttu-id="094f0-119">2</span><span class="sxs-lookup"><span data-stu-id="094f0-119">2</span></span>|<span data-ttu-id="094f0-120">Se permite el uso compartido entre todas las aplicaciones administradas</span><span class="sxs-lookup"><span data-stu-id="094f0-120">Sharing is allowed between all managed apps</span></span>|
|<span data-ttu-id="094f0-121">bloqueado</span><span class="sxs-lookup"><span data-stu-id="094f0-121">blocked</span></span>|<span data-ttu-id="094f0-122">3</span><span class="sxs-lookup"><span data-stu-id="094f0-122">3</span></span>|<span data-ttu-id="094f0-123">Uso compartido entre aplicaciones está deshabilitado</span><span class="sxs-lookup"><span data-stu-id="094f0-123">Sharing between apps is disabled</span></span>|





