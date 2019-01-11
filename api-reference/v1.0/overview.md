---
title: Referencia de la API de REST de Microsoft Graph versión 1.0
description: Bienvenido a la referencia de la API de REST de Microsoft Graph del punto de conexión de la versión 1.0.
localization_priority: Priority
ms.openlocfilehash: 6e0dde56aae7857e9ae042f89ba5eb6b01737efa
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27829079"
---
# <a name="microsoft-graph-rest-api-v10-reference"></a>Referencia de la API de REST de Microsoft Graph versión 1.0

Bienvenido a la referencia de la API de REST de Microsoft Graph del punto de conexión de la versión 1.0.

Los conjuntos de API del punto de conexión de la versión 1.0 (`https://graph.microsoft.com/v1.0`) tienen un estado de disponibilidad general (GA) y han pasado por un proceso riguroso de revisión y comentarios con clientes para satisfacer necesidades prácticas y de producción. Las actualizaciones de las API de este punto de conexión son adicionales por naturaleza y no interfieren con los escenarios de aplicación existentes.

## <a name="common-use-cases"></a>Casos de uso común

El poder de Microsoft Graph está en facilitar la navegación de entidades y relaciones en los diferentes servicios que se exponen en un único punto de conexión de REST de Microsoft Graph.

Varios de estos servicios están diseñados para habilitar escenarios enriquecidos en un entorno de [usuario](./resources/user.md) o [grupo](./resources/group.md).

### <a name="user-centric-use-cases-in-v10"></a>Casos de uso de la versión 1.0 enfocados al usuario

1. [Encuentre el perfil](./api/user-get.md) y la [foto](./resources/profilephoto.md) de una usuaria, Elisa.
2. [Encuentre la información de perfil del administrador de Elisa](./api/user-list-manager.md) y los [Id. de sus subordinados directos](./api/user-list-directreports.md), todo almacenado en Azure Active Directory.
3. [Acceda a archivos de Elisa en OneDrive para la Empresa](./api/driveitem-list-children.md), busque la [identidad](./resources/identityset.md) de la última persona que modificó un [archivo](./resources/driveitem.md) y navegue hasta el perfil de esa persona.
4. [Acceda al calendario de Elisa](./api/calendar-get.md) en Exchange Online y [determine el mejor momento para que se reúna con su equipo](./api/user-findmeetingtimes.md) en las próximas dos semanas.
5. [Suscríbase a](./api/subscription-post-subscriptions.md) al calendario de Elisa y [controle los cambios](./api/event-delta.md) que se realicen en él para informarle a Lisa cuándo pasa más de 80 % de su tiempo en reuniones.
6. [Establezca respuestas automáticas](./api/user-update-mailboxsettings.md#example) cuando Elisa deja la oficina.
7. [Obtenga acceso a las personas más importantes para Elisa](./api/user-list-people.md) en función de relaciones de negocios, colaboraciones y comunicaciones.
8. Obtenga la última proyección de ventas de un [gráfico](./resources/chart.md) en un archivo de Excel de Elisa en OneDrive para la Empresa.
9. [Busque las tareas asignadas a Elisa en Planner](./api/planneruser-list-tasks.md).

### <a name="office-365-group-use-cases-in-v10"></a>Casos de uso de la versión 1.0 enfocados a grupos de Office 365

1. Ejecute un informe en grupos de Office 365 de una organización e identifique el grupo con más [comunicación entre miembros](./api/reportroot-getoffice365groupsactivitycounts.md).
2. [Encuentre los planes de este grupo de Office 365](./api/plannergroup-list-plans.md)y la [asignación de tareas](./resources/plannerassignments.md) en ese plan.
3. [Inicie una nueva conversación](./api/group-post-conversations.md) en el grupo de Office 365 para determinar si los miembros quieren [crear otro grupo](./api/group-post-groups.md) para compartir la carga de trabajo.
4. [Acceda al bloc de notas predeterminado](./api/notebook-get.md) del grupo y [cree una página](./api/section-post-pages.md) para mostrar el resultado de la investigación.

## <a name="other-api-versions"></a>Otras versiones de API

Actualmente hay 2 versiones de las API de REST de Microsoft Graph: la versión 1.0 y la beta.
Si está interesado en las API nuevas o mejoradas que aún estén en estado de vista previa, conlsulte [Referencia de punto de conexión beta de Microsoft Graph](/graph/api/overview?toc=./ref/toc.json&view=graph-rest-beta). Tenga en cuenta que las API en estado de vista previa están sujetas a cambios y podrían interferir en escenarios existentes sin previo aviso. No permita que su producción dependa de API en punto de conexión beta.

Obtenga más información sobre [versiones y compatibilidad](/graph/versioning-and-support).

## <a name="connect-with-us"></a>Comuníquese con nosotros

¿Hay otras API o funciones que le gustaría ver en Microsoft Graph? Publique solicitudes de funciones nuevas en [UserVoice](https://officespdev.uservoice.com/forums/224641-general/filters/new?category_id=101632).

¿Quiere enviar un comentario sobre las API actuales de Microsoft Graph? Comuníquese con nosotros en [Github](https://github.com/microsoftgraph/microsoft-graph-docs/issues).

Para preguntas o ayuda con su código mediante Microsof
