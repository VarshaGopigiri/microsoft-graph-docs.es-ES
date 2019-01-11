---
title: Usar la API de Graph de Intune
description: " No se admiten las implementaciones híbridas de Intune. "
author: tfitzmac
localization_priority: Priority
ms.openlocfilehash: 1222f064b075c8884f5c66c101ae0e15256221c5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27830684"
---
# <a name="working-with-intune-in-microsoft-graph"></a>Trabajar con Intune en Microsoft Graph  

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune-pricing) para el servicio Intune.

La API de Microsoft Graph para Intune permite el acceso mediante programación a la información de Intune para su espacio empresarial; la API realiza las mismas operaciones de Intune que las que están disponibles a través de **Azure Portal**.  

Para escenarios de administración (MDM) del dispositivo móvil, la API de Microsoft Graph para Intune admite implementaciones independientes; No se admiten Intune [implementaciones híbridas](https://docs.microsoft.com/en-us/sccm/mdm/understand/choose-between-standalone-intune-and-hybrid-mobile-device-management) . 

## <a name="using-the-microsoft-graph-api-for-intune"></a>Uso de la API de Microsoft Graph para Intune

Intune proporciona datos a la API de Microsoft Graph igual que lo hacen otros servicios en la nube, con navegación de relaciones e información sobre entidades enriquecida.Usar la API de gráfico de Microsoft para combinar la información de otros servicios y Intune para crear aplicaciones de servicio de entre completas para profesionales de TI o los usuarios finales.     

En el ejemplo siguiente se muestra cómo se puede saber si una aplicación está instalada en el dispositivo del usuario: 

1. Obtenga de Azure Active Directory una lista de dispositivos registrados para un usuario: 

    https://graph.microsoft.com/users/{user}/ownedDevices 

2. A continuación, vea la lista de aplicaciones de su espacio empresarial: 

    https://graph.microsoft.com/deviceAppManagement/mobileApps  

3. Tome el identificador de la aplicación y determine el estado de instalación para la aplicación (y, por tanto, el usuario):

    https://graph.microsoft.com/deviceAppManagement/mobileApps/{id}/deviceStatuses/


## <a name="using-permissions"></a>Uso de permisos

La API de Microsoft Graph controla el acceso a recursos a través de los permisos. Como desarrollador, debe especificar los permisos que necesita tener acceso a recursos de Intune. Normalmente, especifique los permisos en el portal de Azure Active Directory. Para obtener más información, vea [referencia de permisos de Microsoft Graph](https://docs.microsoft.com/en-us/graph/permissions-reference).

## <a name="next-steps"></a>Pasos siguientes

- Obtenga información sobre [cómo usar Azure AD](https://docs.microsoft.com/en-us/intune/intune-graph-apis) para obtener acceso a la API de Microsoft Graph para Intune.  
- Explore los [ejemplos de PowerShell Intune](https://github.com/microsoftgraph/powershell-intune-samples), que muestran cómo usar la API de Microsoft Graph para Intune en contexto de ejemplos de trabajo.
