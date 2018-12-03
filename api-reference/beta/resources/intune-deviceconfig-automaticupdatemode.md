---
title: tipo de enumeración automaticUpdateMode
description: Valores posibles para el modo de actualización automática.
ms.openlocfilehash: b7eac8337d6c8286e538bbe98b5ecbc13a448628
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088921"
---
# <a name="automaticupdatemode-enum-type"></a><span data-ttu-id="4531b-103">tipo de enumeración automaticUpdateMode</span><span class="sxs-lookup"><span data-stu-id="4531b-103">automaticUpdateMode enum type</span></span>

> <span data-ttu-id="4531b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4531b-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4531b-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4531b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="4531b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4531b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4531b-107">Valores posibles para el modo de actualización automática.</span><span class="sxs-lookup"><span data-stu-id="4531b-107">Possible values for automatic update mode.</span></span>
## <a name="members"></a><span data-ttu-id="4531b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="4531b-108">Members</span></span>
|<span data-ttu-id="4531b-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="4531b-109">Member</span></span>|<span data-ttu-id="4531b-110">Valor</span><span class="sxs-lookup"><span data-stu-id="4531b-110">Value</span></span>|<span data-ttu-id="4531b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="4531b-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4531b-112">userDefined</span><span class="sxs-lookup"><span data-stu-id="4531b-112">userDefined</span></span>|<span data-ttu-id="4531b-113">0</span><span class="sxs-lookup"><span data-stu-id="4531b-113">0</span></span>|<span data-ttu-id="4531b-114">Definido por el usuario, valor predeterminado, sin intención.</span><span class="sxs-lookup"><span data-stu-id="4531b-114">User Defined, default value, no intent.</span></span>|
|<span data-ttu-id="4531b-115">notifyDownload</span><span class="sxs-lookup"><span data-stu-id="4531b-115">notifyDownload</span></span>|<span data-ttu-id="4531b-116">1</span><span class="sxs-lookup"><span data-stu-id="4531b-116">1</span></span>|<span data-ttu-id="4531b-117">Notificar al descargarlos.</span><span class="sxs-lookup"><span data-stu-id="4531b-117">Notify on download.</span></span>|
|<span data-ttu-id="4531b-118">autoInstallAtMaintenanceTime</span><span class="sxs-lookup"><span data-stu-id="4531b-118">autoInstallAtMaintenanceTime</span></span>|<span data-ttu-id="4531b-119">2</span><span class="sxs-lookup"><span data-stu-id="4531b-119">2</span></span>|<span data-ttu-id="4531b-120">Instalación automática en tiempo de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="4531b-120">Auto-install at maintenance time.</span></span>|
|<span data-ttu-id="4531b-121">autoInstallAndRebootAtMaintenanceTime</span><span class="sxs-lookup"><span data-stu-id="4531b-121">autoInstallAndRebootAtMaintenanceTime</span></span>|<span data-ttu-id="4531b-122">3</span><span class="sxs-lookup"><span data-stu-id="4531b-122">3</span></span>|<span data-ttu-id="4531b-123">La instalación automática y reinicie el equipo en el momento de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="4531b-123">Auto-install and reboot at maintenance time.</span></span>|
|<span data-ttu-id="4531b-124">autoInstallAndRebootAtScheduledTime</span><span class="sxs-lookup"><span data-stu-id="4531b-124">autoInstallAndRebootAtScheduledTime</span></span>|<span data-ttu-id="4531b-125">4</span><span class="sxs-lookup"><span data-stu-id="4531b-125">4</span></span>|<span data-ttu-id="4531b-126">La instalación automática y reinicie el equipo en la hora programada.</span><span class="sxs-lookup"><span data-stu-id="4531b-126">Auto-install and reboot at scheduled time.</span></span>|
|<span data-ttu-id="4531b-127">autoInstallAndRebootWithoutEndUserControl</span><span class="sxs-lookup"><span data-stu-id="4531b-127">autoInstallAndRebootWithoutEndUserControl</span></span>|<span data-ttu-id="4531b-128">5</span><span class="sxs-lookup"><span data-stu-id="4531b-128">5</span></span>|<span data-ttu-id="4531b-129">La instalación automática y reiniciar sin control de usuario final</span><span class="sxs-lookup"><span data-stu-id="4531b-129">Auto-install and restart without end-user control</span></span>|




