# <a name="hashes-resource-type"></a><span data-ttu-id="50b6f-101">Tipo de recurso Hashes</span><span class="sxs-lookup"><span data-stu-id="50b6f-101">Hashes resource type</span></span>

<span data-ttu-id="50b6f-102">El recurso **Hashes** agrupa hashes disponibles en una sola estructura de un elemento.</span><span class="sxs-lookup"><span data-stu-id="50b6f-102">The **Hashes** resource groups available hashes into a single structure for an item.</span></span>

<span data-ttu-id="50b6f-103">**Nota:** No todos los servicios proporcionan un valor para todas las propiedades de hash enumeradas.</span><span class="sxs-lookup"><span data-stu-id="50b6f-103">**Note:** Not all services provide a value for all hash properties listed.</span></span>

## <a name="json-representation"></a><span data-ttu-id="50b6f-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="50b6f-104">JSON representation</span></span>

<span data-ttu-id="50b6f-105">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="50b6f-105">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "sha1Hash", "crc32Hash", "quickXorHash" ],
  "@odata.type": "microsoft.graph.hashes"
}-->

```json
{
  "crc32Hash": "string",
  "sha1Hash": "string",
  "quickXorHash": "string"
}
```


## <a name="properties"></a><span data-ttu-id="50b6f-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="50b6f-106">Properties</span></span>

| <span data-ttu-id="50b6f-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="50b6f-107">Property</span></span>         | <span data-ttu-id="50b6f-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="50b6f-108">Type</span></span>   | <span data-ttu-id="50b6f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="50b6f-109">Description</span></span>                                                       |
|:-----------------|:-------|:------------------------------------------------------------------|
| <span data-ttu-id="50b6f-110">**sha1Hash**</span><span class="sxs-lookup"><span data-stu-id="50b6f-110">**sha1Hash**</span></span>     | <span data-ttu-id="50b6f-111">String</span><span class="sxs-lookup"><span data-stu-id="50b6f-111">String</span></span> | <span data-ttu-id="50b6f-p101">Hash SHA1 para el contenido del archivo (si está disponible). Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="50b6f-p101">SHA1 hash for the contents of the file (if available). Read-only.</span></span> |
| <span data-ttu-id="50b6f-114">**crc32Hash**</span><span class="sxs-lookup"><span data-stu-id="50b6f-114">**crc32Hash**</span></span>    | <span data-ttu-id="50b6f-115">String</span><span class="sxs-lookup"><span data-stu-id="50b6f-115">String</span></span> | <span data-ttu-id="50b6f-p102">El valor CRC32 del archivo (si está disponible). Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="50b6f-p102">The CRC32 value of the file (if available). Read-only.</span></span>            |
| <span data-ttu-id="50b6f-118">**quickXorHash**</span><span class="sxs-lookup"><span data-stu-id="50b6f-118">**quickXorHash**</span></span> | <span data-ttu-id="50b6f-119">String</span><span class="sxs-lookup"><span data-stu-id="50b6f-119">String</span></span> | <span data-ttu-id="50b6f-p103">Un hash de propietario del archivo que se puede usar para determinar si ha cambiado el contenido del archivo (si está disponible). Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="50b6f-p103">A proprietary hash of the file that can be used to determine if the contents of the file have changed (if available). Read-only.</span></span> |

<span data-ttu-id="50b6f-p104">**Nota:** En algunos casos, puede que no estén disponibles los valores hash. Si este es el caso, los valores hash de un elemento se actualizarán después de que se descargue el elemento.</span><span class="sxs-lookup"><span data-stu-id="50b6f-p104">**Note:** In some cases hash values may not be available. If this is the case, the hash values on an item will be updated after the item is downloaded.</span></span>


## <a name="remarks"></a><span data-ttu-id="50b6f-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="50b6f-124">Remarks</span></span>

<span data-ttu-id="50b6f-p105">En OneDrive para la Empresa, **sha1Hash** y **crc32Hash** no están disponibles. En OneDrive Personal, **quickXorHash** no está disponible.</span><span class="sxs-lookup"><span data-stu-id="50b6f-p105">In OneDrive for Business, **sha1Hash** and **crc32Hash** are not available. In OneDrive Personal, **quickXorHash** is not available.</span></span>

<span data-ttu-id="50b6f-127">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="50b6f-127">For more information about the facets on a [driveItem](driveitem.md), see driveItem.</span></span>


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "hashes resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
