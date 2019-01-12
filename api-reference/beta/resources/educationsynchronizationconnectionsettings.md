---
title: tipo de recurso educationSynchronizationConnectionSettings
description: 'Representa la configuración de conexión del proveedor. Esto permite que el sistema saber cómo conectarse al proveedor de API. '
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: f9bb19ec9c09b06dd007eb2031f3dbb176eb12d3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27978231"
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
| **clientId** | Cadena |  Identificador de cliente que se usa para conectarse al proveedor de. |
| **clientSecret** | Cadena |  Secreto de cliente para autenticar la conexión con el proveedor. |
