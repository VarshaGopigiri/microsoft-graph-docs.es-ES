---
title: tipo de enumeración deviceManagementExchangeAccessState
description: Estado de acceso de dispositivo de Exchange.
author: tfitzmac
ms.openlocfilehash: cb72a3e07f0f14fdd509bb0274605cb9592db241
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27328745"
---
# <a name="devicemanagementexchangeaccessstate-enum-type"></a><span data-ttu-id="b33dd-103">tipo de enumeración deviceManagementExchangeAccessState</span><span class="sxs-lookup"><span data-stu-id="b33dd-103">deviceManagementExchangeAccessState enum type</span></span>

> <span data-ttu-id="b33dd-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b33dd-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b33dd-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b33dd-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b33dd-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b33dd-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b33dd-107">Estado de acceso de dispositivo de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b33dd-107">Device Exchange Access State.</span></span>
## <a name="members"></a><span data-ttu-id="b33dd-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b33dd-108">Members</span></span>
|<span data-ttu-id="b33dd-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="b33dd-109">Member</span></span>|<span data-ttu-id="b33dd-110">Valor</span><span class="sxs-lookup"><span data-stu-id="b33dd-110">Value</span></span>|<span data-ttu-id="b33dd-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b33dd-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b33dd-112">ninguno</span><span class="sxs-lookup"><span data-stu-id="b33dd-112">none</span></span>|<span data-ttu-id="b33dd-113">0</span><span class="sxs-lookup"><span data-stu-id="b33dd-113">0</span></span>|<span data-ttu-id="b33dd-114">No hay ningún estado de acceso detectado desde Exchange</span><span class="sxs-lookup"><span data-stu-id="b33dd-114">No access state discovered from Exchange</span></span>|
|<span data-ttu-id="b33dd-115">desconocido</span><span class="sxs-lookup"><span data-stu-id="b33dd-115">unknown</span></span>|<span data-ttu-id="b33dd-116">1</span><span class="sxs-lookup"><span data-stu-id="b33dd-116">1</span></span>|<span data-ttu-id="b33dd-117">Se desconoce el estado de acceso de dispositivo para Exchange</span><span class="sxs-lookup"><span data-stu-id="b33dd-117">Device access state to Exchange is unknown</span></span>|
|<span data-ttu-id="b33dd-118">permitido</span><span class="sxs-lookup"><span data-stu-id="b33dd-118">allowed</span></span>|<span data-ttu-id="b33dd-119">2</span><span class="sxs-lookup"><span data-stu-id="b33dd-119">2</span></span>|<span data-ttu-id="b33dd-120">Dispositivo tiene acceso a Exchange</span><span class="sxs-lookup"><span data-stu-id="b33dd-120">Device has access to Exchange</span></span>|
|<span data-ttu-id="b33dd-121">bloqueado</span><span class="sxs-lookup"><span data-stu-id="b33dd-121">blocked</span></span>|<span data-ttu-id="b33dd-122">3</span><span class="sxs-lookup"><span data-stu-id="b33dd-122">3</span></span>|<span data-ttu-id="b33dd-123">Dispositivo está bloqueado en Exchange</span><span class="sxs-lookup"><span data-stu-id="b33dd-123">Device is Blocked in Exchange</span></span>|
|<span data-ttu-id="b33dd-124">en cuarentena</span><span class="sxs-lookup"><span data-stu-id="b33dd-124">quarantined</span></span>|<span data-ttu-id="b33dd-125">4</span><span class="sxs-lookup"><span data-stu-id="b33dd-125">4</span></span>|<span data-ttu-id="b33dd-126">Dispositivo está en cuarentena en Exchange</span><span class="sxs-lookup"><span data-stu-id="b33dd-126">Device is Quarantined in Exchange</span></span>|





