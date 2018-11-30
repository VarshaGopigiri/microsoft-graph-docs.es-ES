---
title: Usar la API de REST de OneNote
description: Microsoft Graph permite a la aplicación obtener autorización para obtener acceso a blocs de notas OneNote de un usuario, en las secciones y páginas en una cuenta personal o la organización. Con la correspondiente delegada o permisos de aplicación, la aplicación pueden tener acceso a los datos de OneNote de cualquier usuario en un inquilino o el usuario ha iniciado sesión.
ms.openlocfilehash: c439e7896eea85e84d567e54aaa57bb5191a70d2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028993"
---
# <a name="use-the-onenote-rest-api"></a>Usar la API de REST de OneNote

Microsoft Graph permite a la aplicación obtener autorización para obtener acceso a blocs de notas OneNote de un usuario, en las secciones y páginas en una cuenta personal o la organización. Con los [permisos adecuados de delegado o de la aplicación](/graph/permissions-reference#notes-permissions), la aplicación puede tener acceso a los datos de OneNote del usuario que ha iniciado sesión o cualquier usuario en un inquilino.

## <a name="root-url"></a>Dirección URL raíz
La dirección URL raíz del servicio OneNote utiliza el siguiente formato para todas las llamadas a la API de OneNote.
```
https://graph.microsoft.com/{version}/{location}/onenote/ 
```
El `version` segmento en la dirección URL representa la versión de Microsoft Graph que va a usar:

- `v1.0` corresponde al código de producción estable.
- `beta` corresponde a la prueba de una característica que se encuentra en desarrollo. Pueden cambiar las características y funcionalidad en el extremo de la versión beta; no se recomienda usarlo en el código de producción.

La ubicación puede ser blocs de notas de usuario en Office 365 o consumidor OneDrive, los blocs de notas de grupo o los blocs de notas de equipo hospedada en el sitio de SharePoint en Office 365. 

![Pila de desarrollo de API de OneNote](https://cdn.graph.office.net/prod/GraphDocuments/en-us/concepts/images/onenote-dev-diagram.png)

### <a name="user-notebooks"></a>Blocs de notas de usuario
Para obtener acceso a blocs de notas personales en consumidor OneDrive o OneDrive para la empresa, utilice una de las siguientes direcciones URL:

```
https://graph.microsoft.com/{version}/me/onenote/{notebooks | sections | sectionGroups | pages} 
https://graph.microsoft.com/{version}/users/{userPrincipalName}/onenote/{notebooks | sections | sectionGroups | pages} 
https://graph.microsoft.com/{version}/users/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```

- `me` corresponde a contenido de OneNote al que el usuario actual tiene acceso (de su propiedad y compartido).
- `users/{id}` corresponde a contenido de OneNote que el usuario especificado (en la dirección URL) ha compartido con el usuario actual. Usar la API de [los usuarios](users.md) .
> **Nota:** Puede obtener los identificadores de usuario mediante la realización de una solicitud GET en `https://graph.microsoft.com/v1.0/users`.

### <a name="group-notebooks"></a>Blocs de notas de grupo
Para obtener acceso a blocs de notas que pertenecen a un grupo, utilice la siguiente dirección URL raíz de servicio:

```
https://graph.microsoft.com/{version}/groups/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```
### <a name="sharepoint-site-notebooks"></a>Blocs de notas del sitio de SharePoint

Para obtener acceso a blocs de notas que pertenecen a un sitio de grupo de SharePoint, use la siguiente dirección URL raíz de servicio:

```
https://graph.microsoft.com/{version}/sites/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```

