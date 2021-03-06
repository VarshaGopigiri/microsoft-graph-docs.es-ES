---
title: Tipo de recurso termsAndConditions
description: Contenido de las directivas de C se presenta a los usuarios tras su primer intento de inscribirse en Intune y posteriormente en ediciones donde un administrador necesario re aceptación. Permite que los administradores comuniquen las disposiciones que debe aceptar un usuario para tener los dispositivos inscritos en Intune.
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: aab2ca99726c6e5388dfa5641b19d7c40dd920de
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27965680"
---
# <a name="termsandconditions-resource-type"></a>Tipo de recurso termsAndConditions

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una entidad termsAndConditions representa los contenidos y metadatos de una directiva de Términos y condiciones (TyC) determinada para un grupo específico. El contenido de las directivas de TyC se presenta a los usuarios cuando intentan inscribirse en Intune por primera vez y, después, en las ediciones en que el administrador de un campo exige que se vuelvan a aceptar. Permite que los administradores comuniquen las disposiciones que debe aceptar un usuario para tener los dispositivos inscritos en Intune.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar termsAndConditionses](../api/intune-companyterms-termsandconditions-list.md)|Colección [termsAndConditions](../resources/intune-companyterms-termsandconditions.md)|Enumere las propiedades y las relaciones de los objetos [termsAndConditions](../resources/intune-companyterms-termsandconditions.md).|
|[Obtener termsAndConditions](../api/intune-companyterms-termsandconditions-get.md)|[termsAndConditions](../resources/intune-companyterms-termsandconditions.md)|Lea las propiedades y las relaciones del objeto [termsAndConditions](../resources/intune-companyterms-termsandconditions.md).|
|[Crear termsAndConditions](../api/intune-companyterms-termsandconditions-create.md)|[termsAndConditions](../resources/intune-companyterms-termsandconditions.md)|Cree un objeto [termsAndConditions](../resources/intune-companyterms-termsandconditions.md).|
|[Eliminar termsAndConditions](../api/intune-companyterms-termsandconditions-delete.md)|Ninguno|Elimina un [termsAndConditions](../resources/intune-companyterms-termsandconditions.md).|
|[Actualizar termsAndConditions](../api/intune-companyterms-termsandconditions-update.md)|[termsAndConditions](../resources/intune-companyterms-termsandconditions.md)|Actualice las propiedades de un objeto [termsAndConditions](../resources/intune-companyterms-termsandconditions.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Identificador único de la directiva de TyC.|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto.|
|modifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez.|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez.|
|displayName|Cadena|Nombre proporcionado por el administrador de la directiva de TyC. |
|description|Cadena|Descripción de la directiva de TyC proporcionada por el administrador.|
|title|Cadena|Título de los términos y condiciones proporcionado por el administrador. Se muestra a los usuarios cuando se les solicita que acepten la directiva de TyC.|
|bodyText|Cadena|Texto de cuerpo de los términos y condiciones proporcionado por el administrador, normalmente los propios términos. Se muestra a los usuarios cuando se les solicita que acepten la directiva de TyC.|
|acceptanceStatement|Cadena|Explicación de los términos y condiciones proporcionada por el administrador, normalmente describe lo que implica aceptar los términos y condiciones de la directiva de TyC. Se muestra a los usuarios cuando se les solicita que acepten la directiva de TyC.|
|version|Int32|Entero que indica la versión actual de los términos. Aumenta cuando un administrador realiza un cambio en los términos y quiere que los usuarios tengan que volver a aceptar la directiva de TyC modificada.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|groupAssignments|colección de [termsAndConditionsGroupAssignment](../resources/intune-companyterms-termsandconditionsgroupassignment.md)|La lista de las asignaciones de grupo para esta directiva T & C.|
|asignaciones|Colección [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md)|La lista de asignaciones para esta directiva de TyC.|
|acceptanceStatuses|Colección [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md)|La lista de estados de aceptación para esta directiva de TyC.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.termsAndConditions"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.termsAndConditions",
  "id": "String (identifier)",
  "createdDateTime": "String (timestamp)",
  "modifiedDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "String",
  "description": "String",
  "title": "String",
  "bodyText": "String",
  "acceptanceStatement": "String",
  "version": 1024
}
```





