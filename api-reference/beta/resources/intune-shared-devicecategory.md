---
title: Tipo de recurso deviceCategory
description: A continuación, estas categorías se pueden aplicar a un dispositivo en la consola de Azure de Intune o un usuario puede seleccionarlas durante la inscripción de dispositivos. Puede filtrar los informes y crear grupos de dispositivos de Azure Active Directory dinámicos según las categorías de dispositivos.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: b61927b5d4c6e8c85ba454d241a0d61a20185579
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888826"
---
# <a name="devicecategory-resource-type"></a>Tipo de recurso deviceCategory

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Categorías de dispositivos proporcionan una forma de organizar los dispositivos. Uso de categorías de dispositivos, administradores de la compañía pueden definir categorías exclusivas que tiene sentido para su empresa.A continuación, estas categorías se pueden aplicar a un dispositivo en la consola de Azure de Intune o un usuario puede seleccionarlas durante la inscripción de dispositivos. Puede filtrar los informes y crear grupos de dispositivos de Azure Active Directory dinámicos según las categorías de dispositivos.

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceCategories](../api/intune-shared-devicecategory-list.md)|Colección [deviceCategory](../resources/intune-shared-devicecategory.md)|Enumere las propiedades y las relaciones de los objetos [deviceCategory](../resources/intune-shared-devicecategory.md).|
|[Obtener deviceCategory](../api/intune-shared-devicecategory-get.md)|[deviceCategory](../resources/intune-shared-devicecategory.md)|Lea las propiedades y las relaciones del objeto [deviceCategory](../resources/intune-shared-devicecategory.md).|
|[Crear deviceCategory](../api/intune-shared-devicecategory-create.md)|[deviceCategory](../resources/intune-shared-devicecategory.md)|Cree un objeto [deviceCategory](../resources/intune-shared-devicecategory.md).|
|[Eliminar deviceCategory](../api/intune-shared-devicecategory-delete.md)|Ninguna|Elimina un [deviceCategory](../resources/intune-shared-devicecategory.md).|
|[Actualizar deviceCategory](../api/intune-shared-devicecategory-update.md)|[deviceCategory](../resources/intune-shared-devicecategory.md)|Actualice las propiedades de un objeto [deviceCategory](../resources/intune-shared-devicecategory.md).|

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
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceCategory"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceCategory",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String"
}
```



