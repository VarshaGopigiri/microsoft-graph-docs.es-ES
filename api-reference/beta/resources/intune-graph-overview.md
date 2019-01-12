---
title: Usar la API de Graph de Intune
description: " No se admiten las implementaciones híbridas de Intune. "
author: tfitzmac
localization_priority: Priority
ms.prod: intune
ms.openlocfilehash: 1db77aceaab82e869fc540d2b29cce17ddba100f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27911955"
---
# <a name="working-with-intune-in-microsoft-graph"></a>Trabajar con Intune en Microsoft Graph  

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune-pricing) para el servicio Intune.

La API de Microsoft Graph para Intune permite el acceso mediante programación a la información de Intune para su espacio empresarial; la API realiza las mismas operaciones de Intune que las que están disponibles a través de **Azure Portal**.  

Para escenarios de administración (MDM) del dispositivo móvil, la API de Microsoft Graph para Intune admite implementaciones independientes; No se admiten Intune [implementaciones híbridas](https://docs.microsoft.com/en-us/sccm/mdm/understand/choose-between-standalone-intune-and-hybrid-mobile-device-management) . 

## <a name="using-the-microsoft-graph-api-for-intune"></a>Uso de la API de Microsoft Graph para Intune

En Microsoft Graph, Intune proporciona datos de la misma manera igual que otros servicios de nube, con la navegación de información y la relación de entidad enriquecido.Utilizar Microsoft Graph para combinar la información de otros servicios y Intune para crear aplicaciones de servicio de entre completas para profesionales de TI o los usuarios finales.     

En el ejemplo siguiente se muestra cómo se puede saber si una aplicación está instalada en el dispositivo del usuario: 

1. Obtenga de Azure Active Directory una lista de dispositivos registrados para un usuario: 

    https://graph.microsoft.com/beta/users/{user}/ownedDevices 

2. A continuación, vea la lista de aplicaciones de su espacio empresarial: 

    https://graph.microsoft.com/beta/deviceAppManagement/mobileApps  

3. Tome el identificador de la aplicación y determine el estado de instalación para la aplicación (y, por tanto, el usuario):

    https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{id}/deviceStatuses/


## <a name="using-microsoft-graph-permissions"></a>Uso de permisos de Microsoft Graph

Gráfico de Microsof controla el acceso a recursos a través de los permisos. Como desarrollador, debe especificar los permisos que necesita tener acceso a recursos de Intune. Normalmente, especifique los permisos en el portal de Azure Active Directory. Para obtener más información, vea [referencia de permisos de Microsoft Graph](https://docs.microsoft.com/en-us/graph/permissions-reference).

## <a name="next-steps"></a>Pasos siguientes

- Obtenga información sobre [cómo usar Azure AD](https://docs.microsoft.com/en-us/intune/intune-graph-apis) para obtener acceso a la API de Microsoft Graph para Intune.  
- Explore los [ejemplos de PowerShell Intune](https://github.com/microsoftgraph/powershell-intune-samples), que muestran cómo usar la API de Microsoft Graph para Intune en contexto de ejemplos de trabajo.

