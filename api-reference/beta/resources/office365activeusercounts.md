---
title: tipo de recurso office365ActiveUserCounts
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 2eaeccb1fa3b67c6b3e1d2d7c88a1dfad4e40e88
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27959128"
---
# <a name="office365activeusercounts-resource-type"></a>tipo de recurso office365ActiveUserCounts

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo   | Descripción                              |
| :---------------- | :----- | ---------------------------------------- |
| reportRefreshDate | Fecha   | La fecha más reciente del contenido.          |
| office365         | Int64  | El número de usuarios activos en Office 365. Este número incluye todos los usuarios activos en Exchange, OneDrive, SharePoint, Skype para profesionales, Yammer y Microsoft Teams. Puede encontrar la definición de usuario activo para cada producto en la descripción de la propiedad respectivos. |
| Exchange          | Int64  | El número de usuarios activos en Exchange. Cualquier usuario que puedan leer y enviar correo electrónico se considera un usuario activo. |
| oneDrive          | Int64  | El número de usuarios activos en OneDrive. Cualquier usuario que ve o edita los archivos, archivos compartidos interna o externamente o sincronizado archivos se considera un usuario activo. |
| sharePoint        | Int64  | El número de usuarios activos en SharePoint. Cualquier usuario que ve o edita los archivos, archivos compartidos internamente o externamente, sincronizado los archivos o las páginas de SharePoint se considera un usuario activo. |
| skypeForBusiness  | Int64  | El número de usuarios activos en Skype para profesionales. Cualquier usuario que organiza o participaron en conferencias o se unió a las sesiones de punto a punto se considera un usuario activo. |
| yammer            | Int64  | El número de usuarios activos en Yammer. Cualquier usuario que puede enviar, leer o mensajes se considera un usuario activo. |
| equipos             | Int64  | El número de usuarios activos en Microsoft Teams. Cualquier usuario que mensajes expuestos en los canales de equipo, los mensajes enviados en las sesiones de chat privado o participaron en las reuniones o las llamadas se considera un usuario activo. |
| reportDate        | Fecha   | La fecha en la que se activa un número de usuarios. |
| reportPeriod      | Cadena | El número de días que cubre el informe.    |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.office365ActiveUserCounts"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "office365": 1024, 
  "exchange": 1024, 
  "oneDrive": 1024, 
  "sharePoint": 1024, 
  "skypeForBusiness": 1024, 
  "yammer": 1024, 
  "teams": 1024, 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
