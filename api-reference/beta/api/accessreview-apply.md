---
title: Aplicar accessReview
description: 'En Azure AD tener acceso a la característica de revisiones, se aplican las decisiones de un accessReview completado.  El objeto de destino puede ser una revisión de acceso única o una instancia de una revisión periódica de access.  '
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: e230a9638e865fbca69448f3a7683b95db954598
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27951337"
---
# <a name="apply-accessreview"></a>Aplicar accessReview

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, se aplican las decisiones de un completado [accessReview](../resources/accessreview.md).  El objeto de destino puede ser una revisión de acceso única o una instancia de una revisión periódica de access.  


Una vez finalizada una revisión de access, ya sea porque alcanza la fecha de finalización o un administrador detuvo manualmente y aplicar automáticamente no se ha configurado para la revisión, puede llamar a aplicar para aplicar los cambios. Hasta que se produzca aplicar, las decisiones para quitar los derechos de acceso no aparecen en el recurso de origen, por ejemplo, los usuarios conservan sus pertenencias a grupos. Al llamar a aplicar, el resultado de la revisión se implementa mediante la actualización de la aplicación o el grupo. Si se denegó el acceso de un usuario en la revisión, cuando un administrador llama a esta API, Azure AD quita su asignación pertenencia o aplicación. 

Después de una revisión de access haya terminado y aplicar automáticamente se configuran, a continuación, el estado de la revisión cambiará de completado a través de los estados intermedios y por último cambiará a estado se aplica. Puede esperar ver los usuarios denegados, si alguna, eliminando desde el recurso de grupo integrantes o la aplicación de asignación en unos minutos.

Un automático configurado aplicar la revisión, o si selecciona aplicar no tiene un efecto en un grupo que se origina en un directorio local o un grupo dinámico. Si desea cambiar un grupo que se origina local, descargue los resultados y aplicar esos cambios a la representación del grupo en ese directorio.


## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso                        | Permisos (de menos a más privilegiados)              |
|:--------------------------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa)     | AccessReview.ReadWrite.All |
|Delegado (cuenta personal de Microsoft) | No admitida. |
|Aplicación                            | No admitida. |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /accessReviews('<id>')/applyDecisions()
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre         | Tipo        | Descripción |
|:-------------|:------------|:------------|
| Autorización | string | Bearer \{token\}. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.


## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.

## <a name="see-also"></a>Vea también

- [Procedimiento para llevar a cabo una revisión de access](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-azure-ad-controls-complete-access-review)

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
<!-- {
  "blockType": "request",
  "name": "apply_accessReview"
}-->
```http
POST https://graph.microsoft.com/beta/accessReviews('2975E9B5-44CE-4E71-93D3-30F03B5AA992')/applyDecisions()
```
##### <a name="response"></a>Respuesta
>**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2017-06-25 00:00:01 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Apply accessReview",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
