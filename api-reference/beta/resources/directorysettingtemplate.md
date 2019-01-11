---
title: tipo de recurso directorySettingTemplate
description: Plantillas de configuración de Active Directory representan definidas por el sistema de configuración disponible para el inquilino. Configuración de Active Directory se puede crear en función de la directorySettingTemplates disponibles y los valores que ha cambiado desde sus valores predeterminados. Plantillas de configuración de Active Directory no se crea, actualiza o elimina. Esta configuración puede representan la configuración de todo el inquilino, o puede representan la configuración de la entidad específica.  Actualmente, las plantillas sólo disponibles se aplican a los grupos de Office e incluyen opciones de configuración, como si los usuarios pueden crear grupos o invitar a personas de fuera de la organización para convertirse en miembros de un grupo.
localization_priority: Normal
ms.openlocfilehash: e0df923854059723ee83380f7aa0f6425cf2afb9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27806149"
---
# <a name="directorysettingtemplate-resource-type"></a><span data-ttu-id="00124-107">tipo de recurso directorySettingTemplate</span><span class="sxs-lookup"><span data-stu-id="00124-107">directorySettingTemplate resource type</span></span>

> <span data-ttu-id="00124-108">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="00124-108">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="00124-109">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="00124-109">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="00124-110">Plantillas de configuración de Active Directory representan definidas por el sistema de configuración disponible para el inquilino.</span><span class="sxs-lookup"><span data-stu-id="00124-110">Directory setting templates represent system-defined settings available to the tenant.</span></span> <span data-ttu-id="00124-111">[Configuración de Active Directory](directorysetting.md) se pueden crear en función de la directorySettingTemplates disponibles y los valores que ha cambiado desde sus valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="00124-111">[Directory settings](directorysetting.md) can be created based on the available directorySettingTemplates, and values changed from their preset defaults.</span></span> <span data-ttu-id="00124-112">Plantillas de configuración de Active Directory no se crea, actualiza o elimina.</span><span class="sxs-lookup"><span data-stu-id="00124-112">Directory setting templates cannot be created, updated or deleted.</span></span> <span data-ttu-id="00124-113">Esta configuración puede representan la configuración de todo el inquilino, o puede representan la configuración de la entidad específica.</span><span class="sxs-lookup"><span data-stu-id="00124-113">These settings can represent tenant-wide settings, or can represent specific entity settings.</span></span>  <span data-ttu-id="00124-114">Actualmente, las plantillas sólo disponibles se aplican a los grupos de Office e incluyen opciones de configuración, como si los usuarios pueden crear grupos o invitar a personas de fuera de la organización para convertirse en miembros de un grupo.</span><span class="sxs-lookup"><span data-stu-id="00124-114">Currently, the only templates available apply to Office groups, and include settings such as whether users can create groups or invite guests from outside the organization to become members of a group.</span></span>

> <span data-ttu-id="00124-115">**Nota**: la versión de /beta del tipo de recurso directorySettingTemplate sólo se aplica a los grupos.</span><span class="sxs-lookup"><span data-stu-id="00124-115">**Note**: The /beta version of the directorySettingTemplate resource type only applies to groups.</span></span> <span data-ttu-id="00124-116">Se ha cambiado la versión de /v1.0 a groupSettingTemplate.</span><span class="sxs-lookup"><span data-stu-id="00124-116">The /v1.0 version has been renamed to groupSettingTemplate.</span></span>

## <a name="methods"></a><span data-ttu-id="00124-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="00124-117">Methods</span></span>

| <span data-ttu-id="00124-118">Método</span><span class="sxs-lookup"><span data-stu-id="00124-118">Method</span></span>           | <span data-ttu-id="00124-119">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00124-119">Return Type</span></span>    |<span data-ttu-id="00124-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="00124-120">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="00124-121">Obtener directorySettingTemplate</span><span class="sxs-lookup"><span data-stu-id="00124-121">Get directorySettingTemplate</span></span>](../api/directorysettingtemplate-get.md) | [<span data-ttu-id="00124-122">directorySettingTemplate</span><span class="sxs-lookup"><span data-stu-id="00124-122">directorySettingTemplate</span></span>](directorysettingtemplate.md) |<span data-ttu-id="00124-123">Lea las propiedades específicas de uno de los objetos de directorySettingTemplate definida por el sistema.</span><span class="sxs-lookup"><span data-stu-id="00124-123">Read the specific properties of one of the system defined directorySettingTemplate objects.</span></span>|
|[<span data-ttu-id="00124-124">Lista directorySettingTemplate</span><span class="sxs-lookup"><span data-stu-id="00124-124">List directorySettingTemplate</span></span>](../api/directorysettingtemplate-list.md) | [<span data-ttu-id="00124-125">Colección de directorySettingTemplate</span><span class="sxs-lookup"><span data-stu-id="00124-125">Collection of directorySettingTemplate</span></span>](directorysettingtemplate.md) |<span data-ttu-id="00124-126">Lista de todos los objetos de directorySettingTemplate definida por el sistema.</span><span class="sxs-lookup"><span data-stu-id="00124-126">List all of the system defined directorySettingTemplate objects.</span></span>|

## <a name="properties"></a><span data-ttu-id="00124-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="00124-127">Properties</span></span>
| <span data-ttu-id="00124-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="00124-128">Property</span></span>     | <span data-ttu-id="00124-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="00124-129">Type</span></span>   |<span data-ttu-id="00124-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="00124-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="00124-131">description</span><span class="sxs-lookup"><span data-stu-id="00124-131">description</span></span>|<span data-ttu-id="00124-132">string</span><span class="sxs-lookup"><span data-stu-id="00124-132">string</span></span>|<span data-ttu-id="00124-133">Descripción de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="00124-133">Description of the template.</span></span> <span data-ttu-id="00124-134">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="00124-134">Read-only.</span></span>|
|<span data-ttu-id="00124-135">displayName</span><span class="sxs-lookup"><span data-stu-id="00124-135">displayName</span></span>|<span data-ttu-id="00124-136">string</span><span class="sxs-lookup"><span data-stu-id="00124-136">string</span></span>|<span data-ttu-id="00124-137">Muestra el nombre de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="00124-137">Display name of the template.</span></span> <span data-ttu-id="00124-138">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="00124-138">Read-only.</span></span> |
|<span data-ttu-id="00124-139">id</span><span class="sxs-lookup"><span data-stu-id="00124-139">id</span></span>|<span data-ttu-id="00124-140">string</span><span class="sxs-lookup"><span data-stu-id="00124-140">string</span></span>| <span data-ttu-id="00124-p107">Identificador único de la plantilla. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="00124-p107">Unique identifier for the template. Read-only.</span></span>|
|<span data-ttu-id="00124-143">values</span><span class="sxs-lookup"><span data-stu-id="00124-143">values</span></span>|<span data-ttu-id="00124-144">Colección de [settingTemplateValue](settingtemplatevalue.md)</span><span class="sxs-lookup"><span data-stu-id="00124-144">[settingTemplateValue](settingtemplatevalue.md) collection</span></span>| <span data-ttu-id="00124-145">Colección de settingTemplateValues que enumera el conjunto de opciones disponibles, los valores predeterminados y los tipos que forman esta plantilla.</span><span class="sxs-lookup"><span data-stu-id="00124-145">Collection of settingTemplateValues that list the set of available settings, defaults and types that make up this template.</span></span>  <span data-ttu-id="00124-146">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="00124-146">Read-only.</span></span> |

## <a name="relationships"></a><span data-ttu-id="00124-147">Relaciones</span><span class="sxs-lookup"><span data-stu-id="00124-147">Relationships</span></span>
<span data-ttu-id="00124-148">Ninguno</span><span class="sxs-lookup"><span data-stu-id="00124-148">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="00124-149">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="00124-149">JSON representation</span></span>

<span data-ttu-id="00124-150">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="00124-150">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.directorySettingTemplate"
}-->

```json
{
  "description": "string",
  "displayName": "string",
  "id": "string (identifier)",
  "values": [{"@odata.type": "microsoft.graph.settingTemplateValue"}]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directorySettingTemplate resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
