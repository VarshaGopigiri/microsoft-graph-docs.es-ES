---
title: tipo de enumeración managedAppDataEncryptionType
description: Representa el nivel a la que se cifran los datos de aplicación para las aplicaciones administradas
ms.openlocfilehash: 7efda037bc2b4d5794c575823845c0955be46477
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031431"
---
# <a name="managedappdataencryptiontype-enum-type"></a><span data-ttu-id="29c83-103">tipo de enumeración managedAppDataEncryptionType</span><span class="sxs-lookup"><span data-stu-id="29c83-103">managedAppDataEncryptionType enum type</span></span>

> <span data-ttu-id="29c83-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="29c83-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="29c83-105">Representa el nivel a la que se cifran los datos de aplicación para las aplicaciones administradas</span><span class="sxs-lookup"><span data-stu-id="29c83-105">Represents the level to which app data is encrypted for managed apps</span></span>
## <a name="members"></a><span data-ttu-id="29c83-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="29c83-106">Members</span></span>
|<span data-ttu-id="29c83-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="29c83-107">Member</span></span>|<span data-ttu-id="29c83-108">Valor</span><span class="sxs-lookup"><span data-stu-id="29c83-108">Value</span></span>|<span data-ttu-id="29c83-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="29c83-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="29c83-110">useDeviceSettings</span><span class="sxs-lookup"><span data-stu-id="29c83-110">useDeviceSettings</span></span>|<span data-ttu-id="29c83-111">0</span><span class="sxs-lookup"><span data-stu-id="29c83-111">0</span></span>|<span data-ttu-id="29c83-112">Datos de aplicación se cifran en función de la configuración predeterminada en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="29c83-112">App data is encrypted based on the default settings on the device.</span></span>|
|<span data-ttu-id="29c83-113">afterDeviceRestart</span><span class="sxs-lookup"><span data-stu-id="29c83-113">afterDeviceRestart</span></span>|<span data-ttu-id="29c83-114">1</span><span class="sxs-lookup"><span data-stu-id="29c83-114">1</span></span>|<span data-ttu-id="29c83-115">Datos de aplicación se cifran cuando se reinicia el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="29c83-115">App data is encrypted when the device is restarted.</span></span>|
|<span data-ttu-id="29c83-116">whenDeviceLockedExceptOpenFiles</span><span class="sxs-lookup"><span data-stu-id="29c83-116">whenDeviceLockedExceptOpenFiles</span></span>|<span data-ttu-id="29c83-117">2</span><span class="sxs-lookup"><span data-stu-id="29c83-117">2</span></span>|<span data-ttu-id="29c83-118">Datos de aplicación asociados con esta directiva se cifran cuando el dispositivo está bloqueado, excepto los datos de los archivos que están abiertos</span><span class="sxs-lookup"><span data-stu-id="29c83-118">App data associated with this policy is encrypted when the device is locked, except data in files that are open</span></span>|
|<span data-ttu-id="29c83-119">whenDeviceLocked</span><span class="sxs-lookup"><span data-stu-id="29c83-119">whenDeviceLocked</span></span>|<span data-ttu-id="29c83-120">3</span><span class="sxs-lookup"><span data-stu-id="29c83-120">3</span></span>|<span data-ttu-id="29c83-121">Datos de aplicación asociados con esta directiva se cifran cuando el dispositivo está bloqueado</span><span class="sxs-lookup"><span data-stu-id="29c83-121">App data associated with this policy is encrypted when the device is locked</span></span>|



