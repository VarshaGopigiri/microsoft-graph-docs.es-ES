---
title: Tipo de recurso managedEBook
description: Una clase abstracta que contiene las propiedades base para el libro electrónico Managed.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a2da2254b5d86a16d3a0e60fae0c0ea4215d54a2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27917863"
---
# <a name="managedebook-resource-type"></a>Tipo de recurso managedEBook

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una clase abstracta que contiene las propiedades base para el libro electrónico Managed.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar managedEBooks](../api/intune-books-managedebook-list.md)|Colección [managedEBook](../resources/intune-books-managedebook.md)|Enumere las propiedades y las relaciones de los objetos [managedEBook](../resources/intune-books-managedebook.md).|
|[Obtener managedEBook](../api/intune-books-managedebook-get.md)|[managedEBook](../resources/intune-books-managedebook.md)|Lea las propiedades y las relaciones del objeto [managedEBook](../resources/intune-books-managedebook.md).|
|[Acción assign](../api/intune-books-managedebook-assign.md)|Ninguno|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|displayName|Cadena|Nombre del libro electrónico|
|descripción|Cadena|Descripción.|
|publicador|Cadena|Publicador.|
|publishedDateTime|DateTimeOffset|La fecha y la hora en que se publicó el libro electrónico.|
|largeCover|[mimeContent](../resources/intune-shared-mimecontent.md)|Cubierta de libro.|
|createdDateTime|DateTimeOffset|La fecha y la hora en que se creó el archivo del libro electrónico.|
|lastModifiedDateTime|DateTimeOffset|La fecha y la hora en que se modificó por última vez el libro electrónico.|
|informationUrl|Cadena|La dirección URL para obtener más información.|
|privacyInformationUrl|Cadena|La dirección URL de la declaración de privacidad.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|asignaciones|Colección [managedEBookAssignment](../resources/intune-books-managedebookassignment.md)|La lista de asignaciones para este libro electrónico.|
|installSummary|[eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md)|Resumen de instalación de las aplicaciones para móviles.|
|deviceStates|Colección [deviceInstallState](../resources/intune-books-deviceinstallstate.md)|La lista de estados de asignaciones para este libro electrónico.|
|userStateSummary|Colección [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md)|La lista de estados de asignaciones para este libro electrónico.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedEBook"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedEBook",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "publisher": "String",
  "publishedDateTime": "String (timestamp)",
  "largeCover": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "String",
    "value": "binary"
  },
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "informationUrl": "String",
  "privacyInformationUrl": "String"
}
```



