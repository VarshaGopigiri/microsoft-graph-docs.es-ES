---
title: tipo de enumeración teamsAsyncOperationStatus
description: Describe el estado actual de un teamsAsyncOperation.
author: nkramer
ms.openlocfilehash: 49b5b81999714627b1a1acd42df208594123b262
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27332007"
---
# <a name="teamsasyncoperationstatus-enum-type"></a><span data-ttu-id="b2c4c-103">tipo de enumeración teamsAsyncOperationStatus</span><span class="sxs-lookup"><span data-stu-id="b2c4c-103">teamsAsyncOperationStatus enum type</span></span>

> <span data-ttu-id="b2c4c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b2c4c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b2c4c-106">Describe el estado actual de un [teamsAsyncOperation](teamsasyncoperation.md).</span><span class="sxs-lookup"><span data-stu-id="b2c4c-106">Describes the current status of a [teamsAsyncOperation](teamsasyncoperation.md).</span></span>

## <a name="members"></a><span data-ttu-id="b2c4c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b2c4c-107">Members</span></span>

| <span data-ttu-id="b2c4c-108">Miembro	</span><span class="sxs-lookup"><span data-stu-id="b2c4c-108">Member</span></span> | <span data-ttu-id="b2c4c-109">Valor</span><span class="sxs-lookup"><span data-stu-id="b2c4c-109">Value</span></span>| <span data-ttu-id="b2c4c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2c4c-110">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="b2c4c-111">No válido</span><span class="sxs-lookup"><span data-stu-id="b2c4c-111">invalid</span></span>|<span data-ttu-id="b2c4c-112">0</span><span class="sxs-lookup"><span data-stu-id="b2c4c-112">0</span></span>|<span data-ttu-id="b2c4c-113">Valor no válido.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-113">Invalid value.</span></span>|
|<span data-ttu-id="b2c4c-114">no iniciado</span><span class="sxs-lookup"><span data-stu-id="b2c4c-114">notStarted</span></span>|<span data-ttu-id="b2c4c-115">1</span><span class="sxs-lookup"><span data-stu-id="b2c4c-115">1</span></span>|<span data-ttu-id="b2c4c-116">La operación no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-116">The operation has not started.</span></span>|
|<span data-ttu-id="b2c4c-117">en curso</span><span class="sxs-lookup"><span data-stu-id="b2c4c-117">inProgress</span></span>|<span data-ttu-id="b2c4c-118">2</span><span class="sxs-lookup"><span data-stu-id="b2c4c-118">2</span></span>|<span data-ttu-id="b2c4c-119">La operación se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-119">The operation is running.</span></span>|
|<span data-ttu-id="b2c4c-120">succeeded</span><span class="sxs-lookup"><span data-stu-id="b2c4c-120">succeeded</span></span>|<span data-ttu-id="b2c4c-121">3</span><span class="sxs-lookup"><span data-stu-id="b2c4c-121">3</span></span>|<span data-ttu-id="b2c4c-122">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-122">The operation succeeded.</span></span>|
|<span data-ttu-id="b2c4c-123">failed</span><span class="sxs-lookup"><span data-stu-id="b2c4c-123">failed</span></span>|<span data-ttu-id="b2c4c-124">4</span><span class="sxs-lookup"><span data-stu-id="b2c4c-124">4</span></span>|<span data-ttu-id="b2c4c-125">Error.</span><span class="sxs-lookup"><span data-stu-id="b2c4c-125">The operation failed.</span></span>|