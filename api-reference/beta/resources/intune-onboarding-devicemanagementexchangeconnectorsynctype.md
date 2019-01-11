---
title: tipo de enumeración deviceManagementExchangeConnectorSyncType
description: El tipo de sincronización de conector de Exchange solicitada.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: bc62e03f61a5170b5495300b0c7f5182262ddafb
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27851775"
---
# <a name="devicemanagementexchangeconnectorsynctype-enum-type"></a><span data-ttu-id="d74c6-103">tipo de enumeración deviceManagementExchangeConnectorSyncType</span><span class="sxs-lookup"><span data-stu-id="d74c6-103">deviceManagementExchangeConnectorSyncType enum type</span></span>

> <span data-ttu-id="d74c6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d74c6-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d74c6-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d74c6-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d74c6-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d74c6-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d74c6-107">El tipo de sincronización de conector de Exchange solicitada.</span><span class="sxs-lookup"><span data-stu-id="d74c6-107">The type of Exchange Connector sync requested.</span></span>
## <a name="members"></a><span data-ttu-id="d74c6-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d74c6-108">Members</span></span>
|<span data-ttu-id="d74c6-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="d74c6-109">Member</span></span>|<span data-ttu-id="d74c6-110">Valor</span><span class="sxs-lookup"><span data-stu-id="d74c6-110">Value</span></span>|<span data-ttu-id="d74c6-111">Description</span><span class="sxs-lookup"><span data-stu-id="d74c6-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d74c6-112">fullSync</span><span class="sxs-lookup"><span data-stu-id="d74c6-112">fullSync</span></span>|<span data-ttu-id="d74c6-113">0</span><span class="sxs-lookup"><span data-stu-id="d74c6-113">0</span></span>|<span data-ttu-id="d74c6-114">Descubrir todos los el dispositivo en Exchange.</span><span class="sxs-lookup"><span data-stu-id="d74c6-114">Discover all the device in Exchange.</span></span>|
|<span data-ttu-id="d74c6-115">deltaSync</span><span class="sxs-lookup"><span data-stu-id="d74c6-115">deltaSync</span></span>|<span data-ttu-id="d74c6-116">1</span><span class="sxs-lookup"><span data-stu-id="d74c6-116">1</span></span>|<span data-ttu-id="d74c6-117">Descubrir sólo el dispositivo en Exchange que se actualizaron durante la ventana de sincronización delta.</span><span class="sxs-lookup"><span data-stu-id="d74c6-117">Discover only the device in Exchange which have updated during the delta sync window.</span></span>|





