# <a name="managedebook-resource-type"></a>Tipo de recurso managedEBook

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una clase abstracta que contiene las propiedades base para el libro electrónico Managed.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar managedEBooks](../api/intune_books_managedebook_list.md)|Colección [managedEBook](../resources/intune_books_managedebook.md)|Enumere las propiedades y las relaciones de los objetos [managedEBook](../resources/intune_books_managedebook.md).|
|[Obtener managedEBook](../api/intune_books_managedebook_get.md)|[managedEBook](../resources/intune_books_managedebook.md)|Lea las propiedades y las relaciones del objeto [managedEBook](../resources/intune_books_managedebook.md).|
|[Acción assign](../api/intune_books_managedebook_assign.md)|Ninguna|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|displayName|String|Nombre del libro electrónico|
|descripción|String|Descripción.|
|publicador|String|Publicador.|
|publishedDateTime|DateTimeOffset|La fecha y la hora en que se publicó el libro electrónico.|
|largeCover|[mimeContent](../resources/intune_shared_mimecontent.md)|Cubierta de libro.|
|createdDateTime|DateTimeOffset|La fecha y la hora en que se creó el archivo del libro electrónico.|
|lastModifiedDateTime|DateTimeOffset|La fecha y la hora en que se modificó por última vez el libro electrónico.|
|informationUrl|Cadena|La dirección URL para obtener más información.|
|privacyInformationUrl|Cadena|La dirección URL de la declaración de privacidad.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|asignaciones|Colección [managedEBookAssignment](../resources/intune_books_managedebookassignment.md)|La lista de asignaciones para este libro electrónico.|
|installSummary|[eBookInstallSummary](../resources/intune_books_ebookinstallsummary.md)|Resumen de instalación de las aplicaciones para móviles.|
|deviceStates|Colección [deviceInstallState](../resources/intune_books_deviceinstallstate.md)|La lista de estados de asignaciones para este libro electrónico.|
|userStateSummary|Colección [userInstallStateSummary](../resources/intune_books_userinstallstatesummary.md)|La lista de estados de asignaciones para este libro electrónico.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedEBook"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.managedEBook",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "publisher": "String",
  "publishedDateTime": "String (timestamp)",
  "largeCover": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "String",
    "value": "binary"
  },
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "informationUrl": "String",
  "privacyInformationUrl": "String"
}
```








