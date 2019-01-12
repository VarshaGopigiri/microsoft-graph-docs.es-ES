---
title: Tipo de recurso directoryRoleTemplate
description: 'Representa una plantilla de rol de Active directory. Una plantilla de rol de Active directory especifica los valores de propiedad de un rol de Active directory (directoryRole). Hay un objeto de plantilla de rol asociados en el directorio para cada uno de los roles de Active directory que se pueden activar en un inquilino. Para leer un rol de Active directory o actualizar a sus miembros, debe activarse en primer lugar en el inquilino. Sólo el rol de Active directory de administradores de la compañía se activa de forma predeterminada. Para activar otros roles de Active directory disponibles enviar una solicitud POST para la `/directoryRoles` extremo con el identificador de la plantilla de rol de Active directory en el que se basa el rol de Active directory especificado en el parámetro **roleTemplateId** de la solicitud. Tras completar correctamente esta solicitud, a continuación, puede iniciar leer y asignar a miembros a la función de Active directory. **Nota**: una plantilla de rol de Active directory se expone para el rol de Active directory de los usuarios. La función de directorio de usuarios está implícita y no es visible para los clientes de Active directory. Todos los usuarios en el inquilino se asigna a este rol en la infraestructura. La función ya está activada. No use esta plantilla.'
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 57dec43699ba75c7e936fa02dbdf09df74dd06ed
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27966996"
---
# <a name="directoryroletemplate-resource-type"></a>Tipo de recurso directoryRoleTemplate

Representa una plantilla de rol de directorio. Una plantilla de rol de directorio especifica los valores de propiedad de un rol de directorio ([directoryRole](directoryrole.md)). Existe un objeto de plantilla de rol de directorio asociado para cada uno de los roles de directorio que puedan activarse en un inquilino. Para leer un rol de directorio o actualizar sus miembros, debe activarse primero en el inquilino. Solo se activa de manera predeterminada el rol de directorio Administradores de la compañía. Para activar otros roles de directorio disponibles, envíe una solicitud POST al extremo `/directoryRoles` con el identificador de la plantilla de rol de directorio en que se basa el rol de directorio especificado en el parámetro **roleTemplateId** de la solicitud. Al completar esta solicitud, puede empezar a leer y asignar miembros al rol de directorio. **Nota**: Una plantilla de rol de directorio se expone para el rol de directorio Usuarios. El rol de directorio Usuarios es implícito y no lo pueden ver los clientes del directorio. La infraestructura asigna a todos los usuarios del inquilino a este rol. El rol ya está activado. No use esta plantilla.


## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Obtener directoryRoleTemplate](../api/directoryroletemplate-get.md) | [directoryRoleTemplate](directoryroletemplate.md) |Lea las propiedades y las relaciones del objeto directoryRoleTemplate.|
|[List directoryRoleTemplate](../api/directoryroletemplate-list.md) | Colección [directoryRoleTemplate](directoryroletemplate.md) |Recupere una lista de objetos directoryRoleTemplate.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|description|String|La descripción del rol de directorio que se establecerá. Solo lectura.|
|displayName|String|El nombre para mostrar del rol de directorio que se establecerá. Solo lectura. |
|id|Cadena|El identificador único de la plantilla. Hereda de [directoryObject](directoryobject.md). Especifique el **id** de la plantilla de rol de directorio de la propiedad **roleTemplateId** en la solicitud POST para activar un [directoryRole](directoryrole.md) en un inquilino. Clave, no admite valores NULL. Solo lectura.|

## <a name="relationships"></a>Relaciones
Ninguno



## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

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
