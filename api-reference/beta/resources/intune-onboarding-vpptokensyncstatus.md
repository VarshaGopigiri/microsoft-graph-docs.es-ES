---
title: tipo de enumeración vppTokenSyncStatus
description: Estados de sincronización posibles asociados con un token de programa de compra de volumen de Apple.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 4101f1338513787b27ce530579ffd42c7756366a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27931289"
---
# <a name="vpptokensyncstatus-enum-type"></a><span data-ttu-id="2ef14-103">tipo de enumeración vppTokenSyncStatus</span><span class="sxs-lookup"><span data-stu-id="2ef14-103">vppTokenSyncStatus enum type</span></span>

> <span data-ttu-id="2ef14-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2ef14-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2ef14-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2ef14-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2ef14-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2ef14-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2ef14-107">Estados de sincronización posibles asociados con un token de programa de compra de volumen de Apple.</span><span class="sxs-lookup"><span data-stu-id="2ef14-107">Possible sync statuses associated with an Apple Volume Purchase Program token.</span></span>
## <a name="members"></a><span data-ttu-id="2ef14-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="2ef14-108">Members</span></span>
|<span data-ttu-id="2ef14-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="2ef14-109">Member</span></span>|<span data-ttu-id="2ef14-110">Valor</span><span class="sxs-lookup"><span data-stu-id="2ef14-110">Value</span></span>|<span data-ttu-id="2ef14-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ef14-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2ef14-112">none</span><span class="sxs-lookup"><span data-stu-id="2ef14-112">none</span></span>|<span data-ttu-id="2ef14-113">0</span><span class="sxs-lookup"><span data-stu-id="2ef14-113">0</span></span>|<span data-ttu-id="2ef14-114">Estado predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2ef14-114">Default status.</span></span>|
|<span data-ttu-id="2ef14-115">en curso</span><span class="sxs-lookup"><span data-stu-id="2ef14-115">inProgress</span></span>|<span data-ttu-id="2ef14-116">1</span><span class="sxs-lookup"><span data-stu-id="2ef14-116">1</span></span>|<span data-ttu-id="2ef14-117">Última sincronización en curso.</span><span class="sxs-lookup"><span data-stu-id="2ef14-117">Last Sync in progress.</span></span>|
|<span data-ttu-id="2ef14-118">completado</span><span class="sxs-lookup"><span data-stu-id="2ef14-118">completed</span></span>|<span data-ttu-id="2ef14-119">2</span><span class="sxs-lookup"><span data-stu-id="2ef14-119">2</span></span>|<span data-ttu-id="2ef14-120">Última sincronización que se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="2ef14-120">Last Sync completed successfully.</span></span>|
|<span data-ttu-id="2ef14-121">failed</span><span class="sxs-lookup"><span data-stu-id="2ef14-121">failed</span></span>|<span data-ttu-id="2ef14-122">3</span><span class="sxs-lookup"><span data-stu-id="2ef14-122">3</span></span>|<span data-ttu-id="2ef14-123">Error en la última sincronización.</span><span class="sxs-lookup"><span data-stu-id="2ef14-123">Last Sync failed.</span></span>|





