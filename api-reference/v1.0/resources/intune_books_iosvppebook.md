# <a name="iosvppebook-resource-type"></a>Tipo de recurso iosVppEBook

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una clase que contiene las propiedades del libro electrónico de VPP de iOS.

Hereda de [managedEBook](../resources/intune_books_managedebook.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar iosVppEBooks](../api/intune_books_iosvppebook_list.md)|Colección [iosVppEBook](../resources/intune_books_iosvppebook.md)|Enumere las propiedades y las relaciones de los objetos [iosVppEBook](../resources/intune_books_iosvppebook.md).|
|[Obtener iosVppEBook](../api/intune_books_iosvppebook_get.md)|[iosVppEBook](../resources/intune_books_iosvppebook.md)|Lea las propiedades y las relaciones del objeto [iosVppEBook](../resources/intune_books_iosvppebook.md).|
|[Crear iosVppEBook](../api/intune_books_iosvppebook_create.md)|[iosVppEBook](../resources/intune_books_iosvppebook.md)|Cree un objeto [iosVppEBook](../resources/intune_books_iosvppebook.md).|
|[Eliminar iosVppEBook](../api/intune_books_iosvppebook_delete.md)|Ninguna|Elimina un [iosVppEBook](../resources/intune_books_iosvppebook.md).|
|[Actualizar iosVppEBook](../api/intune_books_iosvppebook_update.md)|[iosVppEBook](../resources/intune_books_iosvppebook.md)|Actualice las propiedades de un objeto [iosVppEBook](../resources/intune_books_iosvppebook.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Heredado de [managedEBook](../resources/intune_books_managedebook.md)|
|displayName|String|Nombre del libro electrónico Heredado de [managedEBook](../resources/intune_books_managedebook.md)|
|descripción|String|Descripción. Heredado de [managedEBook](../resources/intune_books_managedebook.md)|
|publicador|String|Publicador. Heredado de [managedEBook](../resources/intune_books_managedebook.md)|
|publishedDateTime|DateTimeOffset|La fecha y la hora en que se publicó el libro electrónico. Heredado de [managedEBook](../resources/intune_books_managedebook.md)|
|largeCover|[mimeContent](../resources/intune_shared_mimecontent.md)|Cubierta de libro. Heredado de [managedEBook](../resources/intune_books_managedebook.md)|
|createdDateTime|DateTimeOffset|La fecha y la hora en que se creó el archivo del libro electrónico. Heredado de [managedEBook](../resources/intune_books_managedebook.md)|
|lastModifiedDateTime|DateTimeOffset|La fecha y la hora en que se modificó por última vez el libro electrónico. Heredado de [managedEBook](../resources/intune_books_managedebook.md)|
|informationUrl|Cadena|La dirección URL para obtener más información. Heredado de [managedEBook](../resources/intune_books_managedebook.md)|
|privacyInformationUrl|Cadena|La dirección URL de la declaración de privacidad. Heredado de [managedEBook](../resources/intune_books_managedebook.md)|
|vppTokenId|Guid|El Id. de token de VPP.|
|appleId|String|El ID de Apple asociado a un token de VPP.|
|vppOrganizationName|String|El nombre de la organización del token de VPP.|
|géneros|Colección string|Géneros.|
|language|String|Idioma.|
|vendedor|String|Vendedor.|
|totalLicenseCount|Int32|Número total de licencias.|
|usedLicenseCount|Int32|Número de licencias usadas.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|asignaciones|Colección [managedEBookAssignment](../resources/intune_books_managedebookassignment.md)|La lista de asignaciones para este libro electrónico. Heredado de [managedEBook](../resources/intune_books_managedebook.md)|
|installSummary|[eBookInstallSummary](../resources/intune_books_ebookinstallsummary.md)|Resumen de instalación de las aplicaciones para móviles. Heredado de [managedEBook](../resources/intune_books_managedebook.md)|
|deviceStates|Colección [deviceInstallState](../resources/intune_books_deviceinstallstate.md)|La lista de estados de asignaciones para este libro electrónico. Heredado de [managedEBook](../resources/intune_books_managedebook.md)|
|userStateSummary|Colección [userInstallStateSummary](../resources/intune_books_userinstallstatesummary.md)|La lista de estados de asignaciones para este libro electrónico. Heredado de [managedEBook](../resources/intune_books_managedebook.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.managedEBook",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.iosVppEBook"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.iosVppEBook",
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
  "privacyInformationUrl": "String",
  "vppTokenId": "Guid",
  "appleId": "String",
  "vppOrganizationName": "String",
  "genres": [
    "String"
  ],
  "language": "String",
  "seller": "String",
  "totalLicenseCount": 1024,
  "usedLicenseCount": 1024
}
```








