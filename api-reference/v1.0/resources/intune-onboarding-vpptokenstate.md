---
title: tipo de enumeración vppTokenState
description: Estados posibles asociados con un token de programa de compra de volumen de Apple.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 6bdeb73b6491f3960ce30db91a35d06c0f8ffaf1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27986666"
---
# <a name="vpptokenstate-enum-type"></a><span data-ttu-id="11029-103">tipo de enumeración vppTokenState</span><span class="sxs-lookup"><span data-stu-id="11029-103">vppTokenState enum type</span></span>

> <span data-ttu-id="11029-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="11029-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="11029-105">Estados posibles asociados con un token de programa de compra de volumen de Apple.</span><span class="sxs-lookup"><span data-stu-id="11029-105">Possible states associated with an Apple Volume Purchase Program token.</span></span>
## <a name="members"></a><span data-ttu-id="11029-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="11029-106">Members</span></span>
|<span data-ttu-id="11029-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="11029-107">Member</span></span>|<span data-ttu-id="11029-108">Valor</span><span class="sxs-lookup"><span data-stu-id="11029-108">Value</span></span>|<span data-ttu-id="11029-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="11029-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="11029-110">desconocido</span><span class="sxs-lookup"><span data-stu-id="11029-110">unknown</span></span>|<span data-ttu-id="11029-111">0</span><span class="sxs-lookup"><span data-stu-id="11029-111">0</span></span>|<span data-ttu-id="11029-112">Estado predeterminado.</span><span class="sxs-lookup"><span data-stu-id="11029-112">Default state.</span></span>|
|<span data-ttu-id="11029-113">válido</span><span class="sxs-lookup"><span data-stu-id="11029-113">valid</span></span>|<span data-ttu-id="11029-114">1</span><span class="sxs-lookup"><span data-stu-id="11029-114">1</span></span>|<span data-ttu-id="11029-115">Símbolo (token) es válido.</span><span class="sxs-lookup"><span data-stu-id="11029-115">Token is valid.</span></span>|
|<span data-ttu-id="11029-116">expirado</span><span class="sxs-lookup"><span data-stu-id="11029-116">expired</span></span>|<span data-ttu-id="11029-117">2</span><span class="sxs-lookup"><span data-stu-id="11029-117">2</span></span>|<span data-ttu-id="11029-118">Símbolo (token) ha expirado.</span><span class="sxs-lookup"><span data-stu-id="11029-118">Token is expired.</span></span>|
|<span data-ttu-id="11029-119">No válido</span><span class="sxs-lookup"><span data-stu-id="11029-119">invalid</span></span>|<span data-ttu-id="11029-120">3</span><span class="sxs-lookup"><span data-stu-id="11029-120">3</span></span>|<span data-ttu-id="11029-121">Símbolo (token) no es válido.</span><span class="sxs-lookup"><span data-stu-id="11029-121">Token is invalid.</span></span>|
|<span data-ttu-id="11029-122">assignedToExternalMDM</span><span class="sxs-lookup"><span data-stu-id="11029-122">assignedToExternalMDM</span></span>|<span data-ttu-id="11029-123">4</span><span class="sxs-lookup"><span data-stu-id="11029-123">4</span></span>|<span data-ttu-id="11029-124">Símbolo (token) administrado por otro servicio de MDM.</span><span class="sxs-lookup"><span data-stu-id="11029-124">Token is managed by another MDM Service.</span></span>|



