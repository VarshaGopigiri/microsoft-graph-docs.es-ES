---
title: tipo de enumeración androidDeviceOwnerRequiredPasswordType
description: Directiva de propietario del dispositivo Android requiere contraseña, escriba.
author: tfitzmac
ms.openlocfilehash: e0903bbf5720350b35bf7e5fe5c9a5f9584810c1
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27330229"
---
# <a name="androiddeviceownerrequiredpasswordtype-enum-type"></a><span data-ttu-id="d7f6d-103">tipo de enumeración androidDeviceOwnerRequiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="d7f6d-103">androidDeviceOwnerRequiredPasswordType enum type</span></span>

> <span data-ttu-id="d7f6d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d7f6d-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d7f6d-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d7f6d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d7f6d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d7f6d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d7f6d-107">Directiva de propietario del dispositivo Android requiere contraseña, escriba.</span><span class="sxs-lookup"><span data-stu-id="d7f6d-107">Android Device Owner policy required password type.</span></span>
## <a name="members"></a><span data-ttu-id="d7f6d-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d7f6d-108">Members</span></span>
|<span data-ttu-id="d7f6d-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="d7f6d-109">Member</span></span>|<span data-ttu-id="d7f6d-110">Valor</span><span class="sxs-lookup"><span data-stu-id="d7f6d-110">Value</span></span>|<span data-ttu-id="d7f6d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7f6d-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d7f6d-112">deviceDefault</span><span class="sxs-lookup"><span data-stu-id="d7f6d-112">deviceDefault</span></span>|<span data-ttu-id="d7f6d-113">0</span><span class="sxs-lookup"><span data-stu-id="d7f6d-113">0</span></span>|<span data-ttu-id="d7f6d-114">Valor predeterminado de dispositivo, sin intención.</span><span class="sxs-lookup"><span data-stu-id="d7f6d-114">Device default value, no intent.</span></span>|
|<span data-ttu-id="d7f6d-115">necesario</span><span class="sxs-lookup"><span data-stu-id="d7f6d-115">required</span></span>|<span data-ttu-id="d7f6d-116">1</span><span class="sxs-lookup"><span data-stu-id="d7f6d-116">1</span></span>|<span data-ttu-id="d7f6d-117">Debe haber un conjunto de contraseña, pero no existen restricciones en el tipo.</span><span class="sxs-lookup"><span data-stu-id="d7f6d-117">There must be a password set, but there are no restrictions on type.</span></span>|
|<span data-ttu-id="d7f6d-118">numérico</span><span class="sxs-lookup"><span data-stu-id="d7f6d-118">numeric</span></span>|<span data-ttu-id="d7f6d-119">2</span><span class="sxs-lookup"><span data-stu-id="d7f6d-119">2</span></span>|<span data-ttu-id="d7f6d-120">Al menos numérico.</span><span class="sxs-lookup"><span data-stu-id="d7f6d-120">At least numeric.</span></span>|
|<span data-ttu-id="d7f6d-121">numericComplex</span><span class="sxs-lookup"><span data-stu-id="d7f6d-121">numericComplex</span></span>|<span data-ttu-id="d7f6d-122">3</span><span class="sxs-lookup"><span data-stu-id="d7f6d-122">3</span></span>|<span data-ttu-id="d7f6d-123">Al menos numérico con ninguna secuencia ordenada o de repetición.</span><span class="sxs-lookup"><span data-stu-id="d7f6d-123">At least numeric with no repeating or ordered sequences.</span></span>|
|<span data-ttu-id="d7f6d-124">alfabéticos</span><span class="sxs-lookup"><span data-stu-id="d7f6d-124">alphabetic</span></span>|<span data-ttu-id="d7f6d-125">4</span><span class="sxs-lookup"><span data-stu-id="d7f6d-125">4</span></span>|<span data-ttu-id="d7f6d-126">Contraseña de al menos alfabética.</span><span class="sxs-lookup"><span data-stu-id="d7f6d-126">At least alphabetic password.</span></span>|
|<span data-ttu-id="d7f6d-127">alfanuméricos</span><span class="sxs-lookup"><span data-stu-id="d7f6d-127">alphanumeric</span></span>|<span data-ttu-id="d7f6d-128">5</span><span class="sxs-lookup"><span data-stu-id="d7f6d-128">5</span></span>|<span data-ttu-id="d7f6d-129">Contraseña alfanumérica al menos</span><span class="sxs-lookup"><span data-stu-id="d7f6d-129">At least alphanumeric password</span></span>|
|<span data-ttu-id="d7f6d-130">alphanumericWithSymbols</span><span class="sxs-lookup"><span data-stu-id="d7f6d-130">alphanumericWithSymbols</span></span>|<span data-ttu-id="d7f6d-131">6</span><span class="sxs-lookup"><span data-stu-id="d7f6d-131">6</span></span>|<span data-ttu-id="d7f6d-132">Al menos alfanumérico con los símbolos.</span><span class="sxs-lookup"><span data-stu-id="d7f6d-132">At least alphanumeric with symbols.</span></span>|





