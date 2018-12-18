---
title: Tipo de recurso omaSetting
description: Definición de la configuración de OMA.
author: tfitzmac
ms.openlocfilehash: 564912635fbcd5e2846965d3546a3830119db252
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27340890"
---
# <a name="omasetting-resource-type"></a><span data-ttu-id="ec206-103">Tipo de recurso omaSetting</span><span class="sxs-lookup"><span data-stu-id="ec206-103">omaSetting resource type</span></span>

> <span data-ttu-id="ec206-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ec206-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ec206-105">Definición de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="ec206-105">OMA Settings definition.</span></span>
## <a name="properties"></a><span data-ttu-id="ec206-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ec206-106">Properties</span></span>
|<span data-ttu-id="ec206-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ec206-107">Property</span></span>|<span data-ttu-id="ec206-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="ec206-108">Type</span></span>|<span data-ttu-id="ec206-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec206-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ec206-110">displayName</span><span class="sxs-lookup"><span data-stu-id="ec206-110">displayName</span></span>|<span data-ttu-id="ec206-111">cadena</span><span class="sxs-lookup"><span data-stu-id="ec206-111">String</span></span>|<span data-ttu-id="ec206-112">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="ec206-112">Display Name.</span></span>|
|<span data-ttu-id="ec206-113">description</span><span class="sxs-lookup"><span data-stu-id="ec206-113">description</span></span>|<span data-ttu-id="ec206-114">String</span><span class="sxs-lookup"><span data-stu-id="ec206-114">String</span></span>|<span data-ttu-id="ec206-115">Descripción.</span><span class="sxs-lookup"><span data-stu-id="ec206-115">Description.</span></span>|
|<span data-ttu-id="ec206-116">omaUri</span><span class="sxs-lookup"><span data-stu-id="ec206-116">omaUri</span></span>|<span data-ttu-id="ec206-117">cadena</span><span class="sxs-lookup"><span data-stu-id="ec206-117">String</span></span>|<span data-ttu-id="ec206-118">OMA.</span><span class="sxs-lookup"><span data-stu-id="ec206-118">OMA.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ec206-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ec206-119">Relationships</span></span>
<span data-ttu-id="ec206-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ec206-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ec206-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ec206-121">JSON Representation</span></span>
<span data-ttu-id="ec206-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ec206-122">Here is a JSON representation of the resource.</span></span>
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



