# <a name="termsandconditionsacceptancestatus-resource-type"></a>Tipo de recurso termsAndConditionsAcceptanceStatus

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una entidad termsAndConditionsAcceptanceStatus representa el estado de aceptación de una directiva de Términos y condiciones (TyC) determinada por un usuario determinado. Los usuarios deben aceptar la versión más actualizada de los términos para conservar el acceso al Portal de empresa.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar termsAndConditionsAcceptanceStatuses](../api/intune_companyterms_termsandconditionsacceptancestatus_list.md)|Colección [termsAndConditionsAcceptanceStatus](../resources/intune_companyterms_termsandconditionsacceptancestatus.md)|Enumere las propiedades y las relaciones de los objetos [termsAndConditionsAcceptanceStatus](../resources/intune_companyterms_termsandconditionsacceptancestatus.md).|
|[Obtener termsAndConditionsAcceptanceStatus](../api/intune_companyterms_termsandconditionsacceptancestatus_get.md)|[termsAndConditionsAcceptanceStatus](../resources/intune_companyterms_termsandconditionsacceptancestatus.md)|Lea las propiedades y las relaciones del objeto [termsAndConditionsAcceptanceStatus](../resources/intune_companyterms_termsandconditionsacceptancestatus.md).|
|[Crear termsAndConditionsAcceptanceStatus](../api/intune_companyterms_termsandconditionsacceptancestatus_create.md)|[termsAndConditionsAcceptanceStatus](../resources/intune_companyterms_termsandconditionsacceptancestatus.md)|Cree un objeto [termsAndConditionsAcceptanceStatus](../resources/intune_companyterms_termsandconditionsacceptancestatus.md).|
|[Eliminar termsAndConditionsAcceptanceStatus](../api/intune_companyterms_termsandconditionsacceptancestatus_delete.md)|Ninguna|Elimina un [termsAndConditionsAcceptanceStatus](../resources/intune_companyterms_termsandconditionsacceptancestatus.md).|
|[Actualizar termsAndConditionsAcceptanceStatus](../api/intune_companyterms_termsandconditionsacceptancestatus_update.md)|[termsAndConditionsAcceptanceStatus](../resources/intune_companyterms_termsandconditionsacceptancestatus.md)|Actualice las propiedades de un objeto [termsAndConditionsAcceptanceStatus](../resources/intune_companyterms_termsandconditionsacceptancestatus.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador único de la entidad.|
|userDisplayName|String|Nombre para mostrar del usuario cuya aceptación representa la entidad.|
|acceptedVersion|Int32|Número de versión más reciente de los TyC aceptados por el usuario.|
|acceptedDateTime|DateTimeOffset|Fecha y hora en la que el usuario aceptó los términos por última vez.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|termsAndConditions|[termsAndConditions](../resources/intune_companyterms_termsandconditions.md)|Vínculo de navegación a los términos y condiciones asignados.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.termsAndConditionsAcceptanceStatus"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.termsAndConditionsAcceptanceStatus",
  "id": "String (identifier)",
  "userDisplayName": "String",
  "acceptedVersion": 1024,
  "acceptedDateTime": "String (timestamp)"
}
```



