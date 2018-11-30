---
title: tipo de enumeración vppTokenState
description: Estados posibles asociados con un token de programa de compra de volumen de Apple.
ms.openlocfilehash: 74d7ea2e0ca2dd03b82b71bea2ab5300214b095d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028852"
---
# <a name="vpptokenstate-enum-type"></a><span data-ttu-id="090ec-103">tipo de enumeración vppTokenState</span><span class="sxs-lookup"><span data-stu-id="090ec-103">vppTokenState enum type</span></span>

> <span data-ttu-id="090ec-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="090ec-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="090ec-105">Estados posibles asociados con un token de programa de compra de volumen de Apple.</span><span class="sxs-lookup"><span data-stu-id="090ec-105">Possible states associated with an Apple Volume Purchase Program token.</span></span>
## <a name="members"></a><span data-ttu-id="090ec-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="090ec-106">Members</span></span>
|<span data-ttu-id="090ec-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="090ec-107">Member</span></span>|<span data-ttu-id="090ec-108">Valor</span><span class="sxs-lookup"><span data-stu-id="090ec-108">Value</span></span>|<span data-ttu-id="090ec-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="090ec-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="090ec-110">desconocido</span><span class="sxs-lookup"><span data-stu-id="090ec-110">unknown</span></span>|<span data-ttu-id="090ec-111">0</span><span class="sxs-lookup"><span data-stu-id="090ec-111">0</span></span>|<span data-ttu-id="090ec-112">Estado predeterminado.</span><span class="sxs-lookup"><span data-stu-id="090ec-112">Default state.</span></span>|
|<span data-ttu-id="090ec-113">válido</span><span class="sxs-lookup"><span data-stu-id="090ec-113">valid</span></span>|<span data-ttu-id="090ec-114">1</span><span class="sxs-lookup"><span data-stu-id="090ec-114">1</span></span>|<span data-ttu-id="090ec-115">Símbolo (token) es válido.</span><span class="sxs-lookup"><span data-stu-id="090ec-115">Token is valid.</span></span>|
|<span data-ttu-id="090ec-116">expirado</span><span class="sxs-lookup"><span data-stu-id="090ec-116">expired</span></span>|<span data-ttu-id="090ec-117">2</span><span class="sxs-lookup"><span data-stu-id="090ec-117">2</span></span>|<span data-ttu-id="090ec-118">Símbolo (token) ha expirado.</span><span class="sxs-lookup"><span data-stu-id="090ec-118">Token is expired.</span></span>|
|<span data-ttu-id="090ec-119">No válido</span><span class="sxs-lookup"><span data-stu-id="090ec-119">invalid</span></span>|<span data-ttu-id="090ec-120">3</span><span class="sxs-lookup"><span data-stu-id="090ec-120">3</span></span>|<span data-ttu-id="090ec-121">Símbolo (token) no es válido.</span><span class="sxs-lookup"><span data-stu-id="090ec-121">Token is invalid.</span></span>|
|<span data-ttu-id="090ec-122">assignedToExternalMDM</span><span class="sxs-lookup"><span data-stu-id="090ec-122">assignedToExternalMDM</span></span>|<span data-ttu-id="090ec-123">4</span><span class="sxs-lookup"><span data-stu-id="090ec-123">4</span></span>|<span data-ttu-id="090ec-124">Símbolo (token) administrado por otro servicio de MDM.</span><span class="sxs-lookup"><span data-stu-id="090ec-124">Token is managed by another MDM Service.</span></span>|



