---
title: tipo de enumeración embeddedSIMDeviceStateValue
description: Describe los diferentes Estados de un código de activación de SIM incrustado.
ms.openlocfilehash: c0b1cffedcae18dab4c1d23a2691cafa8709c0ff
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084257"
---
# <a name="embeddedsimdevicestatevalue-enum-type"></a><span data-ttu-id="e6f8d-103">tipo de enumeración embeddedSIMDeviceStateValue</span><span class="sxs-lookup"><span data-stu-id="e6f8d-103">embeddedSIMDeviceStateValue enum type</span></span>

> <span data-ttu-id="e6f8d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e6f8d-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e6f8d-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e6f8d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e6f8d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e6f8d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e6f8d-107">Describe los diferentes Estados de un código de activación de SIM incrustado.</span><span class="sxs-lookup"><span data-stu-id="e6f8d-107">Describes the various states for an embedded SIM activation code.</span></span>
## <a name="members"></a><span data-ttu-id="e6f8d-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="e6f8d-108">Members</span></span>
|<span data-ttu-id="e6f8d-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="e6f8d-109">Member</span></span>|<span data-ttu-id="e6f8d-110">Valor</span><span class="sxs-lookup"><span data-stu-id="e6f8d-110">Value</span></span>|<span data-ttu-id="e6f8d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6f8d-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e6f8d-112">notEvaluated</span><span class="sxs-lookup"><span data-stu-id="e6f8d-112">notEvaluated</span></span>|<span data-ttu-id="e6f8d-113">0</span><span class="sxs-lookup"><span data-stu-id="e6f8d-113">0</span></span>|<span data-ttu-id="e6f8d-114">Designa que el código de activación de SIM incrustado es gratuito y está disponible para ser asignado a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e6f8d-114">Designates that the embedded SIM activation code is free and available to be assigned to a device.</span></span>|
|<span data-ttu-id="e6f8d-115">failed</span><span class="sxs-lookup"><span data-stu-id="e6f8d-115">failed</span></span>|<span data-ttu-id="e6f8d-116">1</span><span class="sxs-lookup"><span data-stu-id="e6f8d-116">1</span></span>|<span data-ttu-id="e6f8d-117">Designa que Intune Service no se pudo entregar este perfil para un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e6f8d-117">Designates that Intune Service failed to deliver this profile to a device.</span></span>|
|<span data-ttu-id="e6f8d-118">instalar</span><span class="sxs-lookup"><span data-stu-id="e6f8d-118">installing</span></span>|<span data-ttu-id="e6f8d-119">2</span><span class="sxs-lookup"><span data-stu-id="e6f8d-119">2</span></span>|<span data-ttu-id="e6f8d-120">Designa que el código de activación de SIM incrustado se ha asignado a un dispositivo y el dispositivo que instala el token.</span><span class="sxs-lookup"><span data-stu-id="e6f8d-120">Designates that the embedded SIM activation code has been assigned to a device and the device is installing the token.</span></span>|
|<span data-ttu-id="e6f8d-121">instalado</span><span class="sxs-lookup"><span data-stu-id="e6f8d-121">installed</span></span>|<span data-ttu-id="e6f8d-122">3</span><span class="sxs-lookup"><span data-stu-id="e6f8d-122">3</span></span>|<span data-ttu-id="e6f8d-123">Designa que el código de activación de SIM incrustado se ha instalado correctamente en el dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="e6f8d-123">Designates that the embedded SIM activation code has been successfully installed on the target device.</span></span>|
|<span data-ttu-id="e6f8d-124">eliminar</span><span class="sxs-lookup"><span data-stu-id="e6f8d-124">deleting</span></span>|<span data-ttu-id="e6f8d-125">4</span><span class="sxs-lookup"><span data-stu-id="e6f8d-125">4</span></span>|<span data-ttu-id="e6f8d-126">Designa Intune Service está intentando eliminar el perfil desde el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e6f8d-126">Designates that Intune Service is trying to delete the profile from the device.</span></span>|
|<span data-ttu-id="e6f8d-127">error</span><span class="sxs-lookup"><span data-stu-id="e6f8d-127">error</span></span>|<span data-ttu-id="e6f8d-128">5</span><span class="sxs-lookup"><span data-stu-id="e6f8d-128">5</span></span>|<span data-ttu-id="e6f8d-129">Designa que hay error con este perfil.</span><span class="sxs-lookup"><span data-stu-id="e6f8d-129">Designates that there is error with this profile.</span></span>|
|<span data-ttu-id="e6f8d-130">deleted</span><span class="sxs-lookup"><span data-stu-id="e6f8d-130">deleted</span></span>|<span data-ttu-id="e6f8d-131">6</span><span class="sxs-lookup"><span data-stu-id="e6f8d-131">6</span></span>|<span data-ttu-id="e6f8d-132">Designa que se ha eliminado el perfil desde el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e6f8d-132">Designates that the profile is deleted from the device.</span></span>|
|<span data-ttu-id="e6f8d-133">removedByUser</span><span class="sxs-lookup"><span data-stu-id="e6f8d-133">removedByUser</span></span>|<span data-ttu-id="e6f8d-134">7</span><span class="sxs-lookup"><span data-stu-id="e6f8d-134">7</span></span>|<span data-ttu-id="e6f8d-135">Designa que el usuario quite el perfil desde el dispositivo</span><span class="sxs-lookup"><span data-stu-id="e6f8d-135">Designates that the profile is removed from the device by the user</span></span>|





