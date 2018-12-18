---
title: tipo de enumeración deviceManagementExchangeConnectorType
description: El tipo de conector de Exchange.
author: tfitzmac
ms.openlocfilehash: 333a5a7c6f73fead263edbdf3edafeefc3514ed1
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27306737"
---
# <a name="devicemanagementexchangeconnectortype-enum-type"></a><span data-ttu-id="cee10-103">tipo de enumeración deviceManagementExchangeConnectorType</span><span class="sxs-lookup"><span data-stu-id="cee10-103">deviceManagementExchangeConnectorType enum type</span></span>

> <span data-ttu-id="cee10-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cee10-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cee10-105">El tipo de conector de Exchange.</span><span class="sxs-lookup"><span data-stu-id="cee10-105">The type of Exchange Connector.</span></span>
## <a name="members"></a><span data-ttu-id="cee10-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="cee10-106">Members</span></span>
|<span data-ttu-id="cee10-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="cee10-107">Member</span></span>|<span data-ttu-id="cee10-108">Valor</span><span class="sxs-lookup"><span data-stu-id="cee10-108">Value</span></span>|<span data-ttu-id="cee10-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="cee10-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cee10-110">Local</span><span class="sxs-lookup"><span data-stu-id="cee10-110">onPremises</span></span>|<span data-ttu-id="cee10-111">0</span><span class="sxs-lookup"><span data-stu-id="cee10-111">0</span></span>|<span data-ttu-id="cee10-112">Se conecta al entorno de Exchange local.</span><span class="sxs-lookup"><span data-stu-id="cee10-112">Connects to on-premises Exchange Environment.</span></span>|
|<span data-ttu-id="cee10-113">hospedado</span><span class="sxs-lookup"><span data-stu-id="cee10-113">hosted</span></span>|<span data-ttu-id="cee10-114">1</span><span class="sxs-lookup"><span data-stu-id="cee10-114">1</span></span>|<span data-ttu-id="cee10-115">Se conecta al entorno de Exchange de varios inquilino de Office 365</span><span class="sxs-lookup"><span data-stu-id="cee10-115">Connects to O365 multi-tenant Exchange environment</span></span>|
|<span data-ttu-id="cee10-116">serviceToService</span><span class="sxs-lookup"><span data-stu-id="cee10-116">serviceToService</span></span>|<span data-ttu-id="cee10-117">2</span><span class="sxs-lookup"><span data-stu-id="cee10-117">2</span></span>|<span data-ttu-id="cee10-118">Intune Service se conecta directamente al entorno de Exchange de varios inquilino de Office 365</span><span class="sxs-lookup"><span data-stu-id="cee10-118">Intune Service connects directly to O365 multi-tenant Exchange environment</span></span>|
|<span data-ttu-id="cee10-119">dedicada</span><span class="sxs-lookup"><span data-stu-id="cee10-119">dedicated</span></span>|<span data-ttu-id="cee10-120">3</span><span class="sxs-lookup"><span data-stu-id="cee10-120">3</span></span>|<span data-ttu-id="cee10-121">Se conecta al entorno de Exchange dedicados de Office 365.</span><span class="sxs-lookup"><span data-stu-id="cee10-121">Connects to O365 Dedicated Exchange environment.</span></span>|



