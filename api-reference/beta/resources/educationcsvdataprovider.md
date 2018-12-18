---
title: tipo de recurso educationCsvDataProvider
description: 'Se usa para configurar el perfil de sincronización de datos de school cuando los archivos CSV son el origen de entrada.  '
author: mmast-msft
ms.openlocfilehash: 1a816d4e176147d549381465154e35cf0a821b98
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27317902"
---
# <a name="educationcsvdataprovider-resource-type"></a><span data-ttu-id="f527a-103">tipo de recurso educationCsvDataProvider</span><span class="sxs-lookup"><span data-stu-id="f527a-103">educationCsvDataProvider resource type</span></span>

> <span data-ttu-id="f527a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f527a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f527a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f527a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f527a-106">Se usa para configurar el perfil de sincronización de datos de school cuando los archivos CSV son el origen de entrada.</span><span class="sxs-lookup"><span data-stu-id="f527a-106">Used to set up the school data synchronization profile when CSV files are the input source.</span></span>  

<span data-ttu-id="f527a-107">Deriva de [educationSynchronizationDataProvider](educationsynchronizationdataprovider.md).</span><span class="sxs-lookup"><span data-stu-id="f527a-107">Derived from [educationSynchronizationDataProvider](educationsynchronizationdataprovider.md).</span></span>

## <a name="properties"></a><span data-ttu-id="f527a-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f527a-108">Properties</span></span>

| <span data-ttu-id="f527a-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f527a-109">Property</span></span> | <span data-ttu-id="f527a-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="f527a-110">Type</span></span> | <span data-ttu-id="f527a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f527a-111">Description</span></span> |
|:-|:-|:-|
| <span data-ttu-id="f527a-112">**personalizaciones**</span><span class="sxs-lookup"><span data-stu-id="f527a-112">**customizations**</span></span> | [<span data-ttu-id="f527a-113">educationSynchronizationCustomizations</span><span class="sxs-lookup"><span data-stu-id="f527a-113">educationSynchronizationCustomizations</span></span>](educationsynchronizationcustomizations.md) | <span data-ttu-id="f527a-114">Personalizaciones opcionales que se aplicará a los perfiles de sincronización.</span><span class="sxs-lookup"><span data-stu-id="f527a-114">Optional customizations to be applied to the synchronization profile.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="f527a-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f527a-115">JSON representation</span></span>

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
