---
title: tipo de enumeración mobileAppIntent
description: Indica el estado de la aplicación en el dispositivo móvil.
author: tfitzmac
ms.openlocfilehash: 0a230279a947ab60314a53872670fff871eff745
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27347232"
---
# <a name="mobileappintent-enum-type"></a><span data-ttu-id="a2f45-103">tipo de enumeración mobileAppIntent</span><span class="sxs-lookup"><span data-stu-id="a2f45-103">mobileAppIntent enum type</span></span>

> <span data-ttu-id="a2f45-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a2f45-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a2f45-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a2f45-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a2f45-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a2f45-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a2f45-107">Indica el estado de la aplicación en el dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="a2f45-107">Indicates the status of the mobile app on the device.</span></span>
## <a name="members"></a><span data-ttu-id="a2f45-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a2f45-108">Members</span></span>
|<span data-ttu-id="a2f45-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="a2f45-109">Member</span></span>|<span data-ttu-id="a2f45-110">Valor</span><span class="sxs-lookup"><span data-stu-id="a2f45-110">Value</span></span>|<span data-ttu-id="a2f45-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2f45-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a2f45-112">disponible</span><span class="sxs-lookup"><span data-stu-id="a2f45-112">available</span></span>|<span data-ttu-id="a2f45-113">0</span><span class="sxs-lookup"><span data-stu-id="a2f45-113">0</span></span>|<span data-ttu-id="a2f45-114">Disponible</span><span class="sxs-lookup"><span data-stu-id="a2f45-114">Available</span></span>|
|<span data-ttu-id="a2f45-115">no está disponible</span><span class="sxs-lookup"><span data-stu-id="a2f45-115">notAvailable</span></span>|<span data-ttu-id="a2f45-116">1</span><span class="sxs-lookup"><span data-stu-id="a2f45-116">1</span></span>|<span data-ttu-id="a2f45-117">No está disponible</span><span class="sxs-lookup"><span data-stu-id="a2f45-117">Not Available</span></span>|
|<span data-ttu-id="a2f45-118">requiredInstall</span><span class="sxs-lookup"><span data-stu-id="a2f45-118">requiredInstall</span></span>|<span data-ttu-id="a2f45-119">2</span><span class="sxs-lookup"><span data-stu-id="a2f45-119">2</span></span>|<span data-ttu-id="a2f45-120">Instalación necesarios</span><span class="sxs-lookup"><span data-stu-id="a2f45-120">Required Install</span></span>|
|<span data-ttu-id="a2f45-121">requiredUninstall</span><span class="sxs-lookup"><span data-stu-id="a2f45-121">requiredUninstall</span></span>|<span data-ttu-id="a2f45-122">3</span><span class="sxs-lookup"><span data-stu-id="a2f45-122">3</span></span>|<span data-ttu-id="a2f45-123">Desinstalar necesarios</span><span class="sxs-lookup"><span data-stu-id="a2f45-123">Required Uninstall</span></span>|
|<span data-ttu-id="a2f45-124">requiredAndAvailableInstall</span><span class="sxs-lookup"><span data-stu-id="a2f45-124">requiredAndAvailableInstall</span></span>|<span data-ttu-id="a2f45-125">4</span><span class="sxs-lookup"><span data-stu-id="a2f45-125">4</span></span>|<span data-ttu-id="a2f45-126">RequiredAndAvailableInstall</span><span class="sxs-lookup"><span data-stu-id="a2f45-126">RequiredAndAvailableInstall</span></span>|
|<span data-ttu-id="a2f45-127">availableInstallWithoutEnrollment</span><span class="sxs-lookup"><span data-stu-id="a2f45-127">availableInstallWithoutEnrollment</span></span>|<span data-ttu-id="a2f45-128">5</span><span class="sxs-lookup"><span data-stu-id="a2f45-128">5</span></span>|<span data-ttu-id="a2f45-129">AvailableInstallWithoutEnrollment</span><span class="sxs-lookup"><span data-stu-id="a2f45-129">AvailableInstallWithoutEnrollment</span></span>|
|<span data-ttu-id="a2f45-130">excluir</span><span class="sxs-lookup"><span data-stu-id="a2f45-130">exclude</span></span>|<span data-ttu-id="a2f45-131">6</span><span class="sxs-lookup"><span data-stu-id="a2f45-131">6</span></span>|<span data-ttu-id="a2f45-132">Excluir</span><span class="sxs-lookup"><span data-stu-id="a2f45-132">Exclude</span></span>|





