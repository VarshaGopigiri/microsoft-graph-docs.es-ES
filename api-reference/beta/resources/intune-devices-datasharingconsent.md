---
title: tipo de recurso dataSharingConsent
description: Uso compartido de datos consienten de información.
ms.openlocfilehash: 152b367161dc9a734a20e007ac1b2c0d02d0c99f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090922"
---
# <a name="datasharingconsent-resource-type"></a>tipo de recurso dataSharingConsent

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Uso compartido de datos consienten de información.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista dataSharingConsents](../api/intune-devices-datasharingconsent-list.md)|colección de [dataSharingConsent](../resources/intune-devices-datasharingconsent.md)|Propiedades de la lista y relaciones de los objetos [dataSharingConsent](../resources/intune-devices-datasharingconsent.md) .|
|[Obtener dataSharingConsent](../api/intune-devices-datasharingconsent-get.md)|[dataSharingConsent](../resources/intune-devices-datasharingconsent.md)|Leer las propiedades y las relaciones del objeto [dataSharingConsent](../resources/intune-devices-datasharingconsent.md) .|
|[Crear dataSharingConsent](../api/intune-devices-datasharingconsent-create.md)|[dataSharingConsent](../resources/intune-devices-datasharingconsent.md)|Crear un nuevo objeto [dataSharingConsent](../resources/intune-devices-datasharingconsent.md) .|
|[Eliminar dataSharingConsent](../api/intune-devices-datasharingconsent-delete.md)|Ninguno|Elimina un [dataSharingConsent](../resources/intune-devices-datasharingconsent.md).|
|[Actualizar dataSharingConsent](../api/intune-devices-datasharingconsent-update.md)|[dataSharingConsent](../resources/intune-devices-datasharingconsent.md)|Actualizar las propiedades de un objeto [dataSharingConsent](../resources/intune-devices-datasharingconsent.md) .|
|[acción consentToDataSharing](../api/intune-devices-datasharingconsent-consenttodatasharing.md)|[dataSharingConsent](../resources/intune-devices-datasharingconsent.md)|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|El consentimiento de uso compartido de datos Id.|
|nombreDescriptivoDeServicio|String|El nombre para mostrar del flujo de trabajo del servicio|
|termsUrl|String|El TermsUrl para los datos de uso compartido de consentimiento|
|concedido|Booleano|El estado de concedidos para los datos de uso compartido de consentimiento|
|grantDateTime|DateTimeOffset|Esta cuenta se le conceden el consentimiento de tiempo|
|grantedByUpn|String|El Upn del usuario que concederse el consentimiento para esta cuenta|
|grantedByUserId|String|El identificador de usuario del usuario que concederse el consentimiento para esta cuenta|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.dataSharingConsent"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.dataSharingConsent",
  "id": "String (identifier)",
  "serviceDisplayName": "String",
  "termsUrl": "String",
  "granted": true,
  "grantDateTime": "String (timestamp)",
  "grantedByUpn": "String",
  "grantedByUserId": "String"
}
```





