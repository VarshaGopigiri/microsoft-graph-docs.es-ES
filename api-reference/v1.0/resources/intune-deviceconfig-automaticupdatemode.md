---
title: tipo de enumeración automaticUpdateMode
description: Valores posibles para el modo de actualización automática.
ms.openlocfilehash: c98927e1c1f66e3bf10fa07496aa54ac91bad20b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029047"
---
# <a name="automaticupdatemode-enum-type"></a><span data-ttu-id="0f30c-103">tipo de enumeración automaticUpdateMode</span><span class="sxs-lookup"><span data-stu-id="0f30c-103">automaticUpdateMode enum type</span></span>

> <span data-ttu-id="0f30c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0f30c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0f30c-105">Valores posibles para el modo de actualización automática.</span><span class="sxs-lookup"><span data-stu-id="0f30c-105">Possible values for automatic update mode.</span></span>
## <a name="members"></a><span data-ttu-id="0f30c-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="0f30c-106">Members</span></span>
|<span data-ttu-id="0f30c-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="0f30c-107">Member</span></span>|<span data-ttu-id="0f30c-108">Valor</span><span class="sxs-lookup"><span data-stu-id="0f30c-108">Value</span></span>|<span data-ttu-id="0f30c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f30c-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0f30c-110">userDefined</span><span class="sxs-lookup"><span data-stu-id="0f30c-110">userDefined</span></span>|<span data-ttu-id="0f30c-111">0</span><span class="sxs-lookup"><span data-stu-id="0f30c-111">0</span></span>|<span data-ttu-id="0f30c-112">Definido por el usuario, valor predeterminado, sin intención.</span><span class="sxs-lookup"><span data-stu-id="0f30c-112">User Defined, default value, no intent.</span></span>|
|<span data-ttu-id="0f30c-113">notifyDownload</span><span class="sxs-lookup"><span data-stu-id="0f30c-113">notifyDownload</span></span>|<span data-ttu-id="0f30c-114">1</span><span class="sxs-lookup"><span data-stu-id="0f30c-114">1</span></span>|<span data-ttu-id="0f30c-115">Notificar al descargarlos.</span><span class="sxs-lookup"><span data-stu-id="0f30c-115">Notify on download.</span></span>|
|<span data-ttu-id="0f30c-116">autoInstallAtMaintenanceTime</span><span class="sxs-lookup"><span data-stu-id="0f30c-116">autoInstallAtMaintenanceTime</span></span>|<span data-ttu-id="0f30c-117">2</span><span class="sxs-lookup"><span data-stu-id="0f30c-117">2</span></span>|<span data-ttu-id="0f30c-118">Instalación automática en tiempo de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="0f30c-118">Auto-install at maintenance time.</span></span>|
|<span data-ttu-id="0f30c-119">autoInstallAndRebootAtMaintenanceTime</span><span class="sxs-lookup"><span data-stu-id="0f30c-119">autoInstallAndRebootAtMaintenanceTime</span></span>|<span data-ttu-id="0f30c-120">3</span><span class="sxs-lookup"><span data-stu-id="0f30c-120">3</span></span>|<span data-ttu-id="0f30c-121">La instalación automática y reinicie el equipo en el momento de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="0f30c-121">Auto-install and reboot at maintenance time.</span></span>|
|<span data-ttu-id="0f30c-122">autoInstallAndRebootAtScheduledTime</span><span class="sxs-lookup"><span data-stu-id="0f30c-122">autoInstallAndRebootAtScheduledTime</span></span>|<span data-ttu-id="0f30c-123">4</span><span class="sxs-lookup"><span data-stu-id="0f30c-123">4</span></span>|<span data-ttu-id="0f30c-124">La instalación automática y reinicie el equipo en la hora programada.</span><span class="sxs-lookup"><span data-stu-id="0f30c-124">Auto-install and reboot at scheduled time.</span></span>|
|<span data-ttu-id="0f30c-125">autoInstallAndRebootWithoutEndUserControl</span><span class="sxs-lookup"><span data-stu-id="0f30c-125">autoInstallAndRebootWithoutEndUserControl</span></span>|<span data-ttu-id="0f30c-126">5</span><span class="sxs-lookup"><span data-stu-id="0f30c-126">5</span></span>|<span data-ttu-id="0f30c-127">La instalación automática y reiniciar sin control de usuario final</span><span class="sxs-lookup"><span data-stu-id="0f30c-127">Auto-install and restart without end-user control</span></span>|



