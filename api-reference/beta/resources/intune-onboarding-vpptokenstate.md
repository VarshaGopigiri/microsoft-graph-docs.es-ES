---
title: tipo de enumeración vppTokenState
description: Estados posibles asociados con un token de programa de compra de volumen de Apple.
ms.openlocfilehash: 7180364063a48e1b0eeb2778ed4def7c0d3930a6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086381"
---
# <a name="vpptokenstate-enum-type"></a><span data-ttu-id="2a41d-103">tipo de enumeración vppTokenState</span><span class="sxs-lookup"><span data-stu-id="2a41d-103">vppTokenState enum type</span></span>

> <span data-ttu-id="2a41d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2a41d-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2a41d-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2a41d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2a41d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2a41d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2a41d-107">Estados posibles asociados con un token de programa de compra de volumen de Apple.</span><span class="sxs-lookup"><span data-stu-id="2a41d-107">Possible states associated with an Apple Volume Purchase Program token.</span></span>
## <a name="members"></a><span data-ttu-id="2a41d-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="2a41d-108">Members</span></span>
|<span data-ttu-id="2a41d-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="2a41d-109">Member</span></span>|<span data-ttu-id="2a41d-110">Valor</span><span class="sxs-lookup"><span data-stu-id="2a41d-110">Value</span></span>|<span data-ttu-id="2a41d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a41d-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2a41d-112">desconocido</span><span class="sxs-lookup"><span data-stu-id="2a41d-112">unknown</span></span>|<span data-ttu-id="2a41d-113">0</span><span class="sxs-lookup"><span data-stu-id="2a41d-113">0</span></span>|<span data-ttu-id="2a41d-114">Estado predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2a41d-114">Default state.</span></span>|
|<span data-ttu-id="2a41d-115">válido</span><span class="sxs-lookup"><span data-stu-id="2a41d-115">valid</span></span>|<span data-ttu-id="2a41d-116">1</span><span class="sxs-lookup"><span data-stu-id="2a41d-116">1</span></span>|<span data-ttu-id="2a41d-117">Símbolo (token) es válido.</span><span class="sxs-lookup"><span data-stu-id="2a41d-117">Token is valid.</span></span>|
|<span data-ttu-id="2a41d-118">expirado</span><span class="sxs-lookup"><span data-stu-id="2a41d-118">expired</span></span>|<span data-ttu-id="2a41d-119">2</span><span class="sxs-lookup"><span data-stu-id="2a41d-119">2</span></span>|<span data-ttu-id="2a41d-120">Símbolo (token) ha expirado.</span><span class="sxs-lookup"><span data-stu-id="2a41d-120">Token is expired.</span></span>|
|<span data-ttu-id="2a41d-121">No válido</span><span class="sxs-lookup"><span data-stu-id="2a41d-121">invalid</span></span>|<span data-ttu-id="2a41d-122">3</span><span class="sxs-lookup"><span data-stu-id="2a41d-122">3</span></span>|<span data-ttu-id="2a41d-123">Símbolo (token) no es válido.</span><span class="sxs-lookup"><span data-stu-id="2a41d-123">Token is invalid.</span></span>|
|<span data-ttu-id="2a41d-124">assignedToExternalMDM</span><span class="sxs-lookup"><span data-stu-id="2a41d-124">assignedToExternalMDM</span></span>|<span data-ttu-id="2a41d-125">4</span><span class="sxs-lookup"><span data-stu-id="2a41d-125">4</span></span>|<span data-ttu-id="2a41d-126">Símbolo (token) administrado por otro servicio de MDM.</span><span class="sxs-lookup"><span data-stu-id="2a41d-126">Token is managed by another MDM Service.</span></span>|





