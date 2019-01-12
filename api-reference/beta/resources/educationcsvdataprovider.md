---
title: tipo de recurso educationCsvDataProvider
description: 'Se usa para configurar el perfil de sincronización de datos de school cuando los archivos CSV son el origen de entrada.  '
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: 19ef77671f862a0b59b5697b76bb54dc20e42856
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27952758"
---
# <a name="educationcsvdataprovider-resource-type"></a><span data-ttu-id="1d652-103">tipo de recurso educationCsvDataProvider</span><span class="sxs-lookup"><span data-stu-id="1d652-103">educationCsvDataProvider resource type</span></span>

> <span data-ttu-id="1d652-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1d652-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1d652-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1d652-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1d652-106">Se usa para configurar el perfil de sincronización de datos de school cuando los archivos CSV son el origen de entrada.</span><span class="sxs-lookup"><span data-stu-id="1d652-106">Used to set up the school data synchronization profile when CSV files are the input source.</span></span>  

<span data-ttu-id="1d652-107">Deriva de [educationSynchronizationDataProvider](educationsynchronizationdataprovider.md).</span><span class="sxs-lookup"><span data-stu-id="1d652-107">Derived from [educationSynchronizationDataProvider](educationsynchronizationdataprovider.md).</span></span>

## <a name="properties"></a><span data-ttu-id="1d652-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1d652-108">Properties</span></span>

| <span data-ttu-id="1d652-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1d652-109">Property</span></span> | <span data-ttu-id="1d652-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="1d652-110">Type</span></span> | <span data-ttu-id="1d652-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d652-111">Description</span></span> |
|:-|:-|:-|
| <span data-ttu-id="1d652-112">**personalizaciones**</span><span class="sxs-lookup"><span data-stu-id="1d652-112">**customizations**</span></span> | [<span data-ttu-id="1d652-113">educationSynchronizationCustomizations</span><span class="sxs-lookup"><span data-stu-id="1d652-113">educationSynchronizationCustomizations</span></span>](educationsynchronizationcustomizations.md) | <span data-ttu-id="1d652-114">Personalizaciones opcionales que se aplicará a los perfiles de sincronización.</span><span class="sxs-lookup"><span data-stu-id="1d652-114">Optional customizations to be applied to the synchronization profile.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="1d652-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1d652-115">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "#microsoft.graph.educationCsvDataProvider"
}-->

```json
{
    "@odata.type": "#microsoft.graph.educationCsvDataProvider",
    "customizations": { "@odata.type": "microsoft.graph.educationSynchronizationCustomizations" }
}
```
