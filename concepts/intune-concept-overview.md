---
title: Información general sobre la API de dispositivos y aplicaciones de Intune
description: 'Microsoft Intune ayuda a las empresas a administrar dispositivos y aplicaciones de una organización. Puede usar la API de Intune en Microsoft Graph para administrar dispositivos, aplicaciones e incluso configurar Intune usando las herramientas que prefiera. '
ms.openlocfilehash: fced71d317aa5f2aebfd2c44237ea9087a6be4f6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092896"
---
# <a name="intune-devices-and-apps-api-overview"></a>Información general sobre la API de dispositivos y aplicaciones de Intune

Microsoft Intune ayuda a las empresas a administrar dispositivos y aplicaciones de una organización. Puede usar la API de Intune en Microsoft Graph para administrar dispositivos, aplicaciones e incluso configurar Intune usando las herramientas que prefiera. 

Si es un ISV, también puede usar la API de Intune para administrar a los inquilinos de cliente.

## <a name="why-integrate-with-intune"></a>¿Por qué debería realizar la integración con Intune?

Puede usar la API de Intune en Microsoft Graph para acceder a información de dispositivos y aplicaciones de Intune, administrar dispositivos y aplicaciones, y automatizar Intune.

### <a name="manage-devices"></a>Administrar dispositivos

Puede usar la API de Intune para:

- Definir y aplicar directivas de [cumplimiento de dispositivo](/graph/api/resources/intune-deviceconfig-devicecomplianceactionitem?view=graph-rest-1.0), como la complejidad de la contraseña y su duración, el cifrado, los niveles de protección de amenazas y así sucesivamente.  (Las directivas compatibles varían según el sistema operativo y la versión).
- [Proteger los datos de la compañía](/graph/api/resources/intune-mam-windowsinformationprotectionpolicy?view=graph-rest-1.0), independientemente de si la plataforma del dispositivo es Windows, Mac, Android o iOS.
- Crear e implementar directivas de [configuración de dispositivo](/graph/api/resources/intune-deviceconfig-deviceconfiguration?view=graph-rest-1.0), incluyendo la plataforma del sistema operativo y el control de versiones, la pertenencia a un dominio y la administración de las opciones de configuración.
- Crear e implementar directivas de [control de acceso](/graph/api/resources/intune-onboarding-onpremisesconditionalaccesssettings?view=graph-rest-1.0) a dispositivos, incluyendo descarga restringida, acceso accesorio de red y transferencia de archivos.
- Realizar [acciones remotas](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-1.0), como buscar el dispositivo, cambiar la contraseña y borrar el dispositivo.

### <a name="manage-apps"></a>Administrar aplicaciones 

Puede usar la API de Intune para realizar las siguientes tareas de administración de la aplicación:

- Implementar [aplicaciones en dispositivos](/graph/api/resources/intune-apps-mobileapp?view=graph-rest-1.0) o impedir que se implementen aplicaciones.
- Administrar el acceso a [libros electrónicos](/graph/api/resources/intune-books-ebookinstallsummary?view=graph-rest-1.0) y otros servicios relacionados.
- Definir e implementar opciones de configuración, opciones de protección y directivas de uso de la aplicación.

### <a name="automate-intune"></a>Automatizar Intune

Automatice Intune mediante la API de Intune para:

- Definir y asignar controles de acceso [basados en roles](/graph/api/resources/intune-rbac-conceptual?view=graph-rest-1.0).
- Auditar y crear informes de cumplimiento, uso y acceso.
- Administrar [gastos de telecomunicaciones](/graph/api/resources/intune-tem-conceptual?view=graph-rest-1.0).

## <a name="api-reference"></a>Referencia de la API
¿Busca la referencia de la API para este servicio?

- [API de Intune en Microsoft Graph v1.0](/graph/api/resources/intune-graph-overview?view=graph-rest-1.0)
- [API de Intune en Microsoft Graph beta](/graph/api/resources/intune-graph-overview?view=graph-rest-beta)

## <a name="next-steps"></a>Pasos siguientes

- [Usar Azure AD para obtener acceso a la API de Intune](https://docs.microsoft.com/intune/intune-graph-apis).
- Obtenga información sobre cómo realizar tareas comunes con los [ejemplos de Intune de PowerShell](https://github.com/microsoftgraph/powershell-intune-samples).
- Descubra cómo [Usar la API de REST de Intune](/graph/api/resources/intune-graph-overview?view=graph-rest-1.0).
- Consulte el [registro de cambios](changelog.md) para obtener información sobre las novedades de la API de Intune.
- Explore los [ejemplos](https://developer.microsoft.com/graph/graph/examples) para obtener más ideas sobre cómo usar Microsoft Graph.
