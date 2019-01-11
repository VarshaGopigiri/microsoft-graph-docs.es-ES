---
title: tipo de recurso managedEBookCategory
description: Contiene las propiedades para una única categoría de libro electrónico Intune.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: b415554d47c33f06a917c10327dad983db762578
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27894190"
---
# <a name="managedebookcategory-resource-type"></a>tipo de recurso managedEBookCategory

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades para una única categoría de libro electrónico Intune.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista managedEBookCategories](../api/intune-books-managedebookcategory-list.md)|colección de [managedEBookCategory](../resources/intune-books-managedebookcategory.md)|Propiedades de la lista y relaciones de los objetos [managedEBookCategory](../resources/intune-books-managedebookcategory.md) .|
|[Obtener managedEBookCategory](../api/intune-books-managedebookcategory-get.md)|[managedEBookCategory](../resources/intune-books-managedebookcategory.md)|Leer las propiedades y las relaciones del objeto [managedEBookCategory](../resources/intune-books-managedebookcategory.md) .|
|[Crear managedEBookCategory](../api/intune-books-managedebookcategory-create.md)|[managedEBookCategory](../resources/intune-books-managedebookcategory.md)|Crear un nuevo objeto [managedEBookCategory](../resources/intune-books-managedebookcategory.md) .|
|[Eliminar managedEBookCategory](../api/intune-books-managedebookcategory-delete.md)|Ninguno|Elimina un [managedEBookCategory](../resources/intune-books-managedebookcategory.md).|
|[Actualizar managedEBookCategory](../api/intune-books-managedebookcategory-update.md)|[managedEBookCategory](../resources/intune-books-managedebookcategory.md)|Actualizar las propiedades de un objeto [managedEBookCategory](../resources/intune-books-managedebookcategory.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|La clave de la entidad.|
|displayName|Cadena|El nombre de la categoría del libro electrónico.|
|lastModifiedDateTime|DateTimeOffset|La fecha y hora que se modificó por última vez el ManagedEBookCategory.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedEBookCategory"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedEBookCategory",
  "id": "String (identifier)",
  "displayName": "String",
  "lastModifiedDateTime": "String (timestamp)"
}
```





