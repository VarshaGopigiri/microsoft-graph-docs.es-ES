---
title: tipo de enumeración deviceManagementExchangeConnectorType
description: El tipo de conector de Exchange.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 07449df53aa65036ae55e63c514c1687fbbab86a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888518"
---
# <a name="devicemanagementexchangeconnectortype-enum-type"></a><span data-ttu-id="e6a63-103">tipo de enumeración deviceManagementExchangeConnectorType</span><span class="sxs-lookup"><span data-stu-id="e6a63-103">deviceManagementExchangeConnectorType enum type</span></span>

> <span data-ttu-id="e6a63-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e6a63-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e6a63-105">El tipo de conector de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e6a63-105">The type of Exchange Connector.</span></span>
## <a name="members"></a><span data-ttu-id="e6a63-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="e6a63-106">Members</span></span>
|<span data-ttu-id="e6a63-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="e6a63-107">Member</span></span>|<span data-ttu-id="e6a63-108">Valor</span><span class="sxs-lookup"><span data-stu-id="e6a63-108">Value</span></span>|<span data-ttu-id="e6a63-109">Description</span><span class="sxs-lookup"><span data-stu-id="e6a63-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e6a63-110">Local</span><span class="sxs-lookup"><span data-stu-id="e6a63-110">onPremises</span></span>|<span data-ttu-id="e6a63-111">0</span><span class="sxs-lookup"><span data-stu-id="e6a63-111">0</span></span>|<span data-ttu-id="e6a63-112">Se conecta al entorno de Exchange local.</span><span class="sxs-lookup"><span data-stu-id="e6a63-112">Connects to on-premises Exchange Environment.</span></span>|
|<span data-ttu-id="e6a63-113">hospedado</span><span class="sxs-lookup"><span data-stu-id="e6a63-113">hosted</span></span>|<span data-ttu-id="e6a63-114">1</span><span class="sxs-lookup"><span data-stu-id="e6a63-114">1</span></span>|<span data-ttu-id="e6a63-115">Se conecta al entorno de Exchange de varios inquilino de Office 365</span><span class="sxs-lookup"><span data-stu-id="e6a63-115">Connects to O365 multi-tenant Exchange environment</span></span>|
|<span data-ttu-id="e6a63-116">serviceToService</span><span class="sxs-lookup"><span data-stu-id="e6a63-116">serviceToService</span></span>|<span data-ttu-id="e6a63-117">2</span><span class="sxs-lookup"><span data-stu-id="e6a63-117">2</span></span>|<span data-ttu-id="e6a63-118">Intune Service se conecta directamente al entorno de Exchange de varios inquilino de Office 365</span><span class="sxs-lookup"><span data-stu-id="e6a63-118">Intune Service connects directly to O365 multi-tenant Exchange environment</span></span>|
|<span data-ttu-id="e6a63-119">dedicada</span><span class="sxs-lookup"><span data-stu-id="e6a63-119">dedicated</span></span>|<span data-ttu-id="e6a63-120">3</span><span class="sxs-lookup"><span data-stu-id="e6a63-120">3</span></span>|<span data-ttu-id="e6a63-121">Se conecta al entorno de Exchange dedicados de Office 365.</span><span class="sxs-lookup"><span data-stu-id="e6a63-121">Connects to O365 Dedicated Exchange environment.</span></span>|



