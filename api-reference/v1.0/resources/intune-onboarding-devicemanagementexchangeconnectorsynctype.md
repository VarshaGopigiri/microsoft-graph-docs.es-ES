---
title: tipo de enumeración deviceManagementExchangeConnectorSyncType
description: El tipo de sincronización de conector de Exchange solicitada.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 5af14006bd6f3cc8733faecc8e0219cc02e7fcd9
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27983285"
---
# <a name="devicemanagementexchangeconnectorsynctype-enum-type"></a><span data-ttu-id="eb679-103">tipo de enumeración deviceManagementExchangeConnectorSyncType</span><span class="sxs-lookup"><span data-stu-id="eb679-103">deviceManagementExchangeConnectorSyncType enum type</span></span>

> <span data-ttu-id="eb679-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="eb679-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="eb679-105">El tipo de sincronización de conector de Exchange solicitada.</span><span class="sxs-lookup"><span data-stu-id="eb679-105">The type of Exchange Connector sync requested.</span></span>
## <a name="members"></a><span data-ttu-id="eb679-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="eb679-106">Members</span></span>
|<span data-ttu-id="eb679-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="eb679-107">Member</span></span>|<span data-ttu-id="eb679-108">Valor</span><span class="sxs-lookup"><span data-stu-id="eb679-108">Value</span></span>|<span data-ttu-id="eb679-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb679-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="eb679-110">fullSync</span><span class="sxs-lookup"><span data-stu-id="eb679-110">fullSync</span></span>|<span data-ttu-id="eb679-111">0</span><span class="sxs-lookup"><span data-stu-id="eb679-111">0</span></span>|<span data-ttu-id="eb679-112">Descubrir todos los el dispositivo en Exchange.</span><span class="sxs-lookup"><span data-stu-id="eb679-112">Discover all the device in Exchange.</span></span>|
|<span data-ttu-id="eb679-113">deltaSync</span><span class="sxs-lookup"><span data-stu-id="eb679-113">deltaSync</span></span>|<span data-ttu-id="eb679-114">1</span><span class="sxs-lookup"><span data-stu-id="eb679-114">1</span></span>|<span data-ttu-id="eb679-115">Descubrir sólo el dispositivo en Exchange que se actualizaron durante la ventana de sincronización delta.</span><span class="sxs-lookup"><span data-stu-id="eb679-115">Discover only the device in Exchange which have updated during the delta sync window.</span></span>|



