---
title: Usar la API de Graph de Intune
description: " No se admiten las implementaciones híbridas de Intune. "
ms.openlocfilehash: 23f6550fca708b64357b7b5132a2a42060cfa4bd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028563"
---
# <a name="working-with-intune-in-microsoft-graph"></a>Trabajar con Intune en Microsoft Graph  

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune-pricing) para el servicio Intune.

La API de Microsoft Graph para Intune permite el acceso mediante programación a la información de Intune para su espacio empresarial; la API realiza las mismas operaciones de Intune que las que están disponibles a través de **Azure Portal**.  

En los escenarios de administración de dispositivos móviles (MDM), la API de Graph para Intune admite implementaciones independientes; no se admiten las [implementaciones híbridas](https://docs.microsoft.com/en-us/sccm/mdm/understand/choose-between-standalone-intune-and-hybrid-mobile-device-management) de Intune. 

## <a name="using-the-intune-graph-api"></a>Usar la API de Graph de Intune

Intune proporciona datos a la API de Microsoft Graph igual que lo hacen otros servicios en la nube, con navegación de relaciones e información sobre entidades enriquecida.Use la API de Microsoft Graph para combinar la información de otros servicios e Intune para crear completas aplicaciones de servicios cruzados para profesionales de TI o usuarios finales.     

Este es un ejemplo de cómo puede determinar si una aplicación está instalada en el dispositivo de un usuario: 

1. Obtenga de Azure Active Directory una lista de dispositivos registrados para un usuario: 

    https://graph.microsoft.com/users/{user}/ownedDevices 

2. A continuación, vea la lista de aplicaciones de su espacio empresarial: 

    https://graph.microsoft.com/deviceAppManagement/mobileApps  

3. Tome el identificador de la aplicación y determine el estado de instalación para la aplicación (y, por tanto, el usuario):

    https://graph.microsoft.com/deviceAppManagement/mobileApps/{id}/deviceStatuses/


## <a name="using-permission-scopes"></a>Usar los ámbitos de permisos

La API de Microsoft Graph controla el acceso a los recursos que usan los ámbitos de permisos. Como desarrollador, debe especificar los ámbitos de permisos que necesita para tener acceso a los recursos de Intune. Normalmente, los ámbitos de permisos se especifican en el portal de Azure Active Directory. Para obtener más información, consulte [Ámbitos de permiso de Microsoft Graph](https://developer.microsoft.com/graph/docs/authorization/permission_scopes) y [Ámbitos de permisos de Intune](https://developer.microsoft.com/graph/docs/authorization/permission_scopes#permission-scopes-in-preview).

## <a name="next-steps"></a>Pasos siguientes

- Obtenga información sobre [cómo usar Azure AD](https://docs.microsoft.com/en-us/intune/intune-graph-apis) para obtener acceso a la API de Microsoft Graph para Intune.  
- Explore los [ejemplos de PowerShell Intune](https://github.com/microsoftgraph/powershell-intune-samples), que muestran cómo usar las API de gráfico para Intune en contexto de ejemplos de trabajo.