---
title: tipo de enumeración androidDeviceOwnerRequiredPasswordType
description: Directiva de propietario del dispositivo Android requiere contraseña, escriba.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: c53cc67d01886b76a20eef149a59c1d1fef4fc83
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27887650"
---
# <a name="androiddeviceownerrequiredpasswordtype-enum-type"></a><span data-ttu-id="ec8d9-103">tipo de enumeración androidDeviceOwnerRequiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="ec8d9-103">androidDeviceOwnerRequiredPasswordType enum type</span></span>

> <span data-ttu-id="ec8d9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ec8d9-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ec8d9-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ec8d9-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ec8d9-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ec8d9-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ec8d9-107">Directiva de propietario del dispositivo Android requiere contraseña, escriba.</span><span class="sxs-lookup"><span data-stu-id="ec8d9-107">Android Device Owner policy required password type.</span></span>
## <a name="members"></a><span data-ttu-id="ec8d9-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ec8d9-108">Members</span></span>
|<span data-ttu-id="ec8d9-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="ec8d9-109">Member</span></span>|<span data-ttu-id="ec8d9-110">Valor</span><span class="sxs-lookup"><span data-stu-id="ec8d9-110">Value</span></span>|<span data-ttu-id="ec8d9-111">Description</span><span class="sxs-lookup"><span data-stu-id="ec8d9-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ec8d9-112">deviceDefault</span><span class="sxs-lookup"><span data-stu-id="ec8d9-112">deviceDefault</span></span>|<span data-ttu-id="ec8d9-113">0</span><span class="sxs-lookup"><span data-stu-id="ec8d9-113">0</span></span>|<span data-ttu-id="ec8d9-114">Valor predeterminado de dispositivo, sin intención.</span><span class="sxs-lookup"><span data-stu-id="ec8d9-114">Device default value, no intent.</span></span>|
|<span data-ttu-id="ec8d9-115">necesario</span><span class="sxs-lookup"><span data-stu-id="ec8d9-115">required</span></span>|<span data-ttu-id="ec8d9-116">1</span><span class="sxs-lookup"><span data-stu-id="ec8d9-116">1</span></span>|<span data-ttu-id="ec8d9-117">Debe haber un conjunto de contraseña, pero no existen restricciones en el tipo.</span><span class="sxs-lookup"><span data-stu-id="ec8d9-117">There must be a password set, but there are no restrictions on type.</span></span>|
|<span data-ttu-id="ec8d9-118">numérico</span><span class="sxs-lookup"><span data-stu-id="ec8d9-118">numeric</span></span>|<span data-ttu-id="ec8d9-119">2</span><span class="sxs-lookup"><span data-stu-id="ec8d9-119">2</span></span>|<span data-ttu-id="ec8d9-120">Al menos numérico.</span><span class="sxs-lookup"><span data-stu-id="ec8d9-120">At least numeric.</span></span>|
|<span data-ttu-id="ec8d9-121">numericComplex</span><span class="sxs-lookup"><span data-stu-id="ec8d9-121">numericComplex</span></span>|<span data-ttu-id="ec8d9-122">3</span><span class="sxs-lookup"><span data-stu-id="ec8d9-122">3</span></span>|<span data-ttu-id="ec8d9-123">Al menos numérico con ninguna secuencia ordenada o de repetición.</span><span class="sxs-lookup"><span data-stu-id="ec8d9-123">At least numeric with no repeating or ordered sequences.</span></span>|
|<span data-ttu-id="ec8d9-124">alfabéticos</span><span class="sxs-lookup"><span data-stu-id="ec8d9-124">alphabetic</span></span>|<span data-ttu-id="ec8d9-125">4</span><span class="sxs-lookup"><span data-stu-id="ec8d9-125">4</span></span>|<span data-ttu-id="ec8d9-126">Contraseña de al menos alfabética.</span><span class="sxs-lookup"><span data-stu-id="ec8d9-126">At least alphabetic password.</span></span>|
|<span data-ttu-id="ec8d9-127">alfanuméricos</span><span class="sxs-lookup"><span data-stu-id="ec8d9-127">alphanumeric</span></span>|<span data-ttu-id="ec8d9-128">5</span><span class="sxs-lookup"><span data-stu-id="ec8d9-128">5</span></span>|<span data-ttu-id="ec8d9-129">Contraseña alfanumérica al menos</span><span class="sxs-lookup"><span data-stu-id="ec8d9-129">At least alphanumeric password</span></span>|
|<span data-ttu-id="ec8d9-130">alphanumericWithSymbols</span><span class="sxs-lookup"><span data-stu-id="ec8d9-130">alphanumericWithSymbols</span></span>|<span data-ttu-id="ec8d9-131">6</span><span class="sxs-lookup"><span data-stu-id="ec8d9-131">6</span></span>|<span data-ttu-id="ec8d9-132">Al menos alfanumérico con los símbolos.</span><span class="sxs-lookup"><span data-stu-id="ec8d9-132">At least alphanumeric with symbols.</span></span>|





