---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Obtenga carpetas especiales.
ms.openlocfilehash: 8b8b1186682421a5ab564272fd473cb72819202d
ms.sourcegitcommit: 37591c2299c80e7675cd2b5f781e1eeeba628a60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2019
ms.locfileid: "27748503"
---
# <a name="get-a-special-folder-by-name"></a>Obtener una carpeta especial por su nombre

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Use la colección especial para acceder a una carpeta especial por su nombre.

Las carpetas especiales proporcionan alias simples para acceder a carpetas conocidas en OneDrive sin necesidad de buscar la carpeta por su ruta (que requeriría localización) o hacer referencia a la carpeta con un identificador. Si una carpeta especial cambia de nombre o se mueve a otra ubicación de la unidad, esta sintaxis seguirá encontrando esa carpeta.

Las carpetas especiales se crean de forma automática la primera vez que una aplicación intenta escribir en una, si aún no existe. Si un usuario elimina una, se vuelve a crear al volver a escribir en ella.

> **Nota:**  Si tiene permisos de solo lectura y solicita una carpeta especial que no existe, recibirá un error `403 Forbidden`.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|            Tipo de permiso             |                                           Permisos (de menos a más privilegiados)                                            |
| :------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------- |
| Delegado (cuenta profesional o educativa)     | Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All                            |
| Delegado (cuenta personal de Microsoft) | Files.ReadWrite.AppFolder, Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All |
| Aplicación                            | Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All                                                         |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "request", "name": "get-special-folder", "scopes": "files.read" } -->

```http
GET /me/drive/special/{name}
```

### <a name="special-folder-names"></a>Nombres de carpetas especiales

Los siguientes nombres de carpetas especiales están disponibles en OneDrive y OneDrive para la Empresa.

| Nombre        | Id. de carpeta    | Descripción                                                              |
|:------------|:-------------|:-------------------------------------------------------------------------|
| Documentos   | `documents`  | La carpeta Documentos.                                                    |
| Fotos      | `photos`     | La carpeta Fotos.                                                       |
| Álbum de cámara | `cameraroll` | La carpeta de copia de seguridad del álbum de cámara.                                           |
| Raíz de la aplicación    | `approot`    | La carpeta personal de la aplicación. Normalmente en `/Apps/{Application Name}` |
| Música       | `music`      | La carpeta Música.                                                        |


### <a name="optional-query-parameters"></a>Parámetros de consulta opcionales

Este método admite los [parámetros de consulta OData](/graph/query-parameters) `$expand` y `$select` para personalizar la respuesta.

## <a name="response"></a>Respuesta

Este método devuelve un código de respuesta `200 OK` y un objeto [driveItem](../resources/driveitem.md) en el cuerpo de la respuesta.

Puede usar este método de direccionamiento de una carpeta especial junto con llamadas adicionales a las propiedades o relaciones en el objeto driveItem.

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItem", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "id": "0123456789abc",
  "name": "Documents",
  "eTag": "012345819293.1",
  "specialFolder": {
    "name": "documents"
  }
}
```

## <a name="get-children-of-a-special-folder"></a>Obtener elementos secundarios de una carpeta especial

Para solicitar los elementos secundarios de una carpeta especial, puede solicitar la colección `children` o usar la opción [expand](/graph/query-parameters) para expandir la colección de elementos secundarios.

### <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "request", "name": "get-special-children", "scopes": "files.read" } -->

```http
GET /me/drive/special/{name}/children
```

### <a name="response"></a>Respuesta

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItem", "isCollection": true, "truncated": true} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {"name": "myfile.jpg", "size": 2048 },
    {"name": "Documents", "folder": { "childCount": 4} },
    {"name": "Photos", "folder": { "childCount": 203} },
    {"name": "my sheet(1).xlsx", "size": 197 }
  ]
}
```

## <a name="remarks"></a>Comentarios

> **Nota:** Los objetos DriveItems con la faceta `specialFolder` indican que el elemento es una carpeta especial y se puede obtener acceso a ella mediante la colección `special`.

Si la aplicación tiene permisos de solo lectura, la solicitud para obtener una carpeta especial o los elementos secundarios de una carpeta especial puede producir un error `404 Not Found` o `403 Forbidden` si la carpeta especial todavía no existe.

<!-- {
  "type": "#page.annotation",
  "description": "Access known folders in OneDrive through the special folder collection",
  "keywords": "known folders",
  "section": "documentation",
  "tocPath": "OneDrive/Drive/Special folders"
} -->
