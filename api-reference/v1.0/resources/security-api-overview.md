---
title: Usar la API de seguridad de Microsoft Graph
description: 'La API de seguridad de Microsoft Graph proporciona una interfaz unificada y el esquema que se integra con soluciones de seguridad de Microsoft y ecosistema de socios. Esto permite a los clientes a optimizar las operaciones de seguridad y defenderse mejor contra el aumento de las amenazas de Internet. La API de seguridad de Microsoft Graph puede usarse como un servicio de agregación de seguridad federada para enviar consultas a todos los proveedores de seguridad onboarded para obtener respuestas agregadas. Usar API de seguridad de Microsoft Graph para crear aplicaciones que:'
localization_priority: Priority
ms.openlocfilehash: 79a4af5f340bbaf8b8d93938e83a60b524f9be2e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27823803"
---
# <a name="use-the-microsoft-graph-security-api"></a>Usar la API de seguridad de Microsoft Graph

La API de seguridad de Microsoft Graph proporciona una interfaz unificada y el esquema que se integra con soluciones de seguridad de Microsoft y ecosistema de socios. Esto permite a los clientes a optimizar las operaciones de seguridad y defenderse mejor contra el aumento de las amenazas de Internet. La API de seguridad de Microsoft Graph puede usarse como un servicio de agregación de seguridad federada para enviar consultas a todos los proveedores de seguridad onboarded para obtener respuestas agregadas. Usar API de seguridad de Microsoft Graph para crear aplicaciones que:

- Consolidar y correlacionar las alertas de seguridad de varios orígenes
- Desbloquear datos contextuales para informar a las investigaciones
- Automatizar las operaciones de seguridad para aumentar la eficacia
- Proporcionar visibilidad a los datos de seguridad para habilitar la administración de riesgos proactiva

La API de seguridad de Microsoft Graph incluye las siguientes entidades de clave.

## <a name="alerts"></a>Alertas

Las alertas son posibles problemas de seguridad dentro de inquilino de un cliente que las soluciones de seguridad de Microsoft o socio han identificado y están marcadas para acción o notificación. Con la entidad de [alertas](alert.md) de seguridad de Microsoft Graph, puede unificar y optimizar los problemas de seguridad en todas las soluciones integradas. Esto también permite aplicaciones correlacionar las alertas y contexto para mejorar la protección contra amenazas y la respuesta. Estos desbloquear la eficacia operativa de seguridad reduciendo el tiempo de investigación y tiempo de resolución de incidentes. Con la capacidad de actualización de la alerta, puede sincronizar el estado de alertas específicas a través de productos de seguridad diferentes y servicios que se integran con la API de seguridad de Microsoft Graph mediante la actualización de la entidad de [alertas](alert.md) .

Las soluciones de Microsoft Graph seguridad integrada va a recibir alertas de los siguientes proveedores de seguridad:

- [Centro de seguridad de Azure](https://docs.microsoft.com/azure/security-center/security-center-alerts-type)
- [Protección de identidad de Azure Active Directory](https://docs.microsoft.com/azure/active-directory/identity-protection/playbook)
- [Seguridad de aplicaciones de nube de Microsoft](https://docs.microsoft.com/cloud-app-security/monitor-alerts )
- [Windows Defender una protección avanzada](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/attack-simulations-windows-defender-advanced-threat-protection)
- [Protección de la información de Azure](https://docs.microsoft.com/azure/information-protection/faqs#i-see-azure-information-protection-is-listed-as-a-security-provider-for-microsoft-graph-securityhow-does-this-work-and-what-alerts-will-i-receive) **(vista previa)**
- Microsoft Intune **(privada preview)**
- Office 365 **(próximamente)**
- Protección contra amenazas de avanzada Azure **(próximamente)**
- Soluciones de socios, como el marco de aplicaciones de redes de Palo Alto

> **Nota:** Los proveedores de nuevo continuamente son incorporación al ecosistema de seguridad de Microsoft Graph.

## <a name="common-use-cases"></a>Casos de uso común

Las siguientes son algunas de las solicitudes de los más populares para trabajar con la API de seguridad de Microsoft Graph:

| **Casos de uso**   | **Recursos de REST** | **Pruébelo en el Explorador de gráfico** |
|:---------------|:--------|:----------|
| List alerts | [List alerts](../api/alert-list.md) | [https://graph.microsoft.com/v1.0/security/alerts](https://developer.microsoft.com/graph/graph-explorer?request=security/alerts&method=GET&version=v1.0&GraphUrl=https://graph.microsoft.com) |
| Actualización de alertas | [Update alert](../api/alert-update.md) | [https://graph.microsoft.com/v1.0/security/alerts/{alert-id}](https://developer.microsoft.com/graph/graph-explorer?request=security/alerts/{alert-id}&method=PATCH&version=v1.0&GraphUrl=https://graph.microsoft.com) |

Puede utilizar Microsoft Graph [webhooks](/graph/webhooks) para suscribirse a y recibir notificaciones sobre las actualizaciones a las entidades de seguridad de Microsoft Graph.

## <a name="resources"></a>Recursos

Código y contribuir a estos ejemplos de API de seguridad de Microsoft Graph:

- [Ejemplo de ASP.NET (C#)](https://github.com/microsoftgraph/aspnet-security-api-sample)
- [Ejemplo de Python](https://github.com/microsoftgraph/python-security-rest-sample)
- [Ejemplo de Node.js (JavaScript)](https://github.com/microsoftgraph/nodejs-security-sample)

Integrarse con la Comunidad:

- [Únase a la Comunidad de tech](https://aka.ms/graphsecuritycommunity)
- [Se analizan en StackOverflow](https://stackoverflow.com/questions/tagged/microsoft-graph-security)

## <a name="next-steps"></a>Pasos siguientes

La API de seguridad de Microsoft Graph puede abrir nuevas maneras para que pueda integrarse con diferentes soluciones de seguridad de Microsoft y socios. Siga estos pasos para empezar:

- Profundizar en [las alertas](alert.md).
- Pruebe la API en el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer). En **Las consultas de ejemplo**, elija **Mostrar más muestras** y establezca la categoría de seguridad **en**.
- Intente [receptora y suscribirse a las notificaciones](/graph/webhooks) de cambios de la entidad.

¿Necesita más ideas? Vea [cómo algunos de nuestros socios utilizan Microsoft Graph](https://developer.microsoft.com/graph/graph/examples#partners).
