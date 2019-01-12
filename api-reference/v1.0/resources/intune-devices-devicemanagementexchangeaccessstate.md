---
title: tipo de enumeración deviceManagementExchangeAccessState
description: Estado de acceso de dispositivo de Exchange.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: dbfa7b9396a1100f2e3c7e4e78cf697233d840cc
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27947018"
---
# <a name="devicemanagementexchangeaccessstate-enum-type"></a><span data-ttu-id="a2e13-103">tipo de enumeración deviceManagementExchangeAccessState</span><span class="sxs-lookup"><span data-stu-id="a2e13-103">deviceManagementExchangeAccessState enum type</span></span>

> <span data-ttu-id="a2e13-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a2e13-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a2e13-105">Estado de acceso de dispositivo de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a2e13-105">Device Exchange Access State.</span></span>
## <a name="members"></a><span data-ttu-id="a2e13-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="a2e13-106">Members</span></span>
|<span data-ttu-id="a2e13-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="a2e13-107">Member</span></span>|<span data-ttu-id="a2e13-108">Valor</span><span class="sxs-lookup"><span data-stu-id="a2e13-108">Value</span></span>|<span data-ttu-id="a2e13-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2e13-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a2e13-110">none</span><span class="sxs-lookup"><span data-stu-id="a2e13-110">none</span></span>|<span data-ttu-id="a2e13-111">0</span><span class="sxs-lookup"><span data-stu-id="a2e13-111">0</span></span>|<span data-ttu-id="a2e13-112">No hay ningún estado de acceso detectado desde Exchange</span><span class="sxs-lookup"><span data-stu-id="a2e13-112">No access state discovered from Exchange</span></span>|
|<span data-ttu-id="a2e13-113">desconocido</span><span class="sxs-lookup"><span data-stu-id="a2e13-113">unknown</span></span>|<span data-ttu-id="a2e13-114">1</span><span class="sxs-lookup"><span data-stu-id="a2e13-114">1</span></span>|<span data-ttu-id="a2e13-115">Se desconoce el estado de acceso de dispositivo para Exchange</span><span class="sxs-lookup"><span data-stu-id="a2e13-115">Device access state to Exchange is unknown</span></span>|
|<span data-ttu-id="a2e13-116">permitido</span><span class="sxs-lookup"><span data-stu-id="a2e13-116">allowed</span></span>|<span data-ttu-id="a2e13-117">2</span><span class="sxs-lookup"><span data-stu-id="a2e13-117">2</span></span>|<span data-ttu-id="a2e13-118">Dispositivo tiene acceso a Exchange</span><span class="sxs-lookup"><span data-stu-id="a2e13-118">Device has access to Exchange</span></span>|
|<span data-ttu-id="a2e13-119">bloqueado</span><span class="sxs-lookup"><span data-stu-id="a2e13-119">blocked</span></span>|<span data-ttu-id="a2e13-120">3</span><span class="sxs-lookup"><span data-stu-id="a2e13-120">3</span></span>|<span data-ttu-id="a2e13-121">Dispositivo está bloqueado en Exchange</span><span class="sxs-lookup"><span data-stu-id="a2e13-121">Device is Blocked in Exchange</span></span>|
|<span data-ttu-id="a2e13-122">en cuarentena</span><span class="sxs-lookup"><span data-stu-id="a2e13-122">quarantined</span></span>|<span data-ttu-id="a2e13-123">4</span><span class="sxs-lookup"><span data-stu-id="a2e13-123">4</span></span>|<span data-ttu-id="a2e13-124">Dispositivo está en cuarentena en Exchange</span><span class="sxs-lookup"><span data-stu-id="a2e13-124">Device is Quarantined in Exchange</span></span>|



