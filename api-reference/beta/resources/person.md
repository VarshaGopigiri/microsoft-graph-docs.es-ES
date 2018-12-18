---
title: Tipo de recurso person
description: Una agregación de información acerca de una persona de a través de correo, contactos y las redes sociales. Personas pueden ser contactos locales, los contactos de redes sociales, active directory de su organización y personas desde las comunicaciones de recientes (por ejemplo, correo electrónico y Skype).
author: simonhult
ms.openlocfilehash: eccd5da56806b6608f5610579c61a171713990b6
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27308557"
---
# <a name="person-resource-type"></a>Tipo de recurso person

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Una agregación de información acerca de una persona de a través de correo, contactos y las redes sociales. Personas pueden ser contactos locales, los contactos de redes sociales, active directory de su organización y personas desde las comunicaciones de recientes (por ejemplo, correo electrónico y Skype).

## <a name="methods"></a>Métodos

| Método | Tipo de valor devuelto | Descripción |
|:---------------|:--------|:----------|
|[List people](../api/user-list-people.md) | **person** |Obtenga una colección de objetos person ordenados por su relevancia para el [user](../resources/user.md).|

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:---------------|:--------|:----------|
|birthday|string|Cumpleaños del contacto.|
|companyName|string|Nombre de la compañía del contacto.|
|department|string|Departamento del contacto.|
|displayName|string|Nombre para mostrar del contacto.|
|emailAddresses|colección de [rankedEmailAddress](rankedemailaddress.md)|Direcciones de correo electrónico del contacto.|
|givenName|string|Nombre propio del contacto.|
|id|string|Identificador único del contacto. Solo lectura.|
|isFavorite|boolean|`true` si el usuario ha marcado este contacto como favorito.|
|mailboxType|string|El tipo de buzón de correo que está representada por la dirección de correo electrónico de la persona.|
|officeLocation|string|Ubicación de la oficina del contacto.|
|personNotes|string|Notas de forma libre que el usuario ha tomado sobre este contacto.|
|personType|string|El tipo de persona, por ejemplo la lista de distribución.|
|phones|Colección [phone](phone.md)|Número de teléfono del contacto.|
|postalAddresses|Colección [location](location.md)|Direcciones del contacto.|
|profession|string|Profesión del contacto.|
|orígenes|colección de [personDataSource](persondatasource.md)|Los orígenes de los datos de usuario proceden de, por ejemplo, Active Directory o los contactos de Outlook.|
|surname|string|Apellido del contacto.|
|title|string|Título de la persona.|
|userPrincipalName|string|Nombre principal de usuario (UPN) del contacto. El UPN es un nombre de inicio de sesión de Internet del contacto basado en la norma [RFC 822](https://www.ietf.org/rfc/rfc0822.txt). Por convención, se debe asignar al nombre de correo electrónico del contacto. El formato general es alias@domain.|
|websites|Colección [website](website.md)|Sitios web del contacto.|
|yomiCompany|string|Nombre fonético japonés de la compañía del contacto.|

## <a name="relationships"></a>Relaciones

Ninguno

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.person"
}-->

```json
{
  "birthday": "string",
  "companyName": "string",
  "department": "string",
  "displayName": "string",
  "emailAddresses": [{"@odata.type": "microsoft.graph.rankedEmailAddress"}],
  "givenName": "string",
  "id": "string (identifier)",
  "isFavorite": true,
  "mailboxType": "string",
  "officeLocation": "string",
  "personNotes": "string",
  "personType": "string",
  "phones": [{"@odata.type": "microsoft.graph.phone"}],
  "postalAddresses": [{"@odata.type": "microsoft.graph.location"}],
  "profession": "string",
  "sources": [{"@odata.type": "microsoft.graph.personDataSource"}],
  "surname": "string",
  "title": "string",
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
