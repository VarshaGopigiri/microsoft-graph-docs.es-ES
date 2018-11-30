---
title: Trabajar con usuarios en Microsoft Graph
description: Puede usar Microsoft Graph para crear experiencias de aplicaciones convincentes basadas en usuarios, sus relaciones con otros usuarios y grupos y su correo, calendario y archivos.
ms.openlocfilehash: edbf9eb36f3c4d3276b5ddd594b9514e0d8ae15e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030832"
---
# <a name="working-with-users-in-microsoft-graph"></a>Trabajar con usuarios en Microsoft Graph

Puede usar Microsoft Graph para crear experiencias de aplicaciones convincentes basadas en usuarios, sus relaciones con otros usuarios y grupos y su correo, calendario y archivos.

Puede acceder a los [usuarios](user.md) a través de Microsoft Graph de dos formas:

- Mediante su identificador, `/users/{id | userPrincipalName}` 
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

Las siguientes propiedades representan el conjunto predeterminado de propiedades que se devuelven al obtener un usuario o enumerar usuarios. Son un subconjunto de todas las propiedades disponibles. Para obtener más propiedades de usuario, use el parámetro de consulta `$select`. 

|Propiedad |Descripción |
|:----------|:-------------|
|id | El identificador único del usuario.|
|businessPhones | Los números de teléfono del usuario.|
|displayName | El nombre del usuario que aparece en la libreta de direcciones.|
|givenName| El nombre de pila del usuario. |
|jobTitle | El puesto del usuario.|
|mail| La dirección de correo del usuario. |
|mobilePhone | El número de teléfono móvil del usuario.|
|officeLocation | La ubicación de la oficina física del usuario.|
|preferredLanguage | El idioma de preferencia del usuario.|
|surname| El apellido del usuario. |
|userPrincipalName| El nombre principal del usuario. |

<br/>

Para obtener información detallada y una lista de todas las propiedades, consulte el objeto [user](user.md).

## <a name="common-operations"></a>Operaciones comunes

> **Nota:** Algunas de estas operaciones requieren permisos adicionales.

| Ruta de acceso    | Descripción |
|:---------|:-------------|
|[`/users`](../api/user-list.md) | Enumera los usuarios de la organización. |
|[`/users/{id}`](../api/user-get.md) | Obtiene un usuario específico por su identificador. |
|[`/users/{id}/photo/$value`](../api/profilephoto-get.md)| Obtiene la foto de perfil del usuario. |
|[`/users/{id}/manager`](../api/user-list-manager.md) | Obtiene el administrador del usuario. |
|[`/users/{id}/messages`](../api/user-list-messages.md)| Enumera los mensajes de correo electrónico del usuario en su bandeja de entrada principal. |
|[`/users/{id}/events`](../api/user-list-events.md) | Enumera los eventos próximos del usuario en su calendario. |
|[`/users/{id}/drive`](../api/drive-get.md)| Obtiene el almacén de archivos del OneDrive del usuario. |
|[`/users/{id}/memberOf`](../api/user-list-memberof.md)| Enumera los grupos de los que el usuario es miembro. |
