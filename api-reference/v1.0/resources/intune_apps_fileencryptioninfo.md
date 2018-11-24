# <a name="fileencryptioninfo-resource-type"></a>Tipo de recurso fileEncryptionInfo

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades de la información de cifrado de archivos para la versión de contenido de una aplicación de línea de negocio.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|encryptionKey|Binario|La clave que se usa para cifrar el contenido del archivo.|
|initializationVector|Binario|El vector de inicialización utilizado para el algoritmo de cifrado.|
|mac|Binario|El hash del contenido del archivo cifrado + IV (hash de contenido).|
|macKey|Binario|La clave utilizada para obtener el MAC.|
|profileIdentifier|Cadena|El identificador del perfil.|
|fileDigest|Binario|El resumen de los archivos antes del cifrado.|
|fileDigestAlgorithm|Cadena|El algoritmo del resumen de los archivos.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.fileEncryptionInfo"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.fileEncryptionInfo",
  "encryptionKey": "binary",
  "initializationVector": "binary",
  "mac": "binary",
  "macKey": "binary",
  "profileIdentifier": "String",
  "fileDigest": "binary",
  "fileDigestAlgorithm": "String"
}
```



