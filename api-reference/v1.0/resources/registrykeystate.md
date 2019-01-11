---
title: tipo de recurso registryKeyState
description: Contiene información acerca de los cambios clave del registro relacionados con la alerta y el proceso que ha cambiado las claves del registro.
localization_priority: Normal
ms.openlocfilehash: 688c690083e24dc6c8ee7229498910befd0fdf3e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27884829"
---
# <a name="registrykeystate-resource-type"></a>tipo de recurso registryKeyState

Contiene información acerca de los cambios clave del registro relacionados con la alerta y el proceso que ha cambiado las claves del registro.

## <a name="properties"></a>Propiedades

| Propiedad     | Tipo        | Description |
|:-------------|:------------|:------------|
|subárbol|registryHive|Un [subárbol del registro de Windows](https://docs.microsoft.com/en-us/windows/desktop/sysinfo/registry-hives) : <ul><li>HKEY_CURRENT_CONFIG</li> <li>HKEY_CURRENT_USER</li> <li>HKEY_LOCAL_MACHINE\SAM</li> <li>HKEY_LOCAL_MACHINE\Security</li> <li>HKEY_LOCAL_MACHINE\Software</li> <li>HKEY_LOCAL_MACHINE\System</li> <li>HKEY_USERS\\. De forma predeterminada.</li></ul> Los valores posibles son: `unknown`, `currentConfig`, `currentUser`, `localMachineSam`, `localMachineSamSoftware`, `localMachineSystem` y `usersDefault`.|
|Key|Cadena|Clave del registro (es decir, modificado) actual (que no sean SUBÁRBOL).|
|oldKey|Cadena|Anterior (es decir, antes de cambiar) clave del registro (excluye SUBÁRBOL).|
|oldValueData|Cadena|Anterior (es decir, antes de cambiar) los datos de valor de la clave del registro (contenido).|
|oldValueName|Cadena|Anterior (es decir, antes de cambiar) nombre del valor de la clave del registro.|
|operación|registryOperation|Operación que ha cambiado el nombre de la clave del registro o valor. Los valores posibles son: `unknown`, `create`, `modify` y `delete`.|
|processId|Int32|Proceso de identificador (PID) del proceso que modifica la clave del registro (proceso detalles aparecerán en la colección de procesos de alerta' ').|
|datosDeValor|Cadena|Datos de valor de la clave de actuales del registro (es decir, modificado) (contenido).|
|Valor|Cadena|Nombre del valor de la clave del registro (es decir, modificado) actual|
|tipo de valor|registryValueType|[Tipo de valor de la clave del registro](https://docs.microsoft.com/en-us/windows/desktop/sysinfo/registry-value-types) <ul><li>REG_BINARY</li> <li>REG_DWORD</li> <li>REG_DWORD_LITTLE_ENDIAN</li> <li>REG_DWORD_BIG_ENDIAN</li><li>REG_EXPAND_SZ</li> <li>REG_LINK</li> <li>REG_MULTI_SZ</li> <li>REG_NONE</li> <li>REG_QWORD</li> <li>REG_QWORD_LITTLE_ENDIAN</li> <li>REG_SZ</li></ul> Los valores posibles son: `unknown`, `binary`, `dword`, `dwordLittleEndian`, `dwordBigEndian`, `expandSz`, `link`, `multiSz`, `none`, `qword`, `qwordlittleEndian` y `sz`.|

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
