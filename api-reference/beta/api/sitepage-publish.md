---
author: rahmit
ms.author: rahmit
ms.date: 09/10/2018
title: Publicar la página
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 8e59a7aea74e165945757f2513102a66baf64be1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27920243"
---
# <a name="sitepage-publish"></a>sitePage: publicar

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Publicar la versión más reciente de un recurso [sitePage][] , que hace que la versión de la página esté disponible para todos los usuarios. Si la página se desprotege, compruebe en la página y publicarlo. Si la página está desprotegida por el autor de la llamada de esta API, la página se registra automáticamente y, a continuación, se ha publicado.

[sitePage]: ../resources/sitepage.md

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | Files.ReadWrite, Files.ReadWrite.All    |
|Aplicación | Files.ReadWrite.All, Sites.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
POST /sites/{siteId}/pages/{pageId}/publish
```

## <a name="request-body"></a>Cuerpo de la solicitud

Este mensaje no tiene un cuerpo de la solicitud. Se omitirá el cuerpo de la solicitud que se envían.

## <a name="response"></a>Respuesta

Si se realiza correctamente, la llamada API devuelve `204 No Content`.

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 204 No Content
```


<!-- {
  "type": "#page.annotation",
  "description": "Publish a page.",
  "keywords": "publish page",
  "section": "documentation",
  "tocPath": "Pages/Publish"
} -->
