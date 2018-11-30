---
title: Usar la API de Graph de Intune
description: " No se admiten las implementaciones híbridas de Intune. "
ms.openlocfilehash: 2502b5209e9935fc923570947c38c0467534f4ef
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087987"
---
# <a name="working-with-intune-in-microsoft-graph"></a>Trabajar con Intune en Microsoft Graph  

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune-pricing) para el servicio Intune.

La API de Microsoft Graph para Intune permite el acceso mediante programación a la información de Intune para su espacio empresarial; la API realiza las mismas operaciones de Intune que las que están disponibles a través de **Azure Portal**.  

En los escenarios de administración de dispositivos móviles (MDM), la API de Graph para Intune admite implementaciones independientes; no se admiten las [implementaciones híbridas](https://docs.microsoft.com/en-us/sccm/mdm/understand/choose-between-standalone-intune-and-hybrid-mobile-device-management) de Intune. 

## <a name="using-the-intune-graph-api"></a>Usar la API de Graph de Intune

En el Microsoft Graph, Intune proporciona datos de la misma manera igual que otros servicios de nube, con la navegación de información y la relación de entidad enriquecido.Utilizar Microsoft Graph para combinar la información de otros servicios y Intune para crear aplicaciones de servicio de entre completas para profesionales de TI o los usuarios finales.     

Este es un ejemplo de cómo puede determinar si una aplicación está instalada en el dispositivo de un usuario: 

1. Obtenga de Azure Active Directory una lista de dispositivos registrados para un usuario: 

    https://graph.microsoft.com/beta/users/{user}/ownedDevices 

2. A continuación, vea la lista de aplicaciones de su espacio empresarial: 

    https://graph.microsoft.com/beta/deviceAppManagement/mobileApps  

3. Tome el identificador de la aplicación y determine el estado de instalación para la aplicación (y, por tanto, el usuario):

    https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{id}/deviceStatuses/


## <a name="using-graph-permission-scopes"></a>Uso de ámbitos de permiso de gráfico

Gráfico de Microsof controla el acceso a los recursos mediante ámbitos de permisos. Como desarrollador, debe especificar los ámbitos de permisos que necesita para tener acceso a los recursos de Intune. Normalmente, los ámbitos de permisos se especifican en el portal de Azure Active Directory. Para obtener más información, consulte [Ámbitos de permiso de Microsoft Graph](https://developer.microsoft.com/graph/docs/authorization/permission_scopes) y [Ámbitos de permisos de Intune](https://developer.microsoft.com/graph/docs/authorization/permission_scopes#permission-scopes-in-preview).

## <a name="to-use-the-table-of-contents-on-the-microsoft-graph-site"></a>Para usar la tabla de contenido en el sitio de Microsoft Graph
  
Puede examinar la tabla de contenido (en el panel izquierdo del sitio) para buscar los elementos de la documentación de API de gráfico Intune y recursos que desea ver.

1. Haga clic en **Referencia de /Beta** para abrir a los documentos de la versión beta.
2. Desplácese hacia abajo y haga clic en **Intune**.
3. Siga haciendo clic en subsecciones debajo **Intune** para los elementos de la API 
