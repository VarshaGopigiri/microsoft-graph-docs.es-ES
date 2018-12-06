---
title: Principales servicios y características de Microsoft Graph
description: 'Microsoft Graph le permite integrarse con los mejores servicios de Office 365, Windows 10 y Enterprise Mobility + Security en Microsoft 365, con el uso de las API de REST y bibliotecas de cliente. Además, ofrece seguridad e inteligencia social que pueden impulsar la productividad, la creatividad y la colaboración en equipo de los usuarios, así como proteger los datos de los usuarios y los recursos de empresa. '
ms.openlocfilehash: 12092b4b36159ae1b1cbd490815b0b00722e5ad8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092803"
---
# <a name="major-services-and-features-in-microsoft-graph"></a>Principales servicios y características de Microsoft Graph

Microsoft Graph le permite integrarse con los mejores servicios de Office 365, Windows 10 y Enterprise Mobility + Security en Microsoft 365, con el uso de las API de REST y bibliotecas de cliente. Además, ofrece seguridad e inteligencia social que pueden impulsar la productividad, la creatividad y la colaboración en equipo de los usuarios, así como proteger los datos de los usuarios y los recursos de empresa. 

## <a name="users-and-groups"></a>Usuarios y grupos

En el centro de Microsoft Graph se encuentran los conceptos de usuario y grupo. 

Un _usuario_ en Microsoft Graph es uno de los millones de usuarios que utilizan los servicios en la nube de Microsoft 365. Es el punto focal cuya identidad se protege y cuyo acceso está bien administrado. Los datos del usuario son lo que impulsa los negocios. Los servicios de Microsoft Graph ponen estos datos a disposición de las empresas en contextos complejos, actualizaciones en tiempo real información exhaustiva, y siempre solo con los permisos adecuados.

Un _grupo_ de Office 365 es la entidad fundamental que permite a los usuarios colaborar. Se integra con otros servicios, lo que permite escenarios más complejos de planificación de tareas, trabajo en equipo, educación, y mucho más. 

|Característica     |Servicios auxiliares  |Descripción |Más información |
|:-----------|:--------------------|:-----------|:----------------|
| Usuarios | Azure AD y la mayoría de los servicios de productividad, colaboración, inteligencia y educación | El usuario es un eje fundamental de Microsoft Graph, en torno al cual muchos servicios de Microsoft Graph generan funcionalidad centrada en el usuario. | [Información general sobre los usuarios en Microsoft Graph](azuread-users-concept-overview.md)|
|Grupos | Azure AD, OneDrive, OneNote, Outlook y Planner | Un grupo de Office 365 proporciona la unidad de colaboración fundamental para que los usuarios compartan conversaciones, archivos, notas, calendarios, planes y mucho más. | [Información general sobre los grupos de Office 365 en Microsoft Graph](office365-groups-concept-overview.md) |

## <a name="connecting-users-data-microsoft-365-services-and-your-apps"></a>Conectar los datos de los usuarios, los servicios de Microsoft 365 y las aplicaciones

A partir de los usuarios y grupos en el centro, Microsoft Graph forma una red de características y servicios de Microsoft 365 que administran, protegen y extraen datos para admitir escenarios muy diversos. Microsoft Graph le permite tener acceso a esta gran cantidad de datos de usuario respetando siempre la autorización debida.

![Microsoft Graph le conecta con los datos de los usuarios](images/microsoft-graph-connects-users-data.png)

### <a name="services-and-features"></a>Características y servicios

Algunos servicios en Microsoft Graph hacen su debut en ella, otros se han conocido como servicios independientes y ahora convergen en Microsoft Graph. Sus conjuntos de API siguen un diseño racionalizado, tal y como se detalla en las [directrices de la API de REST de Microsoft](https://github.com/Microsoft/api-guidelines), y ahora son accesibles a través del único punto de conexión de REST de Microsoft Graph `https://graph.microsoft.com`. En el resto de este artículo se muestran los principales servicios y características por categoría. 


## <a name="identity-and-access-management"></a>Administración de identidad y acceso

|Característica     |Servicios auxiliares  |Descripción |Más información |
|:-----------|:--------------------|:-----------|:----------------|
| Administración de identidad y acceso | Azure AD | Crea y administra recursos de directorio tales como usuarios, grupos y aplicaciones. Administra el acceso a los recursos y los datos. Ofrece a los clientes acceso a los datos de inicio de sesión y de riesgos de la cuenta en Azure AD.| [Información general sobre Administración de identidad y acceso de Azure AD](azuread-identity-access-management-concept-overview.md)  |


## <a name="productivity"></a>Productividad

|Característica     |Servicios auxiliares  |Descripción |Más información |
|:-----------|:--------------------|:-----------|:----------------|
| Calendario | Outlook  | Permite a los usuarios configurar citas y reuniones en la web, dispositivos móviles y de escritorio. Forma parte del centro de comunicación de mensajería de Outlook en Office 365, que también permite a los usuarios gestionar correos electrónicos y contactos. | [Información general sobre el Calendario de Outlook](outlook-calendar-concept-overview.md)  |
| Archivos | OneDrive y SharePoint | Administra y comparte archivos de usuario en OneDrive y SharePoint. | [Información general sobre el almacenamiento de archivos de OneDrive](onedrive-concept-overview.md) |
| Correo | Outlook | Permite a los usuarios comunicarse, organizar mensajes y administrar prioridades en los flujos de trabajo, en la web y en dispositivos móviles y de escritorio. Forma parte del centro de comunicación de Office 365, que también permite a los usuarios administrar contactos y programar reuniones. | [Información general sobre el Correo de Outlook](outlook-mail-concept-overview.md) |
| Notas | OneNote | Permite a los usuarios planear y organizar ideas e información. | [Información general sobre las notas de OneNote](integrate-with-onenote.md) |
| Contactos personales | Outlook | Administrador de contactos en dispositivos móviles, web y de escritorio. Forma parte del centro de comunicación de mensajería de Outlook en Office 365, que también permite a los usuarios gestionar correos electrónicos y programar reuniones.  | [Información general sobre los contactos personales de Outlook](outlook-contacts-concept-overview.md) |
| Libros y gráficos | Excel | Permite a los usuarios usar hojas de cálculo de Excel para realizar cálculos complejos, seguir, analizar y visualizar datos y generar informes profesionales. | [Información general sobre los libros y gráficos de Excel](excel-concept-overview.md) |


## <a name="collaboration"></a>Colaboración

<!-- Want to update links to concept overviews as they are created over time. 
-->
|Característica     |Servicios auxiliares  |Descripción |Más información |
|:-----------|:--------------------|:-----------|:----------------|
| Listas y sitios  | SharePoint | Plataforma basada en web donde usuarios y grupos de Office 365 comparten, organizan, administran y descubren contenido (listas, archivos y notas incluidos). | [Información general sobre el contenido y los sitios de SharePoint](sharepoint-concept-overview.md) | 
|Tareas y planes | Planner | Permite a los usuarios en grupos de Office 365 crear planes, asignar tareas y seguir el progreso. | [Información general sobre los planes y las tareas de Planner](planner-concept-overview.md) |
|Trabajo en equipo |  Microsoft Teams | Centro digital y área de trabajo basada en chats donde los equipos comparten archivos, notas, calendario y planes. | [Información general sobre el trabajo en equipo de Microsoft Teams](teams-concept-overview.md) |


## <a name="social-intelligence-and-analytics"></a>Análisis e inteligencia social

|Característica     |Servicios auxiliares  |Descripción |Más información |
|:-----------|:--------------------|:-----------|:----------------|
| Inteligencia social: contactos | Azure AD, Outlook, SharePoint, etc. | Obtiene información sobre contactos ordenados por su relevancia para el usuario, que viene determinada por las relaciones empresariales y los patrones de comunicación y colaboración del usuario.  | [Inteligencia social en Microsoft Graph](social-intel-concept-overview.md) |
| Inteligencia social: información de documentos (versión preliminar) | Delve, OneDrive, Outlook y SharePoint | Utiliza técnicas avanzadas de análisis y Machine Learning para obtener documentos sobre tendencias en circulación, que hayan sido vistos, modificados o compartidos por un usuario.  | [Inteligencia social en Microsoft Graph](social-intel-concept-overview.md)  |


## <a name="device-management"></a>Administración de dispositivos

|Característica     |Servicios auxiliares  |Descripción |Más información |
|:-----------|:--------------------|:-----------|:----------------|
|Dispositivos y aplicaciones | Intune | Inscribe y configura los dispositivos y administra las aplicaciones móviles de la organización. | [Información general sobre dispositivos y aplicaciones de Intune](intune-concept-overview.md) |


## <a name="security"></a>Seguridad

|Característica     |Servicios auxiliares  |Descripción |Más información |
|:-----------|:--------------------|:-----------|:----------------|
| Integración de la seguridad | Azure AD Identity Protection, Azure Information Protection, Azure Security Center, Microsoft Cloud Application Security, Protección contra amenazas avanzada de Windows Defender y [más](/graph/api/resources/security-api-overview?view=graph-rest-1.0) | Ofrece una puerta de enlace unificada a las acciones y la información de seguridad de Microsoft y los partners del ecosistema. | [Seguridad en Microsoft Graph](security-concept-overview.md) |



## <a name="cross-device-experiences"></a>Experiencias entre dispositivos

|Característica     |Servicios auxiliares  |Descripción |Más información |
|:-----------|:--------------------|:-----------|:----------------|
| Experiencias entre dispositivos | Fuente de actividades, retransmisión de dispositivo | Permite experiencias de aplicaciones que van más allá de un solo dispositivo y, en su lugar, se mueven con el usuario de un dispositivo a otro, independientemente de su tipo y plataforma. | [Información general sobre experiencias entre dispositivos](cross-device-concept-overview.md) |


## <a name="usage-reports"></a>Informes de uso

|Característica     |Servicios auxiliares  |Descripción |Más información |
|:-----------|:--------------------|:-----------|:----------------|
| Informes | Microsoft Teams, OneDrive, Outlook, SharePoint, Skype Empresarial y Yammer | Obtiene información de la actividad y el uso de un servicio auxiliar. | [Información general sobre informes de uso](reportroot-concept-overview.md) |


## <a name="education"></a>Educación

|Característica     |Servicios auxiliares  |Descripción |Más información |
|:-----------|:--------------------|:-----------|:----------------|
| Educación | Azure AD, Education | Ofrece información relevante para escenarios de educación, que incluye información sobre los centros educativos, las clases, los alumnos, los profesores y las tareas. Permite a los ISV crear aplicaciones para la clase que ahorran tiempo a los profesores y promueven la colaboración y el trabajo en equipo.  | [Información general sobre educación](education-concept-overview.md) |


## <a name="business-applications"></a>Aplicaciones empresariales

|Característica     |Servicios auxiliares  |Descripción |Más información |
|:-----------|:--------------------|:-----------|:----------------|
| Reserva de cliente (versión preliminar) | Microsoft Bookings | Se dirige a pequeñas empresas para que sus clientes puedan reservar servicios directamente en la web o en Facebook. Permite a los operadores de empresa administrar las preferencias de los clientes, los servicios y los precios, las listas y los horarios del personal y otra información comercial común. | [Información general sobre la API de Microsoft Bookings](booking-concept-overview.md) |


## <a name="next-steps"></a>Siguientes pasos

<!-- Need to update the destination page titles and URLs as Matt's v-team finalize on the examples and featured scenarios content 
-->

- Vea [ejemplos](https://developer.microsoft.com/graph/examples) de soluciones creativas basadas en servicios de Microsoft Graph que resuelven problemas reales de clientes.
- En la tabla de contenido, busque en **Aprender** para obtener información sobre los servicios y las características que _se_ pueden usar en los escenarios.
- Pruebe una solicitud de ejemplo en el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer).
- Use los [Inicios rápidos](https://developer.microsoft.com/graph/quick-start) para configurar una aplicación de ejemplo lista para ejecutar.
