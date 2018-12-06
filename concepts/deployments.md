---
title: Implementaciones de nube nacionales
description: Además de en nuestra red global de centros de datos, Servicios en la nube de Microsoft está disponible en tres nubes nacionales independientes. Estas versiones de nube nacional son las instancias aisladas de red físicas y lógicas de los servicios en la nube empresariales de Microsoft, que se confinan a los límites geográficos de países específicos y están operados por personal local. Para más información, vea Microsoft National Clouds.
ms.openlocfilehash: b0f2ab257773faa14fe59566992bb1ed0dd77959
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092774"
---
# <a name="national-cloud-deployments"></a>Implementaciones de nube nacionales


Además de en nuestra red global de centros de datos, Servicios en la nube de Microsoft está disponible en tres nubes nacionales independientes. Estas versiones de nube nacional son las instancias aisladas de red físicas y lógicas de los servicios en la nube empresariales de Microsoft, que se confinan a los límites geográficos de países específicos y están gestionados por personal local. Para más información, vea [Microsoft National Clouds](https://www.microsoft.com/es-ES/TrustCenter/CloudServices/NationalCloud) (Nubes nacionales de Microsoft).

Las nubes nacionales actuales incluyen:

- Microsoft Cloud for US Government
- Microsoft Cloud Alemania
- Azure y Office 365 operado por 21Vianet en China

En este artículo se proporciona información sobre las diferentes implementaciones de nube nacional de Microsoft Graph y las funcionalidades de cada implementación que están disponibles para los desarrolladores.

## <a name="microsoft-graph-and-microsoft-graph-explorer-service-root-endpoints"></a>Puntos de conexión raíz de servicio de Microsoft Graph y Probador de Microsoft Graph

En la tabla siguiente se muestran los puntos de conexión raíz de servicio de Microsoft Graph y Probador de Microsoft Graph para cada nube nacional.

| Nube nacional | Microsoft Graph | Explorador de Microsoft Graph
|---------------------------|----------------|----------------|
| Microsoft Graph China gestionado por 21Vianet | https://microsoftgraph.chinacloudapi.cn | https://developer.microsoft.com/zh-cn/graph/graph-explorer-china |
| Microsoft Graph Alemania | https://graph.microsoft.de | No admitida. |
| Microsoft Graph for US Government | https://graph.microsoft.com | No admitida. |
| Servicio global de Microsoft Graph | https://graph.microsoft.com | https://developer.microsoft.com/graph/graph-explorer |

> **Nota:** Las aplicaciones solo pueden tener acceso a los datos de la organización a través de los puntos de conexión de la nube nacional. Esto significa que solo se puede tener acceso a los datos de los espacios empresariales registrados en la nube nacional específica. Las aplicaciones que intenten tener acceso a los datos de consumidor asociados a cuentas de Microsoft personales a través de Microsoft Graph deben usar el servicio global (https://graph.microsoft.com)). Los tokens de acceso adquiridos para una implementación de nube nacional no son intercambiables con los adquiridos para el servicio global.

## <a name="azure-ad-openid-connect-and-oauth20-endpoints"></a>Puntos de conexión de OpenID Connect y OAuth2.0 de Azure AD

En la tabla siguiente se muestran las direcciones URL base para los puntos de conexión de Azure Active Directory (AD Azure) que se usan para adquirir tokens para llamar a Microsoft Graph en cada nube nacional.

| Nube nacional | Punto final raíz de Azure AD |
|---------------------------|----------------|
| Azure AD China gestionado por 21Vianet |https://login.chinacloudapi.cn |
| Azure AD Germany | https://login.microsoftonline.de |
| Azure AD for US Government | https://login.microsoftonline.us |
| Azure AD (servicio global) | https://login.microsoftonline.com |

Las solicitudes a los puntos de conexión de tokens o de autorización de Azure AD pueden formarse con la dirección URL base específica para la región correspondiente. Por ejemplo, para Alemania:

- El punto de conexión común de autorizaciones es https://login.microsoftonline.de/common/oauth2/authorize.
- El punto de conexión común de tokens es https://login.microsoftonline.de/common/oauth2/token.

Los puntos de conexión específicos del espacio empresarial se pueden formar reemplazando "common" en las direcciones URL anteriores con el identificador del espacio empresarial o un dominio comprobado para el espacio empresarial. El uso de puntos de conexión comunes o específicos del espacio empresarial dependerá de los requisitos de la aplicación y del flujo de autenticación que se use para obtener los tokens. Para obtener más información sobre los tokens de acceso de Azure AD y Microsoft Graph, vea [Obtener tokens de autenticación](./auth-overview.md).

> **Nota:** Los [puntos de conexión de autorización y tokens de Azure AD v2.0](https://azure.microsoft.com/es-ES/documentation/articles/active-directory-appmodel-v2-overview/) solo están disponibles en el servicio global; todavía no son compatibles para su uso con implementaciones de nube nacional.

## <a name="supported-features"></a>Características admitidas

Las siguientes características de Microsoft Graph están disponibles con carácter general (en el punto de conexión `/v1.0`) en todas las implementaciones de nube nacional, excepto donde se indique:

* Usuarios
* Grupos
* Excel (el soporte es limitado en Microsoft Graph operado por 21Vianet en China).
* OneDrive (el soporte es limitado en Microsoft Graph operado por 21Vianet en China).
* Correo de Outlook
* Calendario de Outlook
* Contactos personales 
* SharePoint (el soporte es limitado en Microsoft Graph operado por 21Vianet en China).
* Consulta delta (la compatibilidad varía entre diferentes recursos en cada implementación de nube nacional).
* Webhooks (la compatibilidad varía entre diferentes recursos en cada implementación de nube nacional).

Las siguientes características adicionales de Microsoft Graph están disponibles en versión preliminar (en el punto de conexión `/beta`) en todas las implementaciones de nube nacional, excepto donde se indique:

* Contactos de la organización
* Aplicaciones
* Entidades de servicio

Las siguientes características de Microsoft Graph todavía no se admiten en las implementaciones de nube nacionales:

* Microsoft Planner
* Extensiones de esquema de directorio
* Extensiones de tipo abierto
