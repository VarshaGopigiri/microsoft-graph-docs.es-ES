---
title: Introducción a la API de Microsoft Teams
description: 'Microsoft Teams es el centro definitivo para el trabajo en equipo y las comunicaciones inteligentes. '
author: nkramer
ms.openlocfilehash: 2297f92cb44c8a12512e4e06ffc2392d75626952
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27358859"
---
# <a name="microsoft-teams-api-overview"></a>Introducción a la API de Microsoft Teams

[Microsoft Teams](https://products.office.com/microsoft-teams) es el centro definitivo para el trabajo en equipo y las comunicaciones inteligentes. Basado en la escala y la solidez de [Office 365](https://products.office.com/) con más de 120 millones de usuarios, Microsoft Teams ofrece colaboración basada en chat, reuniones, llamadas y características de telefonía IP empresarial.

## <a name="why-integrate-with-microsoft-teams"></a>¿Por qué integrar con Microsoft Teams?

### <a name="automate-team-lifecycles"></a>Automatizar los ciclos de vida del equipo

Use Microsoft Graph para [ crear un nuevo equipo virtual](/graph/api/team-put-teams?view=graph-rest-1.0) cuando se produzca un nuevo problema empresarial, [agregar a las personas adecuadas](/graph/api/group-post-members?view=graph-rest-1.0) al equipo y configurarlo con [canales](/graph/api/channel-post?view=graph-rest-1.0), [pestañas](/graph/api/teamstab-add?view=graph-rest-1.0) y [aplicaciones](/graph/api/teamsappinstallation-add?view=graph-rest-1.0).
Para reunir al nuevo equipo para discutir sobre el problema empresarial, [agregue un nuevo evento](/graph/api/group-post-events?view=graph-rest-1.0) al calendario de equipo.

![Automatice los ciclos de vida del equipo creando un equipo, agregando a miembros y propietarios, estableciendo la configuración del equipo, agregando canales y pestañas, instalando aplicaciones y archivando o eliminando el equipo cuando llegue el momento de hacerlo.](images/teams-lifecycle.png)

Cuando se solucione el problema empresarial y ya no necesite el equipo, use la API de Microsoft Teams [archivar](/graph/api/team-archive?view=graph-rest-1.0) o [eliminar](/graph/api/group-delete?view=graph-rest-1.0) el equipo.  Si conoce la duración máxima del equipo virtual al crearlo, establezca una [directiva de expiración de grupo de Office 365](https://support.office.com/en-us/article/office-365-group-expiration-policy-8d253fe5-0e09-4b3c-8b5e-f48def064733?ui=en-US&rs=en-US&ad=US) para el equipo para eliminarlo automáticamente de acuerdo con la fecha de la directiva.

### <a name="get-work-done-even-when-no-one-is-around"></a>Trabajar incluso cuando nadie esté disponible

Usar [permisos de aplicación](permissions-reference.md) para trabajar con [equipos](/graph/api/resources/team?view=graph-rest-1.0), [canales](/graph/api/resources/channel?view=graph-rest-1.0) y [pestañas](/graph/api/resources/teamstab?view=graph-rest-1.0) sin necesidad de intervención humana. Crear un nuevo canal cuando el cliente haga un pedido.
Crear equipos para los distintos cursos al principio del año escolar y archivarlos automáticamente al final.

### <a name="create-teams-linked-to-your-app"></a>Crear equipos vinculados a la aplicación

Permitir a los clientes crear nuevos [equipos](/graph/api/resources/team?view=graph-rest-1.0) y [canales](/graph/api/resources/channel?view=graph-rest-1.0). 
[Instalar](/graph/api/teamsappinstallation-add?view=graph-rest-1.0) la [Aplicación Teams](https://docs.microsoft.com/es-ES/microsoftteams/platform/#pivot=home&panel=home-all) en los nuevos equipos. 
[Anclar la aplicación a una pestaña](/graph/api/teamstab-add?view=graph-rest-1.0) en el nuevo canal. 
[Enviar mensajes](/graph/api/channel-post-chatthreads?view=graph-rest-beta) al canal vinculado a su sitio web.

### <a name="create-and-manage-multiple-teams-and-channels"></a>Crear y administrar varios equipos y canales

Con Microsoft Graph resulta más fácil crear grandes cantidades de equipos y rellenarlos con usuarios y canales, al crear y administrar de forma automática [equipos](/graph/api/resources/team?view=graph-rest-1.0), [canales](/graph/api/resources/channel?view=graph-rest-1.0), [pestañas](/graph/api/resources/teamstab?view=graph-rest-1.0) y [aplicaciones](/graph/api/resources/teamsapp?view=graph-rest-1.0).
Microsoft Graph también le permite [buscar](teams-list-all-teams.md) y [archivar](/graph/api/team-archive?view=graph-rest-1.0) los equipos que ya no usa. Esta es la misma API en la que se basan el [Centro de administración de Microsoft Teams](https://docs.microsoft.com/es-ES/microsoftteams/enable-features-office-365) y los [cmdlets de PowerShell de los equipos](https://docs.microsoft.com/es-ES/microsoftteams/teams-powershell-overview).

### <a name="deploy-apps-to-teams"></a>Implementar aplicaciones en los equipos

[Enumerar los equipos de su inquilino](teams-list-all-teams.md) e [instalarles aplicaciones](/graph/api/teamsappinstallation-add?view=graph-rest-1.0). 
[Crear pestañas](/graph/api/teamstab-add?view=graph-rest-1.0) en los canales para que los usuarios tengan acceso rápido a las aplicaciones.

### <a name="use-microsoft-graph-in-any-kind-of-app"></a>Usar Microsoft Graph en cualquier tipo de aplicación

Las aplicaciones de Microsoft Teams ofrecen a los grupos de trabajo una nueva herramienta para conseguir que la colaboración sea una experiencia más productiva e interesante. Con estas aplicaciones, los usuarios de grupos de trabajo pueden compartir activos, interactuar en el chat y programar eventos en el calendario de equipo. Estas aplicaciones también pueden automatizar la creación de equipos, canales y las conversaciones, mejorando así el valor de Microsoft Teams.

Puede crear sitios web, servicios y aplicaciones nativas de plataforma que se ejecutan fuera de la experiencia del usuario de Microsoft Teams y llamar a la API de Teams para automatizar escenarios de equipos.

**Tipos de aplicaciones habilitadas para Microsoft Teams**

![Llamar a la API de Microsoft Teams desde pestañas, bots, sitios web y servicios](images/teamsappendpoints.png)

Entre estas herramientas de colaboración, se incluyen las aplicaciones de bots o pestañas habilitadas para Microsoft Graph que se ejecutan dentro de las aplicaciones de Microsoft Teams. También puede realizar llamadas a Microsoft Graph desde fuera de una aplicación de Microsoft Teams (por ejemplo, desde un sitio web o un servicio web). Si ya habilitó su sitio web para Microsoft Graph, puede usar ese trabajo para Microsoft Teams con la [plataforma para desarrolladores de Microsoft Teams](https://docs.microsoft.com/es-ES/microsoftteams/platform/#pivot=home&panel=home-all) para [crear una pestaña](https://docs.microsoft.com/es-ES/microsoftteams/platform/concepts/tabs/tabs-overview) que use el código del sitio web existente.

Las API de Microsoft Teams pueden mejorar las aplicaciones dentro y fuera de Teams:

|Tipo de aplicación|Descripción del escenario|
|:-------|:-------------------|
| [Pestañas](https://docs.microsoft.com/es-ES/microsoftteams/platform/concepts/tabs/tabs-overview) |Muestran el contenido en Microsoft Teams.|
| [Bots](https://docs.microsoft.com/es-ES/microsoftteams/platform/concepts/bots/bots-overview) |Ayudan a los usuarios a completar tareas en conversaciones.|
| [Conectores](https://docs.microsoft.com/es-ES/microsoftteams/platform/concepts/connectors/connectors) |Publican actualizaciones de servicios externos a canales.|
| [Mensajes que requieren acción](https://docs.microsoft.com/es-ES/microsoftteams/platform/concepts/cards/cards) |Agregan interacción mejorada a las tarjetas del conector.|
| [Extensiones de mensajería](https://docs.microsoft.com/es-ES/microsoftteams/platform/concepts/messaging-extensions) |Permiten a los usuarios consultar y compartir información en conversaciones.|
|Sitios web| Muestran contenido mejorado en las páginas web.|
|Servicios|Mejoran las aplicaciones de cliente con datos de Microsoft Graph mediante el servicio web.|
| [Fuente de actividades](https://docs.microsoft.com/es-ES/microsoftteams/platform/concepts/activity-feed)|Permite interactuar con los usuarios con notificaciones de fuentes.|
| [Llamadas y reuniones en línea (versión preliminar)](/graph/api/resources/calls-api-overview?view=graph-rest-beta) |Crean aplicaciones de Microsoft Teams con bots que pueden iniciar y participar en las llamadas de audio y vídeo, enrutar o transferir llamadas en función de los flujos de respuestas de voz interactivas (IVR) y participar en reuniones en línea.|

## <a name="api-reference"></a>Referencia de la API

¿Busca la referencia de la API para este servicio?

Consulte [API de Teams en Microsoft Graph](/graph/api/resources/teams-api-overview?view=graph-rest-1.0). 

## <a name="next-steps"></a>Pasos siguientes

- Vea el [vídeo de presentación](http://aka.ms/teamsgraph/v1/video).
- Obtenga información sobre cómo [usar la API de Microsoft Teams](/graph/api/resources/teams-api-overview?view=graph-rest-1.0).
- Explore en profundidad los métodos, propiedades y relaciones de los recursos de [equipo](/graph/api/resources/team?view=graph-rest-1.0), [canal](/graph/api/resources/channel?view=graph-rest-1.0) y [grupo](/graph/api/resources/group?view=graph-rest-1.0).
- Pruebe la API en el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer).
- Obtenga más información sobre el [modelo de programación de Microsoft Teams](https://docs.microsoft.com/es-ES/microsoftteams/platform/concepts/concepts-overview).
- Explorar las [API de llamadas y reuniones en línea](/graph/api/resources/calls-api-overview?view=graph-rest-beta).
- Póngase en marcha con código de ejemplo: [Aerolíneas Contoso](https://github.com/microsoftgraph/contoso-airlines-teams-sample), [ C# miniejemplos](https://github.com/microsoftgraph/csharp-teams-sample-graph)
