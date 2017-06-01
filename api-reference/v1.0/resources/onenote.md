# <a name="onenote-resource-type"></a>Tipo de recurso OneNote

Punto de entrada para los recursos de OneNote.

Todas las llamadas al servicio de OneNote a través de la API de Microsoft Graph utilizan esta dirección URL raíz del servicio:

```
https://graph.microsoft.com/{version}/{location}/onenote/ 
```

La ubicación puede ser el bloc de notas del usuario en Office 365 o OneDrive para el cliente, y los blocs de notas de grupo en Office 365. Actualmente no se admiten blocs de notas hospedados por el sitio de SharePoint. 

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

Los siguientes ámbitos de permiso proporcionan niveles de acceso a los blocs de notas de OneNote. Elegir los ámbitos de permiso depende tanto de la ubicación de destino de los blocs de notas como de la funcionalidad de la aplicación. 

**Ámbitos de los blocs de notas personales en OneDrive para el cliente o OneDrive para la Empresa que son propiedad del usuario actual**

| Ámbito | Permiso en Azure Portal | Descripción |
|:-------|:------|:------|
| Notes.Create | Crear blocs de notas de usuario de OneNote | Puede ver las secciones y los títulos de los blocs de notas de OneNote, crear páginas, secciones y blocs de notas nuevos. |
| Notes.Read | Leer blocs de notas de usuario de OneNote | Puede leer los blocs de notas de OneNote. |
| Notes.ReadWrite | Leer y escribir en los blocs de notas de usuario de OneNote | Puede leer, compartir y modificar sus blocs de notas de OneNote. |

**Ámbitos para blocs de notas personales compartidos por otros usuarios y blocs de notas de grupo a los que el usuario actual puede tener acceso**

| Ámbito | Permiso en Azure Portal | Descripción |
|:-------|:------|:------|
| Notes.Read.All | Leer todos los blocs de notas de OneNote a los que el usuario puede tener acceso | Puede leer todos los blocs de notas de OneNote a los que tiene acceso el usuario que ha iniciado sesión. |
| Notes.ReadWrite.All | Leer y escribir todos los blocs de notas de OneNote a los que el usuario puede tener acceso | Puede leer, compartir o modificar todos los blocs de notas de OneNote a los que tiene acceso el usuario que ha iniciado sesión. |

**Nota:** Actualmente no es posible tener acceso a blocs de notas de sitios de SharePoint a través de la API Graph.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "notebooks",
    "pages",
    "resources",
    "sectionGroups",
    "sections"
  ],
  "@odata.type": "microsoft.graph.onenote"
}-->

## <a name="relationships"></a>Relaciones
| Relación | Tipo    |Descripción|
|:---------------|:--------|:----------|
|notebooks|Colección de [blocs de notas](notebook.md)|Colección de blocs de notas de OneNote que son propiedad del usuario o grupo. Solo lectura. Admite valores NULL.|
|operations|Colección de [operaciones](onenoteoperation.md) |El estado de las operaciones de OneNote. No se admite la obtención de una colección de operaciones, pero puede obtener el estado de las operaciones de larga duración si el encabezado `Operation-Location` se devuelve en la respuesta. Solo lectura. Admite valores NULL.|
|pages|Colección de [páginas](page.md)|Páginas de todos los blocs de notas de OneNote que son propiedad del usuario o grupo.  Solo lectura. Admite valores NULL.|
|resources|Colección de [recursos](resource.md) |Imagen y otros recursos de archivo en páginas de OneNote. No se admite la obtención de una colección de recursos, pero puede [obtener el contenido binario de un determinado recurso](resource.md). Solo lectura. Admite valores NULL.|
|sectionGroups|Colección [SectionGroup](sectiongroup.md)|Grupos de secciones de todos los blocs de notas de OneNote que son propiedad del usuario o grupo.  Solo lectura. Admite valores NULL.|
|sections|Colección de [secciones](section.md)|Secciones de todos los blocs de notas de OneNote que son propiedad del usuario o grupo.  Solo lectura. Admite valores NULL.|


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Crear bloc de notas](../api/onenote_post_notebooks.md) |[Bloc de notas](notebook.md)| Crear un bloc de notas mediante su publicación en la colección de blocs de notas.|
|[Enumerar los blocs de notas](../api/onenote_list_notebooks.md) |Colección de [blocs de notas](notebook.md)| Obtener una colección de blocs de notas.|
|[Crear página](../api/onenote_post_pages.md) |[Página](page.md)| Crear una página mediante su publicación en la colección de páginas.|
|[Enumerar páginas](../api/onenote_list_pages.md) |Colección de [páginas](page.md)| Obtener una colección de páginas.|
|[Enumerar grupos de sección](../api/onenote_list_sectiongroups.md) |Colección [SectionGroup](sectiongroup.md)| Obtener una colección de grupos de secciones.|
|[Enumerar secciones](../api/onenote_list_sections.md) |Colección de [secciones](section.md)| Obtener una colección de secciones.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onenote resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
