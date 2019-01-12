---
title: Tipo de recurso device
description: Representa un dispositivo registrado en la organización. Los dispositivos se crean en la nube con el servicio de registro de dispositivos o Intune. Las directivas de acceso condicional los usan para la autenticación multifactor. Estos dispositivos pueden ir desde equipos portátiles y de escritorio hasta teléfonos y tabletas. Se hereda de directoryObject.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: ab03eed26f5e34c2ac149815b3ba66b37fc2090c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27985000"
---
# <a name="device-resource-type"></a>Tipo de recurso device

Representa un dispositivo registrado en la organización. Los dispositivos se crean en la nube con el servicio de registro de dispositivos o Intune. Las directivas de acceso condicional los usan para la autenticación multifactor. Estos dispositivos pueden ir desde equipos portátiles y de escritorio hasta teléfonos y tabletas. Se hereda de [directoryObject](directoryobject.md).

Este recurso le permite agregar sus propios datos a las propiedades personalizadas mediante [extensiones](/graph/extensibility-overview).


## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Obtener dispositivo](../api/device-get.md) | [device](device.md) |Lea las propiedades y relaciones de un objeto device.|
|[Enumerar dispositivos](../api/device-list.md) | Colección [device](device.md)| Recupere una lista de dispositivos registrados en el directorio. |
|[Actualizar dispositivo](../api/device-update.md) | [device](device.md) |Actualice las propiedades de un objeto device. |
|[Eliminar dispositivo](../api/device-delete.md) | Ninguno |Elimine un objeto device. |
|[Enumerar memberOf](../api/device-list-memberof.md) |Colección [directoryObject](directoryobject.md)| Los grupos que el dispositivo es miembro directo de la lista. |
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
|accountEnabled|Booleano| **true** si la cuenta está habilitada; en caso contrario, **false**. Necesario.|
|alternativeSecurityIds|Colección alternativeSecurityId| Solo para uso interno. No admite valores NULL. |
|approximateLastSignInDateTime|DateTimeOffset| El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'` Solo lectura. |
|deviceId|string| Identificador único establecido por el servicio de registro de dispositivos de Azure en el momento del registro. |
|deviceMetadata|String| Solo para uso interno. Establecido en NULL. |
|deviceVersion|Int32| Solo para uso interno. |
|displayName|String|El nombre para mostrar del dispositivo. Necesario. |
|id|String|El identificador único del dispositivo. Hereda de [directoryObject](directoryobject.md). Clave, no admite valores NULL. Solo lectura.|
|isCompliant|Boolean|**true** si el dispositivo cumple con las directivas de administración de dispositivos móviles (MDM); en caso contrario, **false**. Solo lectura. Esto sólo se pueden actualizar por Intune para cualquier tipo de sistema operativo del dispositivo o por un [aprobado MDM aplicación](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) para dispositivos de sistema operativo Windows.|
|isManaged|Boolean|**true** si una aplicación de administración de dispositivos móviles (MDM) administra el dispositivo; en caso contrario, **false**. Esto sólo se pueden actualizar por Intune para cualquier tipo de sistema operativo del dispositivo o por un [aprobado MDM aplicación](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) para dispositivos de sistema operativo Windows. |
|onPremisesLastSyncDateTime|DateTimeOffset|La última hora en que se ha sincronizado el objeto con el directorio local. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'` Solo lectura.|
|onPremisesSyncEnabled|Booleano|**true** si este objeto está sincronizado desde un directorio local; **false** si este objeto se ha sincronizado originalmente desde un directorio local, pero ya no está sincronizado; **null** si este objeto no se ha sincronizado nunca desde un directorio local (valor predeterminado). Solo lectura. |
|operatingSystem|String| El tipo de sistema operativo del dispositivo. Necesario. |
|operatingSystemVersion|String|La versión del sistema operativo del dispositivo. Necesario. |
|physicalIds|Colección string| Solo para uso interno. No admite valores NULL. |
|trustType|String| Tipo de confianza del dispositivo que se ha unido. Solo lectura. Valores posibles: <br />**Área de trabajo**: indica *dispositivos personales BYOD*.<br />**AzureAd**: dispositivos unidos solo a la nube.<br />**ServerAd**: dispositivos unidos al dominio local que se han unido a Azure AD. Para más información, vea [Introducción a la administración de dispositivos en Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/device-management-introduction). |

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|extensions|Colección [Extension](extension.md)|La colección de extensiones abiertas definidas para el dispositivo. Solo lectura. Admite valores NULL.|
|memberOf|Colección [directoryObject](directoryobject.md)|Grupos a los que pertenece este grupo. Métodos HTTP: GET (compatible con todos los grupos). Solo lectura. Admite valores NULL.|
|registeredOwners|Colección [directoryObject](directoryobject.md)|Usuario que ha unido el dispositivo a la nube o que ha registrado su dispositivo personal. El propietario registrado se establece en el momento del registro. Actualmente, solo puede haber un propietario. Solo lectura. Admite valores NULL. |
|registeredUsers|Colección [directoryObject](directoryobject.md)|Colección de usuarios registrados del dispositivo. En el caso de los dispositivos unidos a la nube y los dispositivos personales registrados, los usuarios registrados se establecen en el mismo valor que los propietarios registrados en el momento del registro. Solo lectura. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!--{
  "blockType": "resource",
  "openType": true,
  "optionalProperties": [
    "extensions",
    "registeredOwners",
    "registeredUsers"
  ],
  "keyProperty": "id",
  "baseType": "microsoft.graph.directoryObject",
  "@odata.type": "microsoft.graph.device"
}-->

```json
{
  "accountEnabled": true,
  "alternativeSecurityIds": [{"@odata.type": "microsoft.graph.alternativeSecurityId"}],
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
  "trustType": "string"
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
