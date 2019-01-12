---
title: Tipo de recurso directoryRoleTemplate
description: 'Representa una plantilla de rol de Active directory. Una plantilla de rol de Active directory especifica los valores de propiedad de un rol de Active directory (directoryRole). Hay un objeto de plantilla de rol asociados en el directorio para cada uno de los roles de Active directory que se pueden activar en un inquilino. Para leer un rol de Active directory o actualizar a sus miembros, debe activarse en primer lugar en el inquilino. Sólo el rol de Active directory de administradores de la compañía se activa de forma predeterminada. Para activar otros roles de Active directory disponibles enviar una solicitud POST para la `/directoryRoles` extremo con el identificador de la plantilla de rol de Active directory en el que se basa el rol de Active directory especificado en el parámetro **roleTemplateId** de la solicitud. Tras completar correctamente esta solicitud, a continuación, puede iniciar leer y asignar a miembros a la función de Active directory. **Nota**: una plantilla de rol de Active directory se expone para el rol de Active directory de los usuarios. La función de directorio de usuarios está implícita y no es visible para los clientes de Active directory. Todos los usuarios en el inquilino se asigna a este rol en la infraestructura. La función ya está activada. No use esta plantilla.'
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 2b4a4e79c11f38991da88cd685983229c9f7da7b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27938184"
---
# <a name="directoryroletemplate-resource-type"></a><span data-ttu-id="4659c-114">Tipo de recurso directoryRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="4659c-114">directoryRoleTemplate resource type</span></span>

> <span data-ttu-id="4659c-115">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4659c-115">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4659c-116">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4659c-116">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4659c-p103">Representa una plantilla de rol de directorio. Una plantilla de rol de directorio especifica los valores de propiedad de un rol de directorio ([directoryRole](directoryrole.md)). Existe un objeto de plantilla de rol de directorio asociado para cada uno de los roles de directorio que puedan activarse en un inquilino. Para leer un rol de directorio o actualizar sus miembros, debe activarse primero en el inquilino. Solo se activa de manera predeterminada el rol de directorio Administradores de la compañía. Para activar otros roles de directorio disponibles, envíe una solicitud POST al extremo `/directoryRoles` con el identificador de la plantilla de rol de directorio en que se basa el rol de directorio especificado en el parámetro **roleTemplateId** de la solicitud. Al completar esta solicitud, puede empezar a leer y asignar miembros al rol de directorio. **Nota**: Una plantilla de rol de directorio se expone para el rol de directorio Usuarios. El rol de directorio Usuarios es implícito y no lo pueden ver los clientes del directorio. La infraestructura asigna a todos los usuarios del inquilino a este rol. El rol ya está activado. No use esta plantilla.</span><span class="sxs-lookup"><span data-stu-id="4659c-p103">Represents a directory role template. A directory role template specifies the property values of a directory role ([directoryRole](directoryrole.md)). There is an associated directory role template object for each of the directory roles that may be activated in a tenant. To read a directory role or update its members, it must first be activated in the tenant. Only the Company Administrators directory role is activated by default. To activate other available directory roles you send a POST request to the `/directoryRoles` endpoint with the ID of the directory role template on which the directory role is based specified in the **roleTemplateId** parameter of the request. Upon successful completion of this request, you can then start to read and assign members to the directory role. **Note**: A directory role template is exposed for the Users directory role. The Users directory role is implicit and is not visible to directory clients. Every User in the tenant is assigned to this role by the infrastructure. The role is already activated. Do not use this template.</span></span>


## <a name="methods"></a><span data-ttu-id="4659c-129">Métodos</span><span class="sxs-lookup"><span data-stu-id="4659c-129">Methods</span></span>

| <span data-ttu-id="4659c-130">Método</span><span class="sxs-lookup"><span data-stu-id="4659c-130">Method</span></span>       | <span data-ttu-id="4659c-131">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4659c-131">Return Type</span></span>  |<span data-ttu-id="4659c-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="4659c-132">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="4659c-133">Obtener directoryRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="4659c-133">Get directoryRoleTemplate</span></span>](../api/directoryroletemplate-get.md) | [<span data-ttu-id="4659c-134">directoryRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="4659c-134">directoryRoleTemplate</span></span>](directoryroletemplate.md) |<span data-ttu-id="4659c-135">Lea las propiedades y las relaciones del objeto directoryRoleTemplate.</span><span class="sxs-lookup"><span data-stu-id="4659c-135">Read properties and relationships of directoryRoleTemplate object.</span></span>|

## <a name="properties"></a><span data-ttu-id="4659c-136">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4659c-136">Properties</span></span>
| <span data-ttu-id="4659c-137">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4659c-137">Property</span></span>     | <span data-ttu-id="4659c-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="4659c-138">Type</span></span>   |<span data-ttu-id="4659c-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="4659c-139">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4659c-140">description</span><span class="sxs-lookup"><span data-stu-id="4659c-140">description</span></span>|<span data-ttu-id="4659c-141">String</span><span class="sxs-lookup"><span data-stu-id="4659c-141">String</span></span>|<span data-ttu-id="4659c-p104">La descripción del rol de directorio que se establecerá. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4659c-p104">The description to set for the directory role. Read-only.</span></span>|
|<span data-ttu-id="4659c-144">displayName</span><span class="sxs-lookup"><span data-stu-id="4659c-144">displayName</span></span>|<span data-ttu-id="4659c-145">String</span><span class="sxs-lookup"><span data-stu-id="4659c-145">String</span></span>|<span data-ttu-id="4659c-p105">El nombre para mostrar del rol de directorio que se establecerá. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4659c-p105">The display name to set for the directory role. Read-only.</span></span> |
|<span data-ttu-id="4659c-148">id</span><span class="sxs-lookup"><span data-stu-id="4659c-148">id</span></span>|<span data-ttu-id="4659c-149">Cadena</span><span class="sxs-lookup"><span data-stu-id="4659c-149">String</span></span>|<span data-ttu-id="4659c-p106">El identificador único de la plantilla. Hereda de [directoryObject](directoryobject.md). Especifique el **id** de la plantilla de rol de directorio de la propiedad **roleTemplateId** en la solicitud POST para activar un [directoryRole](directoryrole.md) en un inquilino. Clave, no admite valores NULL. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4659c-p106">The unique identifier for the template. Inherited from [directoryObject](directoryobject.md). You specify the **id** of the directory role template for the **roleTemplateId** property in the POST request activate a [directoryRole](directoryrole.md) in a tenant. Key, Not nullable. Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="4659c-155">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4659c-155">Relationships</span></span>
<span data-ttu-id="4659c-156">Ninguno</span><span class="sxs-lookup"><span data-stu-id="4659c-156">None</span></span>



## <a name="json-representation"></a><span data-ttu-id="4659c-157">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4659c-157">JSON representation</span></span>

<span data-ttu-id="4659c-158">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="4659c-158">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.directoryRoleTemplate"
}-->

```json
{
  "description": "string",
  "displayName": "string",
  "id": "string (identifier)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryRoleTemplate resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
