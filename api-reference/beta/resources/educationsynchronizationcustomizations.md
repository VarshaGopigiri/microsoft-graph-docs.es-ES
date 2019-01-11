---
title: tipo de recurso educationSynchronizationCustomizations
description: Contiene la lista de entidades de sincronización y sus personalizaciones, si hay alguno.
localization_priority: Normal
ms.openlocfilehash: 0c07b166c09b2bfa6bf88159533523dab869a325
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27817041"
---
# <a name="educationsynchronizationcustomizations-resource-type"></a><span data-ttu-id="b64df-103">tipo de recurso educationSynchronizationCustomizations</span><span class="sxs-lookup"><span data-stu-id="b64df-103">educationSynchronizationCustomizations resource type</span></span>

> <span data-ttu-id="b64df-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b64df-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b64df-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b64df-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b64df-106">Contiene la lista de entidades de sincronización y sus [personalizaciones](educationsynchronizationcustomization.md), si hay alguno.</span><span class="sxs-lookup"><span data-stu-id="b64df-106">Contains the list of entities to sync and their [customizations](educationsynchronizationcustomization.md), if any.</span></span>

> <span data-ttu-id="b64df-107">**Nota:** Personalización de las propiedades para la sincronización no se aplica a las entidades **studentEnrollment** y **teacherRoster** .</span><span class="sxs-lookup"><span data-stu-id="b64df-107">**Note:** Customization of properties to sync does not apply to the **studentEnrollment** and **teacherRoster** entities.</span></span>

<span data-ttu-id="b64df-108">Este recurso es miembro de los proveedores de datos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b64df-108">This resource is member of the following data providers:</span></span>

* [<span data-ttu-id="b64df-109">educationCsvDataProvider</span><span class="sxs-lookup"><span data-stu-id="b64df-109">educationCsvDataProvider</span></span>](educationcsvdataprovider.md)
* [<span data-ttu-id="b64df-110">educationPowerSchoolDataProvider</span><span class="sxs-lookup"><span data-stu-id="b64df-110">educationPowerSchoolDataProvider</span></span>](educationpowerschooldataprovider.md)

## <a name="properties"></a><span data-ttu-id="b64df-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b64df-111">Properties</span></span>

| <span data-ttu-id="b64df-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b64df-112">Property</span></span> | <span data-ttu-id="b64df-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="b64df-113">Type</span></span> | <span data-ttu-id="b64df-114">Description</span><span class="sxs-lookup"><span data-stu-id="b64df-114">Description</span></span> |
|:-|:-|:-|
| <span data-ttu-id="b64df-115">**School**</span><span class="sxs-lookup"><span data-stu-id="b64df-115">**school**</span></span> | [<span data-ttu-id="b64df-116">educationSynchronizationCustomization</span><span class="sxs-lookup"><span data-stu-id="b64df-116">educationSynchronizationCustomization</span></span>](educationsynchronizationcustomization.md) |  <span data-ttu-id="b64df-117">Personalización de una entidad de escuela.</span><span class="sxs-lookup"><span data-stu-id="b64df-117">Customization for a school entity.</span></span>        |
| <span data-ttu-id="b64df-118">**section**</span><span class="sxs-lookup"><span data-stu-id="b64df-118">**section**</span></span> | [<span data-ttu-id="b64df-119">educationSynchronizationCustomization</span><span class="sxs-lookup"><span data-stu-id="b64df-119">educationSynchronizationCustomization</span></span>](educationsynchronizationcustomization.md) |  <span data-ttu-id="b64df-120">Personalización de una entidad de sección.</span><span class="sxs-lookup"><span data-stu-id="b64df-120">Customization for a section entity.</span></span>         |
| <span data-ttu-id="b64df-121">**student**</span><span class="sxs-lookup"><span data-stu-id="b64df-121">**student**</span></span> | [<span data-ttu-id="b64df-122">educationSynchronizationCustomization</span><span class="sxs-lookup"><span data-stu-id="b64df-122">educationSynchronizationCustomization</span></span>](educationsynchronizationcustomization.md) |  <span data-ttu-id="b64df-123">Personalización de una entidad de estudiantes.</span><span class="sxs-lookup"><span data-stu-id="b64df-123">Customization for a student entity.</span></span>         |
| <span data-ttu-id="b64df-124">**teacher**</span><span class="sxs-lookup"><span data-stu-id="b64df-124">**teacher**</span></span> | [<span data-ttu-id="b64df-125">educationSynchronizationCustomization</span><span class="sxs-lookup"><span data-stu-id="b64df-125">educationSynchronizationCustomization</span></span>](educationsynchronizationcustomization.md) |  <span data-ttu-id="b64df-126">Personalización de una entidad de profesor.</span><span class="sxs-lookup"><span data-stu-id="b64df-126">Customization for a teacher entity.</span></span>         |
| <span data-ttu-id="b64df-127">**studentEnrollment**</span><span class="sxs-lookup"><span data-stu-id="b64df-127">**studentEnrollment**</span></span> | [<span data-ttu-id="b64df-128">educationSynchronizationCustomization</span><span class="sxs-lookup"><span data-stu-id="b64df-128">educationSynchronizationCustomization</span></span>](educationsynchronizationcustomization.md) |  <span data-ttu-id="b64df-129">Personalización de inscripción de estudiantes.</span><span class="sxs-lookup"><span data-stu-id="b64df-129">Customization for student enrollment.</span></span>           |
| <span data-ttu-id="b64df-130">**teacherRoster**</span><span class="sxs-lookup"><span data-stu-id="b64df-130">**teacherRoster**</span></span> | [<span data-ttu-id="b64df-131">educationSynchronizationCustomization</span><span class="sxs-lookup"><span data-stu-id="b64df-131">educationSynchronizationCustomization</span></span>](educationsynchronizationcustomization.md) |       <span data-ttu-id="b64df-132">Personalización de una lista de participantes profesor.</span><span class="sxs-lookup"><span data-stu-id="b64df-132">Customization for a teacher roster.</span></span>    |

## <a name="json-representation"></a><span data-ttu-id="b64df-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b64df-133">JSON representation</span></span>
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
