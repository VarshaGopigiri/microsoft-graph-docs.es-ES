---
title: tipo de recurso resourceVisualization
description: Tipo complejo que contiene las propiedades de conocimientos.
author: simonhult
localization_priority: Normal
ms.openlocfilehash: 7600c843e36e3bce6c8a4182e0bfda14ad21d7b7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27844981"
---
# <a name="resourcevisualization-resource-type"></a>tipo de recurso resourceVisualization

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Tipo complejo que contiene las propiedades de [conocimientos](insights.md).

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

```json
{
  "title": "string",
  "type"  : "string",
  "mediaType": "string",
  "previewImageUrl": "string",
  "previewText": "string",
  "containerWebUrl": "string",
  "containerDisplayName": "string",
  "containerType": "string"
}
```

## <a name="properties"></a>Propiedades

| Propiedad              | Tipo          | Descripción  |
| -------------         |---------------| -------------|
| title                 | Cadena        | Texto del título del elemento.               |
| type              | Cadena        | El tipo del elemento multimedia. Se puede usar para el filtrado para un archivo específico en función de un tipo específico. Vea más adelante para tipos compatibles. |
| mediaType             | Cadena        | El tipo del elemento multimedia. Se puede usar para el filtrado de un tipo específico de archivo basado en tipos de Mime de medios IANA compatibles. Tenga en cuenta que no todos los tipos Mime de medios son compatibles. |
| previewImageUrl       | Cadena        | Una dirección URL conduce a la imagen de vista previa para el elemento. |
| previewText           | Cadena        | Una vista previa de texto para el elemento. |
| containerWebUrl       | Cadena        | Una ruta de acceso que conduce a la carpeta en la que está almacenado el artículo. |
| containerDisplayName  | Cadena        | Una cadena que describe donde está almacenado el artículo. Por ejemplo, el nombre de un sitio de SharePoint o el nombre de usuario que identifica el propietario de la OneDrive para almacenar el elemento.  |
| containerType         | Cadena | Se puede usar para filtrar por el tipo de contenedor en el que se almacena el archivo. Por ejemplo, sitio o OneDriveBusiness.       |

## <a name="type-property-values"></a>Valores de propiedad de tipo
-   PowerPoint
-   Word
-   Excel
-   PDF
-   OneNote
-   OneNotePage
-   InfoPath
-   Visio
-   Publisher
-   Project
-   Access
-   Correo
-   CSV
-   Archivo
-   Xps
-   Audio
-   Vídeo
-   Image (Imagen)
-   Web
-   Texto
-   Xml
-   Story
-   ExternalContent
-   Folder
-   Otros

Consulta de ejemplo:`https://graph.microsoft.com/beta/me/insights/trending?$filter=ResourceVisualization/Type eq 'PowerPoint'`

## <a name="containertype-property-values"></a>valores de la propiedad containerType
Los tipos admitidos pueden variar en función de en los contenedores desde la que el [entendimiento](insights.md) devuelve los archivos. Por ejemplo, solo los conocimientos [compartidos](insights-shared.md) devuelve los archivos de 'Lista desplegable', 'Cuadro' y 'GDrive'.

-   OneDriveBusiness
-   Site
-   Correo
-   Lista desplegable
-   Cuadro
-   GDrive

Consulta de ejemplo:`https://graph.microsoft.com/beta/me/insights/trending?$filter=ResourceVisualization/containerType eq 'OneDriveBusiness'`
