---
title: tipo de enumeración vppTokenSyncStatus
description: Estados de sincronización posibles asociados con un token de programa de compra de volumen de Apple.
author: tfitzmac
ms.openlocfilehash: c6612c86911fd3d43128a8a7a441db8093ad3656
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27316656"
---
# <a name="vpptokensyncstatus-enum-type"></a><span data-ttu-id="7a7d6-103">tipo de enumeración vppTokenSyncStatus</span><span class="sxs-lookup"><span data-stu-id="7a7d6-103">vppTokenSyncStatus enum type</span></span>

> <span data-ttu-id="7a7d6-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7a7d6-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7a7d6-105">Estados de sincronización posibles asociados con un token de programa de compra de volumen de Apple.</span><span class="sxs-lookup"><span data-stu-id="7a7d6-105">Possible sync statuses associated with an Apple Volume Purchase Program token.</span></span>
## <a name="members"></a><span data-ttu-id="7a7d6-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="7a7d6-106">Members</span></span>
|<span data-ttu-id="7a7d6-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="7a7d6-107">Member</span></span>|<span data-ttu-id="7a7d6-108">Valor</span><span class="sxs-lookup"><span data-stu-id="7a7d6-108">Value</span></span>|<span data-ttu-id="7a7d6-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a7d6-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7a7d6-110">ninguno</span><span class="sxs-lookup"><span data-stu-id="7a7d6-110">none</span></span>|<span data-ttu-id="7a7d6-111">0</span><span class="sxs-lookup"><span data-stu-id="7a7d6-111">0</span></span>|<span data-ttu-id="7a7d6-112">Estado predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7a7d6-112">Default status.</span></span>|
|<span data-ttu-id="7a7d6-113">en curso</span><span class="sxs-lookup"><span data-stu-id="7a7d6-113">inProgress</span></span>|<span data-ttu-id="7a7d6-114">1</span><span class="sxs-lookup"><span data-stu-id="7a7d6-114">1</span></span>|<span data-ttu-id="7a7d6-115">Última sincronización en curso.</span><span class="sxs-lookup"><span data-stu-id="7a7d6-115">Last Sync in progress.</span></span>|
|<span data-ttu-id="7a7d6-116">completado</span><span class="sxs-lookup"><span data-stu-id="7a7d6-116">completed</span></span>|<span data-ttu-id="7a7d6-117">2</span><span class="sxs-lookup"><span data-stu-id="7a7d6-117">2</span></span>|<span data-ttu-id="7a7d6-118">Última sincronización que se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="7a7d6-118">Last Sync completed successfully.</span></span>|
|<span data-ttu-id="7a7d6-119">failed</span><span class="sxs-lookup"><span data-stu-id="7a7d6-119">failed</span></span>|<span data-ttu-id="7a7d6-120">3</span><span class="sxs-lookup"><span data-stu-id="7a7d6-120">3</span></span>|<span data-ttu-id="7a7d6-121">Error en la última sincronización.</span><span class="sxs-lookup"><span data-stu-id="7a7d6-121">Last Sync failed.</span></span>|



