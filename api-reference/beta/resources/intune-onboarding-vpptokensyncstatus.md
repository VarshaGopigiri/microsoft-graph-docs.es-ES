---
title: tipo de enumeración vppTokenSyncStatus
description: Estados de sincronización posibles asociados con un token de programa de compra de volumen de Apple.
ms.openlocfilehash: 443eb87299fbb052edf8788d07b029c68d58c2fe
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089282"
---
# <a name="vpptokensyncstatus-enum-type"></a><span data-ttu-id="0ec38-103">tipo de enumeración vppTokenSyncStatus</span><span class="sxs-lookup"><span data-stu-id="0ec38-103">vppTokenSyncStatus enum type</span></span>

> <span data-ttu-id="0ec38-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0ec38-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0ec38-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0ec38-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0ec38-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0ec38-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0ec38-107">Estados de sincronización posibles asociados con un token de programa de compra de volumen de Apple.</span><span class="sxs-lookup"><span data-stu-id="0ec38-107">Possible sync statuses associated with an Apple Volume Purchase Program token.</span></span>
## <a name="members"></a><span data-ttu-id="0ec38-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0ec38-108">Members</span></span>
|<span data-ttu-id="0ec38-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="0ec38-109">Member</span></span>|<span data-ttu-id="0ec38-110">Valor</span><span class="sxs-lookup"><span data-stu-id="0ec38-110">Value</span></span>|<span data-ttu-id="0ec38-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ec38-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0ec38-112">ninguno</span><span class="sxs-lookup"><span data-stu-id="0ec38-112">none</span></span>|<span data-ttu-id="0ec38-113">0</span><span class="sxs-lookup"><span data-stu-id="0ec38-113">0</span></span>|<span data-ttu-id="0ec38-114">Estado predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0ec38-114">Default status.</span></span>|
|<span data-ttu-id="0ec38-115">en curso</span><span class="sxs-lookup"><span data-stu-id="0ec38-115">inProgress</span></span>|<span data-ttu-id="0ec38-116">1</span><span class="sxs-lookup"><span data-stu-id="0ec38-116">1</span></span>|<span data-ttu-id="0ec38-117">Última sincronización en curso.</span><span class="sxs-lookup"><span data-stu-id="0ec38-117">Last Sync in progress.</span></span>|
|<span data-ttu-id="0ec38-118">completado</span><span class="sxs-lookup"><span data-stu-id="0ec38-118">completed</span></span>|<span data-ttu-id="0ec38-119">2</span><span class="sxs-lookup"><span data-stu-id="0ec38-119">2</span></span>|<span data-ttu-id="0ec38-120">Última sincronización que se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0ec38-120">Last Sync completed successfully.</span></span>|
|<span data-ttu-id="0ec38-121">failed</span><span class="sxs-lookup"><span data-stu-id="0ec38-121">failed</span></span>|<span data-ttu-id="0ec38-122">3</span><span class="sxs-lookup"><span data-stu-id="0ec38-122">3</span></span>|<span data-ttu-id="0ec38-123">Error en la última sincronización.</span><span class="sxs-lookup"><span data-stu-id="0ec38-123">Last Sync failed.</span></span>|





