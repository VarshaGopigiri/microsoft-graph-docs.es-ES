---
title: tipo de enumeración deviceManagementExchangeAccessState
description: Estado de acceso de dispositivo de Exchange.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 73559bf01cfc619e38a30b0393a7d7f3a8754321
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27889092"
---
# <a name="devicemanagementexchangeaccessstate-enum-type"></a><span data-ttu-id="b6711-103">tipo de enumeración deviceManagementExchangeAccessState</span><span class="sxs-lookup"><span data-stu-id="b6711-103">deviceManagementExchangeAccessState enum type</span></span>

> <span data-ttu-id="b6711-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b6711-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b6711-105">Estado de acceso de dispositivo de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b6711-105">Device Exchange Access State.</span></span>
## <a name="members"></a><span data-ttu-id="b6711-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="b6711-106">Members</span></span>
|<span data-ttu-id="b6711-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="b6711-107">Member</span></span>|<span data-ttu-id="b6711-108">Valor</span><span class="sxs-lookup"><span data-stu-id="b6711-108">Value</span></span>|<span data-ttu-id="b6711-109">Description</span><span class="sxs-lookup"><span data-stu-id="b6711-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b6711-110">none</span><span class="sxs-lookup"><span data-stu-id="b6711-110">none</span></span>|<span data-ttu-id="b6711-111">0</span><span class="sxs-lookup"><span data-stu-id="b6711-111">0</span></span>|<span data-ttu-id="b6711-112">No hay ningún estado de acceso detectado desde Exchange</span><span class="sxs-lookup"><span data-stu-id="b6711-112">No access state discovered from Exchange</span></span>|
|<span data-ttu-id="b6711-113">desconocido</span><span class="sxs-lookup"><span data-stu-id="b6711-113">unknown</span></span>|<span data-ttu-id="b6711-114">1</span><span class="sxs-lookup"><span data-stu-id="b6711-114">1</span></span>|<span data-ttu-id="b6711-115">Se desconoce el estado de acceso de dispositivo para Exchange</span><span class="sxs-lookup"><span data-stu-id="b6711-115">Device access state to Exchange is unknown</span></span>|
|<span data-ttu-id="b6711-116">permitido</span><span class="sxs-lookup"><span data-stu-id="b6711-116">allowed</span></span>|<span data-ttu-id="b6711-117">2</span><span class="sxs-lookup"><span data-stu-id="b6711-117">2</span></span>|<span data-ttu-id="b6711-118">Dispositivo tiene acceso a Exchange</span><span class="sxs-lookup"><span data-stu-id="b6711-118">Device has access to Exchange</span></span>|
|<span data-ttu-id="b6711-119">bloqueado</span><span class="sxs-lookup"><span data-stu-id="b6711-119">blocked</span></span>|<span data-ttu-id="b6711-120">3</span><span class="sxs-lookup"><span data-stu-id="b6711-120">3</span></span>|<span data-ttu-id="b6711-121">Dispositivo está bloqueado en Exchange</span><span class="sxs-lookup"><span data-stu-id="b6711-121">Device is Blocked in Exchange</span></span>|
|<span data-ttu-id="b6711-122">en cuarentena</span><span class="sxs-lookup"><span data-stu-id="b6711-122">quarantined</span></span>|<span data-ttu-id="b6711-123">4</span><span class="sxs-lookup"><span data-stu-id="b6711-123">4</span></span>|<span data-ttu-id="b6711-124">Dispositivo está en cuarentena en Exchange</span><span class="sxs-lookup"><span data-stu-id="b6711-124">Device is Quarantined in Exchange</span></span>|



