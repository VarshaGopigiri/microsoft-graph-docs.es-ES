---
title: tipo de recurso parentalControlSettings
description: Especifica la configuración de control parental para una aplicación. Estas configuraciones controlan la experiencia de consentimiento.
localization_priority: Normal
ms.openlocfilehash: bb6f776d5f206fb0ed35a999effc7bbdc0768512
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27806520"
---
# <a name="parentalcontrolsettings-resource-type"></a>tipo de recurso parentalControlSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Especifica la configuración de control parental para una aplicación. Estas configuraciones controlan la experiencia de consentimiento.

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Description |
:---------------|:--------|:----------|
|countriesBlockedForMinors|Colección String| Especifica los [códigos de país de dos letras ISO](https://www.iso.org/iso-3166-country-codes.html). Acceso a la aplicación se bloqueará para menores de los países especificados en esta lista.|
|legalAgeGroupRule| Cadena | Especifica la regla de grupo de edad legal que se aplica a los usuarios de la aplicación. Se puede establecer en uno de los siguientes valores: <table><tr><th>Valor</th><th>Description</th></tr><tr><td>Permitir</td><td>Valor predeterminado. Aplica el mínimo legal. Esto significa que se requiere para menores en la Unión Europea y Corea consentimiento de los padres.</td></tr><tr><td>RequireConsentForPrivacyServices</td><td>Aplica el usuario para especificar la fecha de nacimiento para cumplir con las reglas de COPPA. </td></tr><tr><td>RequireConsentForMinors</td><td>Requiere el consentimiento de los padres para mayores por debajo de 18, independientemente de las reglas de país secundarias.</td></tr><tr><td>RequireConsentForKids</td><td>Requiere el consentimiento de los padres para mayores de debajo de 14, independientemente de las reglas de país secundarias.</td></tr><tr><td>BlockMinors</td><td>Impuesto de bloques de uso de la aplicación.</td></tr></table> |

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

```json
{
  "countriesBlockedForMinors": [ "String" ],
  "legalAgeGroupRule": "String"
}

```
