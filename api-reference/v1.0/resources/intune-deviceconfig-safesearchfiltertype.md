---
title: tipo de enumeración safeSearchFilterType
description: Especifica qué nivel de búsqueda segura (filtrado de contenido para adultos) es necesario
author: tfitzmac
ms.openlocfilehash: eb0c7cfb862364ddc4703c89d19ea844ada6466d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27343200"
---
# <a name="safesearchfiltertype-enum-type"></a><span data-ttu-id="37ebf-103">tipo de enumeración safeSearchFilterType</span><span class="sxs-lookup"><span data-stu-id="37ebf-103">safeSearchFilterType enum type</span></span>

> <span data-ttu-id="37ebf-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="37ebf-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="37ebf-105">Especifica qué nivel de búsqueda segura (filtrado de contenido para adultos) es necesario</span><span class="sxs-lookup"><span data-stu-id="37ebf-105">Specifies what level of safe search (filtering adult content) is required</span></span>
## <a name="members"></a><span data-ttu-id="37ebf-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="37ebf-106">Members</span></span>
|<span data-ttu-id="37ebf-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="37ebf-107">Member</span></span>|<span data-ttu-id="37ebf-108">Valor</span><span class="sxs-lookup"><span data-stu-id="37ebf-108">Value</span></span>|<span data-ttu-id="37ebf-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="37ebf-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="37ebf-110">userDefined</span><span class="sxs-lookup"><span data-stu-id="37ebf-110">userDefined</span></span>|<span data-ttu-id="37ebf-111">0</span><span class="sxs-lookup"><span data-stu-id="37ebf-111">0</span></span>|<span data-ttu-id="37ebf-112">Definido por el usuario, valor predeterminado, sin intención.</span><span class="sxs-lookup"><span data-stu-id="37ebf-112">User Defined, default value, no intent.</span></span>|
|<span data-ttu-id="37ebf-113">estricto</span><span class="sxs-lookup"><span data-stu-id="37ebf-113">strict</span></span>|<span data-ttu-id="37ebf-114">1</span><span class="sxs-lookup"><span data-stu-id="37ebf-114">1</span></span>|<span data-ttu-id="37ebf-115">Estricto, mayor filtrado contra el contenido para adultos.</span><span class="sxs-lookup"><span data-stu-id="37ebf-115">Strict, highest filtering against adult content.</span></span>|
|<span data-ttu-id="37ebf-116">moderado</span><span class="sxs-lookup"><span data-stu-id="37ebf-116">moderate</span></span>|<span data-ttu-id="37ebf-117">2</span><span class="sxs-lookup"><span data-stu-id="37ebf-117">2</span></span>|<span data-ttu-id="37ebf-118">Moderar filtrado contra el contenido para adultos (no se filtrarán los resultados de búsqueda válido).</span><span class="sxs-lookup"><span data-stu-id="37ebf-118">Moderate filtering against adult content (valid search results will not be filtered).</span></span>|



