---
title: tipo de recurso educationSynchronizationCustomizations
description: Contiene la lista de entidades de sincronización y sus personalizaciones, si hay alguno.
localization_priority: Normal
author: mmast-msft
ms.prod: education
ms.openlocfilehash: 3254915887afc1e6b0da0b3b6c44b59689219ab1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27918192"
---
# <a name="educationsynchronizationcustomizations-resource-type"></a><span data-ttu-id="3b67b-103">tipo de recurso educationSynchronizationCustomizations</span><span class="sxs-lookup"><span data-stu-id="3b67b-103">educationSynchronizationCustomizations resource type</span></span>

> <span data-ttu-id="3b67b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3b67b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3b67b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3b67b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3b67b-106">Contiene la lista de entidades de sincronización y sus [personalizaciones](educationsynchronizationcustomization.md), si hay alguno.</span><span class="sxs-lookup"><span data-stu-id="3b67b-106">Contains the list of entities to sync and their [customizations](educationsynchronizationcustomization.md), if any.</span></span>

> <span data-ttu-id="3b67b-107">**Nota:** Personalización de las propiedades para la sincronización no se aplica a las entidades **studentEnrollment** y **teacherRoster** .</span><span class="sxs-lookup"><span data-stu-id="3b67b-107">**Note:** Customization of properties to sync does not apply to the **studentEnrollment** and **teacherRoster** entities.</span></span>

<span data-ttu-id="3b67b-108">Este recurso es miembro de los proveedores de datos siguientes:</span><span class="sxs-lookup"><span data-stu-id="3b67b-108">This resource is member of the following data providers:</span></span>

* [<span data-ttu-id="3b67b-109">educationCsvDataProvider</span><span class="sxs-lookup"><span data-stu-id="3b67b-109">educationCsvDataProvider</span></span>](educationcsvdataprovider.md)
* [<span data-ttu-id="3b67b-110">educationPowerSchoolDataProvider</span><span class="sxs-lookup"><span data-stu-id="3b67b-110">educationPowerSchoolDataProvider</span></span>](educationpowerschooldataprovider.md)

## <a name="properties"></a><span data-ttu-id="3b67b-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3b67b-111">Properties</span></span>

| <span data-ttu-id="3b67b-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3b67b-112">Property</span></span> | <span data-ttu-id="3b67b-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="3b67b-113">Type</span></span> | <span data-ttu-id="3b67b-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b67b-114">Description</span></span> |
|:-|:-|:-|
| <span data-ttu-id="3b67b-115">**School**</span><span class="sxs-lookup"><span data-stu-id="3b67b-115">**school**</span></span> | [<span data-ttu-id="3b67b-116">educationSynchronizationCustomization</span><span class="sxs-lookup"><span data-stu-id="3b67b-116">educationSynchronizationCustomization</span></span>](educationsynchronizationcustomization.md) |  <span data-ttu-id="3b67b-117">Personalización de una entidad de escuela.</span><span class="sxs-lookup"><span data-stu-id="3b67b-117">Customization for a school entity.</span></span>        |
| <span data-ttu-id="3b67b-118">**section**</span><span class="sxs-lookup"><span data-stu-id="3b67b-118">**section**</span></span> | [<span data-ttu-id="3b67b-119">educationSynchronizationCustomization</span><span class="sxs-lookup"><span data-stu-id="3b67b-119">educationSynchronizationCustomization</span></span>](educationsynchronizationcustomization.md) |  <span data-ttu-id="3b67b-120">Personalización de una entidad de sección.</span><span class="sxs-lookup"><span data-stu-id="3b67b-120">Customization for a section entity.</span></span>         |
| <span data-ttu-id="3b67b-121">**student**</span><span class="sxs-lookup"><span data-stu-id="3b67b-121">**student**</span></span> | [<span data-ttu-id="3b67b-122">educationSynchronizationCustomization</span><span class="sxs-lookup"><span data-stu-id="3b67b-122">educationSynchronizationCustomization</span></span>](educationsynchronizationcustomization.md) |  <span data-ttu-id="3b67b-123">Personalización de una entidad de estudiantes.</span><span class="sxs-lookup"><span data-stu-id="3b67b-123">Customization for a student entity.</span></span>         |
| <span data-ttu-id="3b67b-124">**teacher**</span><span class="sxs-lookup"><span data-stu-id="3b67b-124">**teacher**</span></span> | [<span data-ttu-id="3b67b-125">educationSynchronizationCustomization</span><span class="sxs-lookup"><span data-stu-id="3b67b-125">educationSynchronizationCustomization</span></span>](educationsynchronizationcustomization.md) |  <span data-ttu-id="3b67b-126">Personalización de una entidad de profesor.</span><span class="sxs-lookup"><span data-stu-id="3b67b-126">Customization for a teacher entity.</span></span>         |
| <span data-ttu-id="3b67b-127">**studentEnrollment**</span><span class="sxs-lookup"><span data-stu-id="3b67b-127">**studentEnrollment**</span></span> | [<span data-ttu-id="3b67b-128">educationSynchronizationCustomization</span><span class="sxs-lookup"><span data-stu-id="3b67b-128">educationSynchronizationCustomization</span></span>](educationsynchronizationcustomization.md) |  <span data-ttu-id="3b67b-129">Personalización de inscripción de estudiantes.</span><span class="sxs-lookup"><span data-stu-id="3b67b-129">Customization for student enrollment.</span></span>           |
| <span data-ttu-id="3b67b-130">**teacherRoster**</span><span class="sxs-lookup"><span data-stu-id="3b67b-130">**teacherRoster**</span></span> | [<span data-ttu-id="3b67b-131">educationSynchronizationCustomization</span><span class="sxs-lookup"><span data-stu-id="3b67b-131">educationSynchronizationCustomization</span></span>](educationsynchronizationcustomization.md) |       <span data-ttu-id="3b67b-132">Personalización de una lista de participantes profesor.</span><span class="sxs-lookup"><span data-stu-id="3b67b-132">Customization for a teacher roster.</span></span>    |

## <a name="json-representation"></a><span data-ttu-id="3b67b-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3b67b-133">JSON representation</span></span>
<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "#microsoft.graph.educationSynchronizationCustomizations"
}-->

```json
{
  "school": {"@odata.type": "microsoft.graph.educationSynchronizationCustomization"},
  "section": {"@odata.type": "microsoft.graph.educationSynchronizationCustomization"},
  "student": {"@odata.type": "microsoft.graph.educationSynchronizationCustomization"},
  "teacher": {"@odata.type": "microsoft.graph.educationSynchronizationCustomization"},
  "studentEnrollment": {"@odata.type": "microsoft.graph.educationSynchronizationCustomization"},
  "teacherRoster": {"@odata.type": "microsoft.graph.educationSynchronizationCustomization"}
}
```
