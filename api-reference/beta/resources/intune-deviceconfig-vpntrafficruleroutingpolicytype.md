---
title: tipo de enumeración vpnTrafficRuleRoutingPolicyType
description: Especifica la directiva de enrutamiento para una regla de tráfico VPN.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 2c8ec4303dc16c7cb0606e4b9cf86594446f571e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27974955"
---
# <a name="vpntrafficruleroutingpolicytype-enum-type"></a><span data-ttu-id="3995c-103">tipo de enumeración vpnTrafficRuleRoutingPolicyType</span><span class="sxs-lookup"><span data-stu-id="3995c-103">vpnTrafficRuleRoutingPolicyType enum type</span></span>

> <span data-ttu-id="3995c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3995c-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3995c-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3995c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="3995c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3995c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3995c-107">Especifica la directiva de enrutamiento para una regla de tráfico VPN.</span><span class="sxs-lookup"><span data-stu-id="3995c-107">Specifies the routing policy for a VPN traffic rule.</span></span>
## <a name="members"></a><span data-ttu-id="3995c-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="3995c-108">Members</span></span>
|<span data-ttu-id="3995c-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="3995c-109">Member</span></span>|<span data-ttu-id="3995c-110">Valor</span><span class="sxs-lookup"><span data-stu-id="3995c-110">Value</span></span>|<span data-ttu-id="3995c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="3995c-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3995c-112">none</span><span class="sxs-lookup"><span data-stu-id="3995c-112">none</span></span>|<span data-ttu-id="3995c-113">0</span><span class="sxs-lookup"><span data-stu-id="3995c-113">0</span></span>|<span data-ttu-id="3995c-114">Ninguna directiva de enrutamiento especificada.</span><span class="sxs-lookup"><span data-stu-id="3995c-114">No routing policy specified.</span></span>|
|<span data-ttu-id="3995c-115">splitTunnel</span><span class="sxs-lookup"><span data-stu-id="3995c-115">splitTunnel</span></span>|<span data-ttu-id="3995c-116">1</span><span class="sxs-lookup"><span data-stu-id="3995c-116">1</span></span>|<span data-ttu-id="3995c-117">El tráfico de red para la aplicación especificada se enrutarán a través de la VPN.</span><span class="sxs-lookup"><span data-stu-id="3995c-117">Network traffic for the specified app will be routed through the VPN.</span></span>|
|<span data-ttu-id="3995c-118">forceTunnel</span><span class="sxs-lookup"><span data-stu-id="3995c-118">forceTunnel</span></span>|<span data-ttu-id="3995c-119">2</span><span class="sxs-lookup"><span data-stu-id="3995c-119">2</span></span>|<span data-ttu-id="3995c-120">Todo el tráfico de red se enrutarán a través de la VPN.</span><span class="sxs-lookup"><span data-stu-id="3995c-120">All network traffic will be routed through the VPN.</span></span>|





