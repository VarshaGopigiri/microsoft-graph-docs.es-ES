---
title: tipo de enumeración ratingCanadaTelevisionType
description: Etiquetas de clasificación de contenido de TV en Canadá
ms.openlocfilehash: ca5e35f05d76a7135ef73949cdb804b088d61ebe
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089353"
---
# <a name="ratingcanadatelevisiontype-enum-type"></a><span data-ttu-id="54088-103">tipo de enumeración ratingCanadaTelevisionType</span><span class="sxs-lookup"><span data-stu-id="54088-103">ratingCanadaTelevisionType enum type</span></span>

> <span data-ttu-id="54088-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="54088-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="54088-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="54088-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="54088-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="54088-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="54088-107">Etiquetas de clasificación de contenido de TV en Canadá</span><span class="sxs-lookup"><span data-stu-id="54088-107">TV content rating labels in Canada</span></span>
## <a name="members"></a><span data-ttu-id="54088-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="54088-108">Members</span></span>
|<span data-ttu-id="54088-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="54088-109">Member</span></span>|<span data-ttu-id="54088-110">Valor</span><span class="sxs-lookup"><span data-stu-id="54088-110">Value</span></span>|<span data-ttu-id="54088-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="54088-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="54088-112">allAllowed</span><span class="sxs-lookup"><span data-stu-id="54088-112">allAllowed</span></span>|<span data-ttu-id="54088-113">0</span><span class="sxs-lookup"><span data-stu-id="54088-113">0</span></span>|<span data-ttu-id="54088-114">Valor predeterminado, permitir que todos los TV muestra contenido</span><span class="sxs-lookup"><span data-stu-id="54088-114">Default value, allow all TV shows content</span></span>|
|<span data-ttu-id="54088-115">allBlocked</span><span class="sxs-lookup"><span data-stu-id="54088-115">allBlocked</span></span>|<span data-ttu-id="54088-116">1</span><span class="sxs-lookup"><span data-stu-id="54088-116">1</span></span>|<span data-ttu-id="54088-117">No permitir que cualquier TV muestra contenido</span><span class="sxs-lookup"><span data-stu-id="54088-117">Do not allow any TV shows content</span></span>|
|<span data-ttu-id="54088-118">secundario</span><span class="sxs-lookup"><span data-stu-id="54088-118">children</span></span>|<span data-ttu-id="54088-119">2</span><span class="sxs-lookup"><span data-stu-id="54088-119">2</span></span>|<span data-ttu-id="54088-120">La clasificación de C es apropiada para mayores de elementos secundarios de 2 a 7 años</span><span class="sxs-lookup"><span data-stu-id="54088-120">The C classification is suitable for children ages of 2 to 7 years</span></span>|
|<span data-ttu-id="54088-121">childrenAbove8</span><span class="sxs-lookup"><span data-stu-id="54088-121">childrenAbove8</span></span>|<span data-ttu-id="54088-122">3</span><span class="sxs-lookup"><span data-stu-id="54088-122">3</span></span>|<span data-ttu-id="54088-123">La clasificación de C8 es adecuada para elementos secundarios de años 8 +</span><span class="sxs-lookup"><span data-stu-id="54088-123">The C8 classification is suitable for children ages 8+</span></span>|
|<span data-ttu-id="54088-124">general</span><span class="sxs-lookup"><span data-stu-id="54088-124">general</span></span>|<span data-ttu-id="54088-125">4</span><span class="sxs-lookup"><span data-stu-id="54088-125">4</span></span>|<span data-ttu-id="54088-126">La clasificación G es adecuada para una audiencia general</span><span class="sxs-lookup"><span data-stu-id="54088-126">The G classification is suitable for general audience</span></span>|
|<span data-ttu-id="54088-127">parentalGuidance</span><span class="sxs-lookup"><span data-stu-id="54088-127">parentalGuidance</span></span>|<span data-ttu-id="54088-128">5</span><span class="sxs-lookup"><span data-stu-id="54088-128">5</span></span>|<span data-ttu-id="54088-129">PÁGINAS, instrucciones padres</span><span class="sxs-lookup"><span data-stu-id="54088-129">PG, Parental Guidance</span></span>|
|<span data-ttu-id="54088-130">agesAbove14</span><span class="sxs-lookup"><span data-stu-id="54088-130">agesAbove14</span></span>|<span data-ttu-id="54088-131">6</span><span class="sxs-lookup"><span data-stu-id="54088-131">6</span></span>|<span data-ttu-id="54088-132">La clasificación de 14 + está pensado para los visores mayores de 14 años</span><span class="sxs-lookup"><span data-stu-id="54088-132">The 14+ classification is intended for viewers ages 14 and older</span></span>|
|<span data-ttu-id="54088-133">agesAbove18</span><span class="sxs-lookup"><span data-stu-id="54088-133">agesAbove18</span></span>|<span data-ttu-id="54088-134">7</span><span class="sxs-lookup"><span data-stu-id="54088-134">7</span></span>|<span data-ttu-id="54088-135">La clasificación de 18 + está pensado para los visores mayores de 18 años</span><span class="sxs-lookup"><span data-stu-id="54088-135">The 18+ classification is intended for viewers ages 18 and older</span></span>|





