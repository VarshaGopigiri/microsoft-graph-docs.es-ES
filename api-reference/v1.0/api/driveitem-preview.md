---
title: 'driveItem: vista previa'
description: Esta acción le permite obtener corta duración puede incrustar las direcciones URL de un elemento con el fin de representar una vista previa temporal.
ms.openlocfilehash: 741e449c972ad372aae30d9921cdb3b7fa1fc40d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031495"
---
# <a name="driveitem-preview"></a>driveItem: vista previa

Esta acción le permite obtener corta duración puede incrustar las direcciones URL de un elemento con el fin de representar una vista previa temporal.

Si desea obtener vínculos puede incrustar larga duración, use la API [createLink][] en su lugar.

> **Nota:** Actualmente, la acción de **vista previa** sólo está disponible en SharePoint y OneDrive para la empresa.

[createLink]: driveitem-createlink.md

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

| Tipo de permiso                        | Permisos (de menos a más privilegiados)
|:---------------------------------------|:-------------------------------------------
| Delegado (cuenta profesional o educativa)     | Files.Read, Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All
| Delegado (cuenta personal de Microsoft) | Files.Read, Files.ReadWrite, Files.ReadWrite.All
| Aplicación                            | No admitida.

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
POST /drives/{driveId}/items/{itemId}/preview
POST /groups/{groupId}/drive/items/{itemId}/preview
POST /me/drive/items/{itemId}/preview
POST /sites/{siteId}/drive/items/{itemId}/preview
POST /users/{userId}/drive/items/{itemId}/preview
POST /shares/{shareId}/driveItem/preview
```

## <a name="request-body"></a>Cuerpo de la solicitud

El cuerpo de la solicitud define las propiedades de la dirección URL puede incrustar está solicitando la aplicación.
La solicitud debe ser un objeto JSON con las siguientes propiedades.

|   Nombre      |  Tipo         | Descripción
|:------------|:--------------|:-----------------------------------------------
| page        | cadena o número | Opcional. Número de página del documento para iniciar en, si procede. Especificado como cadena para los casos de uso futuro alrededor de tipos de archivo como ZIP.
| zoom        | n?mero        | Opcional. Aumentar nivel para iniciar en, si procede.

## <a name="response"></a>Respuesta

```json
{
    "getUrl": "https://www.onedrive.com/embed?foo=bar&bar=baz",
    "postParameters": "param1=value&param2=another%20value",
    "postUrl": "https://www.onedrive.com/embed_by_post"
}
```

La respuesta será un objeto JSON que contiene las siguientes propiedades:

| Nombre           | Tipo   | Descripción
|:---------------|:-------|:---------------------------------------------------
| getUrl         | string | Dirección URL adecuada para incrustar mediante HTTP GET (IFRAME, etcetera).
| URL para exponer        | string | Dirección URL adecuada para incrustar el uso de HTTP POST (de envío de formulario, JS, etcetera.)
| postParameters | string | Parámetros de entrada para incluir si usa URL para exponer

Es posible que se devolverá getUrl, URL para exponer o ambos según el estado actual del embed compatibilidad con las opciones especificadas.

postParameters es una cadena con formato como `application/x-www-form-urlencoded`, y si se realiza una entrada a la URL para exponer el tipo de contenido se debe establecer en consecuencia. Por ejemplo:
```
POST https://www.onedrive.com/embed_by_post
Content-Type: application/x-www-form-urlencoded

param1=value&param2=another%20value
```

### <a name="pagezoom"></a>Página/zoom

Las opciones de 'zoom' y 'page' podrían no estar disponibles para todas las aplicaciones de vista previa, pero se aplicará si lo admite la aplicación de vista previa.
