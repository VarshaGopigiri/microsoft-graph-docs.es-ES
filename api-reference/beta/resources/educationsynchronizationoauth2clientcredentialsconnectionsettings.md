---
title: recursos de educationSynchronizationOAuth2ClientCredentialsConnectionSettings
description: Al conceder de credenciales de cliente de OAuth2 es que se usará para conectarse al proveedor de datos, debe usarse este tipo de configuración de conexión para configurar el perfil.
ms.openlocfilehash: 901fabb802d4ed5fa0c99538e52b9a07199eb298
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088875"
---
# <a name="educationsynchronizationoauth2clientcredentialsconnectionsettings-resource"></a>recursos de educationSynchronizationOAuth2ClientCredentialsConnectionSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Al [Conceder de credenciales de cliente de OAuth2](https://tools.ietf.org/html/rfc6749#section-4.4) es que se usará para conectarse al proveedor de datos, debe usarse este tipo de configuración de conexión para configurar el perfil.

Deriva de [educationSynchronizationConnectionSettings](educationsynchronizationconnectionsettings.md).

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:-|:-|:-|
| **tokenUrl** | String | La dirección URL para obtener los tokens de acceso para el proveedor de datos. |
| **ámbito** | String | [El ámbito de la solicitud de acceso](https://tools.ietf.org/html/rfc6749#section-3.3). |

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
