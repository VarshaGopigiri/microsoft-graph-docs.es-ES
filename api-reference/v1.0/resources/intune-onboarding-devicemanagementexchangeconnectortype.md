---
title: tipo de enumeración deviceManagementExchangeConnectorType
description: El tipo de conector de Exchange.
ms.openlocfilehash: 694b211afeaaaabb997f03dfc64618fc0301f0ab
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031806"
---
# <a name="devicemanagementexchangeconnectortype-enum-type"></a><span data-ttu-id="2e12b-103">tipo de enumeración deviceManagementExchangeConnectorType</span><span class="sxs-lookup"><span data-stu-id="2e12b-103">deviceManagementExchangeConnectorType enum type</span></span>

> <span data-ttu-id="2e12b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2e12b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2e12b-105">El tipo de conector de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2e12b-105">The type of Exchange Connector.</span></span>
## <a name="members"></a><span data-ttu-id="2e12b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="2e12b-106">Members</span></span>
|<span data-ttu-id="2e12b-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="2e12b-107">Member</span></span>|<span data-ttu-id="2e12b-108">Valor</span><span class="sxs-lookup"><span data-stu-id="2e12b-108">Value</span></span>|<span data-ttu-id="2e12b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e12b-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2e12b-110">Local</span><span class="sxs-lookup"><span data-stu-id="2e12b-110">onPremises</span></span>|<span data-ttu-id="2e12b-111">0</span><span class="sxs-lookup"><span data-stu-id="2e12b-111">0</span></span>|<span data-ttu-id="2e12b-112">Se conecta al entorno de Exchange local.</span><span class="sxs-lookup"><span data-stu-id="2e12b-112">Connects to on-premises Exchange Environment.</span></span>|
|<span data-ttu-id="2e12b-113">hospedado</span><span class="sxs-lookup"><span data-stu-id="2e12b-113">hosted</span></span>|<span data-ttu-id="2e12b-114">1</span><span class="sxs-lookup"><span data-stu-id="2e12b-114">1</span></span>|<span data-ttu-id="2e12b-115">Se conecta al entorno de Exchange de varios inquilino de Office 365</span><span class="sxs-lookup"><span data-stu-id="2e12b-115">Connects to O365 multi-tenant Exchange environment</span></span>|
|<span data-ttu-id="2e12b-116">serviceToService</span><span class="sxs-lookup"><span data-stu-id="2e12b-116">serviceToService</span></span>|<span data-ttu-id="2e12b-117">2</span><span class="sxs-lookup"><span data-stu-id="2e12b-117">2</span></span>|<span data-ttu-id="2e12b-118">Intune Service se conecta directamente al entorno de Exchange de varios inquilino de Office 365</span><span class="sxs-lookup"><span data-stu-id="2e12b-118">Intune Service connects directly to O365 multi-tenant Exchange environment</span></span>|
|<span data-ttu-id="2e12b-119">dedicada</span><span class="sxs-lookup"><span data-stu-id="2e12b-119">dedicated</span></span>|<span data-ttu-id="2e12b-120">3</span><span class="sxs-lookup"><span data-stu-id="2e12b-120">3</span></span>|<span data-ttu-id="2e12b-121">Se conecta al entorno de Exchange dedicados de Office 365.</span><span class="sxs-lookup"><span data-stu-id="2e12b-121">Connects to O365 Dedicated Exchange environment.</span></span>|



