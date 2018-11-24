---
author: kevinlam
ms.author: kevinlam
ms.date: 3/16/2018
title: ItemPreviewInfo
ms.openlocfilehash: 8b8f7a962e237cc20a42503efd31f083996ad715
ms.sourcegitcommit: ebac77d2ca32438e552831de0258fe5e86fa225a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/17/2018
ms.locfileid: "26606530"
---
# <a name="itempreviewinfo-resource-type"></a>tipo de recurso itemPreviewInfo

El recurso **itemPreviewInfo** contiene información acerca de cómo incrustar una vista previa de una [driveItem](driveitem.md).

## <a name="json-representation"></a>Representación JSON

```json
{
    "getUrl": "https://www.onedrive.com/embed?foo=bar&bar=baz",
    "postParameters": "param1=value&param2=another%20value",
    "postUrl": "https://www.onedrive.com/embed_by_post"
}
```

## <a name="properties"></a>Propiedades

| Nombre           | Tipo   | Descripción
|:---------------|:-------|:---------------------------------------------------
| getUrl         | string | Dirección URL adecuada para incrustar mediante HTTP GET (IFRAME, etcetera).
| URL para exponer        | string | Dirección URL adecuada para incrustar el uso de HTTP POST (de envío de formulario, JS, etcetera.)
| postParameters | string | Parámetros de entrada para incluir si usa URL para exponer

Según el estado actual de compatibilidad con las opciones especificadas, se pueden devolver getUrl, URL para exponer o ambos.

postParameters es una cadena con formato como `application/x-www-form-urlencoded`, y si se realiza una entrada a la URL para exponer el tipo de contenido se debe establecer en consecuencia. Por ejemplo:
```
POST https://www.onedrive.com/embed_by_post
Content-Type: application/x-www-form-urlencoded

param1=value&param2=another%20value
```

Los formatos de direcciones URL y los parámetros deben considerarse opacos.
