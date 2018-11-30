---
title: Trabajar con API para el ámbito educativo en Microsoft Graph
description: La formación API en Microsoft Graph mejorar datos con la información que es pertinente para escenarios de educación, incluidas escuelas, a los alumnos, profesores, clases, inscripción y asignaciones y recursos de Office 365. Esto hace que resulte fácil compilar soluciones que se integran con recursos educativos.
ms.openlocfilehash: 610a16af6993397ae9162fb27add97cd6c5af0ed
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090142"
---
# <a name="working-with-education-apis-in-microsoft-graph"></a>Trabajar con API para el ámbito educativo en Microsoft Graph

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

La formación API en Microsoft Graph mejorar datos con la información que es pertinente para escenarios de educación, incluidas escuelas, a los alumnos, profesores, clases, inscripción y asignaciones y recursos de Office 365. Esto hace que resulte fácil compilar soluciones que se integran con recursos educativos.

La formación API incluyen rostering recursos y asignaciones que puede usar para interactuar con los servicios de rostering y asignación en Microsoft Teams. Puede usar estos recursos para administrar una lista de participantes school y automatizar las asignaciones de estudiantes.

## <a name="authorization"></a>Autorización

Para llamar a las API para el ámbito educativo de Microsoft Graph, la aplicación tiene que adquirir un token de acceso. Para obtener más información sobre los tokens de acceso, vea [Obtener tokens de acceso para llamar a Microsoft Graph](https://developer.microsoft.com/graph/docs/concepts/auth_overview). La aplicación también necesitará los permisos adecuados. Para obtener más información, vea [Permisos para el ámbito educativo](/graph/permissions-reference#education-permissions). 

### <a name="app-permissions-to-enable-school-it-admins-to-consent"></a>Permisos de aplicación para habilitar a los administradores de TI del centro educativo para dar consentimiento 

Para implementar aplicaciones que se integran con las API para el ámbito educativo de Microsoft Graph, los administradores de TI del centro educativo deben dar primero consentimiento a los permisos que solicita la aplicación. Este consentimiento únicamente hay que darlo una sola vez, a menos que cambien los permisos. Cuando el administrador da el consentimiento, la aplicación está aprovisionada para todos los usuarios del inquilino.

Para activar un cuadro de diálogo de consentimiento, use la siguiente llamada a REST.

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
- [Obtener todas las clases](../api/educationroot_list_classes.md )
- [Obtener las clases de un centro educativo](../api/educationschool-list-classes.md)
- [Mostrar las clases correspondientes a un usuario](../api/educationuser-list-classes.md)
- [Agregar clases a un centro educativo](../api/educationschool-post-classes.md)
- [Obtener los alumnos y profesores de una clase](../api/educationclass-list-members.md)
- [Agregar miembros a una clase](../api/educationclass-post-members.md) 
- [Mostrar los profesores de una clase](../api/educationclass-list-teachers.md)
- [Obtener los usuarios de un centro educativo](../api/educationschool-list-users.md)

<!-- Should you list delete scenarios here as well? -->

## <a name="assignments"></a>Assignments 

Puede usar la formación relacionados con la asignación de API para integrar con asignaciones en Microsoft Teams. Microsoft Teams en Office 365 para el ámbito educativo se basa en la misma API de formación y proporciona un caso de uso de lo que puede hacer con las API. La aplicación puede usar estas API para interactuar con las asignaciones a lo largo del ciclo de vida de la asignación. 

La asignación de API proporcionan los siguientes recursos claves:

- [educationAssignment](educationassignment.md) - el objeto principal de la API de las asignaciones. Representa una tarea o una unidad de trabajo asignada a un miembro de estudiantes o equipo en una clase como parte de sus estudios.
- [educationSubmission](educationsubmission.md) - representa los recursos que un individuo (o grupo) envía para una asignación y el asociado de remuneración y comentarios para esa asignación.
- [educationResource](educationresource.md) - representa el aprendizaje de objeto que se va a asignar o enviado. Un **educationResource** está asociado con un **educationAssignment** o un **educationSubmission**.

La API de asignación admite los siguientes escenarios:

- [Crear asignación](../api/educationclass-post-assignments.md)
- [Publicación de asignación](../api/educationassignment-publish.md)
- [Crear un recurso de asignación](../api/educationassignment-post-resources.md)
- [Crear un recurso de envío](../api/educationsubmission-post-resources.md)
- [Enviar asignación](../api/educationsubmission-submit.md) 
- [Unsubmit asignación](../api/educationsubmission-unsubmit.md)   
- [Devolver comentarios y calificaciones para estudiantes](../api/educationsubmission-return.md) 
- [Obtener detalles de la asignación](../api/educationuser-list-assignments.md)

Los siguientes son algunos casos de uso común para la formación relacionados con la asignación de API.

|Caso de uso|Descripción|Vea también|
|:-------|:----------|:-------|
|Crear asignaciones|Un sistema externo puede crear una asignación para la clase y adjuntar recursos a la asignación.|[Crear asignación](../api/educationassignment-post-resources.md)|
|Leer la información de asignación|Una aplicación de análisis puede obtener información sobre las asignaciones y los envíos de estudiantes, incluidas las fechas y remuneración.|[Obtener la asignación](../api/educationassignment-get.md)|
|Realizar un seguimiento de los envíos de estudiante|La aplicación puede proporcionar un panel de profesor que muestra cuántos envíos de los alumnos deben ser evaluado.|[Recursos de envío](educationsubmission.md)|

## <a name="school-data-sync-management"></a>Administración de sincronización de datos de School

[Sincronización de datos de School](https://sds.microsoft.com/) ayuda a automatizar el proceso de importación y la sincronización de datos de lista de sistemas de información de estudiantes con Azure Active Directory (AD Azure) y Office 365. Puede usar la API de administración de sincronización de datos de school en Microsoft Graph para configurar la sincronización de un archivo CSV o un conector de SIS API compatible.

Los datos de school sincronización compatibilidad con la API de administración de los siguientes escenarios:

- [Perfiles de sincronización de lista](../api/educationsynchronizationprofile-list.md)
- [Obtener el perfil de sincronización](../api/educationsynchronizationprofile-get.md)
- [Crear perfil de sincronización](../api/educationsynchronizationprofile-post.md)
- [Eliminar el perfil de sincronización](../api/educationsynchronizationprofile-delete.md)
- [Detener una sincronización en curso](../api/educationsynchronizationprofile-pause.md)
- [Reanudar una sincronización en pausa](../api/educationsynchronizationprofile-resume.md)
- [Restablecer una sincronización](../api/educationsynchronizationprofile-reset.md)
- [Iniciar la sincronización para los archivos cargados](../api/educationsynchronizationprofile-start.md) 
- [Obtener una dirección URL de carga](../api/educationsynchronizationprofile-uploadurl.md)
- [Obtener el estado de una sincronización](../api/educationsynchronizationprofilestatus-get.md)
- [Obtener errores de sincronización](../api/educationsynchronizationerrors-get.md)


## <a name="next-steps"></a>Pasos siguientes
Use la API de formación de Microsoft Graph para crear soluciones de educación que tienen acceso a las asignaciones de estudiantes y listas de escuela. Para obtener más información:

- Explore los recursos y los métodos que son más útiles para su escenario.
- Pruebe la API en el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer).

