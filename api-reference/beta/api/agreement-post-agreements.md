---
title: Crear contrato
description: Crear un nuevo objeto de contrato.
localization_priority: Normal
ms.openlocfilehash: 4768912a7c5be722878d6b910d6d68ded460c702
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27870640"
---
# <a name="create-agreement"></a>Crear contrato

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Crear un nuevo objeto de [contrato](../resources/agreement.md) .
## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso                        | Permisos (de menos a más privilegiados)              |
|:--------------------------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa)     | Agreement.ReadWrite.All |
|Delegado (cuenta personal de Microsoft) | No admitida. |
|Aplicación                            | No admitida. |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /agreements
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre         | Tipo        | Descripción |
|:-------------|:------------|:------------|
| Autorización | string | Bearer \{token\}. Necesario. |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación JSON de objeto de [acuerdo](../resources/agreement.md) .

En la tabla siguiente, se muestran las propiedades necesarias al crear un usuario.

| Propiedad     | Tipo        | Descripción |
|:-------------|:------------|:------------|
|displayName|Cadena|Nombre para mostrar del contrato.|
|isViewingBeforeAcceptanceRequired|Booleano|Indica si el usuario tiene que expandir y ver el contrato antes de Aceptar.|
|archivos/nombre de archivo|Cadena|Nombre del archivo de contrato (por ejemplo, TOU.pdf).|
|archivos/isDefault|Booleano|Indica si este es el archivo del contrato de forma predeterminada si ninguno de la referencia cultural coincide con la preferencia de cliente. Si ninguno de los archivos se marca como predeterminada, el primero de ellos se tratará como predeterminado.|
|los archivos y el idioma|Cadena|Referencia cultural del archivo de contrato en el formato languagecode2-país/regioncode2. languagecode2 es un código de dos letras en minúsculas proveniente de ISO 639-1. país/regioncode2 se deriva de ISO 3166 y normalmente consta de dos letras en mayúsculas, o una etiqueta de idioma BCP 47 (por ejemplo, en-US).|
|archivos, fileData/datos|Binario|Datos que representan las condiciones de uso del documento PDF.|

## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `201, Created` objeto de [acuerdo](../resources/agreement.md) y código de respuesta en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
En el cuerpo de la solicitud, proporcionar una representación JSON del objeto de [contrato](../resources/agreement.md) .

<!-- {
  "blockType": "request",
  "name": "create_agreement_from_agreements"
}-->
```http
POST https://graph.microsoft.com/beta/agreements
Content-type: application/json

{
  "displayName": "MSGraph Sample",
  "isViewingBeforeAcceptanceRequired": true,
  "files": [
    {
      "fileName": "TOU.pdf",
      "language": "en",
      "isDefault": true,
      "fileData": {
        "data": "SGVsbG8gd29ybGQ="
      }
    }
  ]
}
```

##### <a name="response"></a>Respuesta
>**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.agreement"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "displayName": "MSGraph Sample",
  "isViewingBeforeAcceptanceRequired": true,
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create agreement",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
