---
title: tipo de enumeración androidRequiredPasswordType
description: Tipo de contraseña requerida para Android.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: dc82ccd0519196495839f533dc09264525ac7fec
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27957553"
---
# <a name="androidrequiredpasswordtype-enum-type"></a><span data-ttu-id="59210-103">tipo de enumeración androidRequiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="59210-103">androidRequiredPasswordType enum type</span></span>

> <span data-ttu-id="59210-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="59210-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="59210-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="59210-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="59210-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="59210-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="59210-107">Tipo de contraseña requerida para Android.</span><span class="sxs-lookup"><span data-stu-id="59210-107">Android required password type.</span></span>
## <a name="members"></a><span data-ttu-id="59210-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="59210-108">Members</span></span>
|<span data-ttu-id="59210-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="59210-109">Member</span></span>|<span data-ttu-id="59210-110">Valor</span><span class="sxs-lookup"><span data-stu-id="59210-110">Value</span></span>|<span data-ttu-id="59210-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="59210-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="59210-112">deviceDefault</span><span class="sxs-lookup"><span data-stu-id="59210-112">deviceDefault</span></span>|<span data-ttu-id="59210-113">0</span><span class="sxs-lookup"><span data-stu-id="59210-113">0</span></span>|<span data-ttu-id="59210-114">Valor predeterminado de dispositivo, sin intención.</span><span class="sxs-lookup"><span data-stu-id="59210-114">Device default value, no intent.</span></span>|
|<span data-ttu-id="59210-115">alfabéticos</span><span class="sxs-lookup"><span data-stu-id="59210-115">alphabetic</span></span>|<span data-ttu-id="59210-116">1</span><span class="sxs-lookup"><span data-stu-id="59210-116">1</span></span>|<span data-ttu-id="59210-117">Contraseña alfabético requerida.</span><span class="sxs-lookup"><span data-stu-id="59210-117">Alphabetic password required.</span></span>|
|<span data-ttu-id="59210-118">alfanuméricos</span><span class="sxs-lookup"><span data-stu-id="59210-118">alphanumeric</span></span>|<span data-ttu-id="59210-119">2</span><span class="sxs-lookup"><span data-stu-id="59210-119">2</span></span>|<span data-ttu-id="59210-120">Se requiere una contraseña alfanumérica.</span><span class="sxs-lookup"><span data-stu-id="59210-120">Alphanumeric password required.</span></span>|
|<span data-ttu-id="59210-121">alphanumericWithSymbols</span><span class="sxs-lookup"><span data-stu-id="59210-121">alphanumericWithSymbols</span></span>|<span data-ttu-id="59210-122">3</span><span class="sxs-lookup"><span data-stu-id="59210-122">3</span></span>|<span data-ttu-id="59210-123">Alfanumérico con contraseña símbolos requerida.</span><span class="sxs-lookup"><span data-stu-id="59210-123">Alphanumeric with symbols password required.</span></span>|
|<span data-ttu-id="59210-124">lowSecurityBiometric</span><span class="sxs-lookup"><span data-stu-id="59210-124">lowSecurityBiometric</span></span>|<span data-ttu-id="59210-125">4</span><span class="sxs-lookup"><span data-stu-id="59210-125">4</span></span>|<span data-ttu-id="59210-126">Contraseña biométrica en función de baja seguridad requerida.</span><span class="sxs-lookup"><span data-stu-id="59210-126">Low security biometrics based password required.</span></span>|
|<span data-ttu-id="59210-127">numérico</span><span class="sxs-lookup"><span data-stu-id="59210-127">numeric</span></span>|<span data-ttu-id="59210-128">5</span><span class="sxs-lookup"><span data-stu-id="59210-128">5</span></span>|<span data-ttu-id="59210-129">Contraseña numérica requerida.</span><span class="sxs-lookup"><span data-stu-id="59210-129">Numeric password required.</span></span>|
|<span data-ttu-id="59210-130">numericComplex</span><span class="sxs-lookup"><span data-stu-id="59210-130">numericComplex</span></span>|<span data-ttu-id="59210-131">6</span><span class="sxs-lookup"><span data-stu-id="59210-131">6</span></span>|<span data-ttu-id="59210-132">Contraseña compleja numérico requerida.</span><span class="sxs-lookup"><span data-stu-id="59210-132">Numeric complex password required.</span></span>|
|<span data-ttu-id="59210-133">cualquiera</span><span class="sxs-lookup"><span data-stu-id="59210-133">any</span></span>|<span data-ttu-id="59210-134">7</span><span class="sxs-lookup"><span data-stu-id="59210-134">7</span></span>|<span data-ttu-id="59210-135">Se requiere una contraseña o patrón y cualquiera es aceptable.</span><span class="sxs-lookup"><span data-stu-id="59210-135">A password or pattern is required, and any is acceptable.</span></span>|





