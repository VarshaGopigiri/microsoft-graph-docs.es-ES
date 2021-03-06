---
title: Tipo de recurso device
description: Representa un dispositivo registrado en el directorio. Los dispositivos se crean en la nube con el servicio de registro de dispositivos o Intune. Las directivas de acceso condicional los usan para la autenticación multifactor. Estos dispositivos pueden ir desde equipos portátiles y de escritorio hasta teléfonos y tabletas. Se hereda de directoryObject.
localization_priority: Normal
ms.openlocfilehash: c39e466d6cf0e1dff3b62ff9acbb2123cafceb0c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27821675"
---
# <a name="device-resource-type"></a>Tipo de recurso device

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa un dispositivo registrado en el directorio. Los dispositivos se crean en la nube con el servicio de registro de dispositivos o Intune. Las directivas de acceso condicional los usan para la autenticación multifactor. Estos dispositivos pueden ir desde equipos portátiles y de escritorio hasta teléfonos y tabletas. Se hereda de [directoryObject](directoryobject.md).

Este recurso le permite agregar sus propios datos a las propiedades personalizadas mediante [extensiones](/graph/extensibility-overview).

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Obtener dispositivo](../api/device-get.md) | [device](device.md) |Leer las propiedades y las relaciones de objeto de dispositivo.|
|[Enumerar dispositivos](../api/device-list.md) | Colección [device](device.md)| Recupere una lista de dispositivos registrados en el directorio. |
|[Actualizar dispositivo](../api/device-update.md) | [device](device.md)  |Actualizar las propiedades del objeto de dispositivo. |
|[Eliminar dispositivo](../api/device-delete.md) | Ninguno |Eliminar el objeto de dispositivo. |
|[Enumerar memberOf](../api/device-list-memberof.md) |Colección [directoryObject](directoryobject.md)| Los grupos que el dispositivo es miembro directo de la lista. |
|[Miembro de lista transitiva](../api/device-list-transitivememberof.md) |Colección [directoryObject](directoryobject.md)| Incluya los grupos que el dispositivo es un miembro de. Esta operación es transitiva. |
|[Enumerar registeredOwners](../api/device-list-registeredowners.md) |Colección [directoryObject](directoryobject.md)| Obtenga los usuarios que son propietarios registrados del dispositivo de la propiedad de navegación registeredOwners.|
|[Enumerar registeredUsers](../api/device-list-registeredusers.md) |Colección [directoryObject](directoryobject.md)| Obtenga los usuarios registrados del dispositivo de la propiedad de navegación registeredUsers.|
|**Extensiones abiertas**| | |
|[Crear extensión abierta](../api/opentypeextension-post-opentypeextension.md) |[openTypeExtension](opentypeextension.md)| Crea una extensión abierta y agrega propiedades personalizadas en una instancia nueva o un recurso existente.|
|[Obtener extensión abierta](../api/opentypeextension-get.md) |Colección [openTypeExtension](opentypeextension.md)| Obtiene una extensión abierta identificada por el nombre de extensión.|
|**Extensiones de esquema**| | |
|[Agregar valores de extensión de esquema](/graph/extensibility-schema-groups) || Cree una definición de extensión de esquema y, después, úsela para agregar datos escritos personalizados a un recurso.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|accountEnabled|Booleano| **true** si la cuenta está habilitada; en caso contrario, **false**. valor predeterminado es true.|
|alternativeSecurityIds|Colección alternativeSecurityId| Solo para uso interno. No admite valores NULL. |
|approximateLastSignInDateTime|DateTimeOffset| El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura. |
|deviceId|Guid| Identificador único establecido por el servicio de registro de dispositivos de Azure en el momento del registro. |
|deviceMetadata|String| Solo para uso interno. Establecido en NULL. |
|deviceVersion|Int32| Solo para uso interno. |
|displayName|String| El nombre para mostrar del dispositivo. Necesario. |
|id|String|El identificador único del dispositivo. Hereda de [directoryObject](directoryobject.md). Clave, no admite valores NULL. Solo lectura.|
|isCompliant|Boolean|**true** si el dispositivo cumple con las directivas de administración de dispositivos móviles (MDM); en caso contrario, **false**. Solo lectura. Esto sólo se pueden actualizar por Intune para cualquier tipo de sistema operativo del dispositivo o por un [aprobado MDM aplicación](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) para dispositivos de sistema operativo Windows.|
|isManaged|Boolean|**true** si una aplicación de administración de dispositivos móviles (MDM) administra el dispositivo; en caso contrario, **false**. Esto sólo se pueden actualizar por Intune para cualquier tipo de sistema operativo del dispositivo o por un [aprobado MDM aplicación](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) para dispositivos de sistema operativo Windows. |
|onPremisesLastSyncDateTime|DateTimeOffset|La última hora en que se ha sincronizado el objeto con el directorio local. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'` Solo lectura. |
|onPremisesSyncEnabled|Booleano|**true** si este objeto está sincronizado desde un directorio local; **false** si este objeto se ha sincronizado originalmente desde un directorio local, pero ya no está sincronizado; **null** si este objeto no se ha sincronizado nunca desde un directorio local (valor predeterminado). Solo lectura.|
|operatingSystem|String| El tipo de sistema operativo del dispositivo. Necesario. |
|operatingSystemVersion|String| Versión del sistema operativo del dispositivo. Necesario. |
|physicalIds|Colección String| Solo para uso interno. No admite valores NULL. |
|trustType|String| Tipo de confianza del dispositivo que se ha unido. Solo lectura. Valores posibles: <br />**Área de trabajo**: indica *dispositivos personales BYOD*.<br />**AzureAd**: dispositivos unidos solo a la nube.<br />**ServerAd**: dispositivos unidos al dominio local que se han unido a Azure AD. Para más información, vea [Introducción a la administración de dispositivos en Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/device-management-introduction). |
|Name| Cadena | Nombre descriptivo de un dispositivo. Devuelve sólo si el usuario cierra con una cuenta de Microsoft como parte del proyecto Roma. |
|Estado | Cadena| Dispositivo está en línea o sin conexión. Devuelve sólo si el usuario cierra con una cuenta de Microsoft como parte del proyecto Roma. |
|Plataforma |Cadena|Plataforma de dispositivo. Devuelve sólo si el usuario cierra con una cuenta de Microsoft como parte del proyecto Roma. Devuelve sólo si el usuario cierra con una cuenta de Microsoft como parte del proyecto Roma.|
|Kind| Cadena| Factor de forma de dispositivo. Devuelve sólo si el usuario cierra con una cuenta de Microsoft como parte del proyecto Roma. |
|Model| Cadena| Modelo de dispositivo. Devuelve sólo si el usuario cierra con una cuenta de Microsoft como parte del proyecto Roma. |
|Fabricante| Cadena| Fabricante del dispositivo. Devuelve sólo si el usuario cierra con una cuenta de Microsoft como parte del proyecto Roma. |

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|extensions|Colección [Extension](extension.md)|La colección de extensiones abiertas definidas para el dispositivo. Solo lectura. Admite valores NULL.|
|registeredOwners|Colección [directoryObject](directoryobject.md)| Usuario que ha unido el dispositivo a la nube o que ha registrado su dispositivo personal. El propietario registrado se establece en el momento del registro. Actualmente, solo puede haber un propietario. Solo lectura. Admite valores NULL.|
|registeredUsers|Colección [directoryObject](directoryobject.md)| Colección de usuarios registrados del dispositivo. En el caso de los dispositivos unidos a la nube y los dispositivos personales registrados, los usuarios registrados se establecen en el mismo valor que los propietarios registrados en el momento del registro. Solo lectura. Admite valores NULL.|
|extensions|Colección de [extensiones](extension.md)|La colección de extensiones de open definidas para el dispositivo. Admite valores NULL.|
|registeredOwners|Colección [directoryObject](directoryobject.md)|Usuarios que son propietarios registrados del dispositivo. Solo lectura. Admite valores NULL.|
|registeredUsers|Colección [directoryObject](directoryobject.md)|Usuarios que son usuarios registrados del dispositivo. Solo lectura. Admite valores NULL.|
|comandos | Collection(Microsoft.Graph.Command) | Conjunto de comandos que se envían a este dispositivo|

## <a name="json-representation"></a>Representación JSON

Esta es una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "extensions",
    "registeredOwners",
    "registeredUsers"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.device"
}-->

```json
{
  "accountEnabled": true,
  "approximateLastSignInDateTime": "String (timestamp)",
  "deviceId": "string",
  "deviceMetadata": "string",
  "deviceVersion": 1024,
  "displayName": "string",
  "id": "string (identifier)",
  "isCompliant": true,
  "isManaged": true,
  "onPremisesLastSyncDateTime": "String (timestamp)",
  "onPremisesSyncEnabled": true,
  "operatingSystem": "string",
  "operatingSystemVersion": "string",
  "physicalIds": ["string"],
  "trustType": "string",
  "Name": "string",
  "Status": "string",
  "Platform": "string",
  "Kind": "string",
  "Model": "string",
  "Manufacturer": "string"
}
```

## <a name="see-also"></a>Vea también

- [Agregar datos personalizados a los recursos mediante extensiones](/graph/extensibility-overview)
- [Agregar datos personalizados a los usuarios mediante extensiones abiertas](/graph/extensibility-open-users)
- [Agregar datos personalizados a los grupos mediante extensiones de esquema](/graph/extensibility-schema-groups)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "device resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
