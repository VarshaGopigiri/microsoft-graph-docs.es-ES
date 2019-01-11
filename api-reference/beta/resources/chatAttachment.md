---
title: tipo de recurso chatMessageAttachment
description: Representa un archivo adjunto a una entidad de mensaje de chat.
localization_priority: Normal
ms.openlocfilehash: 83574a7dbbb35f9c8b95474fac1154154f413470
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805561"
---
# <a name="chatmessageattachment-resource-type"></a>tipo de recurso chatMessageAttachment

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa un archivo adjunto a una entidad de mensaje de chat.

Una entidad de tipo `chatMessageAttachment` se devuelve como parte de los [mensajes del canal de obtener](../api/channel-list-messages.md) API, como parte de la entidad [chatMessage](chatmessage.md) .

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|string| Solo lectura. Identificador único de los datos adjuntos|
|contentType| string | El tipo de medio de los datos adjuntos del contenido. Puede tener los valores siguientes: <br><ul><li>referencia: los datos adjuntos están un vínculo a otro archivo. Rellenar la contentURL con el vínculo al objeto<br></li><li>archivo: datos adjuntos del archivo sin procesar. Rellenar el campo contenturl con la codificación base64 del archivo de datos: formato<br></li><li>imagen /: tipo de imagen con el tipo de la imagen especificada ej: imagen/png, image/jpeg, imagen o gif. Rellenar el campo contentUrl con la codificación base64 del archivo de datos: formato<br></li><li>vídeo /: tipo de vídeo con el formato especificado. Ex: vídeo / mp4. Rellenar el campo contentUrl con la codificación base64 del archivo de datos: formato<br></li><li>audio /: tipo de Audio con el formato especificado. Ex: audio / wmw. Rellenar el campo contentUrl con la codificación base64 del archivo de datos: formato<br></li><li>tipo de aplicación/tarjeta: enriquecido de tarjetas de tipo de datos adjuntos con el tipo de tarjeta que especifica el formato exacto de tarjeta desea utilizar. Establezca el contenido con el formato json de la tarjeta. Los valores admitidos para el tipo de tarjeta son:<br><ul><li>Application/vnd.Microsoft.Card.Adaptive: una tarjeta enriquecida que puede contener cualquier combinación de texto, voz, imágenes,, los botones y los campos de entrada. Establecer la propiedad de contenido a un objeto AdaptiveCard.</li><li>Application/vnd.Microsoft.Card.Animation: una tarjeta enriquecida que se reproduce la animación. Establezca la propiedad de contenido, en un AnimationCardobject.</li><li>Application/vnd.Microsoft.Card.audio: una tarjeta enriquecida que reproduce los archivos de audio. Establezca la propiedad de contenido, a un objeto AudioCard.</li><li>Application/vnd.Microsoft.Card.video: una tarjeta enriquecida que reproduce vídeos. Establezca la propiedad de contenido, en un objeto de la tarjeta de vídeo.</li><li>Application/vnd.Microsoft.Card.Hero: una tarjeta Hero. Establecer la propiedad de contenido a un objeto HeroCard.</li><li>Application/vnd.Microsoft.Card.Thumbnail: una tarjeta de vista en miniatura. Establecer la propiedad de contenido a un objeto ThumbnailCard.</li><li>Application/vnd.Microsoft.com.Card.Receipt: una tarjeta de confirmación. Establecer la propiedad de contenido a un objeto ReceiptCard.</li><li>Application/vnd.Microsoft.com.Card.SignIn: una tarjeta de inicio de sesión de usuario. Establecer la propiedad de contenido a un objeto SignInCard.</ul></ul>|
|contentUrl|string|Dirección URL para el contenido de los datos adjuntos. Protocolos admitidos: http, https, archivos y datos|
|content|string|El contenido de los datos adjuntos. Si los datos adjuntos son una tarjeta enriquecida, establezca la propiedad en el objeto de tarjeta enriquecido. Esta propiedad y contentUrl son mutuamente excluyentes|
|name|string|Nombre de los datos adjuntos|
|thumbnailUrl| string |Dirección URL de un una imagen en miniatura que puede usar el canal si admite el uso de un formulario alternativo, más pequeño de contenido o contentUrl. Por ejemplo, si se establece contentType en la aplicación y word y establece contentUrl a la ubicación del documento de Word, podría incluir una imagen en miniatura que representa el documento. El canal podría mostrar la imagen en miniatura en lugar del documento. Cuando el usuario hace clic en la imagen, el canal abra el documento.|

## <a name="json-representation"></a>Representación JSON
 La siguiente es una representación de JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "thumbnailUrl",
    "content",
    "contentUrl"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.chatMessageAttachment"
}-->

```json
{
  "id": "string (identifier)",
  "contentType": "string",
  "contentUrl": "string",
  "content": "string",
  "name": "string",
  "thumbnailUrl": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "chat attachment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
