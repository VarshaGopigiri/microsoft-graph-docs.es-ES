---
title: tipo de enumeración appListType
description: Posibles valores de la lista de aplicaciones de cumplimiento.
ms.openlocfilehash: 2733723252f3b8f03cf08fda6d0b09f207ae5550
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032345"
---
# <a name="applisttype-enum-type"></a><span data-ttu-id="5e55c-103">tipo de enumeración appListType</span><span class="sxs-lookup"><span data-stu-id="5e55c-103">appListType enum type</span></span>

> <span data-ttu-id="5e55c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5e55c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5e55c-105">Posibles valores de la lista de aplicaciones de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="5e55c-105">Possible values of the compliance app list.</span></span>
## <a name="members"></a><span data-ttu-id="5e55c-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="5e55c-106">Members</span></span>
|<span data-ttu-id="5e55c-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="5e55c-107">Member</span></span>|<span data-ttu-id="5e55c-108">Valor</span><span class="sxs-lookup"><span data-stu-id="5e55c-108">Value</span></span>|<span data-ttu-id="5e55c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e55c-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5e55c-110">ninguno</span><span class="sxs-lookup"><span data-stu-id="5e55c-110">none</span></span>|<span data-ttu-id="5e55c-111">0</span><span class="sxs-lookup"><span data-stu-id="5e55c-111">0</span></span>|<span data-ttu-id="5e55c-112">Valor predeterminado, sin intención.</span><span class="sxs-lookup"><span data-stu-id="5e55c-112">Default value, no intent.</span></span>|
|<span data-ttu-id="5e55c-113">appsInListCompliant</span><span class="sxs-lookup"><span data-stu-id="5e55c-113">appsInListCompliant</span></span>|<span data-ttu-id="5e55c-114">1</span><span class="sxs-lookup"><span data-stu-id="5e55c-114">1</span></span>|<span data-ttu-id="5e55c-115">La lista representa las aplicaciones que se considerarán compatibles con (solo son compatibles con las aplicaciones de la lista).</span><span class="sxs-lookup"><span data-stu-id="5e55c-115">The list represents the apps that will be considered compliant (only apps on the list are compliant).</span></span>|
|<span data-ttu-id="5e55c-116">appsNotInListCompliant</span><span class="sxs-lookup"><span data-stu-id="5e55c-116">appsNotInListCompliant</span></span>|<span data-ttu-id="5e55c-117">2</span><span class="sxs-lookup"><span data-stu-id="5e55c-117">2</span></span>|<span data-ttu-id="5e55c-118">La lista representa las aplicaciones que se considerarán no conformes (todas las aplicaciones son compatibles excepto en la lista de aplicaciones).</span><span class="sxs-lookup"><span data-stu-id="5e55c-118">The list represents the apps that will be considered non compliant (all apps are compliant except apps on the list).</span></span>|



