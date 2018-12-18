---
title: tipo de enumeración safeSearchFilterType
description: Especifica qué nivel de búsqueda segura (filtrado de contenido para adultos) es necesario
author: tfitzmac
ms.openlocfilehash: 7bec68919b6af5d773c34caadaf0c1d85b0f5224
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27351418"
---
# <a name="safesearchfiltertype-enum-type"></a><span data-ttu-id="ab61c-103">tipo de enumeración safeSearchFilterType</span><span class="sxs-lookup"><span data-stu-id="ab61c-103">safeSearchFilterType enum type</span></span>

> <span data-ttu-id="ab61c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ab61c-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ab61c-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ab61c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ab61c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ab61c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ab61c-107">Especifica qué nivel de búsqueda segura (filtrado de contenido para adultos) es necesario</span><span class="sxs-lookup"><span data-stu-id="ab61c-107">Specifies what level of safe search (filtering adult content) is required</span></span>
## <a name="members"></a><span data-ttu-id="ab61c-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ab61c-108">Members</span></span>
|<span data-ttu-id="ab61c-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="ab61c-109">Member</span></span>|<span data-ttu-id="ab61c-110">Valor</span><span class="sxs-lookup"><span data-stu-id="ab61c-110">Value</span></span>|<span data-ttu-id="ab61c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab61c-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ab61c-112">userDefined</span><span class="sxs-lookup"><span data-stu-id="ab61c-112">userDefined</span></span>|<span data-ttu-id="ab61c-113">0</span><span class="sxs-lookup"><span data-stu-id="ab61c-113">0</span></span>|<span data-ttu-id="ab61c-114">Definido por el usuario, valor predeterminado, sin intención.</span><span class="sxs-lookup"><span data-stu-id="ab61c-114">User Defined, default value, no intent.</span></span>|
|<span data-ttu-id="ab61c-115">estricto</span><span class="sxs-lookup"><span data-stu-id="ab61c-115">strict</span></span>|<span data-ttu-id="ab61c-116">1</span><span class="sxs-lookup"><span data-stu-id="ab61c-116">1</span></span>|<span data-ttu-id="ab61c-117">Estricto, mayor filtrado contra el contenido para adultos.</span><span class="sxs-lookup"><span data-stu-id="ab61c-117">Strict, highest filtering against adult content.</span></span>|
|<span data-ttu-id="ab61c-118">moderado</span><span class="sxs-lookup"><span data-stu-id="ab61c-118">moderate</span></span>|<span data-ttu-id="ab61c-119">2</span><span class="sxs-lookup"><span data-stu-id="ab61c-119">2</span></span>|<span data-ttu-id="ab61c-120">Moderar filtrado contra el contenido para adultos (no se filtrarán los resultados de búsqueda válido).</span><span class="sxs-lookup"><span data-stu-id="ab61c-120">Moderate filtering against adult content (valid search results will not be filtered).</span></span>|





