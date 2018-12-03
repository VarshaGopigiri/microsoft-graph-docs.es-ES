---
title: tipo de recurso de directiva
description: 'Representa una directiva de Azure AD. Las directivas son las reglas personalizadas que se pueden aplicar en las aplicaciones, entidades de seguridad de servicio, grupos o que están asignados a toda la organización. Actualmente, sólo está disponible un tipo de directiva:'
ms.openlocfilehash: 05f4539d069c290a410d313102eeb7f87ce7eac2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089800"
---
# <a name="policy-resource-type"></a>tipo de recurso de directiva

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa una directiva de Azure AD. Las directivas son las reglas personalizadas que se pueden aplicar en las aplicaciones, entidades de seguridad de servicio, grupos o que están asignados a toda la organización. Actualmente, sólo está disponible un tipo de directiva:

- Directiva de duración de token - especifica la duración del período de duración de tokens emitidos para las aplicaciones y entidades de seguridad de servicio.

Esta directiva se describe con más detalle a continuación.

## <a name="methods"></a>Métodos
| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
| [Obtener la directiva](../api/policy-get.md) |Directiva|Lee las propiedades y las relaciones del objeto de usuario.|
|[Crear directiva](../api/policy-post.md)|Directiva|Crear un nuevo objeto de directiva.|
|[Directiva de actualización](../api/policy-update.md)|Ninguno|Actualizar el objeto de directiva.|
|[Eliminar directiva](../api/policy-delete.md)|Ninguno|Eliminar el objeto de directiva.|
|[Asignar directiva](../api/policy-assign.md)|Ninguno|Asignar una directiva a una aplicación principal de servicio.|
|[Directivas de lista](../api/policy-list.md)|Colección de directivas|Obtener todos los objetos de directiva de la organización.|
|[Directivas de la lista asignada](../api/policy-list-assigned.md)|Colección de directivas|Obtener todos los objetos de directiva asignados a una aplicación o un servicio de entidad de seguridad.|

### <a name="common-properties"></a>Propiedades comunes
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|definición|String|La versión de la directiva específica de la cadena. Véalo a continuación. Necesario.|
|displayName|String|Un nombre personalizado para la directiva. Obligatorio.|
|IsOrganizationDefault|Booleano|Si establece en true, se activa esta directiva. Puede haber muchas directivas para el mismo tipo de directiva, pero se puede activar sólo uno como el valor predeterminado de la organización. Opcional, valor predeterminado es false.|
|type|String|Especifica el tipo de directiva. Actualmente debe ser "TokenLifetimePolicy". Obligatorio.|

#### <a name="common-relationships"></a>Relaciones comunes
|Relación|Tipo|Descripción|
|:-------------|:-----------|:-----------|
|appliesTo|Colección [directoryObject](../resources/directoryobject.md)|Los principales de servicio, grupos, organización o aplicaciones la directiva se aplica a.|

## <a name="token-lifetime-policy"></a>Directiva de duración de símbolo (token)
Especifica la duración de tokens emitidos para diversos fines. Este tipo de directiva puede ser [asignado](../api/policy-assign.md) a las aplicaciones y entidades de seguridad del servicio. Hay cuatro tipos de tokens se puede configurar cuya duración. Pares de token de acceso y actualización se obtienen durante la autenticación a través de un cliente, mientras que los pares de símbolo (token) de sesión o identificador se obtienen durante la autenticación a través de un explorador.

- **El Token de acceso** contiene información acerca de la identidad y los privilegios asociados con una cuenta de usuario que utiliza los clientes para tener acceso a recursos protegidos como aplicaciones.
- **Actualizar el Token** se obtiene junto con el token de acceso cuando un usuario se autentica con Azure AD a través de un cliente para tener acceso a un recurso protegido. Mientras no se ha revocado o izquierda no usado más el MaxInactiveTime (a continuación), se puede usar para obtener un nuevo par de token de acceso o actualizar cuando expire el token de acceso actual.
- **Identificador de símbolo (token)** se comporta como un token de acceso, pero obtenidos a través del explorador.
- **El Token de sesión** se comporta como un token de actualización, pero obtenidos a través del explorador.

## <a name="properties"></a>Propiedades
Las siguientes propiedades de formulario del objeto JSON que representa una directiva de duración del token. Este objeto JSON debe ser **convertir en una cadena con presupuestos con caracteres de escape** que se insertará en la propiedad directiva común de "definición". A continuación se muestra un ejemplo.

>Nota: Todas las duraciones de tiempo en estas propiedades se especifican en el formato "especifíquelo".

>Nota: Los valores máximos para las propiedades que se indican en "días" están quedando sin el número de días como indica el icono de 1 segundo. Por ejemplo, se especifica el valor máximo de 1 días como "23: 59:59".

| Propiedad     | Tipo   |Descripción| Valor mínimo | Valor máximo | Valor predeterminado|
|:---------------|:--------|:----------|:--------|:--------|:----|
|AccessTokenLifetime|String|Controla cuánto **acceso y los tokens de identificador** se consideran válido.|10 minutos|1 día|1 hora|
|MaxInactiveTime|String|Controla la antigüedad máxima que puede ser un token de actualización antes de que un cliente ya no puede utilizar para recuperar un par de token de acceso y actualización nueva para obtener acceso a un recurso.|10 minutos|90 días|14 días|
|MaxAgeSingleFactor|String|Controles de cuánto un usuario puede seguir a usar tokens de actualización para obtener acceso o actualiza los nuevo pares de símbolo (token) después de la última vez que les autenticado correctamente con solo un factor único. Dado que solo factor se considera menos segura que la autenticación multifactor, se recomienda que esta directiva se establece en un valor igual o menor a la MultiFactorRefreshTokenMaxAge.|10 minutos|hasta revocado|365 días o hasta que revocado|
|MaxAgeMultiFactor|String|Controles de cuánto un usuario puede seguir a usar tokens de actualización para obtener acceso o actualiza los nuevo pares de símbolo (token) después de la última vez que les autenticado correctamente con varios factores.|10 minutos|hasta revocado|365 días o hasta que revocado|
|MaxAgeSessionSingleFactor|String|Controles de cuánto un usuario puede seguir a usar tokens de sesión para obtener nuevos tokens de identificador/sesión después de la última vez que les autenticado correctamente con solo un factor único. Dado que solo factor se considera menos segura que la autenticación multifactor, se recomienda que esta directiva se establece en un valor igual o menor a la MultiFactorSessionTokenMaxAge|10 minutos|hasta revocado|365 o revocado hasta|
|MaxAgeSessionMultiFactor|String|Controles de cuánto un usuario puede seguir a usar tokens de sesión para obtener nuevos tokens de identificador/sesión después de la última vez que les autenticado correctamente con varios factores.|10 minutos|hasta revocado|365 o revocado hasta|
|Version|Integer|Establezca el valor de 1. Obligatorio.|Ninguno|Ninguno|Ninguno|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

```json
{
  "definition":["{\"TokenLifetimePolicy\":{\"Version\":1,\"AccessTokenLifetime\":\"8:00:00\",\"MaxInactiveTime\":\"20:00:00\",}}"],
  "displayName":"Test Policy",
  "isOrganizationDefault":false,
  "type":"TokenLifetimePolicy",
}
```
