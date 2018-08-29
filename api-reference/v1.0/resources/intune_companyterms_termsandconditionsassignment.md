# <a name="termsandconditionsassignment-resource-type"></a>Tipo de recurso termsAndConditionsAssignment

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una entidad termsAndConditionsAssignment representa la asignación de una directiva de Términos y condiciones (TyC) determinada para un grupo específico. Se solicitará a los usuarios del grupo que acepten los términos para inscribir sus dispositivos en Intune.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar termsAndConditionsAssignments](../api/intune_companyterms_termsandconditionsassignment_list.md)|Colección [termsAndConditionsAssignment](../resources/intune_companyterms_termsandconditionsassignment.md)|Enumere las propiedades y las relaciones de los objetos [termsAndConditionsAssignment](../resources/intune_companyterms_termsandconditionsassignment.md).|
|[Obtener termsAndConditionsAssignment](../api/intune_companyterms_termsandconditionsassignment_get.md)|[termsAndConditionsAssignment](../resources/intune_companyterms_termsandconditionsassignment.md)|Lea las propiedades y las relaciones del objeto [termsAndConditionsAssignment](../resources/intune_companyterms_termsandconditionsassignment.md).|
|[Crear termsAndConditionsAssignment](../api/intune_companyterms_termsandconditionsassignment_create.md)|[termsAndConditionsAssignment](../resources/intune_companyterms_termsandconditionsassignment.md)|Cree un objeto [termsAndConditionsAssignment](../resources/intune_companyterms_termsandconditionsassignment.md).|
|[Eliminar termsAndConditionsAssignment](../api/intune_companyterms_termsandconditionsassignment_delete.md)|Ninguna|Elimina un [termsAndConditionsAssignment](../resources/intune_companyterms_termsandconditionsassignment.md)|
|[Actualizar termsAndConditionsAssignment](../api/intune_companyterms_termsandconditionsassignment_update.md)|[termsAndConditionsAssignment](../resources/intune_companyterms_termsandconditionsassignment.md)|Actualice las propiedades de un objeto [termsAndConditionsAssignment](../resources/intune_companyterms_termsandconditionsassignment.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador único de la entidad.|
|target|[deviceAndAppManagementAssignmentTarget](../resources/intune_shared_deviceandappmanagementassignmenttarget.md)|Destino de asignación al que está asignada la directiva de términos y condiciones.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.termsAndConditionsAssignment"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.termsAndConditionsAssignment",
  "id": "String (identifier)",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```



