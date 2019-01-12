---
title: tipo de enumeración vpnProviderType
description: Tipo de proveedor de VPN por cada aplicación.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 1eeb0acf2f6e7b0773cbf4697e5a27699d1f2f27
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27937729"
---
# <a name="vpnprovidertype-enum-type"></a><span data-ttu-id="40c70-103">tipo de enumeración vpnProviderType</span><span class="sxs-lookup"><span data-stu-id="40c70-103">vpnProviderType enum type</span></span>

> <span data-ttu-id="40c70-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="40c70-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="40c70-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="40c70-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="40c70-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="40c70-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="40c70-107">Tipo de proveedor de VPN por cada aplicación.</span><span class="sxs-lookup"><span data-stu-id="40c70-107">Provider type for per-app VPN.</span></span>
## <a name="members"></a><span data-ttu-id="40c70-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="40c70-108">Members</span></span>
|<span data-ttu-id="40c70-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="40c70-109">Member</span></span>|<span data-ttu-id="40c70-110">Valor</span><span class="sxs-lookup"><span data-stu-id="40c70-110">Value</span></span>|<span data-ttu-id="40c70-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="40c70-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="40c70-112">No configurado</span><span class="sxs-lookup"><span data-stu-id="40c70-112">notConfigured</span></span>|<span data-ttu-id="40c70-113">0</span><span class="sxs-lookup"><span data-stu-id="40c70-113">0</span></span>|<span data-ttu-id="40c70-114">El tráfico de túnel no está configurado de forma explícita.</span><span class="sxs-lookup"><span data-stu-id="40c70-114">Tunnel traffic is not explicitly configured.</span></span>|
|<span data-ttu-id="40c70-115">appProxy</span><span class="sxs-lookup"><span data-stu-id="40c70-115">appProxy</span></span>|<span data-ttu-id="40c70-116">1</span><span class="sxs-lookup"><span data-stu-id="40c70-116">1</span></span>|<span data-ttu-id="40c70-117">Tráfico de túnel en el nivel de aplicación.</span><span class="sxs-lookup"><span data-stu-id="40c70-117">Tunnel traffic at the application layer.</span></span>|
|<span data-ttu-id="40c70-118">packetTunnel</span><span class="sxs-lookup"><span data-stu-id="40c70-118">packetTunnel</span></span>|<span data-ttu-id="40c70-119">2</span><span class="sxs-lookup"><span data-stu-id="40c70-119">2</span></span>|<span data-ttu-id="40c70-120">Tráfico de túnel en la capa IP.</span><span class="sxs-lookup"><span data-stu-id="40c70-120">Tunnel traffic at the IP layer.</span></span>|





