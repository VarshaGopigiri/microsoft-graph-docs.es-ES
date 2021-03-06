---
title: tipo de recurso Web
description: Especifica la configuración para una aplicación web.
localization_priority: Normal
ms.openlocfilehash: 26efe59eda739597e7193fa1ff79443f3d64b5a7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27890205"
---
# <a name="web-resource-type"></a>tipo de recurso Web

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Especifica la configuración para una aplicación web.

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Description |
|:---------|:-----|:------------|
|implicitGrantSettings|[implicitGrantSettings](implicitgrantsettings.md)| Especifica si esta aplicación web puede solicitar tokens con el flujo de OAuth 2.0 implícita.|
|logoutUrl|Cadena| Especifica la dirección URL que usará el servicio de autorización de Microsoft para cerrar sesión de un usuario mediante [canal de frente](https://openid.net/specs/openid-connect-frontchannel-1_0.html), [back canal](https://openid.net/specs/openid-connect-backchannel-1_0.html) o protocolos de cierre de sesión SAML. |
|oauth2AllowImplicitFlow|Booleano| En desuso. No la use. | 
|redirectUris|Colección String| Especifica las direcciones URL que los tokens de usuario se envían a para el inicio de sesión o el redireccionamiento de los códigos de autorización de los URI que OAuth 2.0 y tokens de acceso se envían a. |

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.web"
}-->

```json
{
  "implicitGrantSettings": {"@odata.type": "microsoft.graph.implicitGrantSettings"},
  "logoutUrl": "String",
  "oauth2AllowImplicitFlow": false,
  "redirectUris": ["String"]
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "web resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
