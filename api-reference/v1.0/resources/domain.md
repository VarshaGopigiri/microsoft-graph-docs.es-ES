---
title: Tipo de recurso de dominio
description: Representa un dominio asociado al inquilino.
author: lleonard-msft
localization_priority: Normal
ms.openlocfilehash: c7bf09d86be2b8ec95b8b2f11e74b44c69bc33cb
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27851810"
---
# <a name="domain-resource-type"></a>Tipo de recurso de dominio

Representa un dominio asociado al inquilino.

Use operaciones de dominio para asociar dominios a un arrendatario, verifique la propiedad del dominio y configure los servicios compatibles.  Las operaciones de dominio permiten a los registradores automatizar la asociación de dominio para servicios como Office 365. Por ejemplo, como parte de la suscripción de dominio, un registrador puede habilitar un dominio de cortesía para correo electrónico, sitios web, autenticación, etc.

Para asociar un dominio a un espacio empresarial:

1. [Asociar](../api/domain-post-domains.md) un dominio a un inquilino.

2. [Recupere](../api/domain-list-verificationdnsrecords.md) los registros de comprobación de dominio. Agregue los detalles de registro de comprobación para el archivo de zona del dominio mediante el registrador de dominio o la configuración del servidor DNS.

3. [Validar](../api/domain-verify.md) la propiedad del dominio. Se validará el dominio y se establecerá la propiedad *isVerified* en *verdadera*.

4. [Indique](../api/domain-update.md) los servicios admitidos que planea usar con el dominio.

5. [Configure](../api/domain-list-serviceconfigurationrecords.md) los servicios admitidos al recuperar una lista de registros necesarios para habilitar los servicios para el dominio. Agregar los detalles de registro de configuración para el archivo de zona del dominio mediante el registrador de dominio o la configuración del servidor DNS.

## <a name="methods"></a>Métodos

| Método   | Tipo de valor devuelto |Descripción|
|:---------------|:--------|:----------|
|[Obtener dominio](../api/domain-get.md) | [dominio](domain.md) | Lea las propiedades y relaciones de un objeto de dominio.|
|[Crear un dominio](../api/domain-post-domains.md) | [dominio](domain.md) | Agregue un dominio al inquilino. |
|[Enumerar domainNameReference](../api/domain-list-domainnamereferences.md) |Colección [directoryObject](directoryobject.md)| Recuperar una lista de objetos de directorio con una referencia al dominio.|
|[Enumerar serviceConfigurationRecords](../api/domain-list-serviceconfigurationrecords.md) |Colección [domainDnsRecord](domaindnsrecord.md)|  Recuperar una lista de registros DNS del dominio para la configuración del dominio.|
|[Enumerar verificationDnsRecords](../api/domain-list-verificationdnsrecords.md) |Colección [domainDnsRecord](domaindnsrecord.md)|  Recuperar una lista de registros DNS del dominio para la comprobación del dominio.|
|[Actualizar dominio](../api/domain-update.md) | [dominio](domain.md) |Actualizar un dominio.|
|[Eliminar dominio](../api/domain-delete.md) | Ninguno |Eliminar un dominio.|
|[Dominio ForceDelete](../api/domain-forcedelete.md)|Ninguno|Elimina un dominio mediante una operación asincrónica.|
|[Comprobar dominio](../api/domain-verify.md)|[dominio](domain.md)|Valide la propiedad del dominio.|

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo | Descripción |
|:---------------|:--------|:----------|
|authenticationType|Cadena| Indica el tipo de autenticación configurado para el dominio. El valor es *Managed* (administrado) o *Federated* (federado).<br> *Managed* indica un dominio administrado en la nube donde Azure AD realiza la autenticación del usuario.<br>*Federated* indica que la autenticación está asociada a un proveedor de identidad como la instancia local de Active Directory del inquilino a través de los Servicios de federación de Active Directory. No admite valores NULL |
|availabilityStatus|String| Esta propiedad es siempre NULL, excepto cuando se usa la acción de [comprobación](../api/domain-verify.md). Cuando se usa la acción de [comprobación](../api/domain-verify.md), se devuelve una entidad de **dominio** en la respuesta. La propiedad **availabilityStatus** de la entidad de **dominio** en la respuesta es *AvailableImmediately* o *EmailVerifiedDomainTakeoverScheduled*.|
|id|Cadena| Especifica el nombre completo del dominio. Clave, inmutable, no acepta valores NULL, único |
|isAdminManaged|Boolean| El valor de la propiedad es falso si la administración de registros DNS del dominio se ha delegado a Office 365. En caso contrario, el valor es verdadero. No admite valores NULL |
|isDefault|Boolean| Es verdadero si este es el dominio predeterminado que se utiliza para la creación de usuarios. Solo hay un dominio predeterminado por empresa. No admite valores NULL |
|isInitial|Boolean| Es verdadero si se trata del dominio inicial creado por Microsoft Online Services (companyname.onmicrosoft.com). Solo hay un dominio inicial por empresa. No admite valores NULL |
|isRoot|Boolean| Es verdadero si el dominio es un dominio raíz comprobado. En caso contrario, es falso si el dominio es un subdominio o no está comprobado. No admite valores NULL |
|isVerified|Boolean| Es verdadero si el dominio ha completado la comprobación de propiedad de dominio. No admite valores NULL |
|supportedServices|Colección de cadenas| Funciones asignadas al dominio.<br><br>Puede incluir 0, 1 o más de los siguientes valores: *Email*, *Sharepoint*, *EmailInternalRelayOnly*, *OfficeCommunicationsOnline*, *SharePointDefaultDomain*, *FullRedelegation*, *SharePointPublic*, *OrgIdAuthentication*, *Yammer*, *Intune*<br><br> Los valores que puede agregar o quitar mediante la API de Graph incluyen: *Email*, *OfficeCommunicationsOnline*, *Yammer*<br>No admite valores NULL|
|state|[domainState](domainstate.md)| Estado de las operaciones asincrónicas programadas para el dominio. |

## <a name="relationships"></a>Relaciones

Las relaciones entre un dominio y otros objetos en el directorio, como sus registros de comprobación y registros de configuración de servicio, se exponen a través de las propiedades de navegación. Para leer estas relaciones, puede abordar las propiedades de navegación en las solicitudes.

| Relación | Tipo |Descripción|
|:---------------|:--------|:----------|
|domainNameReferences|Colección [directoryObject](directoryobject.md)| Solo lectura, admite valores NULL|
|serviceConfigurationRecords|Colección [domainDnsRecord](domaindnsrecord.md)| Registros DNS que el cliente agrega al archivo de zona de DNS del dominio antes de que Microsoft Online Services pueda usar el dominio.<br>Solo lectura, admite valores NULL |
|verificationDnsRecords|Colección [domainDnsRecord](domaindnsrecord.md)| Registros DNS que el cliente agrega al archivo de zona de DNS del dominio antes de que el cliente pueda completar la comprobación de propiedad de dominio con Azure AD.<br>Solo lectura, admite valores NULL|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.domain"
}-->

```json
{
  "authenticationType": "String",
  "availabilityStatus": "String",
  "id": "String (identifier)",
  "isAdminManaged": true,
  "isDefault": true,
  "isInitial": true,
  "isRoot": true,
  "isVerified": true,
  "state": {"@odata.type": "microsoft.graph.domainState"},
  "supportedServices": ["String"]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "domain resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
