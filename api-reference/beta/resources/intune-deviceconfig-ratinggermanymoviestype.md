---
title: tipo de enumeración ratingGermanyMoviesType
description: Películas clasificación etiquetas en Alemania
author: tfitzmac
ms.openlocfilehash: 2dc78b1de99c193ab575b28ef3658ddd2b5f6df2
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27312344"
---
# <a name="ratinggermanymoviestype-enum-type"></a><span data-ttu-id="475b2-103">tipo de enumeración ratingGermanyMoviesType</span><span class="sxs-lookup"><span data-stu-id="475b2-103">ratingGermanyMoviesType enum type</span></span>

> <span data-ttu-id="475b2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="475b2-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="475b2-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="475b2-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="475b2-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="475b2-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="475b2-107">Películas clasificación etiquetas en Alemania</span><span class="sxs-lookup"><span data-stu-id="475b2-107">Movies rating labels in Germany</span></span>
## <a name="members"></a><span data-ttu-id="475b2-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="475b2-108">Members</span></span>
|<span data-ttu-id="475b2-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="475b2-109">Member</span></span>|<span data-ttu-id="475b2-110">Valor</span><span class="sxs-lookup"><span data-stu-id="475b2-110">Value</span></span>|<span data-ttu-id="475b2-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="475b2-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="475b2-112">allAllowed</span><span class="sxs-lookup"><span data-stu-id="475b2-112">allAllowed</span></span>|<span data-ttu-id="475b2-113">0</span><span class="sxs-lookup"><span data-stu-id="475b2-113">0</span></span>|<span data-ttu-id="475b2-114">Valor predeterminado, permitir que el contenido de todas las películas</span><span class="sxs-lookup"><span data-stu-id="475b2-114">Default value, allow all movies content</span></span>|
|<span data-ttu-id="475b2-115">allBlocked</span><span class="sxs-lookup"><span data-stu-id="475b2-115">allBlocked</span></span>|<span data-ttu-id="475b2-116">1</span><span class="sxs-lookup"><span data-stu-id="475b2-116">1</span></span>|<span data-ttu-id="475b2-117">No permitir cualquier contenido de películas</span><span class="sxs-lookup"><span data-stu-id="475b2-117">Do not allow any movies content</span></span>|
|<span data-ttu-id="475b2-118">general</span><span class="sxs-lookup"><span data-stu-id="475b2-118">general</span></span>|<span data-ttu-id="475b2-119">2</span><span class="sxs-lookup"><span data-stu-id="475b2-119">2</span></span>|<span data-ttu-id="475b2-120">Jahren AB 0, no hay restricciones de edad</span><span class="sxs-lookup"><span data-stu-id="475b2-120">Ab 0 Jahren, no age restrictions</span></span>|
|<span data-ttu-id="475b2-121">agesAbove6</span><span class="sxs-lookup"><span data-stu-id="475b2-121">agesAbove6</span></span>|<span data-ttu-id="475b2-122">3</span><span class="sxs-lookup"><span data-stu-id="475b2-122">3</span></span>|<span data-ttu-id="475b2-123">AB 6 Jahren, envejece 6 y anteriores</span><span class="sxs-lookup"><span data-stu-id="475b2-123">Ab 6 Jahren, ages 6 and older</span></span>|
|<span data-ttu-id="475b2-124">agesAbove12</span><span class="sxs-lookup"><span data-stu-id="475b2-124">agesAbove12</span></span>|<span data-ttu-id="475b2-125">4</span><span class="sxs-lookup"><span data-stu-id="475b2-125">4</span></span>|<span data-ttu-id="475b2-126">AB 12 Jahren, envejece 12 y más antiguos</span><span class="sxs-lookup"><span data-stu-id="475b2-126">Ab 12 Jahren, ages 12 and older</span></span>|
|<span data-ttu-id="475b2-127">agesAbove16</span><span class="sxs-lookup"><span data-stu-id="475b2-127">agesAbove16</span></span>|<span data-ttu-id="475b2-128">5</span><span class="sxs-lookup"><span data-stu-id="475b2-128">5</span></span>|<span data-ttu-id="475b2-129">AB 16 Jahren, envejece 16 y anteriores</span><span class="sxs-lookup"><span data-stu-id="475b2-129">Ab 16 Jahren, ages 16 and older</span></span>|
|<span data-ttu-id="475b2-130">adultos</span><span class="sxs-lookup"><span data-stu-id="475b2-130">adults</span></span>|<span data-ttu-id="475b2-131">6</span><span class="sxs-lookup"><span data-stu-id="475b2-131">6</span></span>|<span data-ttu-id="475b2-132">AB 18 Jahren, sólo para adultos</span><span class="sxs-lookup"><span data-stu-id="475b2-132">Ab 18 Jahren, adults only</span></span>|





