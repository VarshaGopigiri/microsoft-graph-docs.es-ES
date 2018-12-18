---
title: tipo de enumeración androidRequiredPasswordType
description: Tipo de contraseña requerida para Android.
author: tfitzmac
ms.openlocfilehash: e08df0ef61b6d60227f9dec2382a57884c2f4bdf
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27355989"
---
# <a name="androidrequiredpasswordtype-enum-type"></a><span data-ttu-id="16ea8-103">tipo de enumeración androidRequiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="16ea8-103">androidRequiredPasswordType enum type</span></span>

> <span data-ttu-id="16ea8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="16ea8-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="16ea8-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="16ea8-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="16ea8-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="16ea8-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="16ea8-107">Tipo de contraseña requerida para Android.</span><span class="sxs-lookup"><span data-stu-id="16ea8-107">Android required password type.</span></span>
## <a name="members"></a><span data-ttu-id="16ea8-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="16ea8-108">Members</span></span>
|<span data-ttu-id="16ea8-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="16ea8-109">Member</span></span>|<span data-ttu-id="16ea8-110">Valor</span><span class="sxs-lookup"><span data-stu-id="16ea8-110">Value</span></span>|<span data-ttu-id="16ea8-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="16ea8-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="16ea8-112">deviceDefault</span><span class="sxs-lookup"><span data-stu-id="16ea8-112">deviceDefault</span></span>|<span data-ttu-id="16ea8-113">0</span><span class="sxs-lookup"><span data-stu-id="16ea8-113">0</span></span>|<span data-ttu-id="16ea8-114">Valor predeterminado de dispositivo, sin intención.</span><span class="sxs-lookup"><span data-stu-id="16ea8-114">Device default value, no intent.</span></span>|
|<span data-ttu-id="16ea8-115">alfabéticos</span><span class="sxs-lookup"><span data-stu-id="16ea8-115">alphabetic</span></span>|<span data-ttu-id="16ea8-116">1</span><span class="sxs-lookup"><span data-stu-id="16ea8-116">1</span></span>|<span data-ttu-id="16ea8-117">Contraseña alfabético requerida.</span><span class="sxs-lookup"><span data-stu-id="16ea8-117">Alphabetic password required.</span></span>|
|<span data-ttu-id="16ea8-118">alfanuméricos</span><span class="sxs-lookup"><span data-stu-id="16ea8-118">alphanumeric</span></span>|<span data-ttu-id="16ea8-119">2</span><span class="sxs-lookup"><span data-stu-id="16ea8-119">2</span></span>|<span data-ttu-id="16ea8-120">Se requiere una contraseña alfanumérica.</span><span class="sxs-lookup"><span data-stu-id="16ea8-120">Alphanumeric password required.</span></span>|
|<span data-ttu-id="16ea8-121">alphanumericWithSymbols</span><span class="sxs-lookup"><span data-stu-id="16ea8-121">alphanumericWithSymbols</span></span>|<span data-ttu-id="16ea8-122">3</span><span class="sxs-lookup"><span data-stu-id="16ea8-122">3</span></span>|<span data-ttu-id="16ea8-123">Alfanumérico con contraseña símbolos requerida.</span><span class="sxs-lookup"><span data-stu-id="16ea8-123">Alphanumeric with symbols password required.</span></span>|
|<span data-ttu-id="16ea8-124">lowSecurityBiometric</span><span class="sxs-lookup"><span data-stu-id="16ea8-124">lowSecurityBiometric</span></span>|<span data-ttu-id="16ea8-125">4</span><span class="sxs-lookup"><span data-stu-id="16ea8-125">4</span></span>|<span data-ttu-id="16ea8-126">Contraseña biométrica en función de baja seguridad requerida.</span><span class="sxs-lookup"><span data-stu-id="16ea8-126">Low security biometrics based password required.</span></span>|
|<span data-ttu-id="16ea8-127">numérico</span><span class="sxs-lookup"><span data-stu-id="16ea8-127">numeric</span></span>|<span data-ttu-id="16ea8-128">5</span><span class="sxs-lookup"><span data-stu-id="16ea8-128">5</span></span>|<span data-ttu-id="16ea8-129">Contraseña numérica requerida.</span><span class="sxs-lookup"><span data-stu-id="16ea8-129">Numeric password required.</span></span>|
|<span data-ttu-id="16ea8-130">numericComplex</span><span class="sxs-lookup"><span data-stu-id="16ea8-130">numericComplex</span></span>|<span data-ttu-id="16ea8-131">6</span><span class="sxs-lookup"><span data-stu-id="16ea8-131">6</span></span>|<span data-ttu-id="16ea8-132">Contraseña compleja numérico requerida.</span><span class="sxs-lookup"><span data-stu-id="16ea8-132">Numeric complex password required.</span></span>|
|<span data-ttu-id="16ea8-133">cualquiera</span><span class="sxs-lookup"><span data-stu-id="16ea8-133">any</span></span>|<span data-ttu-id="16ea8-134">7</span><span class="sxs-lookup"><span data-stu-id="16ea8-134">7</span></span>|<span data-ttu-id="16ea8-135">Se requiere una contraseña o patrón y cualquiera es aceptable.</span><span class="sxs-lookup"><span data-stu-id="16ea8-135">A password or pattern is required, and any is acceptable.</span></span>|





