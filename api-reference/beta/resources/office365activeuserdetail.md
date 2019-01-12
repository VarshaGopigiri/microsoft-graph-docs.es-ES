---
title: tipo de recurso office365ActiveUserDetail
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 14c785069868783b1e248b41a5b339c9adb4710a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27929287"
---
# <a name="office365activeuserdetail-resource-type"></a>tipo de recurso office365ActiveUserDetail

## <a name="properties"></a>Propiedades

| Propiedad                          | Tipo              | Descripción                              |
| :-------------------------------- | :---------------- | ---------------------------------------- |
| reportRefreshDate                 | Fecha              | La fecha más reciente del contenido.          |
| userPrincipalName                 | Cadena            | El nombre principal de usuario (UPN) del usuario. El UPN es un nombre de inicio de sesión de estilo de Internet para el usuario según el estándar de Internet RFC 822. Por convención, esto se debe asignar al nombre de correo electrónico del usuario. El formato general es alias@domain, donde el dominio debe estar presente en la colección del inquilino de dominios verificados. Esta propiedad es necesaria cuando se crea un usuario. |
| displayName                       | Cadena            | Nombre del usuario que aparece en la libreta de direcciones. Suele ser la combinación del nombre del usuario, la inicial del segundo nombre y el apellido. Esta propiedad es necesaria al crearse un usuario y no puede borrarse durante las actualizaciones. |
| isDeleted                         | Booleano           | Si este usuario se ha eliminado o suave eliminados. |
| deletedDate                       | Fecha              | La fecha cuando ha pasado con la operación de eliminación. Valor predeterminado es "null" cuando el usuario no se ha eliminado. |
| hasExchangeLicense                | Booleano           | Si el usuario se ha asignado una licencia de Exchange. |
| hasOneDriveLicense                | Booleano           | Si el usuario se ha asignado una licencia de OneDrive. |
| hasSharePointLicense              | Booleano           | Si el usuario se ha asignado una licencia de SharePoint. |
| hasSkypeForBusinessLicense        | Booleano           | Si el usuario se ha asignado una licencia de Skype para profesionales. |
| hasYammerLicense                  | Booleano           | Si el usuario se ha asignado una licencia de Yammer. |
| hasTeamsLicense                   | Booleano           | Si el usuario se ha asignado una licencia de los equipos. |
| exchangeLastActivityDate          | Fecha              | La fecha cuando el usuario por última vez lee o enviar correo electrónico. |
| oneDriveLastActivityDate          | Fecha              | La fecha cuando el usuario por última vez visualizar ni editar los archivos, archivos compartidos interna o externamente o sincronizar los archivos. |
| sharePointLastActivityDate        | Fecha              | La fecha cuando el usuario por última vez visualizar ni editar los archivos, archivos compartidos internamente o externamente, sincronizado archivos o ve las páginas de SharePoint. |
| skypeForBusinessLastActivityDate  | Fecha              | La fecha al usuario por última vez organizados o participaron en conferencias o se unió a las sesiones de punto a punto. |
| yammerLastActivityDate            | Fecha              | La fecha al usuario por última vez registrado, lee o había gustado mensaje. |
| teamsLastActivityDate             | Fecha              | La fecha de usuario por última vez los mensajes en los canales de equipo, los mensajes enviados en las sesiones de chat privado o participaron en las reuniones o las llamadas. |
| exchangeLicenseAssignDate         | Fecha              | La última fecha cuando el usuario se ha asignado una licencia de Exchange. |
| oneDriveLicenseAssignDate         | Fecha              | La última fecha cuando el usuario se ha asignado una licencia de OneDrive. |
| sharePointLicenseAssignDate       | Fecha              | La última fecha cuando el usuario se ha asignado una licencia de SharePoint. |
| skypeForBusinessLicenseAssignDate | Fecha              | La última fecha cuando el usuario se ha asignado una licencia de Skype para profesionales. |
| yammerLicenseAssignDate           | Fecha              | La última fecha cuando el usuario se ha asignado una licencia de Yammer. |
| teamsLicenseAssignDate            | Fecha              | La última fecha cuando el usuario se ha asignado una licencia de los equipos. |
| assignedProducts                  | Colección String | Todos los productos asignados para el usuario.  |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.office365ActiveUserDetail"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "userPrincipalName": "String", 
  "displayName": "String", 
  "isDeleted": true, 
  "deletedDate": "Date", 
  "hasExchangeLicense": true, 
  "hasOneDriveLicense": true, 
  "hasSharePointLicense": true, 
  "hasSkypeForBusinessLicense": true, 
  "hasYammerLicense": true, 
  "hasTeamsLicense": true, 
  "exchangeLastActivityDate": "Date", 
  "oneDriveLastActivityDate": "Date", 
  "sharePointLastActivityDate": "Date", 
  "skypeForBusinessLastActivityDate": "Date", 
  "yammerLastActivityDate": "Date", 
  "teamsLastActivityDate": "Date", 
  "exchangeLicenseAssignDate": "Date", 
  "oneDriveLicenseAssignDate": "Date", 
  "sharePointLicenseAssignDate": "Date", 
  "skypeForBusinessLicenseAssignDate": "Date", 
  "yammerLicenseAssignDate": "Date", 
  "teamsLicenseAssignDate": "Date", 
  "assignedProducts": ["String"]
}
```
