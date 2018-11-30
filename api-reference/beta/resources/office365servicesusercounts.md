---
title: tipo de recurso office365ServicesUserCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 975a70b040ac5886ea36219a5407f580a42aeadc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084075"
---
# <a name="office365servicesusercounts-resource-type"></a>tipo de recurso office365ServicesUserCounts

## <a name="properties"></a>Propiedades

| Propiedad                 | Tipo   | Descripción                              |
| :----------------------- | :----- | ---------------------------------------- |
| reportRefreshDate        | Fecha   | La fecha más reciente del contenido.          |
| exchangeActive           | Int64  | El número de usuarios activos en Exchange. Cualquier usuario que puedan leer y enviar correo electrónico se considera un usuario activo. |
| exchangeInactive         | Int64  | El número de usuarios inactivos en Exchange. |
| oneDriveActive           | Int64  | El número de usuarios activos en OneDrive. Cualquier usuario que ve o edita los archivos, archivos compartidos interna o externamente o sincronizado archivos se considera un usuario activo. |
| oneDriveInactive         | Int64  | El número de usuarios inactivos en OneDrive. |
| sharePointActive         | Int64  | El número de usuarios activos de SharePoint. Cualquier usuario que ve o edita los archivos, archivos compartidos internamente o externamente, sincronizado los archivos o las páginas de SharePoint se considera un usuario activo. |
| sharePointInactive       | Int64  | El número de usuarios inactivos en SharePoint. |
| skypeForBusinessActive   | Int64  | El número de usuarios activos en Skype para su negocio. Cualquier usuario que organiza o participaron en conferencias o se unió a las sesiones de punto a punto se considera un usuario activo. |
| skypeForBusinessInactive | Int64  | El número de usuarios inactivos en Skype para su negocio. |
| yammerActive             | Int64  | El número de usuarios activos en Yammer. Cualquier usuario que puede enviar, leer o mensajes se considera un usuario activo. |
| yammerInactive           | Int64  | El número de usuarios inactivos en Yammer.  |
| teamsActive              | Int64  | El número de usuarios activos en los equipos. Cualquier usuario que mensajes expuestos en los canales de equipo, los mensajes enviados en las sesiones de chat privado o participaron en las reuniones o las llamadas se considera un usuario activo. |
| teamsInactive            | Int64  | El número de usuarios activos en los equipos.     |
| reportPeriod             | String | El número de días que cubre el informe.    |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.office365ServicesUserCounts"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "exchangeActive": 1024, 
  "exchangeInactive": 1024, 
  "oneDriveActive": 1024, 
  "oneDriveInactive": 1024, 
  "sharePointActive": 1024, 
  "sharePointInactive": 1024, 
  "skypeForBusinessActive": 1024, 
  "skypeForBusinessInactive": 1024, 
  "yammerActive": 1024, 
  "yammerInactive": 1024, 
  "teamsActive": 1024, 
  "teamsInactive": 1024, 
  "reportPeriod": "String"
}
```
