---
title: tipo de enumeración embeddedSIMDeviceStateValue
description: Describe los diferentes Estados de un código de activación de SIM incrustado.
author: tfitzmac
ms.openlocfilehash: 51e550669d9cd29d7d5bb246fe2cba017b02187c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27320597"
---
# <a name="embeddedsimdevicestatevalue-enum-type"></a><span data-ttu-id="57d92-103">tipo de enumeración embeddedSIMDeviceStateValue</span><span class="sxs-lookup"><span data-stu-id="57d92-103">embeddedSIMDeviceStateValue enum type</span></span>

> <span data-ttu-id="57d92-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="57d92-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="57d92-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="57d92-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="57d92-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="57d92-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="57d92-107">Describe los diferentes Estados de un código de activación de SIM incrustado.</span><span class="sxs-lookup"><span data-stu-id="57d92-107">Describes the various states for an embedded SIM activation code.</span></span>
## <a name="members"></a><span data-ttu-id="57d92-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="57d92-108">Members</span></span>
|<span data-ttu-id="57d92-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="57d92-109">Member</span></span>|<span data-ttu-id="57d92-110">Valor</span><span class="sxs-lookup"><span data-stu-id="57d92-110">Value</span></span>|<span data-ttu-id="57d92-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="57d92-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="57d92-112">notEvaluated</span><span class="sxs-lookup"><span data-stu-id="57d92-112">notEvaluated</span></span>|<span data-ttu-id="57d92-113">0</span><span class="sxs-lookup"><span data-stu-id="57d92-113">0</span></span>|<span data-ttu-id="57d92-114">Designa que el código de activación de SIM incrustado es gratuito y está disponible para ser asignado a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="57d92-114">Designates that the embedded SIM activation code is free and available to be assigned to a device.</span></span>|
|<span data-ttu-id="57d92-115">failed</span><span class="sxs-lookup"><span data-stu-id="57d92-115">failed</span></span>|<span data-ttu-id="57d92-116">1</span><span class="sxs-lookup"><span data-stu-id="57d92-116">1</span></span>|<span data-ttu-id="57d92-117">Designa que Intune Service no se pudo entregar este perfil para un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="57d92-117">Designates that Intune Service failed to deliver this profile to a device.</span></span>|
|<span data-ttu-id="57d92-118">instalar</span><span class="sxs-lookup"><span data-stu-id="57d92-118">installing</span></span>|<span data-ttu-id="57d92-119">2</span><span class="sxs-lookup"><span data-stu-id="57d92-119">2</span></span>|<span data-ttu-id="57d92-120">Designa que el código de activación de SIM incrustado se ha asignado a un dispositivo y el dispositivo que instala el token.</span><span class="sxs-lookup"><span data-stu-id="57d92-120">Designates that the embedded SIM activation code has been assigned to a device and the device is installing the token.</span></span>|
|<span data-ttu-id="57d92-121">instalado</span><span class="sxs-lookup"><span data-stu-id="57d92-121">installed</span></span>|<span data-ttu-id="57d92-122">3</span><span class="sxs-lookup"><span data-stu-id="57d92-122">3</span></span>|<span data-ttu-id="57d92-123">Designa que el código de activación de SIM incrustado se ha instalado correctamente en el dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="57d92-123">Designates that the embedded SIM activation code has been successfully installed on the target device.</span></span>|
|<span data-ttu-id="57d92-124">eliminar</span><span class="sxs-lookup"><span data-stu-id="57d92-124">deleting</span></span>|<span data-ttu-id="57d92-125">4</span><span class="sxs-lookup"><span data-stu-id="57d92-125">4</span></span>|<span data-ttu-id="57d92-126">Designa Intune Service está intentando eliminar el perfil desde el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="57d92-126">Designates that Intune Service is trying to delete the profile from the device.</span></span>|
|<span data-ttu-id="57d92-127">error</span><span class="sxs-lookup"><span data-stu-id="57d92-127">error</span></span>|<span data-ttu-id="57d92-128">5</span><span class="sxs-lookup"><span data-stu-id="57d92-128">5</span></span>|<span data-ttu-id="57d92-129">Designa que hay error con este perfil.</span><span class="sxs-lookup"><span data-stu-id="57d92-129">Designates that there is error with this profile.</span></span>|
|<span data-ttu-id="57d92-130">deleted</span><span class="sxs-lookup"><span data-stu-id="57d92-130">deleted</span></span>|<span data-ttu-id="57d92-131">6</span><span class="sxs-lookup"><span data-stu-id="57d92-131">6</span></span>|<span data-ttu-id="57d92-132">Designa que se ha eliminado el perfil desde el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="57d92-132">Designates that the profile is deleted from the device.</span></span>|
|<span data-ttu-id="57d92-133">removedByUser</span><span class="sxs-lookup"><span data-stu-id="57d92-133">removedByUser</span></span>|<span data-ttu-id="57d92-134">7</span><span class="sxs-lookup"><span data-stu-id="57d92-134">7</span></span>|<span data-ttu-id="57d92-135">Designa que el usuario quite el perfil desde el dispositivo</span><span class="sxs-lookup"><span data-stu-id="57d92-135">Designates that the profile is removed from the device by the user</span></span>|





