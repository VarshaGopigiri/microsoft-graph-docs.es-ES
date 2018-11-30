---
title: Establecer el tipo de recurso
description: Configuración del directorio puede crear en función de la directorySettingTemplates disponibles y se ha cambiado desde sus valores predeterminados. Esta configuración puede controlar comportamientos de entidad o una característica, en un nivel de todo el inquilino o en un nivel de la entidad específica. Cuando la misma configuración se define en el nivel de entidad todo el inquilino y específica, la configuración del nivel de entidad específica puede voluntaria de la configuración de todo el inquilino.  Por ejemplo, la configuración de todo el inquilino puede permitir que los invitados puedan ser invitados por los miembros de grupos existentes, pero una configuración de grupo específico puede voluntaria y no permitir que los invitados puedan ser invitados por los miembros del grupo. Actualmente configuraciones de definidas por el sistema sólo se rigen el comportamiento de los grupos de Office.
ms.openlocfilehash: 4a807d22bfd5d6651b4064542d33fe285b637a3f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086785"
---
# <a name="directorysetting-resource-type"></a><span data-ttu-id="590fb-107">Establecer el tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="590fb-107">directorySetting resource type</span></span>

> <span data-ttu-id="590fb-108">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="590fb-108">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="590fb-109">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="590fb-109">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="590fb-110">Configuración del directorio puede crear en función de la disponible [directorySettingTemplates](directorysettingtemplate.md)y se ha cambiado desde sus valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="590fb-110">Directory settings can be created based on the available [directorySettingTemplates](directorysettingtemplate.md), and changed from their preset defaults.</span></span> <span data-ttu-id="590fb-111">Esta configuración puede controlar comportamientos de entidad o una característica, en un nivel de todo el inquilino o en un nivel de la entidad específica.</span><span class="sxs-lookup"><span data-stu-id="590fb-111">These settings can govern entity or feature behaviors, both at a tenant-wide level or at a specific entity level.</span></span> <span data-ttu-id="590fb-112">Cuando la misma configuración se define en el nivel de entidad todo el inquilino y específica, la configuración del nivel de entidad específica puede voluntaria de la configuración de todo el inquilino.</span><span class="sxs-lookup"><span data-stu-id="590fb-112">When the same setting is defined at both the tenant-wide and specific entity level, the specific entity level setting may opt-out from the tenant-wide setting.</span></span>  <span data-ttu-id="590fb-113">Por ejemplo, la configuración de todo el inquilino puede permitir que los invitados puedan ser invitados por los miembros de grupos existentes, pero una configuración de grupo específico puede voluntaria y no permitir que los invitados puedan ser invitados por los miembros del grupo.</span><span class="sxs-lookup"><span data-stu-id="590fb-113">For example, the tenant-wide setting may allow guests to be invited by existing members of groups, but a specific group setting may opt-out and not allow guests to be invited by members of the group.</span></span> <span data-ttu-id="590fb-114">Actualmente configuraciones de definidas por el sistema sólo se rigen el comportamiento de los grupos de Office.</span><span class="sxs-lookup"><span data-stu-id="590fb-114">Currently system defined settings are only govern Office groups behavior.</span></span>

> <span data-ttu-id="590fb-115">**Nota**: la versión de /beta del tipo de recurso establecer solo se aplica a los grupos.</span><span class="sxs-lookup"><span data-stu-id="590fb-115">**Note**: The /beta version of the directorySetting resource type only applies to groups.</span></span> <span data-ttu-id="590fb-116">Se ha cambiado la versión de /v1.0 a groupSetting.</span><span class="sxs-lookup"><span data-stu-id="590fb-116">The /v1.0 version has been renamed to groupSetting.</span></span>

## <a name="methods"></a><span data-ttu-id="590fb-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="590fb-117">Methods</span></span>

| <span data-ttu-id="590fb-118">Método</span><span class="sxs-lookup"><span data-stu-id="590fb-118">Method</span></span>           | <span data-ttu-id="590fb-119">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="590fb-119">Return Type</span></span>    |<span data-ttu-id="590fb-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="590fb-120">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="590fb-121">Create setting</span><span class="sxs-lookup"><span data-stu-id="590fb-121">Create setting</span></span>](../api/directorysetting-post-settings.md) | [<span data-ttu-id="590fb-122">Establecer</span><span class="sxs-lookup"><span data-stu-id="590fb-122">directorySetting</span></span>](directorysetting.md) |<span data-ttu-id="590fb-123">Crear un objeto de configuración basado en un directorySettingTemplate.</span><span class="sxs-lookup"><span data-stu-id="590fb-123">Create a setting object based on a directorySettingTemplate.</span></span> <span data-ttu-id="590fb-124">La solicitud POST debe proporcionar settingValues para toda la configuración definida en la plantilla.</span><span class="sxs-lookup"><span data-stu-id="590fb-124">The POST request must provide settingValues for all the settings defined in the template.</span></span>|
|[<span data-ttu-id="590fb-125">Get setting</span><span class="sxs-lookup"><span data-stu-id="590fb-125">Get setting</span></span>](../api/directorysetting-get.md) | [<span data-ttu-id="590fb-126">Establecer</span><span class="sxs-lookup"><span data-stu-id="590fb-126">directorySetting</span></span>](directorysetting.md) |<span data-ttu-id="590fb-127">Lee las propiedades de un objeto de configuración específico.</span><span class="sxs-lookup"><span data-stu-id="590fb-127">Read properties of a specific setting object.</span></span>|
|[<span data-ttu-id="590fb-128">List settings</span><span class="sxs-lookup"><span data-stu-id="590fb-128">List settings</span></span>](../api/directorysetting-list.md) | <span data-ttu-id="590fb-129">colección de [establecer](directorysetting.md)</span><span class="sxs-lookup"><span data-stu-id="590fb-129">[directorySetting](directorysetting.md) collection</span></span> |<span data-ttu-id="590fb-130">Enumera las propiedades de todos los objetos de configuración.</span><span class="sxs-lookup"><span data-stu-id="590fb-130">List properties of all setting objects.</span></span>|
|[<span data-ttu-id="590fb-131">Configuración de actualización</span><span class="sxs-lookup"><span data-stu-id="590fb-131">Update setting</span></span>](../api/directorysetting-update.md) | [<span data-ttu-id="590fb-132">Establecer</span><span class="sxs-lookup"><span data-stu-id="590fb-132">directorySetting</span></span>](directorysetting.md)  |<span data-ttu-id="590fb-133">Actualiza el objeto de configuración.</span><span class="sxs-lookup"><span data-stu-id="590fb-133">Update a setting object.</span></span> <span data-ttu-id="590fb-134">SettingValues sólo se puede cambiar en una actualización.</span><span class="sxs-lookup"><span data-stu-id="590fb-134">Only settingValues can be changed in an update.</span></span>|
|[<span data-ttu-id="590fb-135">Delete setting</span><span class="sxs-lookup"><span data-stu-id="590fb-135">Delete setting</span></span>](../api/directorysetting-delete.md) | <span data-ttu-id="590fb-136">Ninguno</span><span class="sxs-lookup"><span data-stu-id="590fb-136">None</span></span> |<span data-ttu-id="590fb-137">Elimina un objeto de configuración.</span><span class="sxs-lookup"><span data-stu-id="590fb-137">Delete a setting object.</span></span> |

## <a name="properties"></a><span data-ttu-id="590fb-138">Propiedades</span><span class="sxs-lookup"><span data-stu-id="590fb-138">Properties</span></span>
| <span data-ttu-id="590fb-139">Propiedad</span><span class="sxs-lookup"><span data-stu-id="590fb-139">Property</span></span>     | <span data-ttu-id="590fb-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="590fb-140">Type</span></span>   |<span data-ttu-id="590fb-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="590fb-141">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="590fb-142">displayName</span><span class="sxs-lookup"><span data-stu-id="590fb-142">displayName</span></span>|<span data-ttu-id="590fb-143">string</span><span class="sxs-lookup"><span data-stu-id="590fb-143">string</span></span>|<span data-ttu-id="590fb-144">El nombre para mostrar de este grupo de configuraciones, que proviene de la plantilla asociada.</span><span class="sxs-lookup"><span data-stu-id="590fb-144">Display name of this group of settings, which comes from the associated template.</span></span> <span data-ttu-id="590fb-145">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="590fb-145">Read-only.</span></span>|
|<span data-ttu-id="590fb-146">id</span><span class="sxs-lookup"><span data-stu-id="590fb-146">id</span></span>|<span data-ttu-id="590fb-147">string</span><span class="sxs-lookup"><span data-stu-id="590fb-147">string</span></span>| <span data-ttu-id="590fb-p108">Identificador único de esta configuración. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="590fb-p108">Unique identifier for these settings. Read-only.</span></span>|
|<span data-ttu-id="590fb-150">templateId</span><span class="sxs-lookup"><span data-stu-id="590fb-150">templateId</span></span>|<span data-ttu-id="590fb-151">string</span><span class="sxs-lookup"><span data-stu-id="590fb-151">string</span></span>| <span data-ttu-id="590fb-p109">Identificador único para la plantilla que se usa para crear este grupo de configuraciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="590fb-p109">Unique identifier for the template used to create this group of settings. Read-only.</span></span>|
|<span data-ttu-id="590fb-154">values</span><span class="sxs-lookup"><span data-stu-id="590fb-154">values</span></span>|<span data-ttu-id="590fb-155">Colección de [settingValue](settingvalue.md)</span><span class="sxs-lookup"><span data-stu-id="590fb-155">[settingValue](settingvalue.md) collection</span></span>| <span data-ttu-id="590fb-p110">Colección de pares de nombre y valor. Debe contener y establecer todas las configuraciones definidas en la plantilla.</span><span class="sxs-lookup"><span data-stu-id="590fb-p110">Collection of name value pairs. Must contain and set all the settings defined in the template.</span></span>|

## <a name="relationships"></a><span data-ttu-id="590fb-158">Relaciones</span><span class="sxs-lookup"><span data-stu-id="590fb-158">Relationships</span></span>
<span data-ttu-id="590fb-159">Ninguno</span><span class="sxs-lookup"><span data-stu-id="590fb-159">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="590fb-160">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="590fb-160">JSON representation</span></span>

<span data-ttu-id="590fb-161">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="590fb-161">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.directorySetting"
}-->

```json
{
  "displayName": "string",
  "id": "string (identifier)",
  "templateId": "string",
  "values": [{"@odata.type": "microsoft.graph.settingValue"}]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directorySetting resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->