---
title: 'driveItem: vista previa'
description: Esta acción le permite obtener corta duración puede incrustar las direcciones URL de un elemento con el fin de representar una vista previa temporal.
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: be96a0cd451bb3f1c75c32f235d7669ce0bd7509
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27980880"
---
# <a name="driveitem-preview"></a>driveItem: vista previa

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

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
| Visor de      | string        | Opcional. Aplicación de vista previa para que utilice. `onedrive` o `office`. Si es null, se seleccionará automáticamente un visor adecuado.
| sin cromo  | boolean       | Opcional. Si `true` (valor predeterminado), la vista incrustada no incluirá todos los controles.
| allowEdit   | boolean       | Opcional. Si `true`, se puede editar el archivo desde la interfaz de usuario incrustado.
| page        | cadena o número | Opcional. Número de página del documento para iniciar en, si procede. Especificado como cadena para los casos de uso futuro alrededor de tipos de archivo como ZIP.
| zoom        | number        | Opcional. Aumentar nivel para iniciar en, si procede.

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

### <a name="viewers"></a>Visores

Se permiten los siguientes valores para el parámetro **Visor** .

| Valor del tipo | Descripción
|:-----------|:----------------------------------------------------------------
| (null)     | Elige una aplicación adecuada para representar el archivo. En la mayoría de los casos esto va a usar el `onedrive` controlador de vista previa, pero pueden variar según el tipo de archivo.
| `onedrive` | Use la aplicación de vista previa de OneDrive para representar el archivo.
| `office`   | Use el WAC (Office online) para representar el archivo. Sólo es válido para documentos de Office.

### <a name="chrome-vs-chromeless"></a>Cromo vs sin cromo

Si `chromeless` es true, la vista previa será una representación reconstrucción del archivo.
De lo contrario, puede haber otros barras de herramientas o botones que se muestran para interactuar con la vista de documento.

### <a name="viewedit"></a>Ver o modificar

Si `allowEdit` es true, el documento se puede modificar mediante la interacción del usuario con la vista previa incrustada.
Esta función no esté disponible para todas las aplicaciones de la vista previa o tipos de archivo.

### <a name="pagezoom"></a>Página/zoom

El `page` y `zoom` opciones podrían no estar disponibles para todas las aplicaciones de vista previa, pero se aplicará si lo admite la aplicación de vista previa.
