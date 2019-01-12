---
title: Configuración de los tipos de pestañas integradas en Microsoft Teams
description: Crear o configurar una pestaña de Microsoft Teams mediante las API de Microsoft Graph
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 34db44b1048431f8d1bf0be715e35bcdab6ae80b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27970755"
---
# <a name="configuring-the-built-in-tab-types-in-microsoft-teams"></a>Configuración de los tipos de pestañas integradas en Microsoft Teams

Para [crear](/graph/api/teamstab-add?view=graph-rest-beta) o [configurar](/graph/api/teamstab-update?view=graph-rest-beta) una pestaña de Microsoft Teams mediante las API de Microsoft Graph, necesitará saber el `teamsAppId` de la aplicación y `entityId`, `contentUrl`, `removeUrl` y `websiteUrl` para proporcionarle a ese tipo de aplicación.
En este artículo se explica cómo obtener esos valores para los tipos de pestañas integradas.

## <a name="custom-tabs"></a>Pestañas personalizadas

Para usar Microsoft Graph para configurar una pestaña asociada a un [proveedor de pestañas](https://docs.microsoft.com/es-ES/microsoftteams/platform/concepts/tabs/tabs-overview) que haya escrito, identifique el `entityId`, `contentUrl`, `removeUrl`, y `websiteUrl` que la interfaz de usuario de configuración de la aplicación [ proporciona a Microsoft Teams](https://docs.microsoft.com/en-us/javascript/api/@microsoft/teams-js/microsoftteams.settings.settings?view=msteams-client-js-latest) y coloque los mismos valores de `entityId`, `contentUrl`, `removeUrl` y `websiteUrl` en Microsoft Graph.

El `teamsAppId` es el mismo que el `id` en el [esquema de manifiesto de aplicación para Microsoft Teams](https://docs.microsoft.com/es-ES/microsoftteams/platform/resources/schema/manifest-schema).

## <a name="website-tabs"></a>Pestañas de sitios Web

Para las pestañas de sitios Web, el `teamsAppId` es `com.microsoft.teamspace.tab.web`. La configuración es la siguiente.

| Propiedad   | Tipo        | Descripción                                              |
| ---------- | ----------- | -------------------------------------------------------- |
| entityId   | string      | Null                                                     |
| contentUrl | string      | Dirección URL del sitio web                                       |
| removeUrl  | string      | Null                                                     |
| websiteUrl | string      | Dirección URL del sitio web                                       |

## <a name="planner-tabs"></a>Pestañas de Planner

Para las pestañas de Planner, el teamsAppId es `com.microsoft.teamspace.tab.planner`. La configuración es la siguiente.

| Propiedad   | Tipo        | Descripción                                              |
| ---------- | ----------- | -------------------------------------------------------- |
| entityId   | string      | El ID del plan (el ID para usar con GET /planner/plans/{id}).                                              |
| contentUrl | string      | `https://tasks.office.com/{tenantName}/Home/PlannerFrame?page=7&planId={planId}`, donde {tenantName} es el nombre del inquilino (por ejemplo, example.onmicrosoft.com) y {planId} es el mismo que el ID de la entidad.  |
| removeUrl  | string      | El mismo valor que contentUrl.    |
| websiteUrl | string      | El mismo valor que contentUrl.   |

Para crear un nuevo plan para mostrar en la pestaña de Planner, vea [Crear plannerPlan](/graph/api/planner-post-plans?view=graph-rest-beta).

## <a name="microsoft-stream-tabs"></a>Pestañas de Microsoft Stream

Para las pestañas de Microsoft Stream, el `teamsAppId` es `com.microsoftstream.embed.skypeteamstab`. La configuración es la siguiente.

| Propiedad   | Tipo        | Descripción                                              |
| ---------- | ----------- | -------------------------------------------------------- |
| entityId   | string      | Null                                                     |
| contentUrl | string      | `https://web.microsoftstream.com/embed/video/{id}?autoplay=false&showinfo=true&app=microsoftteams&l={locale}`, donde {id} es el ID de la secuencia de vídeo. Para buscar el {id} de una secuencia, abra la secuencia en el explorador y observe la dirección URL: tendrá el siguiente formato `https://{domain}.microsoftstream.com/video/{id}`.  |
| removeUrl  | string      | Null                                                     |
| websiteUrl | string      | `https://web.microsoftstream.com/video/{id}`, donde {id} es el ID de la secuencia de vídeo.    |

## <a name="microsoft-forms-tabs"></a>Pestañas de Microsoft Forms

Para las pestañas de Microsoft Forms, el `teamsAppId` es `81fef3a6-72aa-4648-a763-de824aeafb7d`.
Configuración:

| Propiedad   | Tipo        | Descripción                                              |
| ---------- | ----------- | -------------------------------------------------------- |
| entityId   | string      | El ID del formulario.  Defina este valor, desplácese hasta el formulario en el sitio Web de Forms y busque la dirección URL del formulario `https://forms.office.com/Pages/DesignPage.aspx#FormId={formId}`.      |
| contentUrl | string      | `https://forms.office.com/Pages/TeamsDesignPage.aspx?Host=Teams&lang={locale}&groupId={groupId}&tid={tid}&teamsTheme={theme}&upn={upn}&fragment=FormId%3D{formId}`, donde {formId} es igual al ID de la entidad y {locale}, {groupId}, {tid}, {upn} son literales.   |
| removeUrl  | string      | Null                                                     |
| websiteUrl | string      |  `https://forms.office.com`    |

## <a name="word-excel-powerpoint-and-pdf-tabs"></a>Pestañas de Word, Excel, PowerPoint y PDF.

En la siguiente tabla se enumeran los `teamsAppId` para cada aplicación.

| App   | teamsAppId | type (extension)                                              |
| ---------- | ----------- | -------------------------------------------------------- |
| Word | `com.microsoft.teamspace.tab.file.staticviewer.word` | `docx` |
| Excel | `com.microsoft.teamspace.tab.file.staticviewer.excel` | `xlsx` |
| PowerPoint  | `com.microsoft.teamspace.tab.file.staticviewer.powerpoint` | `pptx` |
| PDF | `com.microsoft.teamspace.tab.file.staticviewer.pdf` | `pdf` |

Esta configuración no se admite.

## <a name="wiki-tabs"></a>Pestañas de Wiki

Para las pestañas de Wiki, el `teamsAppId` es `com.microsoft.teamspace.tab.wiki`.
Las pestañas de Wiki no admiten la configuración mediante Graph.
Tenga en cuenta que no hay mucho que configurar, en una pestaña de Wiki, el primer usuario solo tiene que hacer clic en **Configurar pestaña** y realizar los cambios necesarios.

## <a name="document-library-tabs"></a>Pestañas de bibliotecas de documentos

Para las pestañas de bibliotecas de documentos, el `teamsAppId` es `com.microsoft.teamspace.tab.files.sharepoint`. Esta configuración no se admite.

## <a name="onenote-tabs"></a>Pestañas de OneNote

Para las pestañas de OneNote, el `teamsAppId` es `0d820ecd-def2-4297-adad-78056cde7c78`. La configuración es la siguiente.

| Propiedad   | Tipo        | Descripción                                              |
| ---------- | ----------- | -------------------------------------------------------- |
| entityId   | string      | `{randomGuid}_{notebookId}`, donde {randomGuid} es el GUID que genere.                                      |
| contentUrl | string      | Una dirección URL del formulario `https://www.onenote.com/teams/TabContent?entityid=%7BentityId%7D&subentityid=%7BsubEntityId%7D&auth_upn=%7Bupn%7D&notebookSource=New&notebookSelfUrl=https%3A%2F%2Fwww.onenote.com%2Fapi%2Fv1.0%2FmyOrganization%2Fgroups%2F{sectionsUrl}%2Fnotes%2Fnotebooks%2F{notebookId}&oneNoteWebUrl={oneNoteWebUrl}&notebookName=note&ui={locale}&tenantId={tid}`, donde `{sectionsUrl}`, `{notebookId}` y `{oneNoteWebUrl}` se encuentran en [GET/groups/{id}/onenote/notebooks](/graph/api/onenote-list-notebooks?view=graph-rest-beta). Las barras diagonales deben ser de escape. {locale} y {tid} son literales. |
| removeUrl  | string      | Una dirección URL del formulario `https://www.onenote.com/teams/TabRemove?entityid=%7BentityId%7D&subentityid=%7BsubEntityId%7D&auth_upn=%7Bupn%7D&notebookSource=New&notebookSelfUrl=https%3A%2F%2Fwww.onenote.com%2Fapi%2Fv1.0%2FmyOrganization%2Fgroups%2F{sectionsUrl}%2Fnotes%2Fnotebooks%2F{notebookId}&oneNoteWebUrl={oneNoteWebUrl}&notebookName=note&ui={locale}&tenantId={tid}`, donde `{sectionsUrl}`, `{notebookId}` y `{oneNoteWebUrl}` se encuentran en [GET/groups/{id}/onenote/notebooks](/graph/api/onenote-list-notebooks?view=graph-rest-beta). Las barras diagonales deben ser de escape. {locale} y {tid} son literales. |
| websiteUrl | string      | Una dirección URL del formulario `https://www.onenote.com/teams/TabRedirect?redirectUrl={oneNoteWebUrl}`, donde `oneNoteWebUrl` se encuentra en [GET/groups/{id}/onenote/notebooks](/graph/api/onenote-list-notebooks?view=graph-rest-beta) |

## <a name="power-bi-tabs"></a>Pestañas de Power BI

Para las pestañas de Power BI, el `teamsAppId` es `com.microsoft.teamspace.tab.powerbi`.
Esta configuración no se admite.

## <a name="sharepoint-page-and-list-tabs"></a>Pestañas de páginas y listas de SharePoint

Para las pestañas de páginas y listas de SharePoint el `teamsAppId` es `2a527703-1f6f-4559-a332-d8a7d288cd88`.
Esta configuración no se admite.
Si se desea configurar los valores, considere usar una pestaña de sitio Web.
