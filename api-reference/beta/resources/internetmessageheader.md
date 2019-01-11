---
title: Tipo de recurso internetMessageHeader
description: 'Un par de clave y valor que representa un encabezado de mensaje de Internet, tal como se define por RFC5322, que proporciona '
localization_priority: Normal
ms.openlocfilehash: b4bc08a03d9d37738b84f7f1c9938278fb921a37
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27828500"
---
# <a name="internetmessageheader-resource-type"></a><span data-ttu-id="3b7d4-103">Tipo de recurso internetMessageHeader</span><span class="sxs-lookup"><span data-stu-id="3b7d4-103">internetMessageHeader resource type</span></span>

> <span data-ttu-id="3b7d4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3b7d4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3b7d4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3b7d4-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3b7d4-106">Par de clave y valor que representa un encabezado de mensaje de Internet, tal y como se define con [RFC5322](https://www.ietf.org/rfc/rfc5322.txt), que proporciona los detalles de la ruta de acceso a la red que sigue un mensaje del remitente al destinatario.</span><span class="sxs-lookup"><span data-stu-id="3b7d4-106">A key-value pair that represents an Internet message header, as defined by [RFC5322](https://www.ietf.org/rfc/rfc5322.txt), that provides details of the network path taken by a message from the sender to the recipient.</span></span> 

<span data-ttu-id="3b7d4-107">Para examinar ejemplos de un encabezado de mensaje de Internet, consulte [Ver encabezados de mensajes de internet](https://support.office.com/en-us/article/View-e-mail-message-headers-CD039382-DC6E-4264-AC74-C048563D212C#bm4).</span><span class="sxs-lookup"><span data-stu-id="3b7d4-107">For examples of an Internet message header, see [View e-mail message headers](https://support.office.com/en-us/article/View-e-mail-message-headers-CD039382-DC6E-4264-AC74-C048563D212C#bm4).</span></span>


## <a name="properties"></a><span data-ttu-id="3b7d4-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3b7d4-108">Properties</span></span>
| <span data-ttu-id="3b7d4-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3b7d4-109">Property</span></span>     | <span data-ttu-id="3b7d4-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="3b7d4-110">Type</span></span>   |<span data-ttu-id="3b7d4-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b7d4-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3b7d4-112">name</span><span class="sxs-lookup"><span data-stu-id="3b7d4-112">name</span></span>|<span data-ttu-id="3b7d4-113">string</span><span class="sxs-lookup"><span data-stu-id="3b7d4-113">string</span></span>|<span data-ttu-id="3b7d4-114">Representa la clave de un par de clave y valor.</span><span class="sxs-lookup"><span data-stu-id="3b7d4-114">Represents the key in a key-value pair.</span></span>|
|<span data-ttu-id="3b7d4-115">value</span><span class="sxs-lookup"><span data-stu-id="3b7d4-115">value</span></span>|<span data-ttu-id="3b7d4-116">string</span><span class="sxs-lookup"><span data-stu-id="3b7d4-116">string</span></span>|<span data-ttu-id="3b7d4-117">Valor de un par de clave y valor.</span><span class="sxs-lookup"><span data-stu-id="3b7d4-117">The value in a key-value pair.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="3b7d4-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3b7d4-118">JSON representation</span></span>

<span data-ttu-id="3b7d4-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3b7d4-119">Here is a JSON representation of the resource.</span></span>

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
