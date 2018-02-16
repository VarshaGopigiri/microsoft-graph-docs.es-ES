# <a name="deviceappmanagement-resource-type"></a>Tipo de recurso deviceAppManagement

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Entidad singleton que actúa como un contenedor para todas las funcionalidades de administración de aplicaciones de dispositivos.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener deviceAppManagement](../api/intune_books_deviceappmanagement_get.md)|[deviceAppManagement](../resources/intune_books_deviceappmanagement.md)|Lea las propiedades y las relaciones del objeto [deviceAppManagement](../resources/intune_books_deviceappmanagement.md).|
|[Actualizar deviceAppManagement](../api/intune_books_deviceappmanagement_update.md)|[deviceAppManagement](../resources/intune_books_deviceappmanagement.md)|Actualice las propiedades de un objeto [deviceAppManagement](../resources/intune_books_deviceappmanagement.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|Clave de la entidad.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|managedEBooks|Colección [managedEBook](../resources/intune_books_managedebook.md)|El libro electrónico Managed.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceAppManagement"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceAppManagement",
  "id": "String (identifier)"
}
```



