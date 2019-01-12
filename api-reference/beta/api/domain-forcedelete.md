---
title: 'dominio: forceDelete'
description: Elimina un dominio mediante una operación asincrónica.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 6c3d942352a0db20d6e46a4b00686ad948bd6798
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27965127"
---
# <a name="domain-forcedelete"></a>dominio: forceDelete

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Elimina un dominio mediante una operación asincrónica.

Como parte de esta operación, se realizan las siguientes acciones:

* Cambia el nombre el UPN, EmailAddress y ProxyAddress de usuarios con referencias al dominio eliminado.

* Cambia el nombre de la EmailAddress de grupos con referencias al dominio eliminado.

* Cambia el nombre de la identifierUris de aplicaciones con referencias al dominio eliminado.

* Si el número de objetos que se puede cambiar el nombre es mayor que 1000, se devuelve un error.

* Si una de las aplicaciones se cambia el nombre es una aplicación de varios inquilino, se devuelve un error.

Una vez completada la eliminación del dominio, las operaciones de API para el dominio eliminado devolverá un código de respuesta HTTP 404. Para comprobar la eliminación de un dominio, puede realizar una operación [obtener el dominio](domain-get.md). Si el dominio se eliminó correctamente, se devolverá un código de respuesta 404 de HTTP en la respuesta.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).


|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Directory.AccessAsUser.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | Domain.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->
```http
POST /domains/{id}/forceDelete
```

> En {id}, especifique el dominio con su nombre completo.

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre       | Descripción|
|:---------------|:----------|
| Authorization  | {token} de portador. Obligatorio.|
| Content-Type  | application/json |

## <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.

| Parámetro    | Tipo   |Descripción|
|:---------------|:--------|:----------|
|disableUserAccounts|Booleano| Opción para deshabilitar las cuentas de usuario cuyo nombre ha cambiado. Si una cuenta de usuario está deshabilitada, el usuario no podrá iniciar sesión.<br>*Es true* (valor predeterminado) - usuario cambió como parte de una operación de cuentas están deshabilitadas.<br>*False* : las cuentas de usuario para cambiar el nombre como parte de esta operación no estén deshabilitados. |

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. 

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
<!-- {
  "blockType": "request",
  "name": "domain_forcedelete"
}-->
```http
POST https://graph.microsoft.com/beta/domains/contoso.com/forceDelete
Content-type: application/json
Content-length: 33

{
  "disableUserAccounts": true
}
```

##### <a name="response"></a>Respuesta

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
} -->

```http
HTTP/1.1 200 OK
```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "domain: forcedelete",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
