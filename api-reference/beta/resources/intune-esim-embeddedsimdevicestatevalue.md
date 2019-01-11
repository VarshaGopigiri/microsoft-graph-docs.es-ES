---
title: tipo de enumeración embeddedSIMDeviceStateValue
description: Describe los diferentes Estados de un código de activación de SIM incrustado.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: a3974c0df65ef9f59242f390b7166e11c3e0c592
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27886061"
---
# <a name="embeddedsimdevicestatevalue-enum-type"></a><span data-ttu-id="40630-103">tipo de enumeración embeddedSIMDeviceStateValue</span><span class="sxs-lookup"><span data-stu-id="40630-103">embeddedSIMDeviceStateValue enum type</span></span>

> <span data-ttu-id="40630-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="40630-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="40630-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="40630-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="40630-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="40630-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="40630-107">Describe los diferentes Estados de un código de activación de SIM incrustado.</span><span class="sxs-lookup"><span data-stu-id="40630-107">Describes the various states for an embedded SIM activation code.</span></span>
## <a name="members"></a><span data-ttu-id="40630-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="40630-108">Members</span></span>
|<span data-ttu-id="40630-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="40630-109">Member</span></span>|<span data-ttu-id="40630-110">Valor</span><span class="sxs-lookup"><span data-stu-id="40630-110">Value</span></span>|<span data-ttu-id="40630-111">Description</span><span class="sxs-lookup"><span data-stu-id="40630-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="40630-112">notEvaluated</span><span class="sxs-lookup"><span data-stu-id="40630-112">notEvaluated</span></span>|<span data-ttu-id="40630-113">0</span><span class="sxs-lookup"><span data-stu-id="40630-113">0</span></span>|<span data-ttu-id="40630-114">Designa que el código de activación de SIM incrustado es gratuito y está disponible para ser asignado a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="40630-114">Designates that the embedded SIM activation code is free and available to be assigned to a device.</span></span>|
|<span data-ttu-id="40630-115">failed</span><span class="sxs-lookup"><span data-stu-id="40630-115">failed</span></span>|<span data-ttu-id="40630-116">1</span><span class="sxs-lookup"><span data-stu-id="40630-116">1</span></span>|<span data-ttu-id="40630-117">Designa que Intune Service no se pudo entregar este perfil para un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="40630-117">Designates that Intune Service failed to deliver this profile to a device.</span></span>|
|<span data-ttu-id="40630-118">instalar</span><span class="sxs-lookup"><span data-stu-id="40630-118">installing</span></span>|<span data-ttu-id="40630-119">2</span><span class="sxs-lookup"><span data-stu-id="40630-119">2</span></span>|<span data-ttu-id="40630-120">Designa que el código de activación de SIM incrustado se ha asignado a un dispositivo y el dispositivo que instala el token.</span><span class="sxs-lookup"><span data-stu-id="40630-120">Designates that the embedded SIM activation code has been assigned to a device and the device is installing the token.</span></span>|
|<span data-ttu-id="40630-121">instalado</span><span class="sxs-lookup"><span data-stu-id="40630-121">installed</span></span>|<span data-ttu-id="40630-122">3</span><span class="sxs-lookup"><span data-stu-id="40630-122">3</span></span>|<span data-ttu-id="40630-123">Designa que el código de activación de SIM incrustado se ha instalado correctamente en el dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="40630-123">Designates that the embedded SIM activation code has been successfully installed on the target device.</span></span>|
|<span data-ttu-id="40630-124">eliminar</span><span class="sxs-lookup"><span data-stu-id="40630-124">deleting</span></span>|<span data-ttu-id="40630-125">4</span><span class="sxs-lookup"><span data-stu-id="40630-125">4</span></span>|<span data-ttu-id="40630-126">Designa Intune Service está intentando eliminar el perfil desde el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="40630-126">Designates that Intune Service is trying to delete the profile from the device.</span></span>|
|<span data-ttu-id="40630-127">error</span><span class="sxs-lookup"><span data-stu-id="40630-127">error</span></span>|<span data-ttu-id="40630-128">5</span><span class="sxs-lookup"><span data-stu-id="40630-128">5</span></span>|<span data-ttu-id="40630-129">Designa que hay error con este perfil.</span><span class="sxs-lookup"><span data-stu-id="40630-129">Designates that there is error with this profile.</span></span>|
|<span data-ttu-id="40630-130">deleted</span><span class="sxs-lookup"><span data-stu-id="40630-130">deleted</span></span>|<span data-ttu-id="40630-131">6</span><span class="sxs-lookup"><span data-stu-id="40630-131">6</span></span>|<span data-ttu-id="40630-132">Designa que se ha eliminado el perfil desde el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="40630-132">Designates that the profile is deleted from the device.</span></span>|
|<span data-ttu-id="40630-133">removedByUser</span><span class="sxs-lookup"><span data-stu-id="40630-133">removedByUser</span></span>|<span data-ttu-id="40630-134">7</span><span class="sxs-lookup"><span data-stu-id="40630-134">7</span></span>|<span data-ttu-id="40630-135">Designa que el usuario quite el perfil desde el dispositivo</span><span class="sxs-lookup"><span data-stu-id="40630-135">Designates that the profile is removed from the device by the user</span></span>|





