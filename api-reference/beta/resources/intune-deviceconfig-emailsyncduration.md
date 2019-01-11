---
title: tipo de enumeración emailSyncDuration
description: Valores posibles para la duración de la sincronización de correo electrónico.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: d83a1ceb82820ddc44d8753e8ed05e00de09e36e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27819386"
---
# <a name="emailsyncduration-enum-type"></a><span data-ttu-id="f341a-103">tipo de enumeración emailSyncDuration</span><span class="sxs-lookup"><span data-stu-id="f341a-103">emailSyncDuration enum type</span></span>

> <span data-ttu-id="f341a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f341a-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f341a-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f341a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f341a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f341a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f341a-107">Valores posibles para la duración de la sincronización de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f341a-107">Possible values for email sync duration.</span></span>
## <a name="members"></a><span data-ttu-id="f341a-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f341a-108">Members</span></span>
|<span data-ttu-id="f341a-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="f341a-109">Member</span></span>|<span data-ttu-id="f341a-110">Valor</span><span class="sxs-lookup"><span data-stu-id="f341a-110">Value</span></span>|<span data-ttu-id="f341a-111">Description</span><span class="sxs-lookup"><span data-stu-id="f341a-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f341a-112">userDefined</span><span class="sxs-lookup"><span data-stu-id="f341a-112">userDefined</span></span>|<span data-ttu-id="f341a-113">0</span><span class="sxs-lookup"><span data-stu-id="f341a-113">0</span></span>|<span data-ttu-id="f341a-114">Definido por el usuario, valor predeterminado, sin intención.</span><span class="sxs-lookup"><span data-stu-id="f341a-114">User Defined, default value, no intent.</span></span>|
|<span data-ttu-id="f341a-115">undía</span><span class="sxs-lookup"><span data-stu-id="f341a-115">oneDay</span></span>|<span data-ttu-id="f341a-116">1</span><span class="sxs-lookup"><span data-stu-id="f341a-116">1</span></span>|<span data-ttu-id="f341a-117">Sincronización de un día de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f341a-117">Sync one day of email.</span></span>|
|<span data-ttu-id="f341a-118">tresdías</span><span class="sxs-lookup"><span data-stu-id="f341a-118">threeDays</span></span>|<span data-ttu-id="f341a-119">2</span><span class="sxs-lookup"><span data-stu-id="f341a-119">2</span></span>|<span data-ttu-id="f341a-120">Sincronización de tres días de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f341a-120">Sync three days of email.</span></span>|
|<span data-ttu-id="f341a-121">unasemana</span><span class="sxs-lookup"><span data-stu-id="f341a-121">oneWeek</span></span>|<span data-ttu-id="f341a-122">3</span><span class="sxs-lookup"><span data-stu-id="f341a-122">3</span></span>|<span data-ttu-id="f341a-123">Sincronización de una semana de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f341a-123">Sync one week of email.</span></span>|
|<span data-ttu-id="f341a-124">twoWeeks</span><span class="sxs-lookup"><span data-stu-id="f341a-124">twoWeeks</span></span>|<span data-ttu-id="f341a-125">4</span><span class="sxs-lookup"><span data-stu-id="f341a-125">4</span></span>|<span data-ttu-id="f341a-126">Sincronizar dos semanas de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f341a-126">Sync two weeks of email.</span></span>|
|<span data-ttu-id="f341a-127">oneMonth</span><span class="sxs-lookup"><span data-stu-id="f341a-127">oneMonth</span></span>|<span data-ttu-id="f341a-128">5</span><span class="sxs-lookup"><span data-stu-id="f341a-128">5</span></span>|<span data-ttu-id="f341a-129">Sincronización de un mes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f341a-129">Sync one month of email.</span></span>|
|<span data-ttu-id="f341a-130">ilimitado</span><span class="sxs-lookup"><span data-stu-id="f341a-130">unlimited</span></span>|<span data-ttu-id="f341a-131">6</span><span class="sxs-lookup"><span data-stu-id="f341a-131">6</span></span>|<span data-ttu-id="f341a-132">Sincronizar una duración ilimitada de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f341a-132">Sync an unlimited duration of email.</span></span>|





