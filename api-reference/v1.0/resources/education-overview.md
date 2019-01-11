---
title: Trabajar con API para el ámbito educativo en Microsoft Graph
description: Las API para el ámbito educativo de Microsoft Graph mejoran los recursos y los datos de Office 365 con la información pertinente para los escenarios de educación, que incluye centros educativos, estudiantes, profesores, clases e inscripciones. Esto hace que resulte fácil compilar soluciones que se integran con recursos educativos.
localization_priority: Priority
ms.openlocfilehash: 8c2131c0806bf17e7241b0a95dc3094c6496505d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27880272"
---
# <a name="working-with-education-apis-in-microsoft-graph"></a>Trabajar con API para el ámbito educativo en Microsoft Graph

Las API para el ámbito educativo de Microsoft Graph mejoran los recursos y los datos de Office 365 con la información pertinente para los escenarios de educación, que incluye centros educativos, estudiantes, profesores, clases e inscripciones. Esto hace que resulte fácil compilar soluciones que se integran con recursos educativos.

Las API para el ámbito educativo incluyen recursos de generación de listados y de tareas que puede usar para interactuar con los servicios de generación de listas de Microsoft Teams. Puede usar estos recursos para administrar un listado de centro educativo.

## <a name="authorization"></a>Autorización

Para llamar a las API para el ámbito educativo de Microsoft Graph, la aplicación tiene que adquirir un token de acceso. Para obtener más información sobre los tokens de acceso, vea [Obtener tokens de acceso para llamar a Microsoft Graph](https://developer.microsoft.com/graph/docs/concepts/auth_overview). La aplicación también necesitará los permisos adecuados. Para obtener más información, vea [Permisos para el ámbito educativo](/graph/permissions-reference#education-permissions). 

### <a name="app-permissions-to-enable-school-it-admins-to-consent"></a>Permisos de aplicación para habilitar a los administradores de TI del centro educativo para dar consentimiento 

Para implementar aplicaciones que se integran con las API para el ámbito educativo de Microsoft Graph, los administradores de TI del centro educativo deben dar primero consentimiento a los permisos que solicita la aplicación. Este consentimiento únicamente hay que darlo una sola vez, a menos que cambien los permisos. Cuando el administrador da el consentimiento, la aplicación se aprovisiona para todos los usuarios del inquilino.

Para mostrar un cuadro de diálogo de consentimiento, use la siguiente llamada a REST.

```
GET https://login.microsoftonline.com/{tenant}/adminconsent?
client_id={clientId}&state=12345&redirect_uri={redirectUrl}
```

|Parámetro|Descripción|
|:--------|:----------|
|Tenant|Identificador de inquilino del centro educativo. Use el identificador completo, que incluye onmicrosoft.com.|
|clientId|Identificador de cliente de la aplicación.|
|redirectUrl|Dirección URL de redireccionamiento de la aplicación|


## <a name="rostering"></a>Generación de listados

Las API de generación de listados permiten extraer datos de un inquilino de Office 365 del centro educativo aprovisionado con [Microsoft School Data Sync](https://sds.microsoft.com/). Estas API ofrecen acceso a información sobre centros educativos, secciones, profesores, alumnos y listados. La API admiten tanto escenarios solo de aplicación (sincronización) como escenarios de aplicación y usuario (interactivos). Las API que admiten escenarios interactivos aplican directivas de RBAC adecuadas a la región según el rol de usuario que llama a la API. Esto proporciona una API coherente y una superficie de directiva mínima, independientemente de la configuración de administración de inquilinos. Además, las API proporcionan también permisos específicos del ámbito educativo para asegurarse de que el usuario correcto tiene acceso a los datos.

Puede usar las API de generación de listados para permitir que un usuario de la aplicación conozca:

- Quién soy
- Clases a las que asisto o que imparto
- Lo que tengo que hacer y cuándo

Las API de generación de listados ofrecen los siguientes recursos claves:

- [educationSchool](educationschool.md): representa el centro educativo.
- [educationClass](educationclass.md): representa una clase en un centro educativo.
- [educationTerm](educationterm.md): representa una parte designada del año académico.
- [educationTeacher](educationteacher.md): representa un usuario con el rol principal de "Profesor".
- [educationStudent](educationstudent.md): representa un usuario con el rol principal de "alumno".

Las API de generación de listados admiten los siguientes escenarios:

- [Mostrar todos los centros educativos](../api/educationroot-list-schools.md) 
- [Mostrar los centros educativos en los que se imparte una clase](../api/educationclass-list-schools.md)
- [Mostrar los centros educativos correspondientes a un usuario](../api/educationuser-list-schools.md)
- [Obtener todas las clases](../api/educationroot-list-classes.md)
- [Obtener las clases de un centro educativo](../api/educationschool-list-classes.md)
- [Mostrar las clases correspondientes a un usuario](../api/educationuser-list-classes.md)
- [Agregar clases a un centro educativo](../api/educationschool-post-classes.md)
- [Obtener los alumnos y profesores de una clase](../api/educationclass-list-members.md)
- [Agregar miembros a una clase](../api/educationclass-post-members.md) 
- [Mostrar los profesores de una clase](../api/educationclass-list-teachers.md)
- [Obtener los usuarios de un centro educativo](../api/educationschool-list-users.md)

<!-- Should you list delete scenarios here as well? -->

## <a name="next-steps"></a>Pasos siguientes
Use las API para el ámbito educativo de Microsoft Graph para compilar soluciones educativas con acceso a listados de centro educativo. Para obtener más información:

- Explore los recursos y los métodos que son más útiles para su escenario.
- Pruebe la API en el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer).

