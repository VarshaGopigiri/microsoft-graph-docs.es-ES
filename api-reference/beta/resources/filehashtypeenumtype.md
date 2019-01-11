---
title: enumeración fileHashType
description: Enumeración de tipos de hash de archivo.
localization_priority: Normal
ms.openlocfilehash: e1c31aaea6c8cea40817efea61dc8654d3d17fae
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27816334"
---
# <a name="filehashtype-enum"></a><span data-ttu-id="f0086-103">enumeración fileHashType</span><span class="sxs-lookup"><span data-stu-id="f0086-103">fileHashType enum</span></span>

> <span data-ttu-id="f0086-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f0086-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f0086-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f0086-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f0086-106">Enumeración de tipos de hash de archivo.</span><span class="sxs-lookup"><span data-stu-id="f0086-106">Enum for file hash types.</span></span>

## <a name="members"></a><span data-ttu-id="f0086-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f0086-107">Members</span></span>

|<span data-ttu-id="f0086-108">Miembro	</span><span class="sxs-lookup"><span data-stu-id="f0086-108">Member</span></span>|<span data-ttu-id="f0086-109">Valor</span><span class="sxs-lookup"><span data-stu-id="f0086-109">Value</span></span>|<span data-ttu-id="f0086-110">Description</span><span class="sxs-lookup"><span data-stu-id="f0086-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f0086-111">desconocido</span><span class="sxs-lookup"><span data-stu-id="f0086-111">unknown</span></span>|<span data-ttu-id="f0086-112">0</span><span class="sxs-lookup"><span data-stu-id="f0086-112">0</span></span>|<span data-ttu-id="f0086-113">Tipo desconocido.</span><span class="sxs-lookup"><span data-stu-id="f0086-113">Unknown type.</span></span>|
|<span data-ttu-id="f0086-114">SHA1</span><span class="sxs-lookup"><span data-stu-id="f0086-114">sha1</span></span>|<span data-ttu-id="f0086-115">1</span><span class="sxs-lookup"><span data-stu-id="f0086-115">1</span></span>|<span data-ttu-id="f0086-116">Tipo de hash de SHA1.</span><span class="sxs-lookup"><span data-stu-id="f0086-116">SHA1 hash type.</span></span>|
|<span data-ttu-id="f0086-117">SHA256</span><span class="sxs-lookup"><span data-stu-id="f0086-117">sha256</span></span>|<span data-ttu-id="f0086-118">2</span><span class="sxs-lookup"><span data-stu-id="f0086-118">2</span></span>| <span data-ttu-id="f0086-119">Tipo de hash SHA256.</span><span class="sxs-lookup"><span data-stu-id="f0086-119">SHA256 hash type.</span></span>|
|<span data-ttu-id="f0086-120">MD5</span><span class="sxs-lookup"><span data-stu-id="f0086-120">md5</span></span>|<span data-ttu-id="f0086-121">3</span><span class="sxs-lookup"><span data-stu-id="f0086-121">3</span></span>| <span data-ttu-id="f0086-122">Tipo de hash MD5.</span><span class="sxs-lookup"><span data-stu-id="f0086-122">MD5 hash type.</span></span>|
|<span data-ttu-id="f0086-123">authenticodeHash256</span><span class="sxs-lookup"><span data-stu-id="f0086-123">authenticodeHash256</span></span>|<span data-ttu-id="f0086-124">4</span><span class="sxs-lookup"><span data-stu-id="f0086-124">4</span></span>| <span data-ttu-id="f0086-125">Tipo de algoritmo hash AuthenticodeHash256.</span><span class="sxs-lookup"><span data-stu-id="f0086-125">AuthenticodeHash256 hash type.</span></span>|
|<span data-ttu-id="f0086-126">lsHash</span><span class="sxs-lookup"><span data-stu-id="f0086-126">lsHash</span></span>|<span data-ttu-id="f0086-127">5</span><span class="sxs-lookup"><span data-stu-id="f0086-127">5</span></span>| <span data-ttu-id="f0086-128">Tipo de algoritmo hash LsHash.</span><span class="sxs-lookup"><span data-stu-id="f0086-128">LsHash hash type.</span></span>|
|<span data-ttu-id="f0086-129">ctph</span><span class="sxs-lookup"><span data-stu-id="f0086-129">ctph</span></span>|<span data-ttu-id="f0086-130">6</span><span class="sxs-lookup"><span data-stu-id="f0086-130">6</span></span>| <span data-ttu-id="f0086-131">Tipo de algoritmo hash CTPH.</span><span class="sxs-lookup"><span data-stu-id="f0086-131">CTPH hash type.</span></span>|
|<span data-ttu-id="f0086-132">peSha1</span><span class="sxs-lookup"><span data-stu-id="f0086-132">peSha1</span></span>|<span data-ttu-id="f0086-133">7</span><span class="sxs-lookup"><span data-stu-id="f0086-133">7</span></span>| <span data-ttu-id="f0086-134">Tipo de algoritmo hash PESHA1.</span><span class="sxs-lookup"><span data-stu-id="f0086-134">PESHA1 hash type.</span></span>|
|<span data-ttu-id="f0086-135">peSha256</span><span class="sxs-lookup"><span data-stu-id="f0086-135">peSha256</span></span>|<span data-ttu-id="f0086-136">8</span><span class="sxs-lookup"><span data-stu-id="f0086-136">8</span></span>| <span data-ttu-id="f0086-137">Tipo de algoritmo hash PESHA256.</span><span class="sxs-lookup"><span data-stu-id="f0086-137">PESHA256 hash type.</span></span>|
