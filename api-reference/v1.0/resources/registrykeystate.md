# <a name="registrykeystate-resource-type"></a>Tipo de recurso registryKeyState

Contiene información acerca de los cambios clave del registro relacionados con la alerta y el proceso que ha cambiado las claves del registro.

## <a name="properties"></a>Propiedades

| Propiedad     | Tipo        | Descripción |
|:-------------|:------------|:------------|
|colmena|registryHive|Una [colmena del registro de Windows](https://docs.microsoft.com/en-us/windows/desktop/sysinfo/registry-hives): <ul><li>HKEY_CURRENT_CONFIG</li> <li>HKEY_CURRENT_USER</li> <li>HKEY_LOCAL_MACHINE\SAM</li> <li>HKEY_LOCAL_MACHINE\Security</li> <li>HKEY_LOCAL_MACHINE\Software</li> <li>HKEY_LOCAL_MACHINE\System</li> <li>HKEY_USERS\\.Default.</li></ul> Los valores posibles son: `unknown`, `currentConfig`, `currentUser`, `localMachineSam`, `localMachineSamSoftware`, `localMachineSystem`, `usersDefault`.|
|Key|Cadena|Clave de registro actual (es decir, modificada) (excluye la COLMENA).|
|oldKey|Cadena|Clave de registro anterior (es decir, antes de que haya sido cambiada) (excluye la COLMENA).|
|oldValueData|Cadena|Datos de valor (contenidos) de la clave de registro anterior (es decir, antes de que haya sido cambiada).|
|oldValueName|Cadena|Nombre de valor de la clave de registro anterior (es decir, antes de que haya sido cambiada)|
|operación|registryOperation|Operación que ha cambiado el nombre y/ valor de la clave de registro. Los valores posibles son: `unknown`, `create`, `modify` y `delete`.|
|processId|Int32|Identificador del proceso (PID) del proceso que modifica la clave de registro (los detalles del proceso aparecerán en la colección 'procesos' de alerta).|
|valueData|Cadena|Datos de valor (contenidos) de la clave de registro actual (es decir, cambiados).|
|valueName|Cadena|Nombre de valor de la clave de registro actual (es decir, cambiado)|
|valueType|registryValueType|[Tipo del valor de la clave de registro](https://docs.microsoft.com/en-us/windows/desktop/sysinfo/registry-value-types) <ul><li>REG_BINARY</li> <li>REG_DWORD</li> <li>REG_DWORD_LITTLE_ENDIAN</li> <li>REG_DWORD_BIG_ENDIAN</li><li>REG_EXPAND_SZ</li> <li>REG_LINK</li> <li>REG_MULTI_SZ</li> <li>REG_NONE</li> <li>REG_QWORD</li> <li>REG_QWORD_LITTLE_ENDIAN</li> <li>REG_SZ</li></ul> Los valores posibles son: `unknown`, `binary`, `dword`, `dwordLittleEndian`, `dwordBigEndian`, `expandSz`, `link`, `multiSz`, `none`, `qword`, `qwordlittleEndian` y `sz`.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.registryKeyState"
}-->

```json
{
  "hive": "@odata.type: microsoft.graph.registryHive",
  "key": "String",
  "oldKey": "String",
  "oldValueData": "String",
  "oldValueName": "String",
  "operation": "@odata.type: microsoft.graph.registryOperation",
  "processId": 1024,
  "valueData": "String",
  "valueName": "String",
  "valueType": "@odata.type: microsoft.graph.registryValueType"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "registryKeyState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->