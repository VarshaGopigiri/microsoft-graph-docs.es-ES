---
title: Tipo de recurso deviceCategory
description: A continuación, estas categorías se pueden aplicar a un dispositivo en la consola de Azure de Intune o un usuario puede seleccionarlas durante la inscripción de dispositivos. Puede filtrar los informes y crear grupos de dispositivos de Azure Active Directory dinámicos según las categorías de dispositivos.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 80f8f1f36198ecfab1021e30cb2f28fa4377852c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27810839"
---
# <a name="devicecategory-resource-type"></a>Tipo de recurso deviceCategory

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Las categorías de dispositivo proporcionan una forma de organizar sus dispositivos. Al usar categorías de dispositivos, los administradores de la compañía pueden definir las categorías de forma pertinente para su empresa.A continuación, estas categorías se pueden aplicar a un dispositivo en la consola de Azure de Intune o un usuario puede seleccionarlas durante la inscripción de dispositivos. Puede filtrar los informes y crear grupos de dispositivos de Azure Active Directory dinámicos según las categorías de dispositivos.

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|Colección de [lista deviceCategories](../api/intune-shared-devicecategory-list.md)|Enumere las propiedades y las relaciones de los objetos [deviceCategory](../resources/intune-shared-devicecategory.md).|
|[Obtener deviceCategory](../api/intune-shared-devicecategory-get.md)|Lea las propiedades y las relaciones del objeto [deviceCategory](../resources/intune-shared-devicecategory.md).|
|[Crear deviceCategory](../api/intune-shared-devicecategory-create.md)|Cree un objeto [deviceCategory](../resources/intune-shared-devicecategory.md).|
|[Eliminar deviceCategory](../api/intune-shared-devicecategory-delete.md).|
|[Actualizar deviceCategory](../api/intune-shared-devicecategory-update.md)|Actualice las propiedades de un objeto [deviceCategory](../resources/intune-shared-devicecategory.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|El identificador único de la categoría de dispositivo. Solo lectura.|
|**Incorporación de redes**|
|displayName|Cadena|Nombre para mostrar de la categoría de dispositivo.|
|descripción|Cadena|Descripción opcional de la categoría de dispositivo.|

## <a name="relationships"></a>Relaciones
Ninguna

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.deviceCategory"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceCategory",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String"
}
```



