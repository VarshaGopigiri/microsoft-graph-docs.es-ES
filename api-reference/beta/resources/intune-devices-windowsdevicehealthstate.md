---
title: tipo de enumeración windowsDeviceHealthState
description: Estado de protección de extremo de equipo
author: tfitzmac
ms.openlocfilehash: b794f8121132e396459f9198c644084690fe95b4
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27326330"
---
# <a name="windowsdevicehealthstate-enum-type"></a><span data-ttu-id="74127-103">tipo de enumeración windowsDeviceHealthState</span><span class="sxs-lookup"><span data-stu-id="74127-103">windowsDeviceHealthState enum type</span></span>

> <span data-ttu-id="74127-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="74127-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="74127-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="74127-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="74127-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="74127-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="74127-107">Estado de protección de extremo de equipo</span><span class="sxs-lookup"><span data-stu-id="74127-107">Computer endpoint protection state</span></span>
## <a name="members"></a><span data-ttu-id="74127-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="74127-108">Members</span></span>
|<span data-ttu-id="74127-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="74127-109">Member</span></span>|<span data-ttu-id="74127-110">Valor</span><span class="sxs-lookup"><span data-stu-id="74127-110">Value</span></span>|<span data-ttu-id="74127-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="74127-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="74127-112">clean</span><span class="sxs-lookup"><span data-stu-id="74127-112">clean</span></span>|<span data-ttu-id="74127-113">0</span><span class="sxs-lookup"><span data-stu-id="74127-113">0</span></span>|<span data-ttu-id="74127-114">Equipo está limpio y no se requiere ninguna acción</span><span class="sxs-lookup"><span data-stu-id="74127-114">Computer is clean and no action is required</span></span>|
|<span data-ttu-id="74127-115">fullScanPending</span><span class="sxs-lookup"><span data-stu-id="74127-115">fullScanPending</span></span>|<span data-ttu-id="74127-116">1</span><span class="sxs-lookup"><span data-stu-id="74127-116">1</span></span>|<span data-ttu-id="74127-117">Equipo está en estado de examen completo pendiente</span><span class="sxs-lookup"><span data-stu-id="74127-117">Computer is in pending full scan state</span></span>|
|<span data-ttu-id="74127-118">rebootPending</span><span class="sxs-lookup"><span data-stu-id="74127-118">rebootPending</span></span>|<span data-ttu-id="74127-119">2</span><span class="sxs-lookup"><span data-stu-id="74127-119">2</span></span>|<span data-ttu-id="74127-120">Equipo está en estado de reinicio pendiente</span><span class="sxs-lookup"><span data-stu-id="74127-120">Computer is in pending reboot state</span></span>|
|<span data-ttu-id="74127-121">manualStepsPending</span><span class="sxs-lookup"><span data-stu-id="74127-121">manualStepsPending</span></span>|<span data-ttu-id="74127-122">4</span><span class="sxs-lookup"><span data-stu-id="74127-122">4</span></span>|<span data-ttu-id="74127-123">Equipo está en estado de pasos manuales pendiente</span><span class="sxs-lookup"><span data-stu-id="74127-123">Computer is in pending manual steps state</span></span>|
|<span data-ttu-id="74127-124">offlineScanPending</span><span class="sxs-lookup"><span data-stu-id="74127-124">offlineScanPending</span></span>|<span data-ttu-id="74127-125">8</span><span class="sxs-lookup"><span data-stu-id="74127-125">8</span></span>|<span data-ttu-id="74127-126">Equipo está en estado de análisis sin conexión pendiente</span><span class="sxs-lookup"><span data-stu-id="74127-126">Computer is in pending offline scan state</span></span>|
|<span data-ttu-id="74127-127">crítico</span><span class="sxs-lookup"><span data-stu-id="74127-127">critical</span></span>|<span data-ttu-id="74127-128">16</span><span class="sxs-lookup"><span data-stu-id="74127-128">16</span></span>|<span data-ttu-id="74127-129">Equipo está en estado de error crítico</span><span class="sxs-lookup"><span data-stu-id="74127-129">Computer is in critical failure state</span></span>|





