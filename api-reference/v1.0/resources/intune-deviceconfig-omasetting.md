---
title: Tipo de recurso omaSetting
description: Definición de la configuración de OMA.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 42b6d5fcea7b3b46acf8d0a119213f679d99aed6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27961487"
---
# <a name="omasetting-resource-type"></a><span data-ttu-id="d0e3b-103">Tipo de recurso omaSetting</span><span class="sxs-lookup"><span data-stu-id="d0e3b-103">omaSetting resource type</span></span>

> <span data-ttu-id="d0e3b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d0e3b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d0e3b-105">Definición de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="d0e3b-105">OMA Settings definition.</span></span>
## <a name="properties"></a><span data-ttu-id="d0e3b-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d0e3b-106">Properties</span></span>
|<span data-ttu-id="d0e3b-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d0e3b-107">Property</span></span>|<span data-ttu-id="d0e3b-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="d0e3b-108">Type</span></span>|<span data-ttu-id="d0e3b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0e3b-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d0e3b-110">displayName</span><span class="sxs-lookup"><span data-stu-id="d0e3b-110">displayName</span></span>|<span data-ttu-id="d0e3b-111">cadena</span><span class="sxs-lookup"><span data-stu-id="d0e3b-111">String</span></span>|<span data-ttu-id="d0e3b-112">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="d0e3b-112">Display Name.</span></span>|
|<span data-ttu-id="d0e3b-113">description</span><span class="sxs-lookup"><span data-stu-id="d0e3b-113">description</span></span>|<span data-ttu-id="d0e3b-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="d0e3b-114">String</span></span>|<span data-ttu-id="d0e3b-115">Descripción.</span><span class="sxs-lookup"><span data-stu-id="d0e3b-115">Description.</span></span>|
|<span data-ttu-id="d0e3b-116">omaUri</span><span class="sxs-lookup"><span data-stu-id="d0e3b-116">omaUri</span></span>|<span data-ttu-id="d0e3b-117">cadena</span><span class="sxs-lookup"><span data-stu-id="d0e3b-117">String</span></span>|<span data-ttu-id="d0e3b-118">OMA.</span><span class="sxs-lookup"><span data-stu-id="d0e3b-118">OMA.</span></span>|

## <a name="relationships"></a><span data-ttu-id="d0e3b-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d0e3b-119">Relationships</span></span>
<span data-ttu-id="d0e3b-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="d0e3b-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="d0e3b-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d0e3b-121">JSON Representation</span></span>
<span data-ttu-id="d0e3b-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d0e3b-122">Here is a JSON representation of the resource.</span></span>
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



