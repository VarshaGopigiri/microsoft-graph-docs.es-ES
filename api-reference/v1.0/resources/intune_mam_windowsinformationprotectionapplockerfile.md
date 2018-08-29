# <a name="windowsinformationprotectionapplockerfile-resource-type"></a>Tipo de recurso windowsInformationProtectionAppLockerFile

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Archivo de bloqueo de aplicaciones de Windows Information Protection
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar windowsInformationProtectionAppLockerFiles](../api/intune_mam_windowsinformationprotectionapplockerfile_list.md)|Colección [windowsInformationProtectionAppLockerFile](../resources/intune_mam_windowsinformationprotectionapplockerfile.md)|Enumere las propiedades y las relaciones de los objetos [windowsInformationProtectionAppLockerFile](../resources/intune_mam_windowsinformationprotectionapplockerfile.md).|
|[Obtener windowsInformationProtectionAppLockerFile](../api/intune_mam_windowsinformationprotectionapplockerfile_get.md)|[windowsInformationProtectionAppLockerFile](../resources/intune_mam_windowsinformationprotectionapplockerfile.md)|Lea las propiedades y las relaciones del objeto [windowsInformationProtectionAppLockerFile](../resources/intune_mam_windowsinformationprotectionapplockerfile.md).|
|[Crear windowsInformationProtectionAppLockerFile](../api/intune_mam_windowsinformationprotectionapplockerfile_create.md)|[windowsInformationProtectionAppLockerFile](../resources/intune_mam_windowsinformationprotectionapplockerfile.md)|Cree un objeto [windowsInformationProtectionAppLockerFile](../resources/intune_mam_windowsinformationprotectionapplockerfile.md).|
|[Eliminar windowsInformationProtectionAppLockerFile](../api/intune_mam_windowsinformationprotectionapplockerfile_delete.md)|Ninguna|Elimina un [windowsInformationProtectionAppLockerFile](../resources/intune_mam_windowsinformationprotectionapplockerfile.md).|
|[Actualizar windowsInformationProtectionAppLockerFile](../api/intune_mam_windowsinformationprotectionapplockerfile_update.md)|[windowsInformationProtectionAppLockerFile](../resources/intune_mam_windowsinformationprotectionapplockerfile.md)|Actualice las propiedades de un objeto [windowsInformationProtectionAppLockerFile](../resources/intune_mam_windowsinformationprotectionapplockerfile.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|String|El nombre descriptivo|
|fileHash|String|Hash del archivo SHA256|
|file|Binario|Archivo como una matriz de bytes|
|id|Cadena|Clave de la entidad.|
|version|String|Versión de la entidad.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.windowsInformationProtectionAppLockerFile"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionAppLockerFile",
  "displayName": "String",
  "fileHash": "String",
  "file": "binary",
  "id": "String (identifier)",
  "version": "String"
}
```



