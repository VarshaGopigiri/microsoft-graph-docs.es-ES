---
title: tipo de enumeración automaticUpdateMode
description: Valores posibles para el modo de actualización automática.
author: tfitzmac
ms.openlocfilehash: 01e71e51a47a06aff12dd82e132d7eb468f26229
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27346994"
---
# <a name="automaticupdatemode-enum-type"></a><span data-ttu-id="29699-103">tipo de enumeración automaticUpdateMode</span><span class="sxs-lookup"><span data-stu-id="29699-103">automaticUpdateMode enum type</span></span>

> <span data-ttu-id="29699-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="29699-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="29699-105">Valores posibles para el modo de actualización automática.</span><span class="sxs-lookup"><span data-stu-id="29699-105">Possible values for automatic update mode.</span></span>
## <a name="members"></a><span data-ttu-id="29699-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="29699-106">Members</span></span>
|<span data-ttu-id="29699-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="29699-107">Member</span></span>|<span data-ttu-id="29699-108">Valor</span><span class="sxs-lookup"><span data-stu-id="29699-108">Value</span></span>|<span data-ttu-id="29699-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="29699-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="29699-110">userDefined</span><span class="sxs-lookup"><span data-stu-id="29699-110">userDefined</span></span>|<span data-ttu-id="29699-111">0</span><span class="sxs-lookup"><span data-stu-id="29699-111">0</span></span>|<span data-ttu-id="29699-112">Definido por el usuario, valor predeterminado, sin intención.</span><span class="sxs-lookup"><span data-stu-id="29699-112">User Defined, default value, no intent.</span></span>|
|<span data-ttu-id="29699-113">notifyDownload</span><span class="sxs-lookup"><span data-stu-id="29699-113">notifyDownload</span></span>|<span data-ttu-id="29699-114">1</span><span class="sxs-lookup"><span data-stu-id="29699-114">1</span></span>|<span data-ttu-id="29699-115">Notificar al descargarlos.</span><span class="sxs-lookup"><span data-stu-id="29699-115">Notify on download.</span></span>|
|<span data-ttu-id="29699-116">autoInstallAtMaintenanceTime</span><span class="sxs-lookup"><span data-stu-id="29699-116">autoInstallAtMaintenanceTime</span></span>|<span data-ttu-id="29699-117">2</span><span class="sxs-lookup"><span data-stu-id="29699-117">2</span></span>|<span data-ttu-id="29699-118">Instalación automática en tiempo de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="29699-118">Auto-install at maintenance time.</span></span>|
|<span data-ttu-id="29699-119">autoInstallAndRebootAtMaintenanceTime</span><span class="sxs-lookup"><span data-stu-id="29699-119">autoInstallAndRebootAtMaintenanceTime</span></span>|<span data-ttu-id="29699-120">3</span><span class="sxs-lookup"><span data-stu-id="29699-120">3</span></span>|<span data-ttu-id="29699-121">La instalación automática y reinicie el equipo en el momento de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="29699-121">Auto-install and reboot at maintenance time.</span></span>|
|<span data-ttu-id="29699-122">autoInstallAndRebootAtScheduledTime</span><span class="sxs-lookup"><span data-stu-id="29699-122">autoInstallAndRebootAtScheduledTime</span></span>|<span data-ttu-id="29699-123">4</span><span class="sxs-lookup"><span data-stu-id="29699-123">4</span></span>|<span data-ttu-id="29699-124">La instalación automática y reinicie el equipo en la hora programada.</span><span class="sxs-lookup"><span data-stu-id="29699-124">Auto-install and reboot at scheduled time.</span></span>|
|<span data-ttu-id="29699-125">autoInstallAndRebootWithoutEndUserControl</span><span class="sxs-lookup"><span data-stu-id="29699-125">autoInstallAndRebootWithoutEndUserControl</span></span>|<span data-ttu-id="29699-126">5</span><span class="sxs-lookup"><span data-stu-id="29699-126">5</span></span>|<span data-ttu-id="29699-127">La instalación automática y reiniciar sin control de usuario final</span><span class="sxs-lookup"><span data-stu-id="29699-127">Auto-install and restart without end-user control</span></span>|



