---
title: Información general sobre la API de informes de Microsoft Graph
description: Los informes de uso en el Centro de administración de Microsoft 365 permiten a los administradores comprender el uso de su empresa de servicios de Office 365. Puede usar la API de informes de Microsoft Graph para realizar la integración con los informes de uso de Office 365.
ms.openlocfilehash: d923d0003a276be15620998c53693a9bab7116d5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092897"
---
# <a name="microsoft-graph-reports-api-overview"></a>Información general sobre la API de informes de Microsoft Graph

Los informes de uso en el Centro de administración de Microsoft 365 permiten a los administradores comprender el uso de su empresa de servicios de Office 365. Puede usar la API de informes de Microsoft Graph para realizar la integración con los informes de uso de Office 365.

## <a name="why-use-the-reports-api"></a>¿Por qué debería usar la API de informes?

### <a name="integrate-office-365-usage-reporting-into-your-organizations-existing-reporting-solution"></a>Integrar los informes de uso de Office 365 en la solución de informes existente de su organización
Muchas empresas tienen soluciones de informes existentes que usan un portal web o una aplicación de informes. Puede usar la API de informes para incorporar los datos de uso de Office 365 en la solución de informes existente de su organización para que todos los informes de servicio de TI estén en una ubicación unificada.  

### <a name="retain-usage-reports-for-historical-analysis"></a>Conservar los informes de uso para realizar análisis históricos
Puede usar la API de informes para obtener los datos que están disponibles en todos los informes de uso, incluyendo resúmenes por servicio a nivel de la organización, información de uso (usuario, sitios, cuentas) a nivel de entidad de los últimos 7, 30, 90 y 180 días y agregados actividad diarios. Esto le proporciona la opción de mantener la información de uso histórica mientras sea necesario.

## <a name="what-data-can-i-access-by-using-the-reports-api"></a>¿A qué datos se puede acceder a través de la API de informes?

Puede usar la API de informes para acceder a los conjuntos de datos que se muestran en la tabla siguiente.

|Aplicación de Office 365|Conjunto de datos|
|:--------|:--------|
|Microsoft Teams|[Uso de dispositivos](/graph/api/resources/microsoft-teams-device-usage-reports?view=graph-rest-1.0)<br/>|[Actividad de usuario](/graph/api/resources/microsoft-teams-user-activity-reports?view=graph-rest-1.0)|
|Office 365 (general) |[Activaciones](/graph/api/resources/office-365-activations-reports?view=graph-rest-1.0)<br/>[Usuarios activos](/graph/api/resources/office-365-active-users-reports?view=graph-rest-1.0)<br/>[Actividad de grupos](/graph/api/resources/office-365-groups-activity-reports?view=graph-rest-1.0)|
|OneDrive |[Actividad](/graph/api/resources/onedrive-activity-reports?view=graph-rest-1.0)<br/>[Uso](/graph/api/resources/onedrive-usage-reports?view=graph-rest-1.0)|
|Outlook|[Actividad](/graph/api/resources/email-activity-reports?view=graph-rest-1.0)<br/>[Uso de la aplicación](/graph/api/resources/email-app-usage-reports?view=graph-rest-1.0)<br/>[Uso del buzón](/graph/api/resources/mailbox-usage-reports?view=graph-rest-1.0)|
|SharePoint |[Actividad](/graph/api/resources/sharepoint-activity-reports?view=graph-rest-1.0)<br/>[Uso del sitio](/graph/api/resources/sharepoint-site-usage-reports?view=graph-rest-1.0)|
|Skype Empresarial |[Actividad](/graph/api/resources/skype-for-business-activity-reports?view=graph-rest-1.0)<br/>[Uso de dispositivos](/graph/api/resources/skype-for-business-device-usage-reports?view=graph-rest-1.0)<br/>[Uso de dispositivos](/graph/api/resources/skype-for-business-device-usage-reports?view=graph-rest-1.0)<br/>[Actividad de participantes](/graph/api/resources/skype-for-business-participant-activity-reports?view=graph-rest-1.0)<br/>[Actividad punto a punto de](/graph/api/resources/skype-for-business-peer-to-peer-activity?view=graph-rest-1.0)|
|Yammer |[Actividad](/graph/api/resources/yammer-activity-reports?view=graph-rest-1.0)<br/>[Uso de dispositivos](/graph/api/resources/yammer-device-usage-reports?view=graph-rest-1.0)<br/>[Actividad de grupos](/graph/api/resources/yammer-groups-activity-reports?view=graph-rest-1.0)|

## <a name="api-reference"></a>Referencia de la API
¿Busca la referencia de la API para este servicio?

- [API de informes de uso de Office 365 en Microsoft Graph v1.0](/graph/api/resources/report?view=graph-rest-1.0)
- [API de informes de uso de Office 365 en Microsoft Graph beta](/graph/api/resources/report?view=graph-rest-beta)

## <a name="next-steps"></a>Pasos siguientes

* Pruebe la API en el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer).
* Obtenga más información sobre cómo [usar la API de REST de informes](/graph/api/resources/report?view=graph-rest-1.0).
