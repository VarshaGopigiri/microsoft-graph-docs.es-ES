---
title: tipo de enumeración vpnTrafficRuleRoutingPolicyType
description: Especifica la directiva de enrutamiento para una regla de tráfico VPN.
ms.openlocfilehash: df51851ef0820f5982a6689421503364e9064c78
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085906"
---
# <a name="vpntrafficruleroutingpolicytype-enum-type"></a><span data-ttu-id="9fee6-103">tipo de enumeración vpnTrafficRuleRoutingPolicyType</span><span class="sxs-lookup"><span data-stu-id="9fee6-103">vpnTrafficRuleRoutingPolicyType enum type</span></span>

> <span data-ttu-id="9fee6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9fee6-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9fee6-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9fee6-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="9fee6-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9fee6-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9fee6-107">Especifica la directiva de enrutamiento para una regla de tráfico VPN.</span><span class="sxs-lookup"><span data-stu-id="9fee6-107">Specifies the routing policy for a VPN traffic rule.</span></span>
## <a name="members"></a><span data-ttu-id="9fee6-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="9fee6-108">Members</span></span>
|<span data-ttu-id="9fee6-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="9fee6-109">Member</span></span>|<span data-ttu-id="9fee6-110">Valor</span><span class="sxs-lookup"><span data-stu-id="9fee6-110">Value</span></span>|<span data-ttu-id="9fee6-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fee6-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9fee6-112">ninguno</span><span class="sxs-lookup"><span data-stu-id="9fee6-112">none</span></span>|<span data-ttu-id="9fee6-113">0</span><span class="sxs-lookup"><span data-stu-id="9fee6-113">0</span></span>|<span data-ttu-id="9fee6-114">Ninguna directiva de enrutamiento especificada.</span><span class="sxs-lookup"><span data-stu-id="9fee6-114">No routing policy specified.</span></span>|
|<span data-ttu-id="9fee6-115">splitTunnel</span><span class="sxs-lookup"><span data-stu-id="9fee6-115">splitTunnel</span></span>|<span data-ttu-id="9fee6-116">1</span><span class="sxs-lookup"><span data-stu-id="9fee6-116">1</span></span>|<span data-ttu-id="9fee6-117">El tráfico de red para la aplicación especificada se enrutarán a través de la VPN.</span><span class="sxs-lookup"><span data-stu-id="9fee6-117">Network traffic for the specified app will be routed through the VPN.</span></span>|
|<span data-ttu-id="9fee6-118">forceTunnel</span><span class="sxs-lookup"><span data-stu-id="9fee6-118">forceTunnel</span></span>|<span data-ttu-id="9fee6-119">2</span><span class="sxs-lookup"><span data-stu-id="9fee6-119">2</span></span>|<span data-ttu-id="9fee6-120">Todo el tráfico de red se enrutarán a través de la VPN.</span><span class="sxs-lookup"><span data-stu-id="9fee6-120">All network traffic will be routed through the VPN.</span></span>|





