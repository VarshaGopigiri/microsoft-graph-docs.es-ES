---
title: tipo de recurso educationSynchronizationConnectionSettings
description: 'Representa la configuración de conexión del proveedor. Esto permite que el sistema saber cómo conectarse al proveedor de API. '
author: mmast-msft
ms.openlocfilehash: 4e8b62a46fa6d14508a9d57ffedc46411910433d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27350627"
---
# <a name="educationsynchronizationconnectionsettings-resource-type"></a>tipo de recurso educationSynchronizationConnectionSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa la configuración de conexión del proveedor. Esto permite que el sistema saber cómo conectarse al proveedor de API. 

> **Nota:** Este tipo complejo es abstracta. Hacer referencia a los tipos específicos de la configuración de conexión que aparecen.

## <a name="derived-types"></a>Tipos derivados
| Type | Descripción | 
|:-|:-|
| [**educationSynchronizationOAuth1ConnectionSettings**](educationsynchronizationoauth1connectionsettings.md) | Use este tipo para proporcionar la configuración de conexión de OAuth1. |
| [**educationSynchronizationOAuth2ClientCredentialsConnectionSettings**](educationsynchronizationoauth2clientcredentialsconnectionsettings.md) | Use este tipo para proporcionar la configuración de conexión de concesión de las credenciales de cliente de OAuth2. |

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:-|:-|:-|
| **clientId** | String |  Identificador de cliente que se usa para conectarse al proveedor de. |
| **clientSecret** | String |  Secreto de cliente para autenticar la conexión con el proveedor. |