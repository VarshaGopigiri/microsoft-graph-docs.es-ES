---
title: tipo de recurso de configuración
description: 'La configuración del usuario actual. '
author: dkershaw10
ms.openlocfilehash: c6a130dc9232114110735ebb0a98b0beeecbf835
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27314500"
---
# <a name="settings-resource-type"></a>tipo de recurso de configuración

La configuración del usuario actual. Para obtener información sobre cómo obtener o actualizar la configuración de usuario, vea [obtener la configuración](../api/user-get-settings.md) y [actualización de la configuración](../api/user-update-settings.md).

Este recurso admite:

- Comprobación de si un usuario y la organización del usuario contribuyen a la detección de contenido.
- Habilitación o deshabilitación de detección de contenido para usuarios específicos. Esto también la deshabilita documentos en Office profundizar.

## <a name="methods"></a>Métodos
| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Obtener configuración de usuario](../api/user-get-settings.md) |[Configuración](../resources/user-settings.md)| Obtener la configuración de usuario y organización. |
|[Actualización de la configuración de usuario](../api/user-update-settings.md) |[Configuración](../resources/user-settings.md)| Actualizar la configuración actual del usuario. |

## <a name="properties"></a>Propiedades

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|contributionToContentDiscoveryDisabled|Boolean|Cuando se establece en true, el acceso de delegado para el usuario [tendencias](/graph/api/resources/insights-trending?view=graph-rest-beta) API está deshabilitada. Cuando se deshabilitan establecido en true, documentos en profundizar de Office del usuario. Cuando se establece en true, la relevancia del contenido que se muestra en Office 365, por ejemplo en los sitios que se sugiere en la página principal de SharePoint y se ve afectada la vista del descubrir en OneDrive para la empresa. Los usuarios pueden controlar esta configuración en [Office profundizar](https://support.office.com/en-us/article/are-my-documents-safe-in-office-delve-f5f409a2-37ed-4452-8f61-681e5e1836f3?ui=en-US&rs=en-US&ad=US#bkmk_optout). |
|contributionToContentDiscoveryAsOrganizationDisabled|Boolean|Refleja la [Configuración del nivel de organización](https://support.office.com/en-us/article/office-delve-for-office-365-admins-54f87a42-15a4-44b4-9df0-d36287d9531b#bkmk_delveonoff) de controlar el acceso de delegado a la [tendencia de](/graph/api/resources/insights-trending?view=graph-rest-beta) API. Cuando establece en true, la organización no tiene acceso a Office profundizar. La relevancia del contenido que se muestra en Office 365, por ejemplo en los sitios que se sugiere en la página principal de SharePoint y la vista de detección en OneDrive para la empresa se ve afectada de toda la organización. Esta configuración es de sólo lectura y sólo se puede cambiar por los administradores en el [Centro de administración de SharePoint](https://support.office.com/article/about-the-office-365-admin-center-758befc4-0888-4009-9f14-0d147402fd23?ui=en-US&rs=en-US&ad=US).|


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

```json
{
  "contributionToContentDiscoveryDisabled": false,
  "contributionToContentDiscoveryAsOrganizationDisabled": false
}

```