---
title: tipo de enumeración certificateRevocationStatus
description: Estado de revocación del certificado.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 8c1c77e267da5528088a7a8ef6400a872790aaf3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27983124"
---
# <a name="certificaterevocationstatus-enum-type"></a><span data-ttu-id="d9084-103">tipo de enumeración certificateRevocationStatus</span><span class="sxs-lookup"><span data-stu-id="d9084-103">certificateRevocationStatus enum type</span></span>

> <span data-ttu-id="d9084-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d9084-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d9084-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d9084-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d9084-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d9084-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d9084-107">Estado de revocación del certificado.</span><span class="sxs-lookup"><span data-stu-id="d9084-107">Certificate Revocation Status.</span></span>
## <a name="members"></a><span data-ttu-id="d9084-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d9084-108">Members</span></span>
|<span data-ttu-id="d9084-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="d9084-109">Member</span></span>|<span data-ttu-id="d9084-110">Valor</span><span class="sxs-lookup"><span data-stu-id="d9084-110">Value</span></span>|<span data-ttu-id="d9084-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9084-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d9084-112">none</span><span class="sxs-lookup"><span data-stu-id="d9084-112">none</span></span>|<span data-ttu-id="d9084-113">0</span><span class="sxs-lookup"><span data-stu-id="d9084-113">0</span></span>|<span data-ttu-id="d9084-114">No se ha revocado.</span><span class="sxs-lookup"><span data-stu-id="d9084-114">Not revoked.</span></span>|
|<span data-ttu-id="d9084-115">pendiente</span><span class="sxs-lookup"><span data-stu-id="d9084-115">pending</span></span>|<span data-ttu-id="d9084-116">1</span><span class="sxs-lookup"><span data-stu-id="d9084-116">1</span></span>|<span data-ttu-id="d9084-117">Revocación pendientes.</span><span class="sxs-lookup"><span data-stu-id="d9084-117">Revocation pending.</span></span>|
|<span data-ttu-id="d9084-118">emitido</span><span class="sxs-lookup"><span data-stu-id="d9084-118">issued</span></span>|<span data-ttu-id="d9084-119">2</span><span class="sxs-lookup"><span data-stu-id="d9084-119">2</span></span>|<span data-ttu-id="d9084-120">Comando de revocación emitido.</span><span class="sxs-lookup"><span data-stu-id="d9084-120">Revocation command issued.</span></span>|
|<span data-ttu-id="d9084-121">failed</span><span class="sxs-lookup"><span data-stu-id="d9084-121">failed</span></span>|<span data-ttu-id="d9084-122">3</span><span class="sxs-lookup"><span data-stu-id="d9084-122">3</span></span>|<span data-ttu-id="d9084-123">No se pudo revocación.</span><span class="sxs-lookup"><span data-stu-id="d9084-123">Revocation failed.</span></span>|
|<span data-ttu-id="d9084-124">revocado</span><span class="sxs-lookup"><span data-stu-id="d9084-124">revoked</span></span>|<span data-ttu-id="d9084-125">4</span><span class="sxs-lookup"><span data-stu-id="d9084-125">4</span></span>|<span data-ttu-id="d9084-126">Revocado.</span><span class="sxs-lookup"><span data-stu-id="d9084-126">Revoked.</span></span>|





