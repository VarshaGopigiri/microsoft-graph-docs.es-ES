---
title: tipo de enumeración androidRequiredPasswordType
description: Tipo de contraseña requerida para Android.
ms.openlocfilehash: f4f95308791aa443b6eb4b4fd38c70fe2d47b4b4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031694"
---
# <a name="androidrequiredpasswordtype-enum-type"></a><span data-ttu-id="a726c-103">tipo de enumeración androidRequiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="a726c-103">androidRequiredPasswordType enum type</span></span>

> <span data-ttu-id="a726c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a726c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a726c-105">Tipo de contraseña requerida para Android.</span><span class="sxs-lookup"><span data-stu-id="a726c-105">Android required password type.</span></span>
## <a name="members"></a><span data-ttu-id="a726c-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="a726c-106">Members</span></span>
|<span data-ttu-id="a726c-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="a726c-107">Member</span></span>|<span data-ttu-id="a726c-108">Valor</span><span class="sxs-lookup"><span data-stu-id="a726c-108">Value</span></span>|<span data-ttu-id="a726c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a726c-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a726c-110">deviceDefault</span><span class="sxs-lookup"><span data-stu-id="a726c-110">deviceDefault</span></span>|<span data-ttu-id="a726c-111">0</span><span class="sxs-lookup"><span data-stu-id="a726c-111">0</span></span>|<span data-ttu-id="a726c-112">Valor predeterminado de dispositivo, sin intención.</span><span class="sxs-lookup"><span data-stu-id="a726c-112">Device default value, no intent.</span></span>|
|<span data-ttu-id="a726c-113">alfabéticos</span><span class="sxs-lookup"><span data-stu-id="a726c-113">alphabetic</span></span>|<span data-ttu-id="a726c-114">1</span><span class="sxs-lookup"><span data-stu-id="a726c-114">1</span></span>|<span data-ttu-id="a726c-115">Contraseña alfabético requerida.</span><span class="sxs-lookup"><span data-stu-id="a726c-115">Alphabetic password required.</span></span>|
|<span data-ttu-id="a726c-116">alfanuméricos</span><span class="sxs-lookup"><span data-stu-id="a726c-116">alphanumeric</span></span>|<span data-ttu-id="a726c-117">2</span><span class="sxs-lookup"><span data-stu-id="a726c-117">2</span></span>|<span data-ttu-id="a726c-118">Se requiere una contraseña alfanumérica.</span><span class="sxs-lookup"><span data-stu-id="a726c-118">Alphanumeric password required.</span></span>|
|<span data-ttu-id="a726c-119">alphanumericWithSymbols</span><span class="sxs-lookup"><span data-stu-id="a726c-119">alphanumericWithSymbols</span></span>|<span data-ttu-id="a726c-120">3</span><span class="sxs-lookup"><span data-stu-id="a726c-120">3</span></span>|<span data-ttu-id="a726c-121">Alfanumérico con contraseña símbolos requerida.</span><span class="sxs-lookup"><span data-stu-id="a726c-121">Alphanumeric with symbols password required.</span></span>|
|<span data-ttu-id="a726c-122">lowSecurityBiometric</span><span class="sxs-lookup"><span data-stu-id="a726c-122">lowSecurityBiometric</span></span>|<span data-ttu-id="a726c-123">4</span><span class="sxs-lookup"><span data-stu-id="a726c-123">4</span></span>|<span data-ttu-id="a726c-124">Contraseña biométrica en función de baja seguridad requerida.</span><span class="sxs-lookup"><span data-stu-id="a726c-124">Low security biometrics based password required.</span></span>|
|<span data-ttu-id="a726c-125">numérico</span><span class="sxs-lookup"><span data-stu-id="a726c-125">numeric</span></span>|<span data-ttu-id="a726c-126">5</span><span class="sxs-lookup"><span data-stu-id="a726c-126">5</span></span>|<span data-ttu-id="a726c-127">Contraseña numérica requerida.</span><span class="sxs-lookup"><span data-stu-id="a726c-127">Numeric password required.</span></span>|
|<span data-ttu-id="a726c-128">numericComplex</span><span class="sxs-lookup"><span data-stu-id="a726c-128">numericComplex</span></span>|<span data-ttu-id="a726c-129">6</span><span class="sxs-lookup"><span data-stu-id="a726c-129">6</span></span>|<span data-ttu-id="a726c-130">Contraseña compleja numérico requerida.</span><span class="sxs-lookup"><span data-stu-id="a726c-130">Numeric complex password required.</span></span>|
|<span data-ttu-id="a726c-131">cualquiera</span><span class="sxs-lookup"><span data-stu-id="a726c-131">any</span></span>|<span data-ttu-id="a726c-132">7</span><span class="sxs-lookup"><span data-stu-id="a726c-132">7</span></span>|<span data-ttu-id="a726c-133">Se requiere una contraseña o patrón y cualquiera es aceptable.</span><span class="sxs-lookup"><span data-stu-id="a726c-133">A password or pattern is required, and any is acceptable.</span></span>|



