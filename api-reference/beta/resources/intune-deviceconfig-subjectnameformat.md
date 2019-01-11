---
title: tipo de enumeración subjectNameFormat
description: Opciones de formato de nombre de sujeto.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 85a11e8690c360e405df2453229a039ea9f9b1dd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27821339"
---
# <a name="subjectnameformat-enum-type"></a><span data-ttu-id="05fd8-103">tipo de enumeración subjectNameFormat</span><span class="sxs-lookup"><span data-stu-id="05fd8-103">subjectNameFormat enum type</span></span>

> <span data-ttu-id="05fd8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="05fd8-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="05fd8-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="05fd8-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="05fd8-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="05fd8-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="05fd8-107">Opciones de formato de nombre de sujeto.</span><span class="sxs-lookup"><span data-stu-id="05fd8-107">Subject Name Format Options.</span></span>
## <a name="members"></a><span data-ttu-id="05fd8-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="05fd8-108">Members</span></span>
|<span data-ttu-id="05fd8-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="05fd8-109">Member</span></span>|<span data-ttu-id="05fd8-110">Valor</span><span class="sxs-lookup"><span data-stu-id="05fd8-110">Value</span></span>|<span data-ttu-id="05fd8-111">Description</span><span class="sxs-lookup"><span data-stu-id="05fd8-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="05fd8-112">commonName</span><span class="sxs-lookup"><span data-stu-id="05fd8-112">commonName</span></span>|<span data-ttu-id="05fd8-113">0</span><span class="sxs-lookup"><span data-stu-id="05fd8-113">0</span></span>|<span data-ttu-id="05fd8-114">Nombre común.</span><span class="sxs-lookup"><span data-stu-id="05fd8-114">Common name.</span></span>|
|<span data-ttu-id="05fd8-115">commonNameIncludingEmail</span><span class="sxs-lookup"><span data-stu-id="05fd8-115">commonNameIncludingEmail</span></span>|<span data-ttu-id="05fd8-116">1</span><span class="sxs-lookup"><span data-stu-id="05fd8-116">1</span></span>|<span data-ttu-id="05fd8-117">Nombre común incluido el correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="05fd8-117">Common Name Including Email.</span></span>|
|<span data-ttu-id="05fd8-118">commonNameAsEmail</span><span class="sxs-lookup"><span data-stu-id="05fd8-118">commonNameAsEmail</span></span>|<span data-ttu-id="05fd8-119">2</span><span class="sxs-lookup"><span data-stu-id="05fd8-119">2</span></span>|<span data-ttu-id="05fd8-120">Nombre común como correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="05fd8-120">Common Name As Email.</span></span>|
|<span data-ttu-id="05fd8-121">personalizado</span><span class="sxs-lookup"><span data-stu-id="05fd8-121">custom</span></span>|<span data-ttu-id="05fd8-122">3</span><span class="sxs-lookup"><span data-stu-id="05fd8-122">3</span></span>|<span data-ttu-id="05fd8-123">Formato de nombre de sujeto personalizado.</span><span class="sxs-lookup"><span data-stu-id="05fd8-123">Custom subject name format.</span></span>|
|<span data-ttu-id="05fd8-124">commonNameAsIMEI</span><span class="sxs-lookup"><span data-stu-id="05fd8-124">commonNameAsIMEI</span></span>|<span data-ttu-id="05fd8-125">5</span><span class="sxs-lookup"><span data-stu-id="05fd8-125">5</span></span>|<span data-ttu-id="05fd8-126">Nombre común como IMEI.</span><span class="sxs-lookup"><span data-stu-id="05fd8-126">Common Name As IMEI.</span></span>|
|<span data-ttu-id="05fd8-127">commonNameAsSerialNumber</span><span class="sxs-lookup"><span data-stu-id="05fd8-127">commonNameAsSerialNumber</span></span>|<span data-ttu-id="05fd8-128">6</span><span class="sxs-lookup"><span data-stu-id="05fd8-128">6</span></span>|<span data-ttu-id="05fd8-129">Nombre común como número de serie.</span><span class="sxs-lookup"><span data-stu-id="05fd8-129">Common Name As Serial Number.</span></span>|
|<span data-ttu-id="05fd8-130">commonNameAsAadDeviceId</span><span class="sxs-lookup"><span data-stu-id="05fd8-130">commonNameAsAadDeviceId</span></span>|<span data-ttu-id="05fd8-131">7</span><span class="sxs-lookup"><span data-stu-id="05fd8-131">7</span></span>|<span data-ttu-id="05fd8-132">Nombre común como número de serie.</span><span class="sxs-lookup"><span data-stu-id="05fd8-132">Common Name As Serial Number.</span></span>|
|<span data-ttu-id="05fd8-133">commonNameAsIntuneDeviceId</span><span class="sxs-lookup"><span data-stu-id="05fd8-133">commonNameAsIntuneDeviceId</span></span>|<span data-ttu-id="05fd8-134">8</span><span class="sxs-lookup"><span data-stu-id="05fd8-134">8</span></span>|<span data-ttu-id="05fd8-135">Nombre común como número de serie.</span><span class="sxs-lookup"><span data-stu-id="05fd8-135">Common Name As Serial Number.</span></span>|
|<span data-ttu-id="05fd8-136">commonNameAsDurableDeviceId</span><span class="sxs-lookup"><span data-stu-id="05fd8-136">commonNameAsDurableDeviceId</span></span>|<span data-ttu-id="05fd8-137">9</span><span class="sxs-lookup"><span data-stu-id="05fd8-137">9</span></span>|<span data-ttu-id="05fd8-138">Nombre común como número de serie.</span><span class="sxs-lookup"><span data-stu-id="05fd8-138">Common Name As Serial Number.</span></span>|





