---
title: tipo de recurso windows10AssociatedApps
description: Definición de aplicación de Windows 10 asociado.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: d1f6363027ae46263146efdbf3f5ac5254afcd93
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27911913"
---
# <a name="windows10associatedapps-resource-type"></a><span data-ttu-id="60282-103">tipo de recurso windows10AssociatedApps</span><span class="sxs-lookup"><span data-stu-id="60282-103">windows10AssociatedApps resource type</span></span>

> <span data-ttu-id="60282-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="60282-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="60282-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="60282-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="60282-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="60282-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="60282-107">Definición de aplicación de Windows 10 asociado.</span><span class="sxs-lookup"><span data-stu-id="60282-107">Windows 10 Associated Application definition.</span></span>
## <a name="properties"></a><span data-ttu-id="60282-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="60282-108">Properties</span></span>
|<span data-ttu-id="60282-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="60282-109">Property</span></span>|<span data-ttu-id="60282-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="60282-110">Type</span></span>|<span data-ttu-id="60282-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="60282-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="60282-112">tipo de aplicación</span><span class="sxs-lookup"><span data-stu-id="60282-112">appType</span></span>|[<span data-ttu-id="60282-113">windows10AppType</span><span class="sxs-lookup"><span data-stu-id="60282-113">windows10AppType</span></span>](../resources/intune-deviceconfig-windows10apptype.md)|<span data-ttu-id="60282-114">Tipo de aplicación.</span><span class="sxs-lookup"><span data-stu-id="60282-114">Application type.</span></span> <span data-ttu-id="60282-115">Los valores posibles son: `desktop` y `universal`.</span><span class="sxs-lookup"><span data-stu-id="60282-115">Possible values are: `desktop`, `universal`.</span></span>|
|<span data-ttu-id="60282-116">identificador</span><span class="sxs-lookup"><span data-stu-id="60282-116">identifier</span></span>|<span data-ttu-id="60282-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="60282-117">String</span></span>|<span data-ttu-id="60282-118">Identificador.</span><span class="sxs-lookup"><span data-stu-id="60282-118">Identifier.</span></span>|

## <a name="relationships"></a><span data-ttu-id="60282-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="60282-119">Relationships</span></span>
<span data-ttu-id="60282-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="60282-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="60282-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="60282-121">JSON Representation</span></span>
<span data-ttu-id="60282-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="60282-122">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windows10AssociatedApps"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windows10AssociatedApps",
  "appType": "String",
  "identifier": "String"
}
```





