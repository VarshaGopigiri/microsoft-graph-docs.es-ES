# <a name="userinstallstatesummary-resource-type"></a>Tipo de recurso userInstallStateSummary

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades del resumen del estado de la instalación para un usuario.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar userInstallStateSummaries](../api/intune_books_userinstallstatesummary_list.md)|Colección [userInstallStateSummary](../resources/intune_books_userinstallstatesummary.md)|Enumere las propiedades y las relaciones de los objetos [userInstallStateSummary](../resources/intune_books_userinstallstatesummary.md).|
|[Obtener userInstallStateSummary](../api/intune_books_userinstallstatesummary_get.md)|[userInstallStateSummary](../resources/intune_books_userinstallstatesummary.md)|Lea las propiedades y las relaciones del objeto [userInstallStateSummary](../resources/intune_books_userinstallstatesummary.md).|
|[Crear userInstallStateSummary](../api/intune_books_userinstallstatesummary_create.md)|[userInstallStateSummary](../resources/intune_books_userinstallstatesummary.md)|Cree un objeto [userInstallStateSummary](../resources/intune_books_userinstallstatesummary.md).|
|[Eliminar userInstallStateSummary](../api/intune_books_userinstallstatesummary_delete.md)|Ninguna|Elimina un [userInstallStateSummary](../resources/intune_books_userinstallstatesummary.md)|
|[Actualizar userInstallStateSummary](../api/intune_books_userinstallstatesummary_update.md)|[userInstallStateSummary](../resources/intune_books_userinstallstatesummary.md)|Actualice las propiedades de un objeto [userInstallStateSummary](../resources/intune_books_userinstallstatesummary.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|userName|String|Nombre de usuario.|
|installedDeviceCount|Int32|Número de dispositivos instalados.|
|failedDeviceCount|Int32|Número de dispositivos erróneos.|
|notInstalledDeviceCount|Int32|Número de dispositivos no instalados.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|deviceStates|Colección [deviceInstallState](../resources/intune_books_deviceinstallstate.md)|El estado de instalación del libro electrónico.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.userInstallStateSummary"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.userInstallStateSummary",
  "id": "String (identifier)",
  "userName": "String",
  "installedDeviceCount": 1024,
  "failedDeviceCount": 1024,
  "notInstalledDeviceCount": 1024
}
```



