---
title: Tipo de recurso internetMessageHeader
description: 'Un par de clave y valor que representa un encabezado de mensaje de Internet, tal como se define por RFC5322, que proporciona '
ms.openlocfilehash: 44c3e33807f45420f79c8216b8381a19c062e411
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031623"
---
# <a name="internetmessageheader-resource-type"></a><span data-ttu-id="1de52-103">Tipo de recurso internetMessageHeader</span><span class="sxs-lookup"><span data-stu-id="1de52-103">internetMessageHeader resource type</span></span>


<span data-ttu-id="1de52-104">Par de clave y valor que representa un encabezado de mensaje de Internet, tal y como se define con [RFC5322](https://www.ietf.org/rfc/rfc5322.txt), que proporciona los detalles de la ruta de acceso a la red que sigue un mensaje del remitente al destinatario.</span><span class="sxs-lookup"><span data-stu-id="1de52-104">A key-value pair that represents an Internet message header, as defined by [RFC5322](https://www.ietf.org/rfc/rfc5322.txt), that provides details of the network path taken by a message from the sender to the recipient.</span></span> 

<span data-ttu-id="1de52-105">Para examinar ejemplos de un encabezado de mensaje de Internet, consulte [Ver encabezados de mensajes de internet](https://support.office.com/en-us/article/View-e-mail-message-headers-CD039382-DC6E-4264-AC74-C048563D212C#bm4).</span><span class="sxs-lookup"><span data-stu-id="1de52-105">For examples of an Internet message header, see [View e-mail message headers](https://support.office.com/en-us/article/View-e-mail-message-headers-CD039382-DC6E-4264-AC74-C048563D212C#bm4).</span></span>


## <a name="properties"></a><span data-ttu-id="1de52-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1de52-106">Properties</span></span>
| <span data-ttu-id="1de52-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1de52-107">Property</span></span>     | <span data-ttu-id="1de52-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="1de52-108">Type</span></span>   |<span data-ttu-id="1de52-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="1de52-109">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1de52-110">name</span><span class="sxs-lookup"><span data-stu-id="1de52-110">name</span></span>|<span data-ttu-id="1de52-111">string</span><span class="sxs-lookup"><span data-stu-id="1de52-111">string</span></span>|<span data-ttu-id="1de52-112">Representa la clave de un par de clave y valor.</span><span class="sxs-lookup"><span data-stu-id="1de52-112">Represents the key in a key-value pair.</span></span>|
|<span data-ttu-id="1de52-113">value</span><span class="sxs-lookup"><span data-stu-id="1de52-113">value</span></span>|<span data-ttu-id="1de52-114">string</span><span class="sxs-lookup"><span data-stu-id="1de52-114">string</span></span>|<span data-ttu-id="1de52-115">Valor de un par de clave y valor.</span><span class="sxs-lookup"><span data-stu-id="1de52-115">The value in a key-value pair.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="1de52-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1de52-116">JSON representation</span></span>

<span data-ttu-id="1de52-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1de52-117">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.internetMessageHeader"
}-->

```json
{
  "name": "string",
  "value": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "internetMessageHeader resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->