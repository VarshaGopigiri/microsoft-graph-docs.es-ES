---
title: tipo de enumeración windowsDeviceHealthState
description: Estado de protección de extremo de equipo
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 91869502d0d61c25c6eb8dd67ba4e8e32d28fbb2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27885928"
---
# <a name="windowsdevicehealthstate-enum-type"></a><span data-ttu-id="4b486-103">tipo de enumeración windowsDeviceHealthState</span><span class="sxs-lookup"><span data-stu-id="4b486-103">windowsDeviceHealthState enum type</span></span>

> <span data-ttu-id="4b486-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4b486-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4b486-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4b486-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="4b486-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4b486-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4b486-107">Estado de protección de extremo de equipo</span><span class="sxs-lookup"><span data-stu-id="4b486-107">Computer endpoint protection state</span></span>
## <a name="members"></a><span data-ttu-id="4b486-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="4b486-108">Members</span></span>
|<span data-ttu-id="4b486-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="4b486-109">Member</span></span>|<span data-ttu-id="4b486-110">Valor</span><span class="sxs-lookup"><span data-stu-id="4b486-110">Value</span></span>|<span data-ttu-id="4b486-111">Description</span><span class="sxs-lookup"><span data-stu-id="4b486-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4b486-112">clean</span><span class="sxs-lookup"><span data-stu-id="4b486-112">clean</span></span>|<span data-ttu-id="4b486-113">0</span><span class="sxs-lookup"><span data-stu-id="4b486-113">0</span></span>|<span data-ttu-id="4b486-114">Equipo está limpio y no se requiere ninguna acción</span><span class="sxs-lookup"><span data-stu-id="4b486-114">Computer is clean and no action is required</span></span>|
|<span data-ttu-id="4b486-115">fullScanPending</span><span class="sxs-lookup"><span data-stu-id="4b486-115">fullScanPending</span></span>|<span data-ttu-id="4b486-116">1</span><span class="sxs-lookup"><span data-stu-id="4b486-116">1</span></span>|<span data-ttu-id="4b486-117">Equipo está en estado de examen completo pendiente</span><span class="sxs-lookup"><span data-stu-id="4b486-117">Computer is in pending full scan state</span></span>|
|<span data-ttu-id="4b486-118">rebootPending</span><span class="sxs-lookup"><span data-stu-id="4b486-118">rebootPending</span></span>|<span data-ttu-id="4b486-119">2</span><span class="sxs-lookup"><span data-stu-id="4b486-119">2</span></span>|<span data-ttu-id="4b486-120">Equipo está en estado de reinicio pendiente</span><span class="sxs-lookup"><span data-stu-id="4b486-120">Computer is in pending reboot state</span></span>|
|<span data-ttu-id="4b486-121">manualStepsPending</span><span class="sxs-lookup"><span data-stu-id="4b486-121">manualStepsPending</span></span>|<span data-ttu-id="4b486-122">4</span><span class="sxs-lookup"><span data-stu-id="4b486-122">4</span></span>|<span data-ttu-id="4b486-123">Equipo está en estado de pasos manuales pendiente</span><span class="sxs-lookup"><span data-stu-id="4b486-123">Computer is in pending manual steps state</span></span>|
|<span data-ttu-id="4b486-124">offlineScanPending</span><span class="sxs-lookup"><span data-stu-id="4b486-124">offlineScanPending</span></span>|<span data-ttu-id="4b486-125">8</span><span class="sxs-lookup"><span data-stu-id="4b486-125">8</span></span>|<span data-ttu-id="4b486-126">Equipo está en estado de análisis sin conexión pendiente</span><span class="sxs-lookup"><span data-stu-id="4b486-126">Computer is in pending offline scan state</span></span>|
|<span data-ttu-id="4b486-127">crítico</span><span class="sxs-lookup"><span data-stu-id="4b486-127">critical</span></span>|<span data-ttu-id="4b486-128">16</span><span class="sxs-lookup"><span data-stu-id="4b486-128">16</span></span>|<span data-ttu-id="4b486-129">Equipo está en estado de error crítico</span><span class="sxs-lookup"><span data-stu-id="4b486-129">Computer is in critical failure state</span></span>|





