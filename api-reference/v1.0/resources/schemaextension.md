---
title: Tipo de recurso schemaExtension (extensiones de esquema)
description: 'Las extensiones de esquema permiten definir un esquema para extender y agregar datos personalizados fuertemente tipados a un tipo de recurso. Los datos personalizados aparecen como un tipo complejo en el recurso extendido. '
ms.openlocfilehash: 885b315897814cc15f83526086edb9cf298995f7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031542"
---
# <a name="schemaextension-resource-type-schema-extensions"></a><span data-ttu-id="cb7e1-104">Tipo de recurso schemaExtension (extensiones de esquema)</span><span class="sxs-lookup"><span data-stu-id="cb7e1-104">schemaExtension resource type (schema extensions)</span></span>

<span data-ttu-id="cb7e1-p102">Las extensiones de esquema permiten definir un esquema para extender y agregar datos personalizados fuertemente tipados a un tipo de recurso. Los datos personalizados aparecen como un tipo complejo en el recurso extendido.</span><span class="sxs-lookup"><span data-stu-id="cb7e1-p102">Schema extensions allow you to define a schema to extend and add strongly-typed custom data to a resource type. The custom data appears as a complex type on the extended resource.</span></span> 

<span data-ttu-id="cb7e1-107">Las extensiones de esquema son compatibles con los siguientes tipos de recursos:</span><span class="sxs-lookup"><span data-stu-id="cb7e1-107">Schema extensions are supported by the following resource types:</span></span>

 - [<span data-ttu-id="cb7e1-108">contact</span><span class="sxs-lookup"><span data-stu-id="cb7e1-108">contact</span></span>](contact.md)
 - [<span data-ttu-id="cb7e1-109">device</span><span class="sxs-lookup"><span data-stu-id="cb7e1-109">device</span></span>](device.md)
 - <span data-ttu-id="cb7e1-110">[evento](event.md) en un usuario o un calendario de grupo de Office 365</span><span class="sxs-lookup"><span data-stu-id="cb7e1-110">[event](event.md) on a user or Office 365 group calendar</span></span>
 - <span data-ttu-id="cb7e1-111">[post](post.md) de un grupo de Office 365</span><span class="sxs-lookup"><span data-stu-id="cb7e1-111">[post](post.md) of an Office 365 group</span></span>
 - [<span data-ttu-id="cb7e1-112">group</span><span class="sxs-lookup"><span data-stu-id="cb7e1-112">group</span></span>](group.md)
 - [<span data-ttu-id="cb7e1-113">message</span><span class="sxs-lookup"><span data-stu-id="cb7e1-113">message</span></span>](message.md) 
 - [<span data-ttu-id="cb7e1-114">organization</span><span class="sxs-lookup"><span data-stu-id="cb7e1-114">organization</span></span>](organization.md)
 - [<span data-ttu-id="cb7e1-115">user</span><span class="sxs-lookup"><span data-stu-id="cb7e1-115">user</span></span>](user.md)

<span data-ttu-id="cb7e1-116">Consulte el [ejemplo de extensión de esquema](/graph/extensibility-schema-groups) para obtener información sobre cómo agregar datos personalizados a los grupos.</span><span class="sxs-lookup"><span data-stu-id="cb7e1-116">See the [schema extension example](/graph/extensibility-schema-groups) to learn how to add custom data to groups.</span></span>

## <a name="methods"></a><span data-ttu-id="cb7e1-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="cb7e1-117">Methods</span></span>

| <span data-ttu-id="cb7e1-118">Método</span><span class="sxs-lookup"><span data-stu-id="cb7e1-118">Method</span></span>           | <span data-ttu-id="cb7e1-119">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb7e1-119">Return Type</span></span>    |<span data-ttu-id="cb7e1-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="cb7e1-120">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="cb7e1-121">Create</span><span class="sxs-lookup"><span data-stu-id="cb7e1-121">Create</span></span>](../api/schemaextension-post-schemaextensions.md) | <span data-ttu-id="cb7e1-122">schemaExtension</span><span class="sxs-lookup"><span data-stu-id="cb7e1-122">schemaExtension</span></span> |<span data-ttu-id="cb7e1-123">Crea una definición de extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="cb7e1-123">Create a schema extension definition.</span></span>|
|[<span data-ttu-id="cb7e1-124">List</span><span class="sxs-lookup"><span data-stu-id="cb7e1-124">List</span></span>](../api/schemaextension-list.md) | <span data-ttu-id="cb7e1-125">schemaExtension</span><span class="sxs-lookup"><span data-stu-id="cb7e1-125">schemaExtension</span></span> |<span data-ttu-id="cb7e1-126">Enumera las definiciones schemaExtension disponibles y sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="cb7e1-126">List the available schemaExtension definitions and their properties.</span></span>|
|[<span data-ttu-id="cb7e1-127">Get</span><span class="sxs-lookup"><span data-stu-id="cb7e1-127">Get</span></span>](../api/schemaextension-get.md) | <span data-ttu-id="cb7e1-128">schemaExtension</span><span class="sxs-lookup"><span data-stu-id="cb7e1-128">schemaExtension</span></span> |<span data-ttu-id="cb7e1-129">Lee las propiedades de una definición schemaExtension específica.</span><span class="sxs-lookup"><span data-stu-id="cb7e1-129">Read the properties of a specific schemaExtension definition.</span></span>|
|[<span data-ttu-id="cb7e1-130">Update</span><span class="sxs-lookup"><span data-stu-id="cb7e1-130">Update</span></span>](../api/schemaextension-update.md) | <span data-ttu-id="cb7e1-131">schemaExtension</span><span class="sxs-lookup"><span data-stu-id="cb7e1-131">schemaExtension</span></span>   |<span data-ttu-id="cb7e1-132">Actualiza una definición schemaExtension.</span><span class="sxs-lookup"><span data-stu-id="cb7e1-132">Update a schemaExtension definition.</span></span> |
|[<span data-ttu-id="cb7e1-133">Delete</span><span class="sxs-lookup"><span data-stu-id="cb7e1-133">Delete</span></span>](../api/schemaextension-delete.md) | <span data-ttu-id="cb7e1-134">Ninguno</span><span class="sxs-lookup"><span data-stu-id="cb7e1-134">None</span></span> |<span data-ttu-id="cb7e1-135">Elimina una definición schemaExtension.</span><span class="sxs-lookup"><span data-stu-id="cb7e1-135">Delete a schemaExtension definition.</span></span> |

## <a name="properties"></a><span data-ttu-id="cb7e1-136">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cb7e1-136">Properties</span></span>
| <span data-ttu-id="cb7e1-137">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cb7e1-137">Property</span></span>     | <span data-ttu-id="cb7e1-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="cb7e1-138">Type</span></span>   |<span data-ttu-id="cb7e1-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="cb7e1-139">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="cb7e1-140">description</span><span class="sxs-lookup"><span data-stu-id="cb7e1-140">description</span></span>|<span data-ttu-id="cb7e1-141">String</span><span class="sxs-lookup"><span data-stu-id="cb7e1-141">String</span></span>|<span data-ttu-id="cb7e1-142">Descripción de la extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="cb7e1-142">Description for the schema extension.</span></span>|
|<span data-ttu-id="cb7e1-143">id</span><span class="sxs-lookup"><span data-stu-id="cb7e1-143">id</span></span>|<span data-ttu-id="cb7e1-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="cb7e1-144">String</span></span>|<span data-ttu-id="cb7e1-145">Identificador único para la definición de la extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="cb7e1-145">The unique identifier for the schema extension definition.</span></span> <br><span data-ttu-id="cb7e1-146">Puede asignar un valor de dos maneras:</span><span class="sxs-lookup"><span data-stu-id="cb7e1-146">You can assign a value in one of two ways:</span></span> <ul><li><span data-ttu-id="cb7e1-p103">Concatenar el nombre de uno de los dominios comprobados con un nombre para la extensión del esquema con el fin de formar una cadena única en este formato, \{_&#65279;domainName_\}\_\{_&#65279;schemaName_\}. Por ejemplo, `contoso_mySchema`. </span><span class="sxs-lookup"><span data-stu-id="cb7e1-p103">Concatenate the name of one of your verified domains with a name for the schema extension to form a unique string in this format, \{_&#65279;domainName_\}\_\{_&#65279;schemaName_\}. As an example, `contoso_mySchema`. </span></span></li><li><span data-ttu-id="cb7e1-p104">Proporcionar un nombre de esquema y permitir a Microsoft Graph utilizar ese nombre de esquema para completar la asignación del **id.** en este formato: ext\{_&#65279;8-random-alphanumeric-chars_\}\_\{_&#65279;schema-name_\}. Un ejemplo sería `extkvbmkofy_mySchema`.</span><span class="sxs-lookup"><span data-stu-id="cb7e1-p104">Provide a schema name, and let Microsoft Graph use that schema name to complete the **id** assignment in this format: ext\{_&#65279;8-random-alphanumeric-chars_\}\_\{_&#65279;schema-name_\}. An example would be `extkvbmkofy_mySchema`.</span></span></li></ul><span data-ttu-id="cb7e1-151">Una vez creada, esta propiedad no se puede modificar.</span><span class="sxs-lookup"><span data-stu-id="cb7e1-151">This property cannot be changed after creation.</span></span> |
|<span data-ttu-id="cb7e1-152">owner</span><span class="sxs-lookup"><span data-stu-id="cb7e1-152">owner</span></span>|<span data-ttu-id="cb7e1-153">String</span><span class="sxs-lookup"><span data-stu-id="cb7e1-153">String</span></span>|<span data-ttu-id="cb7e1-154">El `appId` de la aplicación que es el propietario de la extensión del esquema.</span><span class="sxs-lookup"><span data-stu-id="cb7e1-154">The `appId` of the application that is the owner of the schema extension.</span></span> <span data-ttu-id="cb7e1-155">Esta propiedad se puede proporcionar en la creación, para establecer el propietario.</span><span class="sxs-lookup"><span data-stu-id="cb7e1-155">This property can be supplied on creation, to set the owner.</span></span>  <span data-ttu-id="cb7e1-156">Si no se proporciona, entonces la aplicación de llamada `appId` se establecerá como la propietaria.</span><span class="sxs-lookup"><span data-stu-id="cb7e1-156">If not supplied, then the calling application's `appId` will be set as the owner.</span></span> <span data-ttu-id="cb7e1-157">En cualquier caso, el usuario que inició sesión debe ser el propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cb7e1-157">In either case, the signed-in user must be the owner of the application.</span></span> <span data-ttu-id="cb7e1-158">Una vez establecida, esta propiedad es de solo lectura y no se puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="cb7e1-158">Once set, this property is read-only and cannot be changed.</span></span>| 
|<span data-ttu-id="cb7e1-159">properties</span><span class="sxs-lookup"><span data-stu-id="cb7e1-159">properties</span></span>|<span data-ttu-id="cb7e1-160">Colección [extensionSchemaProperty](extensionschemaproperty.md)</span><span class="sxs-lookup"><span data-stu-id="cb7e1-160">[extensionSchemaProperty](extensionschemaproperty.md) collection</span></span>|<span data-ttu-id="cb7e1-161">La colección de nombres de propiedad y tipos que conforman la definición de la extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="cb7e1-161">The collection of property names and types that make up the schema extension definition.</span></span>|
|<span data-ttu-id="cb7e1-162">status</span><span class="sxs-lookup"><span data-stu-id="cb7e1-162">status</span></span>|<span data-ttu-id="cb7e1-163">String</span><span class="sxs-lookup"><span data-stu-id="cb7e1-163">String</span></span>|<span data-ttu-id="cb7e1-p106">El estado del ciclo de vida de la extensión de esquema. Los estados posibles son **InDevelopment** (En desarrollo), **Available** (Disponible) y **Deprecated** (En desuso). En el momento de la creación se establece automáticamente en **InDevelopment**. Las [extensiones de esquema](/graph/extensibility-overview#schema-extensions) proporcionan más información sobre los comportamientos y las transiciones de estado posibles.</span><span class="sxs-lookup"><span data-stu-id="cb7e1-p106">The lifecycle state of the schema extension. Possible states are **InDevelopment**, **Available**, and **Deprecated**. Automatically set to **InDevelopment** on creation. [Schema extensions](/graph/extensibility-overview#schema-extensions) provides more information on the possible state transitions and behaviors.</span></span>|
|<span data-ttu-id="cb7e1-168">targetTypes</span><span class="sxs-lookup"><span data-stu-id="cb7e1-168">targetTypes</span></span>|<span data-ttu-id="cb7e1-169">Colección string</span><span class="sxs-lookup"><span data-stu-id="cb7e1-169">String collection</span></span>|<span data-ttu-id="cb7e1-p107">Conjunto de tipos de Microsoft Graph (compatibles con extensiones) a los que se puede aplicar la extensión de esquema. Seleccione **contact**, **device**, **event**, **group**, **message**, **organization**, **post** o **user**.</span><span class="sxs-lookup"><span data-stu-id="cb7e1-p107">Set of Microsoft Graph types (that can support extensions) that the schema extension can be applied to. Select from **contact**, **device**, **event**, **group**, **message**, **organization**, **post**, or **user**.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="cb7e1-172">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cb7e1-172">JSON representation</span></span>

<span data-ttu-id="cb7e1-173">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="cb7e1-173">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.schemaExtension"
}-->

```json
{
  "description": "String",
  "id": "String (identifier)",
  "owner": "String",
  "properties": [{"@odata.type": "microsoft.graph.extensionSchemaProperty"}],
  "status": "String",
  "targetTypes": ["String"]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "schemaExtension resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->