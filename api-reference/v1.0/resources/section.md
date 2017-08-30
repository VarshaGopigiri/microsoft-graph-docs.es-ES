# <a name="section-resource-type"></a>Tipo de recurso section

Una sección en un bloc de notas de OneNote. Las secciones pueden contener páginas.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "pages",
    "parentNotebook",
    "parentSectionGroup"
  ],
  "@odata.type": "microsoft.graph.onenoteSection"
}-->

```json
{
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "id": "string (identifier)",
  "isDefault": true,
  "lastModifiedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedDateTime": "String (timestamp)",
  "links": {"@odata.type": "microsoft.graph.sectionLinks"},
  "displayName": "string",
  "pagesUrl": "string",
  "self": "string"
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|createdBy|[identitySet](identityset.md)|Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.|
|createdDateTime|DateTimeOffset|La fecha y la hora en que se creó la sección. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.|
|id|String|El identificador único de la sección.  Solo lectura.|
|isDefault|Booleano|Indica si se trata de la sección predeterminada del usuario. Solo lectura.|
|lastModifiedBy|[identitySet](identityset.md)|Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.|
|lastModifiedDateTime|DateTimeOffset|La fecha y la hora en que se modificó la sección por última vez. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.|
|vínculos|[SectionLinks](sectionlinks.md)|Vínculos para abrir la sección. El vínculo `oneNoteClientURL` abre la sección en el cliente nativo de OneNote si está instalado. El vínculo `oneNoteWebURL` abre la sección en OneNote Online.|
|displayName|Cadena|Nombre de la sección. |
|pagesUrl|Cadena|El punto de conexión `pages` donde puede obtener información detallada de todas las páginas de la sección. Solo lectura.|
|self|String|El punto de conexión donde puede obtener información detallada sobre la sección. Solo lectura.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|pages|Colección [Page](page.md)|Colección de páginas de la sección.  Solo lectura. Admite valores NULL.|
|parentNotebook|[Notebook](notebook.md)|Bloc de notas que contiene la sección.  Solo lectura.|
|parentSectionGroup|[SectionGroup](sectiongroup.md)|Grupo de secciones que contiene la sección.  Solo lectura.|

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener sección](../api/section_get.md) | [Section](section.md) |Leer las propiedades y las relaciones de la sección.|
|[Crear página](../api/section_post_pages.md) |[Page](page.md)| Crear una página publicándola en la sección especificada de la colección de páginas.|
|[Enumerar páginas](../api/section_list_pages.md) |Colección [Page](page.md)| Obtener una colección de páginas en la sección especificada.|
|[copyToNotebook](../api/section_copytonotebook.md)|Ninguno|Copiar la sección en un bloc de notas específico.|
|[copyToSectionGroup](../api/section_copytosectiongroup.md)|Ninguno|Copiar la sección en un grupo de secciones específico.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onenoteSection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
