# <a name="bitlockerremovabledrivepolicy-resource-type"></a>Tipo de recurso bitLockerRemovableDrivePolicy

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Directivas de unidad extraíble de BitLocker
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|encryptionMethod|[bitLockerEncryptionMethod](../resources/intune_deviceconfig_bitlockerencryptionmethod.md)|Seleccione el método de cifrado para las unidades extraíbles. Los valores posibles son: `aesCbc128`, `aesCbc256`, `xtsAes128`, `xtsAes256`.|
|requireEncryptionForWriteAccess|Booleano|Indica si se bloquea el acceso de escritura a dispositivos configurados en otra organización.  Si requireEncryptionForWriteAccess es false, este valor no se aplica.|
|blockCrossOrganizationWriteAccess|Booleano|Esta configuración de directiva determina si es necesaria la protección BitLocker para que se pueda escribir en las unidades de datos extraíbles en un equipo.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.bitLockerRemovableDrivePolicy"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.bitLockerRemovableDrivePolicy",
  "encryptionMethod": "String",
  "requireEncryptionForWriteAccess": true,
  "blockCrossOrganizationWriteAccess": true
}
```








