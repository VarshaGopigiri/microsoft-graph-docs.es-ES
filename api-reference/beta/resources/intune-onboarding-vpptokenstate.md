---
title: tipo de enumeración vppTokenState
description: Estados posibles asociados con un token de programa de compra de volumen de Apple.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: b91090f64340e398bf9d48aff3741941fc0d778a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27844838"
---
# <a name="vpptokenstate-enum-type"></a><span data-ttu-id="145eb-103">tipo de enumeración vppTokenState</span><span class="sxs-lookup"><span data-stu-id="145eb-103">vppTokenState enum type</span></span>

> <span data-ttu-id="145eb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="145eb-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="145eb-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="145eb-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="145eb-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="145eb-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="145eb-107">Estados posibles asociados con un token de programa de compra de volumen de Apple.</span><span class="sxs-lookup"><span data-stu-id="145eb-107">Possible states associated with an Apple Volume Purchase Program token.</span></span>
## <a name="members"></a><span data-ttu-id="145eb-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="145eb-108">Members</span></span>
|<span data-ttu-id="145eb-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="145eb-109">Member</span></span>|<span data-ttu-id="145eb-110">Valor</span><span class="sxs-lookup"><span data-stu-id="145eb-110">Value</span></span>|<span data-ttu-id="145eb-111">Description</span><span class="sxs-lookup"><span data-stu-id="145eb-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="145eb-112">desconocido</span><span class="sxs-lookup"><span data-stu-id="145eb-112">unknown</span></span>|<span data-ttu-id="145eb-113">0</span><span class="sxs-lookup"><span data-stu-id="145eb-113">0</span></span>|<span data-ttu-id="145eb-114">Estado predeterminado.</span><span class="sxs-lookup"><span data-stu-id="145eb-114">Default state.</span></span>|
|<span data-ttu-id="145eb-115">válido</span><span class="sxs-lookup"><span data-stu-id="145eb-115">valid</span></span>|<span data-ttu-id="145eb-116">1</span><span class="sxs-lookup"><span data-stu-id="145eb-116">1</span></span>|<span data-ttu-id="145eb-117">Símbolo (token) es válido.</span><span class="sxs-lookup"><span data-stu-id="145eb-117">Token is valid.</span></span>|
|<span data-ttu-id="145eb-118">expirado</span><span class="sxs-lookup"><span data-stu-id="145eb-118">expired</span></span>|<span data-ttu-id="145eb-119">2</span><span class="sxs-lookup"><span data-stu-id="145eb-119">2</span></span>|<span data-ttu-id="145eb-120">Símbolo (token) ha expirado.</span><span class="sxs-lookup"><span data-stu-id="145eb-120">Token is expired.</span></span>|
|<span data-ttu-id="145eb-121">No válido</span><span class="sxs-lookup"><span data-stu-id="145eb-121">invalid</span></span>|<span data-ttu-id="145eb-122">3</span><span class="sxs-lookup"><span data-stu-id="145eb-122">3</span></span>|<span data-ttu-id="145eb-123">Símbolo (token) no es válido.</span><span class="sxs-lookup"><span data-stu-id="145eb-123">Token is invalid.</span></span>|
|<span data-ttu-id="145eb-124">assignedToExternalMDM</span><span class="sxs-lookup"><span data-stu-id="145eb-124">assignedToExternalMDM</span></span>|<span data-ttu-id="145eb-125">4</span><span class="sxs-lookup"><span data-stu-id="145eb-125">4</span></span>|<span data-ttu-id="145eb-126">Símbolo (token) administrado por otro servicio de MDM.</span><span class="sxs-lookup"><span data-stu-id="145eb-126">Token is managed by another MDM Service.</span></span>|





