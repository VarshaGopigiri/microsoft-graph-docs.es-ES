---
author: kevinlam
ms.author: kevinlam
ms.date: 3/16/2018
title: ItemPreviewInfo - OneDrive para la API
localization_priority: Normal
ms.openlocfilehash: 0f2a161b9b43a8d372b90530b1b9d9244f77d8e9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27857347"
---
# <a name="itempreviewinfo-resource-type"></a>Tipo de recurso ItemPreviewInfo

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **ItemPreviewInfo** contiene información acerca de cómo incrustar una vista previa de una [DriveItem](driveitem.md).

## <a name="json-representation"></a>Representación JSON

```json
{
    "getUrl": "https://www.onedrive.com/embed?foo=bar&bar=baz",
    "postParameters": "param1=value&param2=another%20value",
    "postUrl": "https://www.onedrive.com/embed_by_post"
}
```

## <a name="properties"></a>Propiedades

| Nombre           | Tipo   | Description
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
