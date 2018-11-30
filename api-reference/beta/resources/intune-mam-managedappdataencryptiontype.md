---
title: tipo de enumeración managedAppDataEncryptionType
description: Representa el nivel a la que se cifran los datos de aplicación para las aplicaciones administradas
ms.openlocfilehash: a642a3efc01f719ca72134f737fe2bdd2596d2b9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089084"
---
# <a name="managedappdataencryptiontype-enum-type"></a><span data-ttu-id="6bdf9-103">tipo de enumeración managedAppDataEncryptionType</span><span class="sxs-lookup"><span data-stu-id="6bdf9-103">managedAppDataEncryptionType enum type</span></span>

> <span data-ttu-id="6bdf9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6bdf9-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6bdf9-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6bdf9-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6bdf9-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6bdf9-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6bdf9-107">Representa el nivel a la que se cifran los datos de aplicación para las aplicaciones administradas</span><span class="sxs-lookup"><span data-stu-id="6bdf9-107">Represents the level to which app data is encrypted for managed apps</span></span>
## <a name="members"></a><span data-ttu-id="6bdf9-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="6bdf9-108">Members</span></span>
|<span data-ttu-id="6bdf9-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="6bdf9-109">Member</span></span>|<span data-ttu-id="6bdf9-110">Valor</span><span class="sxs-lookup"><span data-stu-id="6bdf9-110">Value</span></span>|<span data-ttu-id="6bdf9-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="6bdf9-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6bdf9-112">useDeviceSettings</span><span class="sxs-lookup"><span data-stu-id="6bdf9-112">useDeviceSettings</span></span>|<span data-ttu-id="6bdf9-113">0</span><span class="sxs-lookup"><span data-stu-id="6bdf9-113">0</span></span>|<span data-ttu-id="6bdf9-114">Datos de aplicación se cifran en función de la configuración predeterminada en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6bdf9-114">App data is encrypted based on the default settings on the device.</span></span>|
|<span data-ttu-id="6bdf9-115">afterDeviceRestart</span><span class="sxs-lookup"><span data-stu-id="6bdf9-115">afterDeviceRestart</span></span>|<span data-ttu-id="6bdf9-116">1</span><span class="sxs-lookup"><span data-stu-id="6bdf9-116">1</span></span>|<span data-ttu-id="6bdf9-117">Datos de aplicación se cifran cuando se reinicia el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6bdf9-117">App data is encrypted when the device is restarted.</span></span>|
|<span data-ttu-id="6bdf9-118">whenDeviceLockedExceptOpenFiles</span><span class="sxs-lookup"><span data-stu-id="6bdf9-118">whenDeviceLockedExceptOpenFiles</span></span>|<span data-ttu-id="6bdf9-119">2</span><span class="sxs-lookup"><span data-stu-id="6bdf9-119">2</span></span>|<span data-ttu-id="6bdf9-120">Datos de aplicación asociados con esta directiva se cifran cuando el dispositivo está bloqueado, excepto los datos de los archivos que están abiertos</span><span class="sxs-lookup"><span data-stu-id="6bdf9-120">App data associated with this policy is encrypted when the device is locked, except data in files that are open</span></span>|
|<span data-ttu-id="6bdf9-121">whenDeviceLocked</span><span class="sxs-lookup"><span data-stu-id="6bdf9-121">whenDeviceLocked</span></span>|<span data-ttu-id="6bdf9-122">3</span><span class="sxs-lookup"><span data-stu-id="6bdf9-122">3</span></span>|<span data-ttu-id="6bdf9-123">Datos de aplicación asociados con esta directiva se cifran cuando el dispositivo está bloqueado</span><span class="sxs-lookup"><span data-stu-id="6bdf9-123">App data associated with this policy is encrypted when the device is locked</span></span>|





