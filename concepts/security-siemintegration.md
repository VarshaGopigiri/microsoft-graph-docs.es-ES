---
title: Integrar las alertas de la API de seguridad de Microsoft Graph con un SIEM
description: La API de seguridad de Microsoft Graph permite administrar alertas de seguridad de todos los productos de seguridad de Microsoft, conocidos como proveedores de seguridad de Microsoft Graph, con un único punto de conexión de REST. Puede que algunas organizaciones ya hayan ingerido datos de registro específicos de Azure a través de Azure Monitor en soluciones SIEM. Para facilitar la integración, las alertas de seguridad disponibles a través de la API de seguridad de Microsoft Graph también puede aprovisionarlas el cliente a su suscripción a través de Azure Monitor. Si la organización ya ha configurado la integración de Azure Monitor con su solución SIEM, ahora podrá agregar fácilmente alertas de seguridad de la organización a los datos disponibles a través de Azure Monitor.
author: Preetikr
ms.openlocfilehash: 24b2261e2a320e5384fba97802eab43991c34254
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27327387"
---
# <a name="integrate-microsoft-graph-security-api-alerts-with-a-siem"></a>Integrar las alertas de la API de seguridad de Microsoft Graph con un SIEM

La API de seguridad de Microsoft Graph permite administrar alertas de seguridad de todos los productos de seguridad de Microsoft, conocidos como proveedores de seguridad de Microsoft Graph, con un único punto de conexión de REST. Puede que algunas organizaciones ya hayan ingerido datos de registro específicos de Azure a través de Azure Monitor en soluciones SIEM. Para facilitar la integración, las alertas de seguridad disponibles a través de la API de seguridad de Microsoft Graph también puede aprovisionarlas el cliente a su suscripción a través de Azure Monitor. Si la organización ya ha configurado la integración de Azure Monitor con su solución SIEM, ahora podrá agregar fácilmente alertas de seguridad de la organización a los datos disponibles a través de Azure Monitor.

Azure Monitor es compatible con conectores para varios productos SIEM. Para obtener una lista de productos SIEM compatibles, consulte [enviar datos de supervisión a un centro de eventos](https://docs.microsoft.com/es-ES/azure/monitoring-and-diagnostics/monitor-stream-monitoring-data-event-hubs#what-can-i-do-with-the-monitoring-data-being-sent-to-my-event-hub). La integración de la API de seguridad de Microsoft Graph está disponible actualmente para [Splunk](https://splunkbase.splunk.com/) y [QRadar](https://www.ibm.com/us-en/marketplace/ibm-qradar-siem).

Para obtener información sobre la integración con la API de seguridad de Microsoft Graph para soluciones SIEM específicas, vea:

- [Splunk](security-splunk-siemintegration.md)
- [QRadar](security-qradar-siemintegration.md)
