---
title: Tipo de recurso groupSettingTemplate
description: Las plantillas de configuración de grupo representan configuraciones definidas por el sistema disponibles para el inquilino. La configuración de grupo se puede crear según las plantillas de **groupSettingTemplates** disponibles y se pueden cambiar los valores predeterminados. Las plantillas de configuración de grupo no se pueden crear, actualizar ni eliminar. Esta configuración puede representar configuración para todo el inquilino o una para un grupo específico. Actualmente, las únicas plantillas disponibles se aplican a grupos de Office 365 e incluyen opciones como las que establecen si los usuarios pueden crear grupos o no, o si pueden invitar a usuarios de fuera de la organización para convertirse en miembros de un grupo.
ms.openlocfilehash: 3c4111b2727e79e048778063b259611795733de4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032156"
---
# <a name="groupsettingtemplate-resource-type"></a><span data-ttu-id="c1a81-107">Tipo de recurso groupSettingTemplate</span><span class="sxs-lookup"><span data-stu-id="c1a81-107">groupSettingTemplate resource type</span></span>

<span data-ttu-id="c1a81-p102">Las plantillas de configuración de grupo representan configuraciones definidas por el sistema disponibles para el inquilino. La [configuración de grupo](groupsetting.md) se puede crear según las plantillas de **groupSettingTemplates** disponibles y se pueden cambiar los valores predeterminados. Las plantillas de configuración de grupo no se pueden crear, actualizar ni eliminar. Esta configuración puede representar configuración para todo el inquilino o una para un grupo específico. Actualmente, las únicas plantillas disponibles se aplican a grupos de Office 365 e incluyen opciones como las que establecen si los usuarios pueden crear grupos o no, o si pueden invitar a usuarios de fuera de la organización para convertirse en miembros de un grupo.</span><span class="sxs-lookup"><span data-stu-id="c1a81-p102">Group setting templates represent system-defined settings available to the tenant. [Group settings](groupsetting.md) can be created based on the available **groupSettingTemplates**, and values changed from their preset defaults. Group setting templates cannot be created, updated or deleted. These settings can represent tenant-wide settings, or can represent specific group settings. Currently, the only templates available apply to Office 365 groups, and include settings such as whether users can create groups or invite guests from outside the organization to become members of a group.</span></span>

## <a name="methods"></a><span data-ttu-id="c1a81-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="c1a81-113">Methods</span></span>

| <span data-ttu-id="c1a81-114">Método</span><span class="sxs-lookup"><span data-stu-id="c1a81-114">Method</span></span> | <span data-ttu-id="c1a81-115">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1a81-115">Return Type</span></span> | <span data-ttu-id="c1a81-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1a81-116">Description</span></span> |
|:---------------|:--------|:----------|
|[<span data-ttu-id="c1a81-117">Get groupSettingTemplate</span><span class="sxs-lookup"><span data-stu-id="c1a81-117">Get groupSettingTemplate</span></span>](../api/groupsettingtemplate-get.md) | [<span data-ttu-id="c1a81-118">groupSettingTemplate</span><span class="sxs-lookup"><span data-stu-id="c1a81-118">groupSettingTemplate</span></span>](groupsettingtemplate.md) | <span data-ttu-id="c1a81-119">Lee las propiedades específicas de uno de los objetos groupSettingTemplate definido por el sistema.</span><span class="sxs-lookup"><span data-stu-id="c1a81-119">Read the specific properties of one of the system defined groupSettingTemplate objects.</span></span> |
|[<span data-ttu-id="c1a81-120">List groupSettingTemplate</span><span class="sxs-lookup"><span data-stu-id="c1a81-120">List groupSettingTemplate</span></span>](../api/groupsettingtemplate-list.md) | [<span data-ttu-id="c1a81-121">Colección de groupSettingTemplate</span><span class="sxs-lookup"><span data-stu-id="c1a81-121">Collection of groupSettingTemplate</span></span>](groupsettingtemplate.md) |<span data-ttu-id="c1a81-122">Enumera todos los objetos groupSettingTemplate definidos por el sistema.</span><span class="sxs-lookup"><span data-stu-id="c1a81-122">List all of the system defined groupSettingTemplate objects.</span></span>|

## <a name="properties"></a><span data-ttu-id="c1a81-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c1a81-123">Properties</span></span>

| <span data-ttu-id="c1a81-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c1a81-124">Property</span></span> | <span data-ttu-id="c1a81-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="c1a81-125">Type</span></span> | <span data-ttu-id="c1a81-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1a81-126">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="c1a81-127">description</span><span class="sxs-lookup"><span data-stu-id="c1a81-127">description</span></span>|<span data-ttu-id="c1a81-128">String</span><span class="sxs-lookup"><span data-stu-id="c1a81-128">String</span></span>| <span data-ttu-id="c1a81-129">Descripción de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="c1a81-129">Description of the template.</span></span> |
|<span data-ttu-id="c1a81-130">displayName</span><span class="sxs-lookup"><span data-stu-id="c1a81-130">displayName</span></span>|<span data-ttu-id="c1a81-131">String</span><span class="sxs-lookup"><span data-stu-id="c1a81-131">String</span></span>| <span data-ttu-id="c1a81-132">Muestra el nombre de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="c1a81-132">Display name of the template.</span></span> |
|<span data-ttu-id="c1a81-133">id</span><span class="sxs-lookup"><span data-stu-id="c1a81-133">id</span></span>|<span data-ttu-id="c1a81-134">String</span><span class="sxs-lookup"><span data-stu-id="c1a81-134">String</span></span>| <span data-ttu-id="c1a81-p103">Identificador único de la plantilla. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c1a81-p103">Unique identifier for the template. Read-only.</span></span>|
|<span data-ttu-id="c1a81-137">values</span><span class="sxs-lookup"><span data-stu-id="c1a81-137">values</span></span>|<span data-ttu-id="c1a81-138">Colección de [settingTemplateValue](settingtemplatevalue.md)</span><span class="sxs-lookup"><span data-stu-id="c1a81-138">[settingTemplateValue](settingtemplatevalue.md) collection</span></span>| <span data-ttu-id="c1a81-139">Colección de settingTemplateValues que enumera el conjunto de opciones disponibles, los valores predeterminados y los tipos que forman esta plantilla.</span><span class="sxs-lookup"><span data-stu-id="c1a81-139">Collection of settingTemplateValues that list the set of available settings, defaults and types that make up this template.</span></span> |

## <a name="relationships"></a><span data-ttu-id="c1a81-140">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c1a81-140">Relationships</span></span>

<span data-ttu-id="c1a81-141">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c1a81-141">None.</span></span>


## <a name="json-representation"></a><span data-ttu-id="c1a81-142">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c1a81-142">JSON representation</span></span>

<span data-ttu-id="c1a81-143">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c1a81-143">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "openType": true,
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.directoryObject",
  "@odata.type": "microsoft.graph.groupSettingTemplate"
}-->

```json
{
  "description": "String",
  "displayName": "String",
  "id": "String (identifier)",
  "values": [{"@odata.type": "microsoft.graph.settingTemplateValue"}]
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "groupSettingTemplate resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->