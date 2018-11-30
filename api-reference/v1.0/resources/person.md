---
title: Tipo de recurso person
description: Una agregación de información sobre un contacto de correo electrónico, contactos y redes sociales. Los contactos pueden ser contactos locales, contactos de las redes sociales o el directorio de la organización y contactos de comunicaciones recientes (como de correo electrónico y Skype).
ms.openlocfilehash: 098e1bd67e151b8c08607ad358935ba45065c8d2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029639"
---
# <a name="person-resource-type"></a>Tipo de recurso person

Una agregación de información sobre un contacto de correo electrónico, contactos y redes sociales. Los contactos pueden ser contactos locales, contactos de las redes sociales o el directorio de la organización y contactos de comunicaciones recientes (como de correo electrónico y Skype).

## <a name="methods"></a>Métodos

| Método | Tipo de valor devuelto | Descripción |
|:---------------|:--------|:----------|
|[List people](../api/user-list-people.md) | **person** |Obtenga una colección de objetos person ordenados por su relevancia para el [user](../resources/user.md).|

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:---------------|:--------|:----------|
|birthday|String|Cumpleaños del contacto.|
|companyName|String|Nombre de la compañía del contacto.|
|department|String|Departamento del contacto.|
|displayName|String|Nombre para mostrar del contacto.|
|scoredEmailAddresses|Colección [scoredEmailAddress](scoredemailaddress.md)|Direcciones de correo electrónico del contacto.|
|givenName|String|Nombre propio del contacto.|
|id|String|Identificador único del contacto. Solo lectura.|
|imAddress|String|Dirección del protocolo de inicio de sesión (SIP) de voz sobre IP (VOIP) del servicio de mensajería instantánea correspondiente al usuario. Solo lectura.|
|isFavorite|Boolean|`true` si el usuario ha marcado este contacto como favorito.|
|jobTitle|String|Puesto del contacto.|
|officeLocation|String|Ubicación de la oficina del contacto.|
|personNotes|String|Notas de forma libre que el usuario ha tomado sobre este contacto.|
|personType|[personType](persontype.md) |Tipo de contacto.|
|phones|Colección [phone](phone.md)|Número de teléfono del contacto.|
|postalAddresses|Colección [location](location.md)|Direcciones del contacto.|
|profession|String|Profesión del contacto.|
|surname|String|Apellido del contacto.|
|userPrincipalName|String|Nombre principal de usuario (UPN) del contacto. El UPN es un nombre de inicio de sesión de Internet del contacto basado en la norma [RFC 822](https://www.ietf.org/rfc/rfc0822.txt). Por convención, se debe asignar al nombre de correo electrónico del contacto. El formato general es alias@domain.|
|websites|Colección [website](website.md)|Sitios web del contacto.|
|yomiCompany|String|Nombre fonético japonés de la compañía del contacto.|

## <a name="relationships"></a>Relaciones

Ninguna.

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.person"
}-->

```json
{
  "birthday": "string",
  "companyName": "string",
  "department": "string",
  "displayName": "string",
  "scoredEmailAddresses": [{"@odata.type": "microsoft.graph.scoredEmailAddress"}],
  "givenName": "string",
  "id": "string (identifier)",
  "imAddress": "string",
  "isFavorite": true,
  "jobTitle": "string",
  "officeLocation": "string",
  "personNotes": "string",
  "personType": {"@odata.type": "microsoft.graph.personType"},
  "phones": [{"@odata.type": "microsoft.graph.phone"}],
  "postalAddresses": [{"@odata.type": "microsoft.graph.location"}],
  "profession": "string",
  "surname": "string",
  "userPrincipalName": "string",
  "websites": [{"@odata.type": "microsoft.graph.website"}],
  "yomiCompany": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "person resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
