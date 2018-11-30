---
title: tipo de recurso office365ActivationsUserDetail
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 9cf0f7f841584654176c0069fb0403a86615bfd5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085318"
---
# <a name="office365activationsuserdetail-resource-type"></a>tipo de recurso office365ActivationsUserDetail

## <a name="properties"></a>Propiedades

| Propiedad             | Tipo                                     | Descripción                              |
| :------------------- | :--------------------------------------- | ---------------------------------------- |
| reportRefreshDate    | Fecha                                     | La fecha más reciente del contenido.          |
| userPrincipalName    | String                                   | El nombre principal de usuario (UPN) del usuario. El UPN es un nombre de inicio de sesión de estilo de Internet para el usuario según el estándar de Internet RFC 822. Por convención, esto se debe asignar al nombre de correo electrónico del usuario. El formato general es alias@domain, donde el dominio debe estar presente en la colección del inquilino de dominios verificados. Esta propiedad es necesaria cuando se crea un usuario. |
| displayName          | Cadena                                   | Nombre del usuario que aparece en la libreta de direcciones. Suele ser la combinación del nombre del usuario, la inicial del segundo nombre y el apellido. Esta propiedad es necesaria al crearse un usuario y no puede borrarse durante las actualizaciones. |
| userActivationCounts | colección de [userActivationCounts](../resources/useractivationcounts.md) | Los recuentos de activación del producto más reciente del usuario en todas las plataformas para todos los tipos de producto asignado. |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.office365ActivationsUserDetail"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "userPrincipalName": "String", 
  "displayName": "String", 
  "userActivationCounts": [{"@odata.type":"microsoft.graph.userActivationCounts"}]
}
```
