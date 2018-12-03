---
title: tipo de recurso educationSynchronizationCustomization
description: 'Proporciona opciones de configuración para personalizar la sincronización de perfiles de datos de school de las entidades de recurso. La personalización puede aplicarse a todas las entidades que se están sincronizadas. '
ms.openlocfilehash: 51799e01e5ab48fc5e686d72d2bdb5c85f191e1e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084232"
---
# <a name="educationsynchronizationcustomization-resource-type"></a><span data-ttu-id="838de-104">tipo de recurso educationSynchronizationCustomization</span><span class="sxs-lookup"><span data-stu-id="838de-104">educationSynchronizationCustomization resource type</span></span>

> <span data-ttu-id="838de-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="838de-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="838de-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="838de-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="838de-107">Proporciona opciones de configuración para personalizar la sincronización de perfiles de datos de school de las entidades de recurso.</span><span class="sxs-lookup"><span data-stu-id="838de-107">Provides settings for customizing the school data profile synchronization of the resource entities.</span></span> <span data-ttu-id="838de-108">La personalización puede aplicarse a todas las entidades que se están sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="838de-108">The customization can be applied to all the entities being synchronized.</span></span> 

><span data-ttu-id="838de-109">**Nota:** La propiedad **synchronizationStartDate** sólo se aplica a la entidad **StudentEnrollment** .</span><span class="sxs-lookup"><span data-stu-id="838de-109">**Note:** The **synchronizationStartDate** property only applies to the **StudentEnrollment** entity.</span></span>

## <a name="properties"></a><span data-ttu-id="838de-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="838de-110">Properties</span></span>

| <span data-ttu-id="838de-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="838de-111">Property</span></span> | <span data-ttu-id="838de-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="838de-112">Type</span></span> | <span data-ttu-id="838de-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="838de-113">Description</span></span> |
|:-|:-|:-|
| <span data-ttu-id="838de-114">**optionalPropertiesToSync**</span><span class="sxs-lookup"><span data-stu-id="838de-114">**optionalPropertiesToSync**</span></span> | <span data-ttu-id="838de-115">colección de cadena</span><span class="sxs-lookup"><span data-stu-id="838de-115">collection of string</span></span> |  <span data-ttu-id="838de-116">La colección de nombres de propiedad para la sincronización. Si establece en null, todas las propiedades será sincronizado.</span><span class="sxs-lookup"><span data-stu-id="838de-116">The collection of property names to sync. If set to null, all properties will be synchronized.</span></span>       |
| <span data-ttu-id="838de-117">**synchronizationStartDate**</span><span class="sxs-lookup"><span data-stu-id="838de-117">**synchronizationStartDate**</span></span> | <span data-ttu-id="838de-118">DateTime</span><span class="sxs-lookup"><span data-stu-id="838de-118">DateTime</span></span> |  <span data-ttu-id="838de-119">La fecha en la que debe comenzar la sincronización.</span><span class="sxs-lookup"><span data-stu-id="838de-119">The date that the synchronization should start.</span></span> <span data-ttu-id="838de-120">Este valor debe establecerse en una fecha futura.</span><span class="sxs-lookup"><span data-stu-id="838de-120">This value should be set to a future date.</span></span> <span data-ttu-id="838de-121">Si se establece en null, el recurso se sincronizará cuando se complete la configuración del perfil.</span><span class="sxs-lookup"><span data-stu-id="838de-121">If set to null, the resource will be synchronized when the profile setup completes.</span></span> <span data-ttu-id="838de-122">**Nota:** Esto sólo se aplica a la propiedad **StudentEnrollment** .</span><span class="sxs-lookup"><span data-stu-id="838de-122">**Note:** This only applies to the **StudentEnrollment** property.</span></span>      |
|<span data-ttu-id="838de-123">**isSyncDeferred**</span><span class="sxs-lookup"><span data-stu-id="838de-123">**isSyncDeferred**</span></span> |<span data-ttu-id="838de-124">Booleano</span><span class="sxs-lookup"><span data-stu-id="838de-124">Boolean</span></span> | <span data-ttu-id="838de-125">Indica si la sincronización de la entidad principal se aplaza hasta una fecha posterior.</span><span class="sxs-lookup"><span data-stu-id="838de-125">Indicates whether synchronization of the parent entity is deferred to a later date.</span></span> |
| <span data-ttu-id="838de-126">**allowDisplayNameUpdate**</span><span class="sxs-lookup"><span data-stu-id="838de-126">**allowDisplayNameUpdate**</span></span> | <span data-ttu-id="838de-127">Booleano</span><span class="sxs-lookup"><span data-stu-id="838de-127">Boolean</span></span> |  <span data-ttu-id="838de-128">Indica si el nombre para mostrar del recurso se puede sobrescribir con la sincronización.</span><span class="sxs-lookup"><span data-stu-id="838de-128">Indicates whether the display name of the resource can be overwritten by the sync.</span></span>         |


## <a name="json-representation"></a><span data-ttu-id="838de-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="838de-129">JSON representation</span></span>
<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "#microsoft.graph.educationSynchronizationCustomization"
}-->

```json
{  
    "optionalPropertiesToSync":["String"],
    "synchronizationStartDate": "DateTimeOffset",
    "isSyncDeferred": "Boolean",
    "allowDisplayNameUpdate": "Boolean"
}
```