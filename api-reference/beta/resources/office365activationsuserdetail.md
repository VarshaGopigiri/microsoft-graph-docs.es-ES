---
title: tipo de recurso office365ActivationsUserDetail
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 3e2b7d5fb3c42db02407a187649544b2560f898a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27982858"
---
# <a name="office365activationsuserdetail-resource-type"></a>tipo de recurso office365ActivationsUserDetail

## <a name="properties"></a>Propiedades

| Propiedad             | Tipo                                     | Descripción                              |
| :------------------- | :--------------------------------------- | ---------------------------------------- |
| reportRefreshDate    | Fecha                                     | La fecha más reciente del contenido.          |
| userPrincipalName    | Cadena                                   | El nombre principal de usuario (UPN) del usuario. El UPN es un nombre de inicio de sesión de estilo de Internet para el usuario según el estándar de Internet RFC 822. Por convención, esto se debe asignar al nombre de correo electrónico del usuario. El formato general es alias@domain, donde el dominio debe estar presente en la colección del inquilino de dominios verificados. Esta propiedad es necesaria cuando se crea un usuario. |
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
