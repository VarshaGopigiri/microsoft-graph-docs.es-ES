---
title: Tipo de recurso groupSetting
description: Comportamientos del control de configuración de grupo, como listas de palabras bloqueadas para los nombres para mostrar del grupo o si los usuarios invitados pueden ser propietarios del grupo.
author: dkershaw10
localization_priority: Normal
ms.openlocfilehash: 4508de9c03820031e47e3457e24dc39ed14c36a1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27840771"
---
# <a name="groupsetting-resource-type"></a><span data-ttu-id="dc6ec-103">Tipo de recurso groupSetting</span><span class="sxs-lookup"><span data-stu-id="dc6ec-103">groupSetting resource type</span></span>

<span data-ttu-id="dc6ec-104">Comportamientos del control de configuración de grupo, como listas de palabras bloqueadas para los nombres para mostrar del grupo o si los usuarios invitados pueden ser propietarios del grupo.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-104">Group settings control behaviors such as blocked word lists for group display names or whether guest users are allowed to be group owners.</span></span>

<span data-ttu-id="dc6ec-p101">La configuración de grupo se puede crear según las plantillas de [groupSettingTemplates](groupsettingtemplate.md) disponibles y se pueden cambiar los valores predeterminados. Esta configuración controla el comportamiento del grupo a nivel de todo el inquilino o en un grupo específico. Cuando se establece la misma configuración a nivel de todo el inquilino y en un grupo específico, la configuración de nivel de grupo reemplaza la configuración a nivel de inquilino.  Por ejemplo, puede que una configuración a nivel de todo el inquilino permite que los miembros existentes inviten a otros usuarios, pero la configuración de un grupo concreto puede reemplazarla y no permitir que los miembros del grupo puedan invitar a otros usuarios como invitados. La configuración de grupo solo controla el comportamiento de los grupos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-p101">Group settings can be created based on the available [groupSettingTemplates](groupsettingtemplate.md), and changed from their preset defaults. These settings govern group behaviors at a tenant-wide level or to a specific group. When the same setting is defined at both the tenant-wide and to a specific group, the group-level setting overrides the tenant-wide setting.  For example, the tenant-wide setting may allow guests to be invited by existing members of groups, but an individual group setting can override and not allow guests to be invited by members of the group. Group settings only govern Office 365 groups behavior.</span></span>

## <a name="methods"></a><span data-ttu-id="dc6ec-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="dc6ec-110">Methods</span></span>

| <span data-ttu-id="dc6ec-111">Método</span><span class="sxs-lookup"><span data-stu-id="dc6ec-111">Method</span></span> | <span data-ttu-id="dc6ec-112">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc6ec-112">Return Type</span></span> | <span data-ttu-id="dc6ec-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc6ec-113">Description</span></span> |
|:---------------|:--------|:----------|
|[<span data-ttu-id="dc6ec-114">Create setting</span><span class="sxs-lookup"><span data-stu-id="dc6ec-114">Create setting</span></span>](../api/groupsetting-post-groupsettings.md) | [<span data-ttu-id="dc6ec-115">groupSetting</span><span class="sxs-lookup"><span data-stu-id="dc6ec-115">groupSetting</span></span>](groupsetting.md) |<span data-ttu-id="dc6ec-p102">Crea un objeto de configuración según una plantilla de groupSettingTemplate. La solicitud POST debe proporcionar settingValues para toda la configuración establecida en la plantilla.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-p102">Create a setting object based on a groupSettingTemplate. The POST request must provide settingValues for all the settings defined in the template.</span></span> |
|[<span data-ttu-id="dc6ec-118">Get setting</span><span class="sxs-lookup"><span data-stu-id="dc6ec-118">Get setting</span></span>](../api/groupsetting-get.md) | [<span data-ttu-id="dc6ec-119">groupSetting</span><span class="sxs-lookup"><span data-stu-id="dc6ec-119">groupSetting</span></span>](groupsetting.md) | <span data-ttu-id="dc6ec-120">Lee las propiedades de un objeto de configuración específico.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-120">Read properties of a specific setting object.</span></span> |
|[<span data-ttu-id="dc6ec-121">List settings</span><span class="sxs-lookup"><span data-stu-id="dc6ec-121">List settings</span></span>](../api/groupsetting-list.md) | <span data-ttu-id="dc6ec-122">Colección de [groupSetting](groupsetting.md)</span><span class="sxs-lookup"><span data-stu-id="dc6ec-122">[groupSetting](groupsetting.md) collection</span></span> | <span data-ttu-id="dc6ec-123">Enumera las propiedades de todos los objetos de configuración.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-123">List properties of all setting objects.</span></span> |
|[<span data-ttu-id="dc6ec-124">Update setting</span><span class="sxs-lookup"><span data-stu-id="dc6ec-124">Update setting</span></span>](../api/groupsetting-update.md) | [<span data-ttu-id="dc6ec-125">groupSetting</span><span class="sxs-lookup"><span data-stu-id="dc6ec-125">groupSetting</span></span>](groupsetting.md) | <span data-ttu-id="dc6ec-126">Actualiza el objeto groupSetting.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-126">Update groupsetting object.</span></span> |
|[<span data-ttu-id="dc6ec-127">Delete setting</span><span class="sxs-lookup"><span data-stu-id="dc6ec-127">Delete setting</span></span>](../api/groupsetting-delete.md) | <span data-ttu-id="dc6ec-128">Ninguno</span><span class="sxs-lookup"><span data-stu-id="dc6ec-128">None</span></span> | <span data-ttu-id="dc6ec-129">Elimina un objeto de configuración.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-129">Delete a setting object.</span></span> |

## <a name="properties"></a><span data-ttu-id="dc6ec-130">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dc6ec-130">Properties</span></span>

| <span data-ttu-id="dc6ec-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dc6ec-131">Property</span></span> | <span data-ttu-id="dc6ec-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc6ec-132">Type</span></span> | <span data-ttu-id="dc6ec-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc6ec-133">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="dc6ec-134">displayName</span><span class="sxs-lookup"><span data-stu-id="dc6ec-134">displayName</span></span>|<span data-ttu-id="dc6ec-135">String</span><span class="sxs-lookup"><span data-stu-id="dc6ec-135">String</span></span>| <span data-ttu-id="dc6ec-136">El nombre para mostrar de este grupo de configuraciones, que proviene de la plantilla asociada.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-136">Display name of this group of settings, which comes from the associated template.</span></span> |
|<span data-ttu-id="dc6ec-137">id</span><span class="sxs-lookup"><span data-stu-id="dc6ec-137">id</span></span>|<span data-ttu-id="dc6ec-138">String</span><span class="sxs-lookup"><span data-stu-id="dc6ec-138">String</span></span>| <span data-ttu-id="dc6ec-p103">Identificador único de esta configuración. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-p103">Unique identifier for these settings. Read-only.</span></span> |
|<span data-ttu-id="dc6ec-141">templateId</span><span class="sxs-lookup"><span data-stu-id="dc6ec-141">templateId</span></span>|<span data-ttu-id="dc6ec-142">String</span><span class="sxs-lookup"><span data-stu-id="dc6ec-142">String</span></span>| <span data-ttu-id="dc6ec-p104">Identificador único para la plantilla que se usa para crear este grupo de configuraciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-p104">Unique identifier for the template used to create this group of settings. Read-only.</span></span> |
|<span data-ttu-id="dc6ec-145">values</span><span class="sxs-lookup"><span data-stu-id="dc6ec-145">values</span></span>|<span data-ttu-id="dc6ec-146">Colección de [settingValue](settingvalue.md)</span><span class="sxs-lookup"><span data-stu-id="dc6ec-146">[settingValue](settingvalue.md) collection</span></span>| <span data-ttu-id="dc6ec-p105">Colección de pares de nombre y valor. Debe contener y establecer todas las configuraciones definidas en la plantilla.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-p105">Collection of name value pairs. Must contain and set all the settings defined in the template.</span></span> |

## <a name="relationships"></a><span data-ttu-id="dc6ec-149">Relaciones</span><span class="sxs-lookup"><span data-stu-id="dc6ec-149">Relationships</span></span>

<span data-ttu-id="dc6ec-150">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-150">None.</span></span>

## <a name="json-representation"></a><span data-ttu-id="dc6ec-151">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="dc6ec-151">JSON representation</span></span>

<span data-ttu-id="dc6ec-152">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="dc6ec-152">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "openType": true,
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.groupSetting"
}-->

```json
{
  "displayName": "String",
  "id": "String (identifier)",
  "templateId": "String",
  "values": [{"@odata.type": "microsoft.graph.settingValue"}]
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "groupSetting resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
