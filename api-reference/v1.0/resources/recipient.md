# <a name="recipient-resource-type"></a><span data-ttu-id="ab0be-101">Tipo de recurso recipient</span><span class="sxs-lookup"><span data-stu-id="ab0be-101">recipient resource type</span></span>

<span data-ttu-id="ab0be-102">Representa información sobre un usuario en la finalización del envío o la recepción de un evento, un mensaje o una publicación de grupo.</span><span class="sxs-lookup"><span data-stu-id="ab0be-102">Represents information about a user in the sending or receiving end of an event, message or group post.</span></span> 

## <a name="properties"></a><span data-ttu-id="ab0be-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ab0be-103">Properties</span></span>
| <span data-ttu-id="ab0be-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ab0be-104">Property</span></span>     | <span data-ttu-id="ab0be-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="ab0be-105">Type</span></span>   |<span data-ttu-id="ab0be-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab0be-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ab0be-107">emailAddress</span><span class="sxs-lookup"><span data-stu-id="ab0be-107">emailAddress</span></span>|[<span data-ttu-id="ab0be-108">EmailAddress</span><span class="sxs-lookup"><span data-stu-id="ab0be-108">EmailAddress</span></span>](emailaddress.md)|<span data-ttu-id="ab0be-109">Dirección de correo del destinatario.</span><span class="sxs-lookup"><span data-stu-id="ab0be-109">The recipient's email address.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ab0be-110">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ab0be-110">JSON representation</span></span>

<span data-ttu-id="ab0be-111">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="ab0be-111">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.recipient"
}-->

```json
{
  "emailAddress": {"@odata.type": "microsoft.graph.emailAddress"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "recipient resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->