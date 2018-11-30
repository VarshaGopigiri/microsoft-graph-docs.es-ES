---
title: tipo de enumeración windowsDeviceHealthState
description: Estado de protección de extremo de equipo
ms.openlocfilehash: 601531dd71ee0d44e9f5ebc89eb018ba5e0f2675
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083010"
---
# <a name="windowsdevicehealthstate-enum-type"></a><span data-ttu-id="7a133-103">tipo de enumeración windowsDeviceHealthState</span><span class="sxs-lookup"><span data-stu-id="7a133-103">windowsDeviceHealthState enum type</span></span>

> <span data-ttu-id="7a133-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7a133-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7a133-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7a133-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7a133-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7a133-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7a133-107">Estado de protección de extremo de equipo</span><span class="sxs-lookup"><span data-stu-id="7a133-107">Computer endpoint protection state</span></span>
## <a name="members"></a><span data-ttu-id="7a133-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7a133-108">Members</span></span>
|<span data-ttu-id="7a133-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="7a133-109">Member</span></span>|<span data-ttu-id="7a133-110">Valor</span><span class="sxs-lookup"><span data-stu-id="7a133-110">Value</span></span>|<span data-ttu-id="7a133-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a133-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7a133-112">clean</span><span class="sxs-lookup"><span data-stu-id="7a133-112">clean</span></span>|<span data-ttu-id="7a133-113">0</span><span class="sxs-lookup"><span data-stu-id="7a133-113">0</span></span>|<span data-ttu-id="7a133-114">Equipo está limpio y no se requiere ninguna acción</span><span class="sxs-lookup"><span data-stu-id="7a133-114">Computer is clean and no action is required</span></span>|
|<span data-ttu-id="7a133-115">fullScanPending</span><span class="sxs-lookup"><span data-stu-id="7a133-115">fullScanPending</span></span>|<span data-ttu-id="7a133-116">1</span><span class="sxs-lookup"><span data-stu-id="7a133-116">1</span></span>|<span data-ttu-id="7a133-117">Equipo está en estado de examen completo pendiente</span><span class="sxs-lookup"><span data-stu-id="7a133-117">Computer is in pending full scan state</span></span>|
|<span data-ttu-id="7a133-118">rebootPending</span><span class="sxs-lookup"><span data-stu-id="7a133-118">rebootPending</span></span>|<span data-ttu-id="7a133-119">2</span><span class="sxs-lookup"><span data-stu-id="7a133-119">2</span></span>|<span data-ttu-id="7a133-120">Equipo está en estado de reinicio pendiente</span><span class="sxs-lookup"><span data-stu-id="7a133-120">Computer is in pending reboot state</span></span>|
|<span data-ttu-id="7a133-121">manualStepsPending</span><span class="sxs-lookup"><span data-stu-id="7a133-121">manualStepsPending</span></span>|<span data-ttu-id="7a133-122">4</span><span class="sxs-lookup"><span data-stu-id="7a133-122">4</span></span>|<span data-ttu-id="7a133-123">Equipo está en estado de pasos manuales pendiente</span><span class="sxs-lookup"><span data-stu-id="7a133-123">Computer is in pending manual steps state</span></span>|
|<span data-ttu-id="7a133-124">offlineScanPending</span><span class="sxs-lookup"><span data-stu-id="7a133-124">offlineScanPending</span></span>|<span data-ttu-id="7a133-125">8</span><span class="sxs-lookup"><span data-stu-id="7a133-125">8</span></span>|<span data-ttu-id="7a133-126">Equipo está en estado de análisis sin conexión pendiente</span><span class="sxs-lookup"><span data-stu-id="7a133-126">Computer is in pending offline scan state</span></span>|
|<span data-ttu-id="7a133-127">crítico</span><span class="sxs-lookup"><span data-stu-id="7a133-127">critical</span></span>|<span data-ttu-id="7a133-128">16</span><span class="sxs-lookup"><span data-stu-id="7a133-128">16</span></span>|<span data-ttu-id="7a133-129">Equipo está en estado de error crítico</span><span class="sxs-lookup"><span data-stu-id="7a133-129">Computer is in critical failure state</span></span>|





