---
title: tipo de recurso synchronizationTemplate
description: " cualquier usuario puede recuperar la plantilla para ver la configuración predeterminada, incluido el esquema de sincronización."
ms.openlocfilehash: 90850ad43fdd14fc38ff6ae8cfa97f47806a289d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087234"
---
# <a name="synchronizationtemplate-resource-type"></a><span data-ttu-id="6e579-103">tipo de recurso synchronizationTemplate</span><span class="sxs-lookup"><span data-stu-id="6e579-103">synchronizationTemplate resource type</span></span>

> <span data-ttu-id="6e579-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6e579-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6e579-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6e579-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6e579-106">Proporciona opciones de configuración de sincronización preconfigurado para una aplicación concreta.</span><span class="sxs-lookup"><span data-stu-id="6e579-106">Provides pre-configured synchronization settings for a particular application.</span></span> <span data-ttu-id="6e579-107">Estas opciones de configuración se usará de forma predeterminada para cualquier [trabajo de sincronización](synchronization-synchronizationjob.md) que se basa en la plantilla.</span><span class="sxs-lookup"><span data-stu-id="6e579-107">These settings will be used by default for any [synchronization job](synchronization-synchronizationjob.md) that is based on the template.</span></span> <span data-ttu-id="6e579-108">El desarrollador de la aplicación especifica la plantilla; cualquier usuario puede recuperar la plantilla para ver la configuración predeterminada, incluido el [esquema de sincronización](synchronization-synchronizationschema.md).</span><span class="sxs-lookup"><span data-stu-id="6e579-108">The application developer specifies the template; anyone can retrieve the template to see the default settings, including the [synchronization schema](synchronization-synchronizationschema.md).</span></span>

<span data-ttu-id="6e579-109">Puede proporcionar varias plantillas de una aplicación y designar una plantilla predeterminada.</span><span class="sxs-lookup"><span data-stu-id="6e579-109">You can provide multiple templates for an application, and designate a default template.</span></span> <span data-ttu-id="6e579-110">Si varias plantillas están disponibles para la aplicación que le interesa, seek instrucciones específicas de la aplicación para determinar qué una mejor adapte a sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="6e579-110">If multiple templates are available for the application you're interested in, seek application-specific guidance to determine which one best meets your needs.</span></span>

## <a name="methods"></a><span data-ttu-id="6e579-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="6e579-111">Methods</span></span>

| <span data-ttu-id="6e579-112">Método</span><span class="sxs-lookup"><span data-stu-id="6e579-112">Method</span></span>        | <span data-ttu-id="6e579-113">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e579-113">Return Type</span></span>               | <span data-ttu-id="6e579-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e579-114">Description</span></span>                  |
|:--------------|:--------------------------|:-----------------------------|
|[<span data-ttu-id="6e579-115">List</span><span class="sxs-lookup"><span data-stu-id="6e579-115">List</span></span>](../api/synchronization-synchronizationtemplate-list.md)    |<span data-ttu-id="6e579-116">colección de [synchronizationTemplate](synchronization-synchronizationtemplate.md)</span><span class="sxs-lookup"><span data-stu-id="6e579-116">[synchronizationTemplate](synchronization-synchronizationtemplate.md) collection</span></span>  |<span data-ttu-id="6e579-117">Lista de las plantillas que están disponibles para una aplicación o una instancia de la aplicación (entidad de seguridad de servicio).</span><span class="sxs-lookup"><span data-stu-id="6e579-117">List the templates that are available for an application or application instance (service principal).</span></span>|
|[<span data-ttu-id="6e579-118">Get</span><span class="sxs-lookup"><span data-stu-id="6e579-118">Get</span></span>](../api/synchronization-synchronizationtemplate-get.md)      |[<span data-ttu-id="6e579-119">synchronizationTemplate</span><span class="sxs-lookup"><span data-stu-id="6e579-119">synchronizationTemplate</span></span>](synchronization-synchronizationtemplate.md)   |<span data-ttu-id="6e579-120">Lea las propiedades y relaciones del objeto **synchronizationTemplate** .</span><span class="sxs-lookup"><span data-stu-id="6e579-120">Read the properties and relationships of the **synchronizationTemplate** object.</span></span>|
<!-- 
|[Create](../api/synchronization-synchronizationtemplate-post.md) |[synchronizationTemplate](synchronization-synchronizationtemplate.md)   |Create a new template for an application.|
|[Update](../api/synchronization-synchronizationtemplate-put.md)   |[synchronizationTemplate](synchronization-synchronizationtemplate.md)   |Update the template.| 
-->

## <a name="properties"></a><span data-ttu-id="6e579-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6e579-121">Properties</span></span>

| <span data-ttu-id="6e579-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6e579-122">Property</span></span>      | <span data-ttu-id="6e579-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e579-123">Type</span></span>                      | <span data-ttu-id="6e579-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e579-124">Description</span></span>                  |
|:--------------|:--------------------------|:-----------------------------|
|<span data-ttu-id="6e579-125">id</span><span class="sxs-lookup"><span data-stu-id="6e579-125">id</span></span>             |<span data-ttu-id="6e579-126">String</span><span class="sxs-lookup"><span data-stu-id="6e579-126">String</span></span>                     |<span data-ttu-id="6e579-127">Identificador de plantilla único.</span><span class="sxs-lookup"><span data-stu-id="6e579-127">Unique template identifier.</span></span>|
|<span data-ttu-id="6e579-128">applicationId</span><span class="sxs-lookup"><span data-stu-id="6e579-128">applicationId</span></span>  |<span data-ttu-id="6e579-129">cadena</span><span class="sxs-lookup"><span data-stu-id="6e579-129">String</span></span>                     |<span data-ttu-id="6e579-130">Identificador de la aplicación al que pertenece esta plantilla.</span><span class="sxs-lookup"><span data-stu-id="6e579-130">Identifier of the application this template belongs to.</span></span>|
|<span data-ttu-id="6e579-131">Es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6e579-131">default</span></span>        |<span data-ttu-id="6e579-132">Booleano</span><span class="sxs-lookup"><span data-stu-id="6e579-132">Boolean</span></span>                    |<span data-ttu-id="6e579-133">`true`Si esta plantilla se recomienda que tenga el valor predeterminado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6e579-133">`true` if this template is recommended to be the default for the application.</span></span>|
|<span data-ttu-id="6e579-134">descripción</span><span class="sxs-lookup"><span data-stu-id="6e579-134">description</span></span>    |<span data-ttu-id="6e579-135">String</span><span class="sxs-lookup"><span data-stu-id="6e579-135">String</span></span>                     |<span data-ttu-id="6e579-136">Descripción de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="6e579-136">Description of the template.</span></span>|
|<span data-ttu-id="6e579-137">que se pueda detectar</span><span class="sxs-lookup"><span data-stu-id="6e579-137">discoverable</span></span>   |<span data-ttu-id="6e579-138">String</span><span class="sxs-lookup"><span data-stu-id="6e579-138">String</span></span>                     |<span data-ttu-id="6e579-139">`true`Si esta plantilla debe aparecer en la colección de plantillas disponibles para la instancia de aplicación (entidad de seguridad de servicio).</span><span class="sxs-lookup"><span data-stu-id="6e579-139">`true` if this template should appear in the collection of templates available for the application instance (service principal).</span></span>|
|<span data-ttu-id="6e579-140">factoryTag</span><span class="sxs-lookup"><span data-stu-id="6e579-140">factoryTag</span></span>     |<span data-ttu-id="6e579-141">String</span><span class="sxs-lookup"><span data-stu-id="6e579-141">String</span></span>                     |<span data-ttu-id="6e579-142">Una de las etiquetas de fábrica Well-known compatibles con el motor de sincronización.</span><span class="sxs-lookup"><span data-stu-id="6e579-142">One of the well-known factory tags supported by the synchronization engine.</span></span> <span data-ttu-id="6e579-143">La **factoryTag** indica que el motor de sincronización a qué implementación a utilizar al procesamiento de trabajos basados en esta plantilla.</span><span class="sxs-lookup"><span data-stu-id="6e579-143">The **factoryTag** tells the synchronization engine which implementation to use when processing jobs based on this template.</span></span>|
|<span data-ttu-id="6e579-144">metadatos</span><span class="sxs-lookup"><span data-stu-id="6e579-144">metadata</span></span>       |<span data-ttu-id="6e579-145">colección de metadataEntry</span><span class="sxs-lookup"><span data-stu-id="6e579-145">metadataEntry collection</span></span>   |<span data-ttu-id="6e579-146">Propiedades de extensión adicionales.</span><span class="sxs-lookup"><span data-stu-id="6e579-146">Additional extension properties.</span></span> <span data-ttu-id="6e579-147">A menos que se mencionan explícitamente, no se deben cambiar los valores de metadatos.</span><span class="sxs-lookup"><span data-stu-id="6e579-147">Unless mentioned explicitly, metadata values should not be changed.</span></span>|

## <a name="relationships"></a><span data-ttu-id="6e579-148">Relaciones</span><span class="sxs-lookup"><span data-stu-id="6e579-148">Relationships</span></span>
| <span data-ttu-id="6e579-149">Relación</span><span class="sxs-lookup"><span data-stu-id="6e579-149">Relationship</span></span>      | <span data-ttu-id="6e579-150">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e579-150">Type</span></span>      |<span data-ttu-id="6e579-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e579-151">Description</span></span>|
|:------------------|:----------|:----------|
|<span data-ttu-id="6e579-152">esquema</span><span class="sxs-lookup"><span data-stu-id="6e579-152">schema</span></span>             |[<span data-ttu-id="6e579-153">synchronizationSchema</span><span class="sxs-lookup"><span data-stu-id="6e579-153">synchronizationSchema</span></span>](synchronization-synchronizationschema.md)     |<span data-ttu-id="6e579-154">Esquema de sincronización predeterminado para las tareas basadas en esta plantilla.</span><span class="sxs-lookup"><span data-stu-id="6e579-154">Default synchronization schema for the jobs based on this template.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="6e579-155">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6e579-155">JSON representation</span></span>

<span data-ttu-id="6e579-156">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="6e579-156">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.synchronizationTemplate"
}-->

```json
{
  "applicationId": "String (identifier)",
  "default": true,
  "description": "String",
  "discoverable": true,
  "factoryTag": "String",
  "id": "String (identifier)",
  "metadata": [{"@odata.type": "microsoft.graph.metadataEntry"}],
  "schema": {"@odata.type": "microsoft.graph.synchronizationSchema"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "synchronizationTemplate resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->