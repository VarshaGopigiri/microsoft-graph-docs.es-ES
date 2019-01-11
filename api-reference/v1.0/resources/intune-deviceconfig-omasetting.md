---
title: Tipo de recurso omaSetting
description: Definición de la configuración de OMA.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 86cb06b35a0f64052860c268764696a1db8459e3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888385"
---
# <a name="omasetting-resource-type"></a><span data-ttu-id="58384-103">Tipo de recurso omaSetting</span><span class="sxs-lookup"><span data-stu-id="58384-103">omaSetting resource type</span></span>

> <span data-ttu-id="58384-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="58384-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="58384-105">Definición de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="58384-105">OMA Settings definition.</span></span>
## <a name="properties"></a><span data-ttu-id="58384-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="58384-106">Properties</span></span>
|<span data-ttu-id="58384-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="58384-107">Property</span></span>|<span data-ttu-id="58384-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="58384-108">Type</span></span>|<span data-ttu-id="58384-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="58384-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="58384-110">displayName</span><span class="sxs-lookup"><span data-stu-id="58384-110">displayName</span></span>|<span data-ttu-id="58384-111">cadena</span><span class="sxs-lookup"><span data-stu-id="58384-111">String</span></span>|<span data-ttu-id="58384-112">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="58384-112">Display Name.</span></span>|
|<span data-ttu-id="58384-113">description</span><span class="sxs-lookup"><span data-stu-id="58384-113">description</span></span>|<span data-ttu-id="58384-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="58384-114">String</span></span>|<span data-ttu-id="58384-115">Descripción.</span><span class="sxs-lookup"><span data-stu-id="58384-115">Description.</span></span>|
|<span data-ttu-id="58384-116">omaUri</span><span class="sxs-lookup"><span data-stu-id="58384-116">omaUri</span></span>|<span data-ttu-id="58384-117">cadena</span><span class="sxs-lookup"><span data-stu-id="58384-117">String</span></span>|<span data-ttu-id="58384-118">OMA.</span><span class="sxs-lookup"><span data-stu-id="58384-118">OMA.</span></span>|

## <a name="relationships"></a><span data-ttu-id="58384-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="58384-119">Relationships</span></span>
<span data-ttu-id="58384-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="58384-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="58384-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="58384-121">JSON Representation</span></span>
<span data-ttu-id="58384-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="58384-122">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.omaSetting"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSetting",
  "displayName": "String",
  "description": "String",
  "omaUri": "String"
}
```



