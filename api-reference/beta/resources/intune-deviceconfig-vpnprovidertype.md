---
title: tipo de enumeración vpnProviderType
description: Tipo de proveedor de VPN por cada aplicación.
ms.openlocfilehash: 133b1663ce3c72ba520dd5c1eeadf963154e9cc9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089328"
---
# <a name="vpnprovidertype-enum-type"></a><span data-ttu-id="0cf72-103">tipo de enumeración vpnProviderType</span><span class="sxs-lookup"><span data-stu-id="0cf72-103">vpnProviderType enum type</span></span>

> <span data-ttu-id="0cf72-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0cf72-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0cf72-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0cf72-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0cf72-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0cf72-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0cf72-107">Tipo de proveedor de VPN por cada aplicación.</span><span class="sxs-lookup"><span data-stu-id="0cf72-107">Provider type for per-app VPN.</span></span>
## <a name="members"></a><span data-ttu-id="0cf72-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0cf72-108">Members</span></span>
|<span data-ttu-id="0cf72-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="0cf72-109">Member</span></span>|<span data-ttu-id="0cf72-110">Valor</span><span class="sxs-lookup"><span data-stu-id="0cf72-110">Value</span></span>|<span data-ttu-id="0cf72-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="0cf72-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0cf72-112">No configurado</span><span class="sxs-lookup"><span data-stu-id="0cf72-112">notConfigured</span></span>|<span data-ttu-id="0cf72-113">0</span><span class="sxs-lookup"><span data-stu-id="0cf72-113">0</span></span>|<span data-ttu-id="0cf72-114">El tráfico de túnel no está configurado de forma explícita.</span><span class="sxs-lookup"><span data-stu-id="0cf72-114">Tunnel traffic is not explicitly configured.</span></span>|
|<span data-ttu-id="0cf72-115">appProxy</span><span class="sxs-lookup"><span data-stu-id="0cf72-115">appProxy</span></span>|<span data-ttu-id="0cf72-116">1</span><span class="sxs-lookup"><span data-stu-id="0cf72-116">1</span></span>|<span data-ttu-id="0cf72-117">Tráfico de túnel en el nivel de aplicación.</span><span class="sxs-lookup"><span data-stu-id="0cf72-117">Tunnel traffic at the application layer.</span></span>|
|<span data-ttu-id="0cf72-118">packetTunnel</span><span class="sxs-lookup"><span data-stu-id="0cf72-118">packetTunnel</span></span>|<span data-ttu-id="0cf72-119">2</span><span class="sxs-lookup"><span data-stu-id="0cf72-119">2</span></span>|<span data-ttu-id="0cf72-120">Tráfico de túnel en la capa IP.</span><span class="sxs-lookup"><span data-stu-id="0cf72-120">Tunnel traffic at the IP layer.</span></span>|




