---
title: Trabajar con usuarios en Microsoft Graph
description: Puede usar Microsoft Graph para crear experiencias de aplicaciones convincentes basadas en usuarios, sus relaciones con otros usuarios y grupos y su correo, calendario y archivos.
localization_priority: Priority
author: dkershaw10
ms.prod: microsoft-identity-platform
ms.openlocfilehash: a5e1ed5a2403def740d92b9f77d57a58f6d1a3e6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27912018"
---
# <a name="working-with-users-in-microsoft-graph"></a>Trabajar con usuarios en Microsoft Graph

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Puede usar Microsoft Graph para crear experiencias de aplicaciones convincentes basadas en usuarios, sus relaciones con otros usuarios y grupos y su correo, calendario y archivos.

Puede acceder a los usuarios a través de Microsoft Graph de dos formas:

- Mediante su identificador, `/users/{id}` 
- Mediante el alias `/me` del usuario que ha iniciado sesión, que es el mismo que `/users/{signed-in user's id}`

## <a name="authorization"></a>Authorization
Se requiere uno de los siguientes [permisos](https://developer.microsoft.com/graph/docs/authorization/permission_scopes) para acceder a las operaciones de usuario. Los tres primeros permisos los puede conceder un usuario a una aplicación. El resto solo los puede conceder el administrador a una aplicación.

- User.ReadBasic.All
- User.Read
- User.ReadWrite
- User.Read.All
- User.ReadWrite.All
- Directory.Read.All
- Directory.ReadWrite.All
- Directory.AccessAsUser.All

## <a name="common-properties"></a>Propiedades comunes

| Propiedad | Descripción |
|----------|-------------|
| displayName | El nombre del usuario que aparece en la libreta de direcciones.|
|givenName| El nombre de pila del usuario. |
|surname| El apellido del usuario. |
|mail| La dirección de correo del usuario. |
|photo| Fotografías del perfil del usuario. |

Para obtener información detallada y una lista de todas las propiedades, consulte el objeto [user](user.md).

## <a name="common-operations"></a>Operaciones comunes
>**Nota:** Algunas de estas operaciones requieren permisos adicionales.

| Ruta de acceso    | Descripción |
|---------|-------------|
|[`/users`](../api/user-list.md) | Enumera los usuarios de la organización. |
|[`/users/{id}`](../api/user-get.md) | Obtiene un usuario específico por su identificador. |
|[`/users/{id}/photo/$value`](../api/profilephoto-get.md)| Obtiene la foto de perfil del usuario. |
|[`/users/{id}/manager`](../api/user-list-manager.md) | Obtiene el administrador del usuario. |
|[`/users/{id}/messages`](../api/user-list-messages.md)| Enumera los mensajes de correo electrónico del usuario en su bandeja de entrada principal. |
|[`/users/{id}/events`](../api/user-list-events.md) | Enumera los eventos próximos del usuario en su calendario. |
|[`/users/{id}/drive`](../api/drive-get.md)| Obtiene el almacén de archivos del OneDrive del usuario. |
|[`/users/{id}/memberOf`](../api/user-list-memberof.md)| Enumera los grupos de los que el usuario es miembro. |
|[`/users/{id}/joinedTeams`](../api/user-list-joinedteams.md)| Se enumeran los Teams Microsoft que el usuario es un miembro de. |
