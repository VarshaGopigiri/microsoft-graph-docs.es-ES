---
title: tipo de enumeración automaticUpdateMode
description: Valores posibles para el modo de actualización automática.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 08389dca4379b6fc0222068545ebb9bed250ba94
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27863416"
---
# <a name="automaticupdatemode-enum-type"></a><span data-ttu-id="27f08-103">tipo de enumeración automaticUpdateMode</span><span class="sxs-lookup"><span data-stu-id="27f08-103">automaticUpdateMode enum type</span></span>

> <span data-ttu-id="27f08-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="27f08-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="27f08-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="27f08-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="27f08-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="27f08-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="27f08-107">Valores posibles para el modo de actualización automática.</span><span class="sxs-lookup"><span data-stu-id="27f08-107">Possible values for automatic update mode.</span></span>
## <a name="members"></a><span data-ttu-id="27f08-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="27f08-108">Members</span></span>
|<span data-ttu-id="27f08-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="27f08-109">Member</span></span>|<span data-ttu-id="27f08-110">Valor</span><span class="sxs-lookup"><span data-stu-id="27f08-110">Value</span></span>|<span data-ttu-id="27f08-111">Description</span><span class="sxs-lookup"><span data-stu-id="27f08-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="27f08-112">userDefined</span><span class="sxs-lookup"><span data-stu-id="27f08-112">userDefined</span></span>|<span data-ttu-id="27f08-113">0</span><span class="sxs-lookup"><span data-stu-id="27f08-113">0</span></span>|<span data-ttu-id="27f08-114">Definido por el usuario, valor predeterminado, sin intención.</span><span class="sxs-lookup"><span data-stu-id="27f08-114">User Defined, default value, no intent.</span></span>|
|<span data-ttu-id="27f08-115">notifyDownload</span><span class="sxs-lookup"><span data-stu-id="27f08-115">notifyDownload</span></span>|<span data-ttu-id="27f08-116">1</span><span class="sxs-lookup"><span data-stu-id="27f08-116">1</span></span>|<span data-ttu-id="27f08-117">Notificar al descargarlos.</span><span class="sxs-lookup"><span data-stu-id="27f08-117">Notify on download.</span></span>|
|<span data-ttu-id="27f08-118">autoInstallAtMaintenanceTime</span><span class="sxs-lookup"><span data-stu-id="27f08-118">autoInstallAtMaintenanceTime</span></span>|<span data-ttu-id="27f08-119">2</span><span class="sxs-lookup"><span data-stu-id="27f08-119">2</span></span>|<span data-ttu-id="27f08-120">Instalación automática en tiempo de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="27f08-120">Auto-install at maintenance time.</span></span>|
|<span data-ttu-id="27f08-121">autoInstallAndRebootAtMaintenanceTime</span><span class="sxs-lookup"><span data-stu-id="27f08-121">autoInstallAndRebootAtMaintenanceTime</span></span>|<span data-ttu-id="27f08-122">3</span><span class="sxs-lookup"><span data-stu-id="27f08-122">3</span></span>|<span data-ttu-id="27f08-123">La instalación automática y reinicie el equipo en el momento de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="27f08-123">Auto-install and reboot at maintenance time.</span></span>|
|<span data-ttu-id="27f08-124">autoInstallAndRebootAtScheduledTime</span><span class="sxs-lookup"><span data-stu-id="27f08-124">autoInstallAndRebootAtScheduledTime</span></span>|<span data-ttu-id="27f08-125">4</span><span class="sxs-lookup"><span data-stu-id="27f08-125">4</span></span>|<span data-ttu-id="27f08-126">La instalación automática y reinicie el equipo en la hora programada.</span><span class="sxs-lookup"><span data-stu-id="27f08-126">Auto-install and reboot at scheduled time.</span></span>|
|<span data-ttu-id="27f08-127">autoInstallAndRebootWithoutEndUserControl</span><span class="sxs-lookup"><span data-stu-id="27f08-127">autoInstallAndRebootWithoutEndUserControl</span></span>|<span data-ttu-id="27f08-128">5</span><span class="sxs-lookup"><span data-stu-id="27f08-128">5</span></span>|<span data-ttu-id="27f08-129">La instalación automática y reiniciar sin control de usuario final</span><span class="sxs-lookup"><span data-stu-id="27f08-129">Auto-install and restart without end-user control</span></span>|





