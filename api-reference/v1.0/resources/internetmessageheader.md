# <a name="internetmessageheader-resource-type"></a><span data-ttu-id="8f09d-101">Tipo de recurso internetMessageHeader</span><span class="sxs-lookup"><span data-stu-id="8f09d-101">internetMessageHeader resource type</span></span>


<span data-ttu-id="8f09d-102">Par de clave y valor que representa un encabezado de mensaje de Internet, tal y como se define con [RFC5322](https://www.ietf.org/rfc/rfc5322.txt), que proporciona los detalles de la ruta de acceso a la red que sigue un mensaje del remitente al destinatario.</span><span class="sxs-lookup"><span data-stu-id="8f09d-102">A key-value pair that represents an Internet message header, as defined by [RFC5322](https://www.ietf.org/rfc/rfc5322.txt), that provides details of the network path taken by a message from the sender to the recipient.</span></span> 

<span data-ttu-id="8f09d-103">Para examinar ejemplos de un encabezado de mensaje de Internet, consulte [Ver encabezados de mensajes de internet](https://support.office.com/es-ES/article/View-e-mail-message-headers-CD039382-DC6E-4264-AC74-C048563D212C#bm4).</span><span class="sxs-lookup"><span data-stu-id="8f09d-103">For examples of an Internet message header, see [View e-mail message headers](https://support.office.com/es-ES/article/View-e-mail-message-headers-CD039382-DC6E-4264-AC74-C048563D212C#bm4).</span></span>


## <a name="properties"></a><span data-ttu-id="8f09d-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8f09d-104">Properties</span></span>
| <span data-ttu-id="8f09d-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8f09d-105">Property</span></span>     | <span data-ttu-id="8f09d-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="8f09d-106">Type</span></span>   |<span data-ttu-id="8f09d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f09d-107">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8f09d-108">name</span><span class="sxs-lookup"><span data-stu-id="8f09d-108">name</span></span>|<span data-ttu-id="8f09d-109">string</span><span class="sxs-lookup"><span data-stu-id="8f09d-109">string</span></span>|<span data-ttu-id="8f09d-110">Representa la clave de un par de clave y valor.</span><span class="sxs-lookup"><span data-stu-id="8f09d-110">Represents the key in a key-value pair.</span></span>|
|<span data-ttu-id="8f09d-111">value</span><span class="sxs-lookup"><span data-stu-id="8f09d-111">value</span></span>|<span data-ttu-id="8f09d-112">string</span><span class="sxs-lookup"><span data-stu-id="8f09d-112">string</span></span>|<span data-ttu-id="8f09d-113">Valor de un par de clave y valor.</span><span class="sxs-lookup"><span data-stu-id="8f09d-113">The value in a key-value pair.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="8f09d-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8f09d-114">JSON representation</span></span>

<span data-ttu-id="8f09d-115">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8f09d-115">Here is a JSON representation of the resource.</span></span>

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