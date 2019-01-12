---
title: tipo de recurso office365GroupsActivityDetail
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 2968a3a5459f286e4aac69e2fd606adc1b38e39b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27951827"
---
# <a name="office365groupsactivitydetail-resource-type"></a>tipo de recurso office365GroupsActivityDetail

## <a name="properties"></a>Propiedades

| Propiedad                          | Tipo    | Descripción                              |
| :-------------------------------- | :------ | ---------------------------------------- |
| reportRefreshDate                 | Fecha    | La fecha más reciente del contenido.          |
| groupDisplayName                  | Cadena  | El nombre para mostrar del grupo.           |
| isDeleted                         | Booleano | Si este usuario se ha eliminado o suave eliminados. |
| ownerPrincipalName                | Cadena  | El nombre de entidad de seguridad del propietario de grupo.          |
| lastActivityDate                  | Fecha    | La fecha de última actividad para los siguientes escenarios: grupo de correo electrónico del buzón de correo recibido; usuario ve, edita, compartidos o sincronizados los archivos de biblioteca de documentos de SharePoint; usuario ve las páginas de SharePoint; usuario registrado, lea o había gustado los mensajes en grupos de Yammer. |
| groupType                         | Cadena  | El tipo de grupo. Los valores posibles son: **público** o **privado**. |
| memberCount                       | Int64   | El recuento de miembros de grupo.                  |
| externalMemberCount               | Int64   | El recuento de miembros externos del grupo.         |
| exchangeReceivedEmailCount        | Int64   | El número de correo electrónico que recibió el buzón de correo de grupo. |
| sharePointActiveFileCount         | Int64   | El número de archivos activos en el sitio de grupo de SharePoint. |
| yammerPostedMessageCount          | Int64   | El número de los mensajes enviados a grupos de Yammer. |
| yammerReadMessageCount            | Int64   | El número de mensajes leídos en grupos de Yammer. |
| yammerLikedMessageCount           | Int64   | El número de mensajes en grupos de Yammer. |
| exchangeMailboxTotalItemCount     | Int64   | El número de elementos en el buzón de correo de grupo. |
| exchangeMailboxStorageUsedInBytes | Int64   | El almacenamiento utilizado del buzón de grupo.   |
| sharePointTotalFileCount          | Int64   | El número total de archivos en el sitio de grupo de SharePoint. |
| sharePointSiteStorageUsedInBytes  | Int64   | El almacenamiento usado por el sitio de grupo de SharePoint. |
| reportPeriod                      | Cadena  | El número de días que cubre el informe.    |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.office365GroupsActivityDetail"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "groupDisplayName": "String", 
  "isDeleted": true, 
  "ownerPrincipalName": "String", 
  "lastActivityDate": "Date", 
  "groupType": "String", 
  "memberCount": 1024, 
  "externalMemberCount": 1024, 
  "exchangeReceivedEmailCount": 1024, 
  "sharePointActiveFileCount": 1024, 
  "yammerPostedMessageCount": 1024, 
  "yammerReadMessageCount": 1024, 
  "yammerLikedMessageCount": 1024, 
  "exchangeMailboxTotalItemCount": 1024, 
  "exchangeMailboxStorageUsedInBytes": 1024, 
  "sharePointTotalFileCount": 1024, 
  "sharePointSiteStorageUsedInBytes": 1024, 
  "reportPeriod": "String"
}
```
