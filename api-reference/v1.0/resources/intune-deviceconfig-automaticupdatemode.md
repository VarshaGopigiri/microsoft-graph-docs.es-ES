---
title: tipo de enumeración automaticUpdateMode
description: Valores posibles para el modo de actualización automática.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a31c50b5d16f4b9be8db4f95f2bbd9bd0ca123e4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27987863"
---
# <a name="automaticupdatemode-enum-type"></a><span data-ttu-id="db686-103">tipo de enumeración automaticUpdateMode</span><span class="sxs-lookup"><span data-stu-id="db686-103">automaticUpdateMode enum type</span></span>

> <span data-ttu-id="db686-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="db686-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="db686-105">Valores posibles para el modo de actualización automática.</span><span class="sxs-lookup"><span data-stu-id="db686-105">Possible values for automatic update mode.</span></span>
## <a name="members"></a><span data-ttu-id="db686-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="db686-106">Members</span></span>
|<span data-ttu-id="db686-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="db686-107">Member</span></span>|<span data-ttu-id="db686-108">Valor</span><span class="sxs-lookup"><span data-stu-id="db686-108">Value</span></span>|<span data-ttu-id="db686-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="db686-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="db686-110">userDefined</span><span class="sxs-lookup"><span data-stu-id="db686-110">userDefined</span></span>|<span data-ttu-id="db686-111">0</span><span class="sxs-lookup"><span data-stu-id="db686-111">0</span></span>|<span data-ttu-id="db686-112">Definido por el usuario, valor predeterminado, sin intención.</span><span class="sxs-lookup"><span data-stu-id="db686-112">User Defined, default value, no intent.</span></span>|
|<span data-ttu-id="db686-113">notifyDownload</span><span class="sxs-lookup"><span data-stu-id="db686-113">notifyDownload</span></span>|<span data-ttu-id="db686-114">1</span><span class="sxs-lookup"><span data-stu-id="db686-114">1</span></span>|<span data-ttu-id="db686-115">Notificar al descargarlos.</span><span class="sxs-lookup"><span data-stu-id="db686-115">Notify on download.</span></span>|
|<span data-ttu-id="db686-116">autoInstallAtMaintenanceTime</span><span class="sxs-lookup"><span data-stu-id="db686-116">autoInstallAtMaintenanceTime</span></span>|<span data-ttu-id="db686-117">2</span><span class="sxs-lookup"><span data-stu-id="db686-117">2</span></span>|<span data-ttu-id="db686-118">Instalación automática en tiempo de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="db686-118">Auto-install at maintenance time.</span></span>|
|<span data-ttu-id="db686-119">autoInstallAndRebootAtMaintenanceTime</span><span class="sxs-lookup"><span data-stu-id="db686-119">autoInstallAndRebootAtMaintenanceTime</span></span>|<span data-ttu-id="db686-120">3</span><span class="sxs-lookup"><span data-stu-id="db686-120">3</span></span>|<span data-ttu-id="db686-121">La instalación automática y reinicie el equipo en el momento de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="db686-121">Auto-install and reboot at maintenance time.</span></span>|
|<span data-ttu-id="db686-122">autoInstallAndRebootAtScheduledTime</span><span class="sxs-lookup"><span data-stu-id="db686-122">autoInstallAndRebootAtScheduledTime</span></span>|<span data-ttu-id="db686-123">4</span><span class="sxs-lookup"><span data-stu-id="db686-123">4</span></span>|<span data-ttu-id="db686-124">La instalación automática y reinicie el equipo en la hora programada.</span><span class="sxs-lookup"><span data-stu-id="db686-124">Auto-install and reboot at scheduled time.</span></span>|
|<span data-ttu-id="db686-125">autoInstallAndRebootWithoutEndUserControl</span><span class="sxs-lookup"><span data-stu-id="db686-125">autoInstallAndRebootWithoutEndUserControl</span></span>|<span data-ttu-id="db686-126">5</span><span class="sxs-lookup"><span data-stu-id="db686-126">5</span></span>|<span data-ttu-id="db686-127">La instalación automática y reiniciar sin control de usuario final</span><span class="sxs-lookup"><span data-stu-id="db686-127">Auto-install and restart without end-user control</span></span>|



