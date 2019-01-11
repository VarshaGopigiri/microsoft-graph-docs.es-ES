---
title: tipo de recurso sideLoadingKey
description: Entidad de SideLoadingKey es necesario para Windows 8 y 8.1 dispositivos a instalar línea de las aplicaciones empresariales para un inquilino.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: b08715ebc8cd19ab4086fd82013301ed89efd183
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27814255"
---
# <a name="sideloadingkey-resource-type"></a>tipo de recurso sideLoadingKey

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Entidad de SideLoadingKey es necesario para Windows 8 y 8.1 dispositivos a instalar línea de las aplicaciones empresariales para un inquilino.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista sideLoadingKeies](../api/intune-onboarding-sideloadingkey-list.md)|colección de [sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md)|Propiedades de la lista y relaciones de los objetos [sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md) .|
|[Obtener sideLoadingKey](../api/intune-onboarding-sideloadingkey-get.md)|[sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md)|Leer las propiedades y las relaciones del objeto [sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md) .|
|[Crear sideLoadingKey](../api/intune-onboarding-sideloadingkey-create.md)|[sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md)|Crear un nuevo objeto [sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md) .|
|[Eliminar sideLoadingKey](../api/intune-onboarding-sideloadingkey-delete.md)|Ninguno|Elimina un [sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md).|
|[Actualizar sideLoadingKey](../api/intune-onboarding-sideloadingkey-update.md)|[sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md)|Actualizar las propiedades de un objeto [sideLoadingKey](../resources/intune-onboarding-sideloadingkey.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Lado cargar clave identificador único.|
|valor|String|Valor de clave de carga del lado, es valor de 5 x 5, separados por hiphens.|
|displayName|Cadena|Lado carga de clave de nombre que se muestra a la ITPro Admins.|
|descripción|Cadena|Clave de carga de descripción en el que se muestra a la ITPro Admins..|
|totalActivation|Int32|Lado carga Total activación de la clave que se muestra a la ITPro Admins.|
|lastUpdatedDateTime|Cadena|Lado cargar clave última actualizado fecha que se muestra a la ITPro Admins.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.sideLoadingKey"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.sideLoadingKey",
  "id": "String (identifier)",
  "value": "String",
  "displayName": "String",
  "description": "String",
  "totalActivation": 1024,
  "lastUpdatedDateTime": "String"
}
```





