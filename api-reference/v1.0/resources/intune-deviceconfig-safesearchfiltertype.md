---
title: tipo de enumeración safeSearchFilterType
description: Especifica qué nivel de búsqueda segura (filtrado de contenido para adultos) es necesario
ms.openlocfilehash: cf4f61e1b9e4e9f4fcfd94e6372ce517f3b735e6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030394"
---
# <a name="safesearchfiltertype-enum-type"></a><span data-ttu-id="6ec5c-103">tipo de enumeración safeSearchFilterType</span><span class="sxs-lookup"><span data-stu-id="6ec5c-103">safeSearchFilterType enum type</span></span>

> <span data-ttu-id="6ec5c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6ec5c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6ec5c-105">Especifica qué nivel de búsqueda segura (filtrado de contenido para adultos) es necesario</span><span class="sxs-lookup"><span data-stu-id="6ec5c-105">Specifies what level of safe search (filtering adult content) is required</span></span>
## <a name="members"></a><span data-ttu-id="6ec5c-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="6ec5c-106">Members</span></span>
|<span data-ttu-id="6ec5c-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="6ec5c-107">Member</span></span>|<span data-ttu-id="6ec5c-108">Valor</span><span class="sxs-lookup"><span data-stu-id="6ec5c-108">Value</span></span>|<span data-ttu-id="6ec5c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ec5c-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6ec5c-110">userDefined</span><span class="sxs-lookup"><span data-stu-id="6ec5c-110">userDefined</span></span>|<span data-ttu-id="6ec5c-111">0</span><span class="sxs-lookup"><span data-stu-id="6ec5c-111">0</span></span>|<span data-ttu-id="6ec5c-112">Definido por el usuario, valor predeterminado, sin intención.</span><span class="sxs-lookup"><span data-stu-id="6ec5c-112">User Defined, default value, no intent.</span></span>|
|<span data-ttu-id="6ec5c-113">estricto</span><span class="sxs-lookup"><span data-stu-id="6ec5c-113">strict</span></span>|<span data-ttu-id="6ec5c-114">1</span><span class="sxs-lookup"><span data-stu-id="6ec5c-114">1</span></span>|<span data-ttu-id="6ec5c-115">Estricto, mayor filtrado contra el contenido para adultos.</span><span class="sxs-lookup"><span data-stu-id="6ec5c-115">Strict, highest filtering against adult content.</span></span>|
|<span data-ttu-id="6ec5c-116">moderado</span><span class="sxs-lookup"><span data-stu-id="6ec5c-116">moderate</span></span>|<span data-ttu-id="6ec5c-117">2</span><span class="sxs-lookup"><span data-stu-id="6ec5c-117">2</span></span>|<span data-ttu-id="6ec5c-118">Moderar filtrado contra el contenido para adultos (no se filtrarán los resultados de búsqueda válido).</span><span class="sxs-lookup"><span data-stu-id="6ec5c-118">Moderate filtering against adult content (valid search results will not be filtered).</span></span>|



