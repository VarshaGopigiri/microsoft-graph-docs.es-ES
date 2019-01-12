---
title: tipo de enumeración managedAppDataEncryptionType
description: Representa el nivel a la que se cifran los datos de aplicación para las aplicaciones administradas
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 4417d488a1590f8d8e9c40e13118e6ef0dc044d1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27944435"
---
# <a name="managedappdataencryptiontype-enum-type"></a><span data-ttu-id="99aec-103">tipo de enumeración managedAppDataEncryptionType</span><span class="sxs-lookup"><span data-stu-id="99aec-103">managedAppDataEncryptionType enum type</span></span>

> <span data-ttu-id="99aec-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="99aec-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="99aec-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="99aec-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="99aec-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="99aec-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="99aec-107">Representa el nivel a la que se cifran los datos de aplicación para las aplicaciones administradas</span><span class="sxs-lookup"><span data-stu-id="99aec-107">Represents the level to which app data is encrypted for managed apps</span></span>
## <a name="members"></a><span data-ttu-id="99aec-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="99aec-108">Members</span></span>
|<span data-ttu-id="99aec-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="99aec-109">Member</span></span>|<span data-ttu-id="99aec-110">Valor</span><span class="sxs-lookup"><span data-stu-id="99aec-110">Value</span></span>|<span data-ttu-id="99aec-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="99aec-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="99aec-112">useDeviceSettings</span><span class="sxs-lookup"><span data-stu-id="99aec-112">useDeviceSettings</span></span>|<span data-ttu-id="99aec-113">0</span><span class="sxs-lookup"><span data-stu-id="99aec-113">0</span></span>|<span data-ttu-id="99aec-114">Datos de aplicación se cifran en función de la configuración predeterminada en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="99aec-114">App data is encrypted based on the default settings on the device.</span></span>|
|<span data-ttu-id="99aec-115">afterDeviceRestart</span><span class="sxs-lookup"><span data-stu-id="99aec-115">afterDeviceRestart</span></span>|<span data-ttu-id="99aec-116">1</span><span class="sxs-lookup"><span data-stu-id="99aec-116">1</span></span>|<span data-ttu-id="99aec-117">Datos de aplicación se cifran cuando se reinicia el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="99aec-117">App data is encrypted when the device is restarted.</span></span>|
|<span data-ttu-id="99aec-118">whenDeviceLockedExceptOpenFiles</span><span class="sxs-lookup"><span data-stu-id="99aec-118">whenDeviceLockedExceptOpenFiles</span></span>|<span data-ttu-id="99aec-119">2</span><span class="sxs-lookup"><span data-stu-id="99aec-119">2</span></span>|<span data-ttu-id="99aec-120">Datos de aplicación asociados con esta directiva se cifran cuando el dispositivo está bloqueado, excepto los datos de los archivos que están abiertos</span><span class="sxs-lookup"><span data-stu-id="99aec-120">App data associated with this policy is encrypted when the device is locked, except data in files that are open</span></span>|
|<span data-ttu-id="99aec-121">whenDeviceLocked</span><span class="sxs-lookup"><span data-stu-id="99aec-121">whenDeviceLocked</span></span>|<span data-ttu-id="99aec-122">3</span><span class="sxs-lookup"><span data-stu-id="99aec-122">3</span></span>|<span data-ttu-id="99aec-123">Datos de aplicación asociados con esta directiva se cifran cuando el dispositivo está bloqueado</span><span class="sxs-lookup"><span data-stu-id="99aec-123">App data associated with this policy is encrypted when the device is locked</span></span>|





