# <a name="termsandconditions-resource-type"></a>Tipo de recurso termsAndConditions

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una entidad termsAndConditions representa los contenidos y metadatos de una directiva de Términos y condiciones (TyC) determinada para un grupo específico. El contenido de las directivas de TyC se presenta a los usuarios cuando intentan inscribirse en Intune por primera vez y, después, en las ediciones en que el administrador de un campo exige que se vuelvan a aceptar. Permite que los administradores comuniquen las disposiciones que debe aceptar un usuario para tener los dispositivos inscritos en Intune.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar termsAndConditionses](../api/intune_companyterms_termsandconditions_list.md)|Colección [termsAndConditions](../resources/intune_companyterms_termsandconditions.md)|Enumere las propiedades y las relaciones de los objetos [termsAndConditions](../resources/intune_companyterms_termsandconditions.md).|
|[Obtener termsAndConditions](../api/intune_companyterms_termsandconditions_get.md)|[termsAndConditions](../resources/intune_companyterms_termsandconditions.md)|Lea las propiedades y las relaciones del objeto [termsAndConditions](../resources/intune_companyterms_termsandconditions.md).|
|[Crear termsAndConditions](../api/intune_companyterms_termsandconditions_create.md)|[termsAndConditions](../resources/intune_companyterms_termsandconditions.md)|Cree un objeto [termsAndConditions](../resources/intune_companyterms_termsandconditions.md).|
|[Eliminar termsAndConditions](../api/intune_companyterms_termsandconditions_delete.md)|Ninguno|Elimina un [termsAndConditions](../resources/intune_companyterms_termsandconditions.md).|
|[Actualizar termsAndConditions](../api/intune_companyterms_termsandconditions_update.md)|[termsAndConditions](../resources/intune_companyterms_termsandconditions.md)|Actualice las propiedades de un objeto [termsAndConditions](../resources/intune_companyterms_termsandconditions.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador único de la directiva de TyC.|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto.|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez.|
|displayName|String|Nombre proporcionado por el administrador de la directiva de TyC. |
|description|String|Descripción de la directiva de TyC proporcionada por el administrador.|
|title|String|Título de los términos y condiciones proporcionado por el administrador. Se muestra a los usuarios cuando se les solicita que acepten la directiva de TyC.|
|bodyText|String|Texto de cuerpo de los términos y condiciones proporcionado por el administrador, normalmente los propios términos. Se muestra a los usuarios cuando se les solicita que acepten la directiva de TyC.|
|acceptanceStatement|String|Explicación de los términos y condiciones proporcionada por el administrador, normalmente describe lo que implica aceptar los términos y condiciones de la directiva de TyC. Se muestra a los usuarios cuando se les solicita que acepten la directiva de TyC.|
|version|Int32|Entero que indica la versión actual de los términos. Aumenta cuando un administrador realiza un cambio en los términos y quiere que los usuarios tengan que volver a aceptar la directiva de TyC modificada.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|asignaciones|Colección [termsAndConditionsAssignment](../resources/intune_companyterms_termsandconditionsassignment.md)|La lista de asignaciones para esta directiva de TyC.|
|acceptanceStatuses|Colección [termsAndConditionsAcceptanceStatus](../resources/intune_companyterms_termsandconditionsacceptancestatus.md)|La lista de estados de aceptación para esta directiva de TyC.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.termsAndConditions"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.termsAndConditions",
  "id": "String (identifier)",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "String",
  "description": "String",
  "title": "String",
  "bodyText": "String",
  "acceptanceStatement": "String",
  "version": 1024
}
```



