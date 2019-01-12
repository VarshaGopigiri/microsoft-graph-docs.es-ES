---
title: tipo de enumeración windowsDeviceHealthState
description: Estado de protección de extremo de equipo
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 628450b33a219e8408d5c5887c6902b78ae02bd0
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27923946"
---
# <a name="windowsdevicehealthstate-enum-type"></a><span data-ttu-id="1c1a9-103">tipo de enumeración windowsDeviceHealthState</span><span class="sxs-lookup"><span data-stu-id="1c1a9-103">windowsDeviceHealthState enum type</span></span>

> <span data-ttu-id="1c1a9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1c1a9-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1c1a9-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1c1a9-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1c1a9-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1c1a9-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1c1a9-107">Estado de protección de extremo de equipo</span><span class="sxs-lookup"><span data-stu-id="1c1a9-107">Computer endpoint protection state</span></span>
## <a name="members"></a><span data-ttu-id="1c1a9-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="1c1a9-108">Members</span></span>
|<span data-ttu-id="1c1a9-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="1c1a9-109">Member</span></span>|<span data-ttu-id="1c1a9-110">Valor</span><span class="sxs-lookup"><span data-stu-id="1c1a9-110">Value</span></span>|<span data-ttu-id="1c1a9-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c1a9-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1c1a9-112">clean</span><span class="sxs-lookup"><span data-stu-id="1c1a9-112">clean</span></span>|<span data-ttu-id="1c1a9-113">0</span><span class="sxs-lookup"><span data-stu-id="1c1a9-113">0</span></span>|<span data-ttu-id="1c1a9-114">Equipo está limpio y no se requiere ninguna acción</span><span class="sxs-lookup"><span data-stu-id="1c1a9-114">Computer is clean and no action is required</span></span>|
|<span data-ttu-id="1c1a9-115">fullScanPending</span><span class="sxs-lookup"><span data-stu-id="1c1a9-115">fullScanPending</span></span>|<span data-ttu-id="1c1a9-116">1</span><span class="sxs-lookup"><span data-stu-id="1c1a9-116">1</span></span>|<span data-ttu-id="1c1a9-117">Equipo está en estado de examen completo pendiente</span><span class="sxs-lookup"><span data-stu-id="1c1a9-117">Computer is in pending full scan state</span></span>|
|<span data-ttu-id="1c1a9-118">rebootPending</span><span class="sxs-lookup"><span data-stu-id="1c1a9-118">rebootPending</span></span>|<span data-ttu-id="1c1a9-119">2</span><span class="sxs-lookup"><span data-stu-id="1c1a9-119">2</span></span>|<span data-ttu-id="1c1a9-120">Equipo está en estado de reinicio pendiente</span><span class="sxs-lookup"><span data-stu-id="1c1a9-120">Computer is in pending reboot state</span></span>|
|<span data-ttu-id="1c1a9-121">manualStepsPending</span><span class="sxs-lookup"><span data-stu-id="1c1a9-121">manualStepsPending</span></span>|<span data-ttu-id="1c1a9-122">4</span><span class="sxs-lookup"><span data-stu-id="1c1a9-122">4</span></span>|<span data-ttu-id="1c1a9-123">Equipo está en estado de pasos manuales pendiente</span><span class="sxs-lookup"><span data-stu-id="1c1a9-123">Computer is in pending manual steps state</span></span>|
|<span data-ttu-id="1c1a9-124">offlineScanPending</span><span class="sxs-lookup"><span data-stu-id="1c1a9-124">offlineScanPending</span></span>|<span data-ttu-id="1c1a9-125">8</span><span class="sxs-lookup"><span data-stu-id="1c1a9-125">8</span></span>|<span data-ttu-id="1c1a9-126">Equipo está en estado de análisis sin conexión pendiente</span><span class="sxs-lookup"><span data-stu-id="1c1a9-126">Computer is in pending offline scan state</span></span>|
|<span data-ttu-id="1c1a9-127">crítico</span><span class="sxs-lookup"><span data-stu-id="1c1a9-127">critical</span></span>|<span data-ttu-id="1c1a9-128">16</span><span class="sxs-lookup"><span data-stu-id="1c1a9-128">16</span></span>|<span data-ttu-id="1c1a9-129">Equipo está en estado de error crítico</span><span class="sxs-lookup"><span data-stu-id="1c1a9-129">Computer is in critical failure state</span></span>|





