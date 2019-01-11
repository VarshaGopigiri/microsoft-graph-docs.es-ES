---
title: assignLicense
description: Agregar o quitar licencias para el usuario habilitar o deshabilitar el uso de las ofertas de nube de Microsoft. Por ejemplo, una organización puede tener una suscripción a Office 365 Enterprise E3 con 100 licencias, y esta solicitud de una de las licencias asigna a un usuario determinado. También puede habilitar y deshabilitar planes específicos asociados a una suscripción. Para obtener más información acerca de las suscripciones y las licencias, consulte este artículo de Technet.
localization_priority: Normal
ms.openlocfilehash: 71287b47a0a42ce4f89635fe6a1769c78874ae36
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876205"
---
# <a name="assignlicense"></a>assignLicense

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Agregar o quitar licencias para el usuario habilitar o deshabilitar el uso de las ofertas de nube de Microsoft. Por ejemplo, una organización puede tener una suscripción a Office 365 Enterprise E3 con 100 licencias, y esta solicitud de una de las licencias asigna a un usuario determinado. También puede habilitar y deshabilitar planes específicos asociados a una suscripción. Para obtener más información acerca de las suscripciones y las licencias, vea este [artículo de Technet](https://technet.microsoft.com/en-us/library/mt765146.aspx).

Para obtener las suscripciones disponibles en el directorio, lleve a cabo una [solicitud de subscribedSkus](subscribedsku-list.md). 

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | User.ReadWrite.All, Directory.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | User.ReadWrite.All, Directory.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/assignLicense
```
## <a name="request-headers"></a>Encabezados de solicitud
| Encabezado       | Valor |
|:---------------|:--------|
| Authorization  | {token} de portador. Obligatorio.  |
| Content-Type  | application/json  |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.

| Parámetro    | Tipo   |Descripción|
|:---------------|:--------|:----------|
|addLicenses|Colección [assignedLicense](../resources/assignedlicense.md)|Una colección de objetos [assignedLicense](../resources/assignedlicense.md) que especifican las licencias para agregar. Puede deshabilitar servicePlans asociado con una licencia estableciendo la propiedad **disabledPlans** en un objeto [assignedLicense](../resources/assignedlicense.md) .|
|removeLicenses|Guid|Una colección de skuIds que identifican las licencias para quitar.|

## <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve `200 OK` código de respuesta y un objeto de [usuario](../resources/user.md) de actualizada en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
Agregar licencias para el usuario.
##### <a name="request"></a>Solicitud
<!-- {
  "blockType": "request",
  "name": "user_assignlicense"
}-->
```http
POST https://graph.microsoft.com/beta/me/assignLicense
Content-type: application/json
Content-length: 185

{
  "addLicenses": [
    {
      "disabledPlans": [ "11b0131d-43c8-4bbb-b2c8-e80f9a50834a" ],
      "skuId": "skuId-value-1"
    },
    {
      "disabledPlans": [ "a571ebcc-fqe0-4ca2-8c8c-7a284fd6c235" ],
      "skuId": "skuId-value-2"
    }
  ],
  "removeLicenses": []
}
```

## <a name="example"></a>Ejemplo
Quitar licencias de usuario.

#####<a name="request"></a>Solicitud
```http
POST https://graph.microsoft.com/beta/me/assignLicense
Content-type: application/json
Content-length: 185

{
  "addLicenses": [],
  "removeLicenses": ["skuId-value-1", "skuId-value-2"]
}
```

##### <a name="response"></a>Respuesta
En ambos ejemplos, la respuesta es el objeto de usuario actualizada. Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán desde una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 491

{
  "accountEnabled": true,
  "assignedLicenses": [
    {
      "disabledPlans": [ "11b0131d-43c8-4bbb-b2c8-e80f9a50834a" ],
      "skuId": "skuId-value"
    }
  ],
  "assignedPlans": [
    {
      "assignedDateTime": "2016-10-19T10:37:00Z",
      "capabilityStatus": "capabilityStatus-value",
      "service": "service-value",
      "servicePlanId": "bea13e0c-3828-4daa-a392-28af7ff61a0f"
    }
  ],
  "businessPhones": [
    "businessPhones-value"
  ],
  "city": "city-value",
  "companyName": "companyName-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: assignLicense",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
