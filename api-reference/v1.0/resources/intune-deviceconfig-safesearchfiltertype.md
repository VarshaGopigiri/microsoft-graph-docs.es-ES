---
title: tipo de enumeración safeSearchFilterType
description: Especifica qué nivel de búsqueda segura (filtrado de contenido para adultos) es necesario
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 788a266cdd0161ce1cfef426a7fcf4d9726e3324
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27964616"
---
# <a name="safesearchfiltertype-enum-type"></a><span data-ttu-id="00b06-103">tipo de enumeración safeSearchFilterType</span><span class="sxs-lookup"><span data-stu-id="00b06-103">safeSearchFilterType enum type</span></span>

> <span data-ttu-id="00b06-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="00b06-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="00b06-105">Especifica qué nivel de búsqueda segura (filtrado de contenido para adultos) es necesario</span><span class="sxs-lookup"><span data-stu-id="00b06-105">Specifies what level of safe search (filtering adult content) is required</span></span>
## <a name="members"></a><span data-ttu-id="00b06-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="00b06-106">Members</span></span>
|<span data-ttu-id="00b06-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="00b06-107">Member</span></span>|<span data-ttu-id="00b06-108">Valor</span><span class="sxs-lookup"><span data-stu-id="00b06-108">Value</span></span>|<span data-ttu-id="00b06-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="00b06-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="00b06-110">userDefined</span><span class="sxs-lookup"><span data-stu-id="00b06-110">userDefined</span></span>|<span data-ttu-id="00b06-111">0</span><span class="sxs-lookup"><span data-stu-id="00b06-111">0</span></span>|<span data-ttu-id="00b06-112">Definido por el usuario, valor predeterminado, sin intención.</span><span class="sxs-lookup"><span data-stu-id="00b06-112">User Defined, default value, no intent.</span></span>|
|<span data-ttu-id="00b06-113">estricto</span><span class="sxs-lookup"><span data-stu-id="00b06-113">strict</span></span>|<span data-ttu-id="00b06-114">1</span><span class="sxs-lookup"><span data-stu-id="00b06-114">1</span></span>|<span data-ttu-id="00b06-115">Estricto, mayor filtrado contra el contenido para adultos.</span><span class="sxs-lookup"><span data-stu-id="00b06-115">Strict, highest filtering against adult content.</span></span>|
|<span data-ttu-id="00b06-116">moderado</span><span class="sxs-lookup"><span data-stu-id="00b06-116">moderate</span></span>|<span data-ttu-id="00b06-117">2</span><span class="sxs-lookup"><span data-stu-id="00b06-117">2</span></span>|<span data-ttu-id="00b06-118">Moderar filtrado contra el contenido para adultos (no se filtrarán los resultados de búsqueda válido).</span><span class="sxs-lookup"><span data-stu-id="00b06-118">Moderate filtering against adult content (valid search results will not be filtered).</span></span>|



