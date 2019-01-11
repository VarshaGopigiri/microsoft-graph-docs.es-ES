---
title: tipo de enumeración certificateRevocationStatus
description: Estado de revocación del certificado.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 8d24d515f992ed396c3530595240a107852d83e1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27868309"
---
# <a name="certificaterevocationstatus-enum-type"></a><span data-ttu-id="79c2a-103">tipo de enumeración certificateRevocationStatus</span><span class="sxs-lookup"><span data-stu-id="79c2a-103">certificateRevocationStatus enum type</span></span>

> <span data-ttu-id="79c2a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="79c2a-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="79c2a-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="79c2a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="79c2a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="79c2a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="79c2a-107">Estado de revocación del certificado.</span><span class="sxs-lookup"><span data-stu-id="79c2a-107">Certificate Revocation Status.</span></span>
## <a name="members"></a><span data-ttu-id="79c2a-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="79c2a-108">Members</span></span>
|<span data-ttu-id="79c2a-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="79c2a-109">Member</span></span>|<span data-ttu-id="79c2a-110">Valor</span><span class="sxs-lookup"><span data-stu-id="79c2a-110">Value</span></span>|<span data-ttu-id="79c2a-111">Description</span><span class="sxs-lookup"><span data-stu-id="79c2a-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="79c2a-112">none</span><span class="sxs-lookup"><span data-stu-id="79c2a-112">none</span></span>|<span data-ttu-id="79c2a-113">0</span><span class="sxs-lookup"><span data-stu-id="79c2a-113">0</span></span>|<span data-ttu-id="79c2a-114">No se ha revocado.</span><span class="sxs-lookup"><span data-stu-id="79c2a-114">Not revoked.</span></span>|
|<span data-ttu-id="79c2a-115">pendiente</span><span class="sxs-lookup"><span data-stu-id="79c2a-115">pending</span></span>|<span data-ttu-id="79c2a-116">1</span><span class="sxs-lookup"><span data-stu-id="79c2a-116">1</span></span>|<span data-ttu-id="79c2a-117">Revocación pendientes.</span><span class="sxs-lookup"><span data-stu-id="79c2a-117">Revocation pending.</span></span>|
|<span data-ttu-id="79c2a-118">emitido</span><span class="sxs-lookup"><span data-stu-id="79c2a-118">issued</span></span>|<span data-ttu-id="79c2a-119">2</span><span class="sxs-lookup"><span data-stu-id="79c2a-119">2</span></span>|<span data-ttu-id="79c2a-120">Comando de revocación emitido.</span><span class="sxs-lookup"><span data-stu-id="79c2a-120">Revocation command issued.</span></span>|
|<span data-ttu-id="79c2a-121">failed</span><span class="sxs-lookup"><span data-stu-id="79c2a-121">failed</span></span>|<span data-ttu-id="79c2a-122">3</span><span class="sxs-lookup"><span data-stu-id="79c2a-122">3</span></span>|<span data-ttu-id="79c2a-123">No se pudo revocación.</span><span class="sxs-lookup"><span data-stu-id="79c2a-123">Revocation failed.</span></span>|
|<span data-ttu-id="79c2a-124">revocado</span><span class="sxs-lookup"><span data-stu-id="79c2a-124">revoked</span></span>|<span data-ttu-id="79c2a-125">4</span><span class="sxs-lookup"><span data-stu-id="79c2a-125">4</span></span>|<span data-ttu-id="79c2a-126">Revocado.</span><span class="sxs-lookup"><span data-stu-id="79c2a-126">Revoked.</span></span>|





