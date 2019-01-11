---
title: tipo de recurso agreementFile
description: Representa un términos personalizable del archivo del contrato de uso que administra un inquilino con Azure Active Directory (AD Azure). Contiene los metadatos sobre el archivo del contrato (por ejemplo, el nombre, el idioma, y si éste es el archivo de forma predeterminada).
localization_priority: Normal
ms.openlocfilehash: f06792d63deabf25659a09e8aec5ed0e8f036472
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27804511"
---
# <a name="agreementfile-resource-type"></a>tipo de recurso agreementFile

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa un términos personalizable del archivo del contrato de uso que administra un inquilino con Azure Active Directory (AD Azure). Contiene los metadatos sobre el archivo del contrato (por ejemplo, el nombre, el idioma, y si éste es el archivo de forma predeterminada).

<!--
## Methods

| Method       | Return Type | Description |
|:-------------|:------------|:------------|
| [Get agreementFile](../api/agreementfile-get.md) | [agreementFile](agreementfile.md) | Read properties and relationships of an **agreementFile** object. |
| [Update](../api/agreementfile-update.md) | [agreementFile](agreementfile.md) | Update an **agreementFile** object. |
| [Delete](../api/agreementfile-delete.md) | None | Delete an **agreementFile** object. |
-->

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo        | Description |
|:-------------|:------------|:------------|
|fileData|[agreementFileData](agreementfiledata.md)|Datos que representan las condiciones de usar un documento PDF. Solo lectura.|
|fileName|Cadena|Nombre del archivo de contrato (por ejemplo, TOU.pdf). Solo lectura.|
|id|Cadena|Solo lectura.|
|isDefault|Booleano|Indica si este es el archivo del contrato de forma predeterminada si ninguna de las referencias culturales coincide con la preferencia de cliente. Si ninguno de los archivos están marcado como predeterminada, el primero de ellos se tratará como el valor predeterminado. Solo lectura.|
|language|Cadena|Referencia cultural del archivo de contrato en el formato languagecode2-país/regioncode2. languagecode2 es un código de dos letras en minúsculas proveniente de ISO 639-1. país/regioncode2 se deriva de ISO 3166 y normalmente consta de dos letras en mayúsculas, o una etiqueta de idioma BCP 47 (por ejemplo, en-US). Solo lectura.|

## <a name="relationships"></a>Relaciones
Ninguna.


## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.agreementFile"
}-->

```json
{
  "fileData": {"@odata.type": "microsoft.graph.agreementFileData"},
  "fileName": "String",
  "id": "String (identifier)",
  "isDefault": true,
  "language": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "agreementFile resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
