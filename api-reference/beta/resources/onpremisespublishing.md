---
title: tipo de recurso onPremisesPublishing
description: Aquí tiene una representación JSON del recurso.
ms.openlocfilehash: 8dba505347fc12d3c4a8521ebe32551d738dc4a2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087026"
---
# <a name="onpremisespublishing-resource-type"></a>tipo de recurso onPremisesPublishing

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|customDomainCertificate|String|Detalles del certificado asociado a la aplicación cuando un dominio personalizado está en uso. NULL cuando se usa el dominio predeterminado.|
|externalAuthenticationType|String|Se explica la configuración de la autenticación previa para la aplicación de los valores posibles es: `passthru`, `aadPreAuthentication`.|
|externalUrl|String|La dirección de url externa publicado para la aplicación. Por ejemplohttps://intranet-contoso.msappproxy.net/  |
|internalUrl|String|La dirección url interna de la aplicación. Por ejemplohttps://intranet/ |
|isOnPremPublishingEnabled|Booleano|Indica si la aplicación se publica actualmente o no.|
|applicationServerTimeout|String|La duración el conector esperará una respuesta de la aplicación back-end antes de cerrar la conexión. Los valores posibles son `default`, `long`. Uso `long` si su servidor tarda más de 75 de 60 segundos para responder a las solicitudes. Intente también `long` si no puede tener acceso a la aplicación y el estado de error es "Backend Timeout".|
|isTranslateHostHeaderEnabled|Booleano|Indica si la aplicación debe traducir las direcciones URL en los encabezados de respuesta. Esto incluye la configuración del sitio correcto para las cookies.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.onPremisesPublishing"
}-->

```json
{
  "customDomainCertificate": "String",
  "externalAuthenticationType": "String",
  "externalUrl": "String",
  "internalUrl": "String",
  "isOnPremPublishingEnabled": true,
  "applicationServerTimeout": "String",
  "isTranslateHostHeaderEnabled": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onPremisesPublishing resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
