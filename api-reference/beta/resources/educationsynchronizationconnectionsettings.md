---
title: tipo de recurso educationSynchronizationConnectionSettings
description: 'Representa la configuración de conexión del proveedor. Esto permite que el sistema saber cómo conectarse al proveedor de API. '
ms.openlocfilehash: 27cdd377318d3294be9802b7cf28e940d0ada31c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087406"
---
# <a name="educationsynchronizationconnectionsettings-resource-type"></a>tipo de recurso educationSynchronizationConnectionSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa la configuración de conexión del proveedor. Esto permite que el sistema saber cómo conectarse al proveedor de API. 

> **Nota:** Este tipo complejo es abstracta. Hacer referencia a los tipos específicos de la configuración de conexión que aparecen.

## <a name="derived-types"></a>Tipos derivados
| Tipo | Descripción | 
|:-|:-|
| [**educationSynchronizationOAuth1ConnectionSettings**](educationsynchronizationoauth1connectionsettings.md) | Use este tipo para proporcionar la configuración de conexión de OAuth1. |
| [**educationSynchronizationOAuth2ClientCredentialsConnectionSettings**](educationsynchronizationoauth2clientcredentialsconnectionsettings.md) | Use este tipo para proporcionar la configuración de conexión de concesión de las credenciales de cliente de OAuth2. |

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:-|:-|:-|
| **clientId** | String |  Identificador de cliente que se usa para conectarse al proveedor de. |
| **clientSecret** | String |  Secreto de cliente para autenticar la conexión con el proveedor. |