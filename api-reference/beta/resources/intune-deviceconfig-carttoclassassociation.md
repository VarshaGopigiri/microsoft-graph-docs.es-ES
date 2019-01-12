---
title: tipo de recurso cartToClassAssociation
description: CartToClassAssociation para asociar carros de dispositivo con aulas.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 38d9b940dd3e7a5450854f29ba69b2eac69e2a45
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27943938"
---
# <a name="carttoclassassociation-resource-type"></a>tipo de recurso cartToClassAssociation

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

CartToClassAssociation para asociar carros de dispositivo con aulas.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista cartToClassAssociations](../api/intune-deviceconfig-carttoclassassociation-list.md)|colección de [cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md)|Propiedades de la lista y relaciones de los objetos [cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md) .|
|[Obtener cartToClassAssociation](../api/intune-deviceconfig-carttoclassassociation-get.md)|[cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md)|Leer las propiedades y las relaciones del objeto [cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md) .|
|[Crear cartToClassAssociation](../api/intune-deviceconfig-carttoclassassociation-create.md)|[cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md)|Crear un nuevo objeto [cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md) .|
|[Eliminar cartToClassAssociation](../api/intune-deviceconfig-carttoclassassociation-delete.md)|Ninguno|Elimina un [cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md).|
|[Actualizar cartToClassAssociation](../api/intune-deviceconfig-carttoclassassociation-update.md)|[cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md)|Actualizar las propiedades de un objeto [cartToClassAssociation](../resources/intune-deviceconfig-carttoclassassociation.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto.|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez.|
|version|Int32|Versión de la CartToClassAssociation.|
|displayName|Cadena|Nombre proporcionado por el administrador de la configuración del dispositivo.|
|descripción|Cadena|Descripción de la CartToClassAssociation proporcionada por el administrador.|
|deviceCartIds|Colección String|Identificadores de carros de dispositivo que se asociará con clases.|
|classroomIds|Colección String|Identificadores de aulas que se asociará con carros de dispositivo.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.cartToClassAssociation"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.cartToClassAssociation",
  "id": "String (identifier)",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "version": 1024,
  "displayName": "String",
  "description": "String",
  "deviceCartIds": [
    "String"
  ],
  "classroomIds": [
    "String"
  ]
}
```





