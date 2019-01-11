---
title: tipo de recurso identityProvider
description: Representa un proveedor de identidad de Azure Active Directory (AD Azure). El proveedor de identidad puede ser Microsoft, Google, Facebook, Amazon o LinkedIn.
localization_priority: Normal
ms.openlocfilehash: 0a465b1c7b4ad7f74e6357e77da3692d64294e7e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27858544"
---
# <a name="identityprovider-resource-type"></a>tipo de recurso identityProvider

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa un proveedor de identidad de Azure Active Directory (AD Azure). El proveedor de identidad puede ser Microsoft, Google, Facebook, Amazon o LinkedIn.

Configuración de un proveedor de identidad en el inquilino de Azure AD B2C permite:

* A los usuarios registrarse e iniciar sesión con una cuenta de social en una aplicación de consumidor. Por ejemplo, una aplicación puede utilizar Azure AD B2C para permitir a los usuarios para registrarse y obtener el servicio con una cuenta de Facebook.
* Cuenta a los usuarios vincular a un local existente a una cuenta de social en una aplicación de consumidor. Por ejemplo, un usuario ha creado un nombre de usuario y una contraseña (cuenta local) en la aplicación. El usuario decide más adelante vincular la cuenta local existente a su cuenta de Facebook, por lo que puede iniciar sesión con Facebook.

Configuración de un proveedor de identidad en el inquilino de Azure AD permite escenarios de invitado B2B futuros. Por ejemplo, una organización tiene recursos en Office 365 que deban ser compartidos con un usuario de Gmail. El usuario de Gmail usará sus credenciales de cuenta de Google para autenticar y obtener acceso a los documentos.

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Obtener identityProvider](../api/identityprovider-get.md) |identityProvider|Leer las propiedades de un identityProvider existente.|
|[Crear identityProvider](../api/identityprovider-post-identityproviders.md)|identityProvider|Crear un nuevo identityProvider.|
|[Actualizar identityProvider](../api/identityprovider-update.md)|Ninguno|Actualizar un identityProvider existente.|
|[Eliminar identityProvider](../api/identityprovider-delete.md)|Ninguno|Eliminar un identityProvider existente.|
|[Lista identityProviders](../api/identityprovider-list.md)|colección de identityProvider|Lista de todos los identityProviders configurados en un inquilino.|

## <a name="properties"></a>Propiedades

|Propiedad|Tipo|Obligatorio|Nullable|Descripción|
|:---------------|:--------|:--------|:--------|:----------|
|clientId|Cadena|Sí|No|El identificador de cliente para la aplicación. Este es el identificador de cliente que se obtuvieron cuando se registra la aplicación con el proveedor de identidad.|
|clientSecret|Cadena|Sí|No|El secreto de cliente para la aplicación. Este es el secreto de cliente que se obtuvieron cuando se registra la aplicación con el proveedor de identidad. Esto es de sólo escritura. Una operación de lectura devolverá "\*\*\*\*".|
|id|Cadena|No|No|El identificador del proveedor de identidad.|
|name|Cadena|No|No|El nombre para mostrar del proveedor de identidad.|
|type|Cadena|Sí|No|El tipo de proveedor de identidad. Debe ser uno de los siguientes valores: <ul><li/>Microsoft<li/>Google<li/>Amazon<li/>LinkedIn<li/>Facebook</ul>|

### <a name="where-to-get-the-client-id-and-secret"></a>Dónde obtener al cliente de identificador y el secreto

Cada proveedor de identidad tiene un proceso para la creación de un registro de la aplicación. Por ejemplo, los usuarios crear un registro de la aplicación con Facebook en [developers.facebook.com](https://developers.facebook.com/). El identificador de cliente resultante y el secreto de cliente se pueden pasar al [crear identityProvider](../api/identityprovider-post-identityproviders.md). A continuación, cada objeto de usuario en el directorio se puede federar en cualquiera de los proveedores de identidad del inquilino para la autenticación. Esto permite al usuario iniciar sesión escribiendo las credenciales de inicio de sesión del proveedor de identidad en la página. El símbolo (token) desde el proveedor de identidad se valida por Azure AD antes de que el inquilino emite un token para la aplicación.

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.IdentityProvider"
} -->

```json
{
    "id": "String",
    "type": "String",
    "name": "String",
    "clientId": "String",
    "clientSecret": "String"
}
```
