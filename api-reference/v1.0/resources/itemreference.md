# <a name="itemreference-resource-type"></a><span data-ttu-id="339ce-101">Tipo de recurso ItemReference</span><span class="sxs-lookup"><span data-stu-id="339ce-101">ItemReference resource type</span></span>

<span data-ttu-id="339ce-102">El recurso **ItemReference** proporciona información necesaria para dirigir un [DriveItem](driveitem.md) a través de la API.</span><span class="sxs-lookup"><span data-stu-id="339ce-102">The **ItemReference** resource provides information necessary to address a [DriveItem](driveitem.md) via the API.</span></span>

## <a name="json-representation"></a><span data-ttu-id="339ce-103">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="339ce-103">JSON representation</span></span>

<span data-ttu-id="339ce-104">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="339ce-104">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "path", "shareId", "sharepointIds" ],
  "@odata.type": "microsoft.graph.itemReference"
}-->

```json
{
  "driveId": "string",
  "id": "string",
  "name": "string",
  "path": "string",
  "shareId": "string",
  "sharepointIds": { "@odata.type": "microsoft.graph.sharepointIds" }
}
```

## <a name="properties"></a><span data-ttu-id="339ce-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="339ce-105">Properties</span></span>

| <span data-ttu-id="339ce-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="339ce-106">Property</span></span>      | <span data-ttu-id="339ce-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="339ce-107">Type</span></span>                              | <span data-ttu-id="339ce-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="339ce-108">Description</span></span>                                                                                                |
| :------------ | :-------------------------------- | :--------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="339ce-109">driveId</span><span class="sxs-lookup"><span data-stu-id="339ce-109">driveId</span></span>       | <span data-ttu-id="339ce-110">String</span><span class="sxs-lookup"><span data-stu-id="339ce-110">String</span></span>                            | <span data-ttu-id="339ce-p101">Identificador único de la instancia de la unidad que contiene el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="339ce-p101">Unique identifier of the drive instance that contains the item. Read-only.</span></span>                                 |
| <span data-ttu-id="339ce-113">id</span><span class="sxs-lookup"><span data-stu-id="339ce-113">id</span></span>            | <span data-ttu-id="339ce-114">String</span><span class="sxs-lookup"><span data-stu-id="339ce-114">String</span></span>                            | <span data-ttu-id="339ce-p102">Identificador único del elemento en la unidad. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="339ce-p102">Unique identifier of the item in the drive. Read-only.</span></span>                                                     |
| <span data-ttu-id="339ce-117">name</span><span class="sxs-lookup"><span data-stu-id="339ce-117">name</span></span>          | <span data-ttu-id="339ce-118">String</span><span class="sxs-lookup"><span data-stu-id="339ce-118">String</span></span>                            | <span data-ttu-id="339ce-p103">El nombre del elemento al que se hace referencia. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="339ce-p103">The name of the item being referenced. Read-only.</span></span>                                                          |
| <span data-ttu-id="339ce-121">path</span><span class="sxs-lookup"><span data-stu-id="339ce-121">path</span></span>          | <span data-ttu-id="339ce-122">String</span><span class="sxs-lookup"><span data-stu-id="339ce-122">String</span></span>                            | <span data-ttu-id="339ce-p104">Ruta de acceso que se puede usar para navegar hasta el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="339ce-p104">Path that can be used to navigate to the item. Read-only.</span></span>                                                  |
| <span data-ttu-id="339ce-125">shareId</span><span class="sxs-lookup"><span data-stu-id="339ce-125">shareId</span></span>       | <span data-ttu-id="339ce-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="339ce-126">String</span></span>                            | <span data-ttu-id="339ce-127">Un identificador único para un recurso compartido al que se puede tener acceso a través de la API [Shares](../api/shares_get.md).</span><span class="sxs-lookup"><span data-stu-id="339ce-127">A unique identifier for a shared resource that can be accessed via the [Shares](../api/shares_get.md) API.</span></span> |
| <span data-ttu-id="339ce-128">sharepointIds</span><span class="sxs-lookup"><span data-stu-id="339ce-128">sharepointIds</span></span> | [<span data-ttu-id="339ce-129">sharepointIds</span><span class="sxs-lookup"><span data-stu-id="339ce-129">sharepointIds</span></span>](sharepointids.md) | <span data-ttu-id="339ce-p105">Devuelve los identificadores útiles para la compatibilidad con REST de SharePoint. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="339ce-p105">Returns identifiers useful for SharePoint REST compatibility. Read-only.</span></span>                                   |

## <a name="remarks"></a><span data-ttu-id="339ce-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="339ce-132">Remarks</span></span>

<span data-ttu-id="339ce-133">Para resolver un **driveItem** de un recurso **itemReference**, cree una dirección URL con el formato:</span><span class="sxs-lookup"><span data-stu-id="339ce-133">To address a **driveItem** from an **itemReference** resource, construct a URL of the format:</span></span>

```http
GET https://graph.microsoft.com/v1.0/drives/{driveId}/items/{id}
```

<span data-ttu-id="339ce-134">El valor **path** es una ruta de acceso de API relativa a la unidad de destino, por ejemplo: `/drive/root:/Documents/myfile.docx`.</span><span class="sxs-lookup"><span data-stu-id="339ce-134">The **path** value is an API path relative to the target drive, for example: `/drive/root:/Documents/myfile.docx`.</span></span>

<span data-ttu-id="339ce-135">Para recuperar la ruta de acceso legible de una ruta de navegación, puede ignorar todo hasta la primera `:` en la cadena de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="339ce-135">To retrieve the human-readable path for a breadcrumb, you can safely ignore everything up to the first `:` in the path string.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "itemReference resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
