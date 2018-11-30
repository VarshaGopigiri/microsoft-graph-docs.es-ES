---
title: Tipo de recurso onenote
description: Punto de entrada para los recursos de OneNote.
ms.openlocfilehash: c1b875b686015df8134103b0793a1e342e7f4b89
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085327"
---
# <a name="onenote-resource-type"></a>Tipo de recurso onenote

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Punto de entrada para los recursos de OneNote.

Todas las llamadas al servicio de OneNote a través de la API de Microsoft Graph utilizan esta dirección URL raíz del servicio:

```
https://graph.microsoft.com/{version}/{location}/onenote/ 
```

La ubicación puede ser blocs de notas de usuario en Office 365 o consumidor OneDrive, los blocs de notas de grupo o los blocs de notas de equipo hospedada en el sitio de SharePoint en Office 365. 

**Blocs de notas del usuario** Para obtener acceso a los blocs de notas personales en OneDrive para el cliente o OneDrive para la Empresa, utilice una de las siguientes direcciones URL:

```
https://graph.microsoft.com/{version}/me/onenote/{notebooks | sections | sectionGroups | pages} 
https://graph.microsoft.com/{version}/users/{userPrincipalName}/onenote/{notebooks | sections | sectionGroups | pages} 
https://graph.microsoft.com/{version}/users/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```

**Blocs de notas de grupo** Para obtener acceso a los blocs de notas que pertenecen a un grupo, utilice la siguiente dirección URL raíz de servicio:

```
https://graph.microsoft.com/{version}/groups/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```
**Blocs de notas de sitio de SharePoint** Para obtener acceso a los blocs de notas que pertenecen a un sitio de grupo de SharePoint, use la siguiente dirección URL raíz de servicio:

```
https://graph.microsoft.com/{version}/sites/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```

## <a name="authorization"></a>Autorización

Para obtener información sobre los permisos necesarios para trabajar con las API de OneNote, consulte [Permisos de notas](/graph/permissions-reference#notes-permissions).

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|notebooks|Colección de [notebook](notebook.md)|Colección de blocs de notas de OneNote que son propiedad del usuario o grupo. Solo lectura. Admite valores NULL.|
|operations|Colección de [operations](onenoteoperation.md) |El estado de las operaciones de OneNote. No se admite la obtención de una colección de operaciones, pero puede obtener el estado de las operaciones de larga duración si el encabezado `Operation-Location` se devuelve en la respuesta. Solo lectura. Admite valores NULL.|
|pages|Colección de [page](page.md)|Páginas de todos los blocs de notas de OneNote que son propiedad del usuario o grupo.  Solo lectura. Admite valores NULL.|
|resources|Colección de [resources](resource.md) |Imagen y otros recursos de archivo en páginas de OneNote. No se admite la obtención de una colección de recursos, pero puede [obtener el contenido binario de un determinado recurso](resource.md). Solo lectura. Admite valores NULL.|
|sectionGroups|Colección [SectionGroup](sectiongroup.md)|Grupos de secciones de todos los blocs de notas de OneNote que son propiedad del usuario o grupo.  Solo lectura. Admite valores NULL.|
|sections|Colección de [secciones](section.md)|Secciones de todos los blocs de notas de OneNote que son propiedad del usuario o grupo.  Solo lectura. Admite valores NULL.|

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Crear bloc de notas](../api/onenote-post-notebooks.md) |[Notebook](notebook.md)| Crear un bloc de notas mediante su publicación en la colección de blocs de notas.|
|[Enumerar los blocs de notas](../api/onenote-list-notebooks.md) |Colección de [notebook](notebook.md)| Obtener una colección de blocs de notas.|
|[Crear página](../api/onenote-post-pages.md) |[Page](page.md)| Crear una página mediante su publicación en la colección de páginas.|
|[Enumerar páginas](../api/onenote-list-pages.md) |Colección de [page](page.md)| Obtener una colección de páginas.|
|[Enumerar grupos de sección](../api/onenote-list-sectiongroups.md) |Colección de [SectionGroup](sectiongroup.md)| Obtener una colección de grupos de secciones.|
|[Enumerar secciones](../api/onenote-list-sections.md) |Colección de [secciones](section.md)| Obtener una colección de secciones.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onenote resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
