---
title: Introducción a la API de registro de auditoría de Azure AD
description: Azure Active Directory (AD Azure) realiza un seguimiento de las métricas de actividad e inicio de sesión de usuario y auditoría de crea informes de registro que le ayudarán a comprender la forma en que los usuarios tener acceso y aprovechan los servicios de Azure AD. Usar la API de gráfico de Microsoft para Azure AD para analizar los datos subyacentes de estos informes y para crear soluciones personalizadas adaptadas a necesidades específicas de su organización.
localization_priority: Priority
ms.openlocfilehash: 07d285ce4e7fbf736900c1d6d4acdf159b451424
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27826225"
---
# <a name="azure-ad-audit-log-api-overview"></a>Introducción a la API de registro de auditoría de Azure AD

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Azure Active Directory (AD Azure) realiza un seguimiento de las métricas de actividad e inicio de sesión de usuario y auditoría de crea informes de registro que le ayudarán a comprender la forma en que los usuarios tener acceso y aprovechan los servicios de Azure AD. Usar la API de gráfico de Microsoft para Azure AD para analizar los datos subyacentes de estos informes y para crear soluciones personalizadas adaptadas a necesidades específicas de su organización.

## <a name="what-are-azure-ad-activity-logs"></a>¿Cuáles son las actividades de Azure AD registros?

Azure AD proporciona dos tipos de registros de actividad:

- registros de auditoría 
- registros de inicio de sesión

### <a name="audit-logs"></a>Registros de auditoría

El informe de actividad de los registros de auditoría proporciona acceso al historial de cada tarea que se lleva a cabo en el inquilino. El informe de los registros de auditoría proporciona con los registros de las actividades del sistema para el cumplimiento. Entre otras cosas, los datos proporcionados permiten abordar escenarios comunes, como:

- ¿Quién concedido acceso al grupo de administración a un usuario de Active directory?

- ¿Los usuarios que inicien sesión en una aplicación de adquirido recientemente?

- ¿Restablece las contraseñas cuántos se han realizado en el directorio?

### <a name="sign-in-logs"></a>Inicie sesión en los registros

El informe de actividad de inicios de sesión le ayuda a determinar quién realizó las tareas de los informes de registro de auditoría. El informe de actividad de inicios de sesión le ayudará a responder a preguntas como:

- ¿Qué es la trama de un usuario para iniciar sesión?
- ¿Cuántos usuarios han iniciado sesión en durante la última semana?
- ¿Qué es el estado de estos inicios de sesión?

## <a name="what-can-i-do-with-audit-log-apis-in-microsoft-graph"></a>¿Qué puedo hacer con el registro de auditoría de las API en Microsoft Graph?

Aquí están las solicitudes más populares para trabajar con datos de registro de auditoría:

Operación | URL
:----------|:----
OBTENER A inquilino las actividades del usuario | [https://graph.microsoft.com/beta/auditLogs/directoryAudits](https://developer.microsoft.com/graph/graph-explorer?request=auditLogs/directoryAudits&version=beta)
OBTENER A inquilino inicios de sesión de usuario | [https://graph.microsoft.com/beta/auditLogs/signIns](https://developer.microsoft.com/graph/graph-explorer?request=auditLogs/signIns&version=beta)

## <a name="what-licenses-do-i-need"></a>¿Qué licencias es necesario?

Informes de registro de auditoría están disponibles para las características que ha obtenido una licencia.  Si tiene una licencia para una característica específica, también tiene acceso a sus registros de auditoría.

Por ejemplo, necesita una licencia de Azure AD Premium P1 para acceder a los informes de auditoría de contraseña self-service.  Para obtener más información, vea [licencias de Azure AD](https://azure.microsoft.com/pricing/details/active-directory/).

Inicio de sesión de los informes requieren una licencia de Azure AD Premium.

Para obtener más información, vea [precios de Azure AD](https://azure.microsoft.com/pricing/details/active-directory/).

## <a name="next-steps"></a>Pasos siguientes

- [Registrar la aplicación](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-api-prerequisites-azure-portal) para satisfacer los requisitos previos del registro de auditoría. 
- Obtenga información de [registro de auditoría](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-api-audit-samples) y [ejemplos de inicio de sesión](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-api-sign-in-activity-samples).  
- Revisar [directoryAudit](directoryaudit.md) recurso y acciones.
- Revise los recursos de [Inicio de sesión](signin.md) y acciones. 
