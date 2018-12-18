---
title: Tipo de recurso termsAndConditionsAcceptanceStatus
description: C) de la directiva a un usuario determinado. Los usuarios deben aceptar la versión más actualizada de los términos para conservar el acceso al Portal de empresa.
author: tfitzmac
ms.openlocfilehash: 8e504796be7dbec303bab8691ed171abc80b9a45
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27314640"
---
# <a name="termsandconditionsacceptancestatus-resource-type"></a>Tipo de recurso termsAndConditionsAcceptanceStatus

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una entidad termsAndConditionsAcceptanceStatus representa el estado de aceptación de una directiva de Términos y condiciones (TyC) determinada por un usuario determinado. Los usuarios deben aceptar la versión más actualizada de los términos para conservar el acceso al Portal de empresa.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar termsAndConditionsAcceptanceStatuses](../api/intune-companyterms-termsandconditionsacceptancestatus-list.md)|Colección [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md)|Enumere las propiedades y las relaciones de los objetos [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md).|
|[Obtener termsAndConditionsAcceptanceStatus](../api/intune-companyterms-termsandconditionsacceptancestatus-get.md)|[termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md)|Lea las propiedades y las relaciones del objeto [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md).|
|[Crear termsAndConditionsAcceptanceStatus](../api/intune-companyterms-termsandconditionsacceptancestatus-create.md)|[termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md)|Cree un objeto [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md).|
|[Eliminar termsAndConditionsAcceptanceStatus](../api/intune-companyterms-termsandconditionsacceptancestatus-delete.md)|Ninguna|Elimina un [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md).|
|[Actualizar termsAndConditionsAcceptanceStatus](../api/intune-companyterms-termsandconditionsacceptancestatus-update.md)|[termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md)|Actualice las propiedades de un objeto [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador único de la entidad.|
|userDisplayName|String|Nombre para mostrar del usuario cuya aceptación representa la entidad.|
|acceptedVersion|Int32|Número de versión más reciente de los TyC aceptados por el usuario.|
|acceptedDateTime|DateTimeOffset|Fecha y hora en la que el usuario aceptó los términos por última vez.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|termsAndConditions|[termsAndConditions](../resources/intune-companyterms-termsandconditions.md)|Vínculo de navegación a los términos y condiciones asignados.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.termsAndConditionsAcceptanceStatus"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.termsAndConditionsAcceptanceStatus",
  "id": "String (identifier)",
  "userDisplayName": "String",
  "acceptedVersion": 1024,
  "acceptedDateTime": "String (timestamp)"
}
```





