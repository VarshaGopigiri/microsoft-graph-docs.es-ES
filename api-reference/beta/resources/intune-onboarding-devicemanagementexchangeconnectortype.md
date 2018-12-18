---
title: tipo de enumeración deviceManagementExchangeConnectorType
description: El tipo de conector de Exchange.
author: tfitzmac
ms.openlocfilehash: 31459d4053e2ba1ef22a516995796baef2407dbf
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27301732"
---
# <a name="devicemanagementexchangeconnectortype-enum-type"></a><span data-ttu-id="efcba-103">tipo de enumeración deviceManagementExchangeConnectorType</span><span class="sxs-lookup"><span data-stu-id="efcba-103">deviceManagementExchangeConnectorType enum type</span></span>

> <span data-ttu-id="efcba-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="efcba-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="efcba-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="efcba-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="efcba-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="efcba-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="efcba-107">El tipo de conector de Exchange.</span><span class="sxs-lookup"><span data-stu-id="efcba-107">The type of Exchange Connector.</span></span>
## <a name="members"></a><span data-ttu-id="efcba-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="efcba-108">Members</span></span>
|<span data-ttu-id="efcba-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="efcba-109">Member</span></span>|<span data-ttu-id="efcba-110">Valor</span><span class="sxs-lookup"><span data-stu-id="efcba-110">Value</span></span>|<span data-ttu-id="efcba-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="efcba-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="efcba-112">Local</span><span class="sxs-lookup"><span data-stu-id="efcba-112">onPremises</span></span>|<span data-ttu-id="efcba-113">0</span><span class="sxs-lookup"><span data-stu-id="efcba-113">0</span></span>|<span data-ttu-id="efcba-114">Se conecta al entorno de Exchange local.</span><span class="sxs-lookup"><span data-stu-id="efcba-114">Connects to on-premises Exchange Environment.</span></span>|
|<span data-ttu-id="efcba-115">hospedado</span><span class="sxs-lookup"><span data-stu-id="efcba-115">hosted</span></span>|<span data-ttu-id="efcba-116">1</span><span class="sxs-lookup"><span data-stu-id="efcba-116">1</span></span>|<span data-ttu-id="efcba-117">Se conecta al entorno de Exchange de varios inquilino de Office 365</span><span class="sxs-lookup"><span data-stu-id="efcba-117">Connects to O365 multi-tenant Exchange environment</span></span>|
|<span data-ttu-id="efcba-118">serviceToService</span><span class="sxs-lookup"><span data-stu-id="efcba-118">serviceToService</span></span>|<span data-ttu-id="efcba-119">2</span><span class="sxs-lookup"><span data-stu-id="efcba-119">2</span></span>|<span data-ttu-id="efcba-120">Intune Service se conecta directamente al entorno de Exchange de varios inquilino de Office 365</span><span class="sxs-lookup"><span data-stu-id="efcba-120">Intune Service connects directly to O365 multi-tenant Exchange environment</span></span>|
|<span data-ttu-id="efcba-121">dedicada</span><span class="sxs-lookup"><span data-stu-id="efcba-121">dedicated</span></span>|<span data-ttu-id="efcba-122">3</span><span class="sxs-lookup"><span data-stu-id="efcba-122">3</span></span>|<span data-ttu-id="efcba-123">Se conecta al entorno de Exchange dedicados de Office 365.</span><span class="sxs-lookup"><span data-stu-id="efcba-123">Connects to O365 Dedicated Exchange environment.</span></span>|





