---
title: Usar la protección de identidad de Azure AD API (vista previa)
description: Puede utilizar Microsoft Graph para consultar el recursos identityRiskEvent para cada tipo de evento de riesgo detectado por la protección de la identidad de AD de Azure. Estos eventos están disponibles para los clientes con Azure AD Premium P2. Un subconjunto de eventos está disponible para los clientes con Azure AD Premium P1.
author: cloudhandler
ms.openlocfilehash: 8afee9685d22dfaeea43a01f70a8b2834c8d4ff9
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27310377"
---
# <a name="use-the-azure-ad-identity-protection-api-preview"></a>Usar la protección de identidad de Azure AD API (vista previa)

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Puede utilizar Microsoft Graph para consultar el recursos [identityRiskEvent](identityriskevent.md) para cada tipo de evento de riesgo detectado por la [protección de la identidad de AD de Azure](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-identityprotection). Estos eventos están disponibles para los clientes con Azure AD Premium P2. Un subconjunto de eventos está disponible para los clientes con Azure AD Premium P1.

* [inicios de sesión desde las direcciones IP anónimas](anonymousipriskevent.md)
* [inicios de sesión desde dispositivos infectados con malware](malwareriskevent.md)
* [Imposible desplazarse a ubicaciones atípicos](impossibletravelriskevent.md)
* [usuarios con credenciales perdidas](leakedcredentialsriskevent.md)
* [inicios de sesión desde sospechosas direcciones IP](suspiciousipriskevent.md)
* [inicios de sesión desde ubicaciones familiarizadas](unfamiliarlocationriskevent.md)

Utilice las siguientes operaciones para obtener estos eventos y la información asociada:

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Lista identityRiskEvent](../api/identityriskevent-get.md) |[identityRiskEvent](identityriskevent.md)| Obtener la colección de identityRiskEvent. |
|[Obtener identityRiskEvent](../api/identityriskevent-get.md) |[identityRiskEvent](identityriskevent.md)| Obtener el objeto identityRiskEvent. |
|[Lista anonymousIpRiskEvent](../api/anonymousipriskevent-get.md) |[anonymousIpRiskEvent](anonymousipriskevent.md)| Obtener la colección de anonymousIpRiskEvent. |
|[Obtener anonymousIpRiskEvent](../api/anonymousipriskevent-get.md) |[anonymousIpRiskEvent](anonymousipriskevent.md)| Obtener el objeto anonymousIpRiskEvent. |
|[Lista impossibleTravelRiskEvent](../api/impossibletravelriskevent-get.md) |[impossibleTravelRiskEvent](impossibletravelriskevent.md)| Obtener la colección de impossibleTravelRiskEvent. |
|[Obtener impossibleTravelRiskEvent](../api/impossibletravelriskevent-get.md) |[impossibleTravelRiskEvent](impossibletravelriskevent.md)| Obtener el objeto impossibleTravelRiskEvent. |
|[Lista leakedCredentialsRiskEvent](../api/leakedcredentialsriskevent-get.md) |[leakedCredentialsRiskEvent](leakedcredentialsriskevent.md)| Obtener la colección de leakedCredentialsRiskEvent. |
|[Obtener leakedCredentialsRiskEvent](../api/leakedcredentialsriskevent-get.md) |[leakedCredentialsRiskEvent](leakedcredentialsriskevent.md)| Obtener el objeto leakedCredentialsRiskEvent. |
|[Lista malwareRiskEvent](../api/malwareriskevent-get.md) |[malwareRiskEvent](malwareriskevent.md)| Obtener la colección de malwareRiskEvent. |
|[Obtener malwareRiskEvent](../api/malwareriskevent-get.md) |[malwareRiskEvent](malwareriskevent.md)| Obtener el objeto malwareRiskEvent. |
|[Lista suspiciousIpRiskEvent](../api/suspiciousipriskevent-get.md) |[suspiciousIpRiskEvent](suspiciousipriskevent.md)| Obtener la colección de suspiciousIpRiskEvent. |
|[Obtener suspiciousIpRiskEvent](../api/suspiciousipriskevent-get.md) |[suspiciousIpRiskEvent](suspiciousipriskevent.md)| Obtener el objeto suspiciousIpRiskEvent. |
|[Lista unfamiliarLocationRiskEvent](../api/unfamiliarlocationriskevent-get.md) |[unfamiliarLocationRiskEvent](unfamiliarlocationriskevent.md)| Obtener la colección de unfamiliarLocationRiskEvent. |
|[Obtener unfamiliarLocationRiskEvent](../api/unfamiliarlocationriskevent-get.md) |[unfamiliarLocationRiskEvent](unfamiliarlocationriskevent.md)| Obtener el objeto unfamiliarLocationRiskEvent. |

# <a name="see-also"></a>Vea también

* [Acerca de la protección de identidad de Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-identityprotection)
* [Empezar a trabajar con protección de la identidad de Azure Active Directory y Microsoft Graph](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-identityprotection-graph-getting-started)
