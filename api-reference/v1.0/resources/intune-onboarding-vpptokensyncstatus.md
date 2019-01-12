---
title: tipo de enumeración vppTokenSyncStatus
description: Estados de sincronización posibles asociados con un token de programa de compra de volumen de Apple.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: dfdb80ae40abcc505927b94a33330bc09454e790
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27965085"
---
# <a name="vpptokensyncstatus-enum-type"></a><span data-ttu-id="3e2b0-103">tipo de enumeración vppTokenSyncStatus</span><span class="sxs-lookup"><span data-stu-id="3e2b0-103">vppTokenSyncStatus enum type</span></span>

> <span data-ttu-id="3e2b0-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3e2b0-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3e2b0-105">Estados de sincronización posibles asociados con un token de programa de compra de volumen de Apple.</span><span class="sxs-lookup"><span data-stu-id="3e2b0-105">Possible sync statuses associated with an Apple Volume Purchase Program token.</span></span>
## <a name="members"></a><span data-ttu-id="3e2b0-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="3e2b0-106">Members</span></span>
|<span data-ttu-id="3e2b0-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="3e2b0-107">Member</span></span>|<span data-ttu-id="3e2b0-108">Valor</span><span class="sxs-lookup"><span data-stu-id="3e2b0-108">Value</span></span>|<span data-ttu-id="3e2b0-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3e2b0-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3e2b0-110">none</span><span class="sxs-lookup"><span data-stu-id="3e2b0-110">none</span></span>|<span data-ttu-id="3e2b0-111">0</span><span class="sxs-lookup"><span data-stu-id="3e2b0-111">0</span></span>|<span data-ttu-id="3e2b0-112">Estado predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3e2b0-112">Default status.</span></span>|
|<span data-ttu-id="3e2b0-113">en curso</span><span class="sxs-lookup"><span data-stu-id="3e2b0-113">inProgress</span></span>|<span data-ttu-id="3e2b0-114">1</span><span class="sxs-lookup"><span data-stu-id="3e2b0-114">1</span></span>|<span data-ttu-id="3e2b0-115">Última sincronización en curso.</span><span class="sxs-lookup"><span data-stu-id="3e2b0-115">Last Sync in progress.</span></span>|
|<span data-ttu-id="3e2b0-116">completado</span><span class="sxs-lookup"><span data-stu-id="3e2b0-116">completed</span></span>|<span data-ttu-id="3e2b0-117">2</span><span class="sxs-lookup"><span data-stu-id="3e2b0-117">2</span></span>|<span data-ttu-id="3e2b0-118">Última sincronización que se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="3e2b0-118">Last Sync completed successfully.</span></span>|
|<span data-ttu-id="3e2b0-119">failed</span><span class="sxs-lookup"><span data-stu-id="3e2b0-119">failed</span></span>|<span data-ttu-id="3e2b0-120">3</span><span class="sxs-lookup"><span data-stu-id="3e2b0-120">3</span></span>|<span data-ttu-id="3e2b0-121">Error en la última sincronización.</span><span class="sxs-lookup"><span data-stu-id="3e2b0-121">Last Sync failed.</span></span>|



