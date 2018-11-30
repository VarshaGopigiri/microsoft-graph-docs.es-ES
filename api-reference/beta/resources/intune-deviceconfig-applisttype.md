---
title: tipo de enumeración appListType
description: Posibles valores de la lista de aplicaciones de cumplimiento.
ms.openlocfilehash: 3fcfecde8dbc9efe92f842e9d2b45b7f1579c217
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088173"
---
# <a name="applisttype-enum-type"></a><span data-ttu-id="5c773-103">tipo de enumeración appListType</span><span class="sxs-lookup"><span data-stu-id="5c773-103">appListType enum type</span></span>

> <span data-ttu-id="5c773-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5c773-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5c773-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5c773-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5c773-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5c773-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5c773-107">Posibles valores de la lista de aplicaciones de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="5c773-107">Possible values of the compliance app list.</span></span>
## <a name="members"></a><span data-ttu-id="5c773-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="5c773-108">Members</span></span>
|<span data-ttu-id="5c773-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="5c773-109">Member</span></span>|<span data-ttu-id="5c773-110">Valor</span><span class="sxs-lookup"><span data-stu-id="5c773-110">Value</span></span>|<span data-ttu-id="5c773-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c773-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5c773-112">ninguno</span><span class="sxs-lookup"><span data-stu-id="5c773-112">none</span></span>|<span data-ttu-id="5c773-113">0</span><span class="sxs-lookup"><span data-stu-id="5c773-113">0</span></span>|<span data-ttu-id="5c773-114">Valor predeterminado, sin intención.</span><span class="sxs-lookup"><span data-stu-id="5c773-114">Default value, no intent.</span></span>|
|<span data-ttu-id="5c773-115">appsInListCompliant</span><span class="sxs-lookup"><span data-stu-id="5c773-115">appsInListCompliant</span></span>|<span data-ttu-id="5c773-116">1</span><span class="sxs-lookup"><span data-stu-id="5c773-116">1</span></span>|<span data-ttu-id="5c773-117">La lista representa las aplicaciones que se considerarán compatibles con (solo son compatibles con las aplicaciones de la lista).</span><span class="sxs-lookup"><span data-stu-id="5c773-117">The list represents the apps that will be considered compliant (only apps on the list are compliant).</span></span>|
|<span data-ttu-id="5c773-118">appsNotInListCompliant</span><span class="sxs-lookup"><span data-stu-id="5c773-118">appsNotInListCompliant</span></span>|<span data-ttu-id="5c773-119">2</span><span class="sxs-lookup"><span data-stu-id="5c773-119">2</span></span>|<span data-ttu-id="5c773-120">La lista representa las aplicaciones que se considerarán no conformes (todas las aplicaciones son compatibles excepto en la lista de aplicaciones).</span><span class="sxs-lookup"><span data-stu-id="5c773-120">The list represents the apps that will be considered non compliant (all apps are compliant except apps on the list).</span></span>|





