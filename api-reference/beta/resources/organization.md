---
title: Tipo de recurso organization
description: 'Representa a un inquilino de Azure Active Directory. '
ms.openlocfilehash: 2e9a9a32411164e270e2eb3a8830fa811ba5f9cb
ms.sourcegitcommit: 6b1ba9b3be038cd6247de54a255bad560034fe42
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2019
ms.locfileid: "27771831"
---
# <a name="organization-resource-type"></a>Tipo de recurso organization

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa al inquilino de Azure Active Directory que el usuario o la aplicación ha iniciado sesión en. Sólo las operaciones de lectura y la actualización son compatibles con este recurso; crear y eliminar no son compatibles. Se hereda de [directoryObject](directoryobject.md).

Este recurso le permite agregar sus propios datos a las propiedades personalizadas mediante [extensiones](/graph/extensibility-overview).

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Obtener organización](../api/organization-get.md) | [organization](organization.md) |Lea las propiedades y las relaciones del objeto organization.|
|[Actualizar](../api/organization-update.md) | [organization](organization.md)  |Actualizar el objeto organization. Las únicas propiedades que pueden actualizarse son: **marketingNotificationMails**, **technicalNotificationMails**, **securityComplianceNotificationMails**, **securityComplianceNotificationPhones** y **privacyProfile**. |
|**Extensiones abiertas**| | |
|[Crear extensión abierta](../api/opentypeextension-post-opentypeextension.md) |[openTypeExtension](opentypeextension.md)| Crea una extensión abierta y agrega propiedades personalizadas en una instancia nueva o un recurso existente.|
|[Obtener extensión abierta](../api/opentypeextension-get.md) |Colección [openTypeExtension](opentypeextension.md)| Obtiene una extensión abierta identificada por el nombre de extensión.|
|**Extensiones de esquema**| | |
|[Agregar valores de extensión de esquema](/graph/extensibility-schema-groups) || Cree una definición de extensión de esquema y, después, úsela para agregar datos escritos personalizados a un recurso.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|assignedPlans|Colección [assignedPlan](assignedplan.md)|La colección de planes de servicio asociados con el inquilino. No admite valores NULL.            |
| businessPhones                      | Colección String                                         | Número de teléfono de la organización. **Nota:** Aunque se trata de una colección de cadenas, solo se puede establecer un número para esta propiedad.                                                                                            |
|ciudad|String| Nombre de la ciudad de la dirección de la organización. |
|companyLastDirSyncTime|DateTimeOffset|La fecha y hora en que se ha sincronizado por última vez el inquilino con el directorio local. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|country|String| Nombre del país o región de la dirección de la organización. |
|countryLetterCode|String| Abreviatura del país o región de la organización. |
|createdDateTime|DateTimeOffset| Marca de hora de cuándo se creó la organización. El valor no puede modificarse y se rellena automáticamente cuando se crea la organización. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura. |
| deletedDateTime                    | DateTimeOffset                                                    | Representa la fecha y hora de cuando se ha eliminado el inquilino de Azure AD con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.                                                                                     |
|dirSyncEnabled|Boolean|**true** si este objeto está sincronizado desde un directorio local; **false** si este objeto se ha sincronizado originalmente desde un directorio local, pero ya no está sincronizado; **null** si este objeto no se ha sincronizado nunca desde un directorio local (valor predeterminado).|
|displayName|String|El nombre para mostrar del inquilino.|
|id|String|El identificador de inquilino, un identificador único que representa la organización (o inquilino). Heredado de [directoryObject](directoryobject.md). Clave. No admite valores NULL. Solo lectura.|
|isMultipleDataLocationsForServicesEnabled|Booleano|**true** si la organización está habilitado; Multi-Geo **false** si la organización no está habilitado para Multi-ubican; **null** (valor predeterminado). Solo lectura. Para obtener más información, vea [OneDrive en línea Multi-ubican](https://docs.microsoft.com/sharepoint/dev/solution-guidance/multigeo-introduction).|
|marketingNotificationEmails|Colección String| No admite valores NULL.            |
|objectType|String|Una cadena que identifica el tipo de objeto. Para los inquilinos, el valor es siempre "Company". |
|postalCode|String| Código postal de la dirección de la organización. |
|preferredLanguage|String| El idioma preferido de la organización. Debe seguir el código ISO 639-1; por ejemplo, "es". |
|privacyProfile|[privacyProfile](privacyprofile.md)| Perfil de privacidad de una organización.            |
|provisionedPlans|Colección [ProvisionedPlan](provisionedplan.md)| No admite valores NULL.            |
|provisioningErrors|Colección ProvisioningError| No admite valores NULL.            |
|securityComplianceNotificationMails|Colección String||
|securityComplianceNotificationPhones|Colección String||
|state|String| Nombre del estado de la dirección de la organización. |
|street|String| Nombre de la calle de la dirección de la organización. |
|technicalNotificationMails|Colección String| No admite valores NULL. |
|verifiedDomains|Colección [VerifiedDomain](verifieddomain.md)|La colección de dominios asociados a este inquilino. No admite valores NULL.            |

## <a name="relationships"></a>Relaciones

| Relación     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|extensions|Colección de [extensiones](extension.md)|La colección de extensiones de open definidas para el recurso de la organización. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "extensions"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.organization"
}-->

```json
{
  "assignedPlans": [{"@odata.type": "microsoft.graph.assignedPlan"}],
  "businessPhones": ["string"],
  "city": "string",
  "country": "string",
  "countryLetterCode": "string",
  "createdDateTime": "String (timestamp)",
  "deletedDateTime": "String (timestamp)",
  "displayName": "string",
  "id": "string (identifier)",
  "isMultipleDataLocationsForServicesEnabled": "boolean",
  "marketingNotificationEmails": ["string"],
  "objectType": "string",
  "onPremisesLastSyncDateTime": "String (timestamp)",
  "onPremisesSyncEnabled": true,
  "postalCode": "string",
  "preferredLanguage": "string",
  "privacyProfile": {"@odata.type": "microsoft.graph.privacyProfile"},
  "provisionedPlans": [{"@odata.type": "microsoft.graph.provisionedPlan"}],
  "securityComplianceNotificationMails": ["string"],
  "securityComplianceNotificationPhones": ["string"],
  "state": "string",
  "street": "string",
  "technicalNotificationMails": ["string"],
  "verifiedDomains": [{"@odata.type": "microsoft.graph.verifiedDomain"}]
}
```

## <a name="see-also"></a>Vea también

- [Agregar datos personalizados a los recursos mediante extensiones](/graph/extensibility-overview)
- [Agregar datos personalizados a los usuarios mediante extensiones abiertas](/graph/extensibility-open-users)
- [Agregar datos personalizados a los grupos mediante extensiones de esquema](/graph/extensibility-schema-groups)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "organization resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
