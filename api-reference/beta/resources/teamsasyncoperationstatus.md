---
title: tipo de enumeración teamsAsyncOperationStatus
description: Describe el estado actual de un teamsAsyncOperation.
ms.openlocfilehash: f553242ace983651b8d4fda77370de712f9d08b6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084099"
---
# <a name="teamsasyncoperationstatus-enum-type"></a><span data-ttu-id="00f9a-103">tipo de enumeración teamsAsyncOperationStatus</span><span class="sxs-lookup"><span data-stu-id="00f9a-103">teamsAsyncOperationStatus enum type</span></span>

> <span data-ttu-id="00f9a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="00f9a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="00f9a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="00f9a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="00f9a-106">Describe el estado actual de un [teamsAsyncOperation](teamsasyncoperation.md).</span><span class="sxs-lookup"><span data-stu-id="00f9a-106">Describes the current status of a [teamsAsyncOperation](teamsasyncoperation.md).</span></span>

## <a name="members"></a><span data-ttu-id="00f9a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="00f9a-107">Members</span></span>

| <span data-ttu-id="00f9a-108">Miembro	</span><span class="sxs-lookup"><span data-stu-id="00f9a-108">Member</span></span> | <span data-ttu-id="00f9a-109">Valor</span><span class="sxs-lookup"><span data-stu-id="00f9a-109">Value</span></span>| <span data-ttu-id="00f9a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="00f9a-110">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="00f9a-111">No válido</span><span class="sxs-lookup"><span data-stu-id="00f9a-111">invalid</span></span>|<span data-ttu-id="00f9a-112">0</span><span class="sxs-lookup"><span data-stu-id="00f9a-112">0</span></span>|<span data-ttu-id="00f9a-113">Valor no válido.</span><span class="sxs-lookup"><span data-stu-id="00f9a-113">Invalid value.</span></span>|
|<span data-ttu-id="00f9a-114">no iniciado</span><span class="sxs-lookup"><span data-stu-id="00f9a-114">notStarted</span></span>|<span data-ttu-id="00f9a-115">1</span><span class="sxs-lookup"><span data-stu-id="00f9a-115">1</span></span>|<span data-ttu-id="00f9a-116">La operación no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="00f9a-116">The operation has not started.</span></span>|
|<span data-ttu-id="00f9a-117">en curso</span><span class="sxs-lookup"><span data-stu-id="00f9a-117">inProgress</span></span>|<span data-ttu-id="00f9a-118">2</span><span class="sxs-lookup"><span data-stu-id="00f9a-118">2</span></span>|<span data-ttu-id="00f9a-119">La operación se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="00f9a-119">The operation is running.</span></span>|
|<span data-ttu-id="00f9a-120">succeeded</span><span class="sxs-lookup"><span data-stu-id="00f9a-120">succeeded</span></span>|<span data-ttu-id="00f9a-121">3</span><span class="sxs-lookup"><span data-stu-id="00f9a-121">3</span></span>|<span data-ttu-id="00f9a-122">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="00f9a-122">The operation succeeded.</span></span>|
|<span data-ttu-id="00f9a-123">failed</span><span class="sxs-lookup"><span data-stu-id="00f9a-123">failed</span></span>|<span data-ttu-id="00f9a-124">4</span><span class="sxs-lookup"><span data-stu-id="00f9a-124">4</span></span>|<span data-ttu-id="00f9a-125">Error.</span><span class="sxs-lookup"><span data-stu-id="00f9a-125">The operation failed.</span></span>|