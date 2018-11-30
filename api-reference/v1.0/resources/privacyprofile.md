---
title: Tipo de recurso privacyProfile
description: Representa el perfil de privacidad de una compañía; incluye la dirección URL de una declaración de privacidad y una persona de contacto para las preguntas sobre la declaración de privacidad.
ms.openlocfilehash: 5d1a8e48a2d8310f45c71fbc73485e8ec4fe8697
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032081"
---
# <a name="privacyprofile-resource-type"></a>Tipo de recurso privacyProfile

Representa el perfil de privacidad de una compañía; incluye la dirección URL de una declaración de privacidad y una persona de contacto para las preguntas sobre la declaración de privacidad.

## <a name="properties"></a>Propiedades
| Propiedad   | Tipo|Descripción|
|:---------------|:--------|:----------|
|contactEmail|String| Dirección de correo electrónico smtp válida para el contacto de la declaración de privacidad. No se requiere.|
|statementUrl|String| Formato de URL válido que empiece por http:// o https://. La longitud máxima es de 255 caracteres. Dirección URL que se dirige a la declaración de privacidad de la compañía. No se requiere.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.privacyProfile"
}-->

```json
{
  "contactEmail": "string",
  "statementUrl": "string"
}
```