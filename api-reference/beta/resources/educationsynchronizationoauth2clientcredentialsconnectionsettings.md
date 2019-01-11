---
title: recursos de educationSynchronizationOAuth2ClientCredentialsConnectionSettings
description: Al conceder de credenciales de cliente de OAuth2 es que se usará para conectarse al proveedor de datos, debe usarse este tipo de configuración de conexión para configurar el perfil.
localization_priority: Normal
ms.openlocfilehash: 49a0a267ddb3a8f3a954888679806ea7913e24f0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27822585"
---
# <a name="educationsynchronizationoauth2clientcredentialsconnectionsettings-resource"></a>recursos de educationSynchronizationOAuth2ClientCredentialsConnectionSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Al [Conceder de credenciales de cliente de OAuth2](https://tools.ietf.org/html/rfc6749#section-4.4) es que se usará para conectarse al proveedor de datos, debe usarse este tipo de configuración de conexión para configurar el perfil.

Deriva de [educationSynchronizationConnectionSettings](educationsynchronizationconnectionsettings.md).

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Description |
|:-|:-|:-|
| **tokenUrl** | Cadena | La dirección URL para obtener los tokens de acceso para el proveedor de datos. |
| **ámbito** | Cadena | [El ámbito de la solicitud de acceso](https://tools.ietf.org/html/rfc6749#section-3.3). |

## <a name="json-representation"></a>Representación JSON
<!-- {
  "blockType": "resource",
  "@odata.type": "#microsoft.graph.educationSynchronizationOAuth2ClientCredentialsConnectionSettings"
}-->

```json
"connectionSettings": {
    "@odata.type": "#microsoft.graph.educationSynchronizationOAuth2ClientCredentialsConnectionSettings",
    "clientId": "String",
    "clientSecret": "String",
    "tokenUrl": "String",
    "scope": "String"
}
```
