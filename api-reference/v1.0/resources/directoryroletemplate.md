---
title: Tipo de recurso directoryRoleTemplate
description: 'Representa una plantilla de rol de Active directory. Una plantilla de rol de Active directory especifica los valores de propiedad de un rol de Active directory (directoryRole). Hay un objeto de plantilla de rol asociados en el directorio para cada uno de los roles de Active directory que se pueden activar en un inquilino. Para leer un rol de Active directory o actualizar a sus miembros, debe activarse en primer lugar en el inquilino. Sólo el rol de Active directory de administradores de la compañía se activa de forma predeterminada. Para activar otros roles de Active directory disponibles enviar una solicitud POST para la `/directoryRoles` extremo con el identificador de la plantilla de rol de Active directory en el que se basa el rol de Active directory especificado en el parámetro **roleTemplateId** de la solicitud. Tras completar correctamente esta solicitud, a continuación, puede iniciar leer y asignar a miembros a la función de Active directory. **Nota**: una plantilla de rol de Active directory se expone para el rol de Active directory de los usuarios. La función de directorio de usuarios está implícita y no es visible para los clientes de Active directory. Todos los usuarios en el inquilino se asigna a este rol en la infraestructura. La función ya está activada. No use esta plantilla.'
ms.openlocfilehash: e654ab8c14a0c5e831b2cbf818047fea0e2d95c9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031668"
---
# <a name="directoryroletemplate-resource-type"></a><span data-ttu-id="45936-114">Tipo de recurso directoryRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="45936-114">directoryRoleTemplate resource type</span></span>

<span data-ttu-id="45936-p102">Representa una plantilla de rol de directorio. Una plantilla de rol de directorio especifica los valores de propiedad de un rol de directorio ([directoryRole](directoryrole.md)). Existe un objeto de plantilla de rol de directorio asociado para cada uno de los roles de directorio que puedan activarse en un inquilino. Para leer un rol de directorio o actualizar sus miembros, debe activarse primero en el inquilino. Solo se activa de manera predeterminada el rol de directorio Administradores de la compañía. Para activar otros roles de directorio disponibles, envíe una solicitud POST al extremo `/directoryRoles` con el identificador de la plantilla de rol de directorio en que se basa el rol de directorio especificado en el parámetro **roleTemplateId** de la solicitud. Al completar esta solicitud, puede empezar a leer y asignar miembros al rol de directorio. **Nota**: Una plantilla de rol de directorio se expone para el rol de directorio Usuarios. El rol de directorio Usuarios es implícito y no lo pueden ver los clientes del directorio. La infraestructura asigna a todos los usuarios del inquilino a este rol. El rol ya está activado. No use esta plantilla.</span><span class="sxs-lookup"><span data-stu-id="45936-p102">Represents a directory role template. A directory role template specifies the property values of a directory role ([directoryRole](directoryrole.md)). There is an associated directory role template object for each of the directory roles that may be activated in a tenant. To read a directory role or update its members, it must first be activated in the tenant. Only the Company Administrators directory role is activated by default. To activate other available directory roles you send a POST request to the `/directoryRoles` endpoint with the ID of the directory role template on which the directory role is based specified in the **roleTemplateId** parameter of the request. Upon successful completion of this request, you can then start to read and assign members to the directory role. **Note**: A directory role template is exposed for the Users directory role. The Users directory role is implicit and is not visible to directory clients. Every User in the tenant is assigned to this role by the infrastructure. The role is already activated. Do not use this template.</span></span>


## <a name="methods"></a><span data-ttu-id="45936-127">Métodos</span><span class="sxs-lookup"><span data-stu-id="45936-127">Methods</span></span>

| <span data-ttu-id="45936-128">Método</span><span class="sxs-lookup"><span data-stu-id="45936-128">Method</span></span>       | <span data-ttu-id="45936-129">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45936-129">Return Type</span></span>  |<span data-ttu-id="45936-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="45936-130">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="45936-131">Obtener directoryRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="45936-131">Get directoryRoleTemplate</span></span>](../api/directoryroletemplate-get.md) | [<span data-ttu-id="45936-132">directoryRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="45936-132">directoryRoleTemplate</span></span>](directoryroletemplate.md) |<span data-ttu-id="45936-133">Lea las propiedades y las relaciones del objeto directoryRoleTemplate.</span><span class="sxs-lookup"><span data-stu-id="45936-133">Read properties and relationships of directoryRoleTemplate object.</span></span>|
|[<span data-ttu-id="45936-134">List directoryRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="45936-134">List directoryRoleTemplate</span></span>](../api/directoryroletemplate-list.md) | <span data-ttu-id="45936-135">Colección [directoryRoleTemplate](directoryroletemplate.md)</span><span class="sxs-lookup"><span data-stu-id="45936-135">[directoryRoleTemplate](directoryroletemplate.md) collection</span></span> |<span data-ttu-id="45936-136">Recupere una lista de objetos directoryRoleTemplate.</span><span class="sxs-lookup"><span data-stu-id="45936-136">Retrieve a list of directoryRoleTemplate objects.</span></span>|

## <a name="properties"></a><span data-ttu-id="45936-137">Propiedades</span><span class="sxs-lookup"><span data-stu-id="45936-137">Properties</span></span>
| <span data-ttu-id="45936-138">Propiedad</span><span class="sxs-lookup"><span data-stu-id="45936-138">Property</span></span>     | <span data-ttu-id="45936-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="45936-139">Type</span></span>   |<span data-ttu-id="45936-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="45936-140">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="45936-141">description</span><span class="sxs-lookup"><span data-stu-id="45936-141">description</span></span>|<span data-ttu-id="45936-142">String</span><span class="sxs-lookup"><span data-stu-id="45936-142">String</span></span>|<span data-ttu-id="45936-p103">La descripción del rol de directorio que se establecerá. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="45936-p103">The description to set for the directory role. Read-only.</span></span>|
|<span data-ttu-id="45936-145">displayName</span><span class="sxs-lookup"><span data-stu-id="45936-145">displayName</span></span>|<span data-ttu-id="45936-146">String</span><span class="sxs-lookup"><span data-stu-id="45936-146">String</span></span>|<span data-ttu-id="45936-p104">El nombre para mostrar del rol de directorio que se establecerá. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="45936-p104">The display name to set for the directory role. Read-only.</span></span> |
|<span data-ttu-id="45936-149">id</span><span class="sxs-lookup"><span data-stu-id="45936-149">id</span></span>|<span data-ttu-id="45936-150">String</span><span class="sxs-lookup"><span data-stu-id="45936-150">String</span></span>|<span data-ttu-id="45936-p105">El identificador único de la plantilla. Hereda de [directoryObject](directoryobject.md). Especifique el **id** de la plantilla de rol de directorio de la propiedad **roleTemplateId** en la solicitud POST para activar un [directoryRole](directoryrole.md) en un inquilino. Clave, no admite valores NULL. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="45936-p105">The unique identifier for the template. Inherited from [directoryObject](directoryobject.md). You specify the **id** of the directory role template for the **roleTemplateId** property in the POST request activate a [directoryRole](directoryrole.md) in a tenant. Key, Not nullable. Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="45936-156">Relaciones</span><span class="sxs-lookup"><span data-stu-id="45936-156">Relationships</span></span>
<span data-ttu-id="45936-157">Ninguno</span><span class="sxs-lookup"><span data-stu-id="45936-157">None</span></span>



## <a name="json-representation"></a><span data-ttu-id="45936-158">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="45936-158">JSON representation</span></span>

<span data-ttu-id="45936-159">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="45936-159">Here is a JSON representation of the resource</span></span>

<!--{
  "blockType": "resource",
  "openType": true,
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.directoryObject",
  "@odata.type": "microsoft.graph.directoryRoleTemplate",
  "@odata.annotations": [
    {
      "capabilities": {
        "toppable": false
      }
    }
  ]
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
