# <a name="filehash-resource-type"></a><span data-ttu-id="1584a-101">Tipo de recurso fileHash</span><span class="sxs-lookup"><span data-stu-id="1584a-101">fileHash resource type</span></span>

<span data-ttu-id="1584a-102">Contiene información con estado acerca de los valores de hash de archivo (criptográficos y de ubicación).</span><span class="sxs-lookup"><span data-stu-id="1584a-102">Contains stateful information about file hashes (cryptographic and location-sensitive).</span></span>

## <a name="properties"></a><span data-ttu-id="1584a-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1584a-103">Properties</span></span>

| <span data-ttu-id="1584a-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1584a-104">Property</span></span>     | <span data-ttu-id="1584a-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="1584a-105">Type</span></span>        | <span data-ttu-id="1584a-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="1584a-106">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="1584a-107">hashType</span><span class="sxs-lookup"><span data-stu-id="1584a-107">hashType</span></span>|<span data-ttu-id="1584a-108">fileHashType</span><span class="sxs-lookup"><span data-stu-id="1584a-108">fileHashType</span></span>|<span data-ttu-id="1584a-109">Tipo de hash de archivo.</span><span class="sxs-lookup"><span data-stu-id="1584a-109">File hash type.</span></span> <span data-ttu-id="1584a-110">Los valores posibles son: `unknown`, `sha1`, `sha256`, `md5`, `authenticodeHash256`, `lsHash`, `ctph`, `peSha1` y `peSha256`.</span><span class="sxs-lookup"><span data-stu-id="1584a-110">Possible values are: `unknown`, `sha1`, `sha256`, `md5`, `authenticodeHash256`, `lsHash`, `ctph`, `peSha1`, `peSha256`.</span></span>|
|<span data-ttu-id="1584a-111">hashValue</span><span class="sxs-lookup"><span data-stu-id="1584a-111">hashValue</span></span>|<span data-ttu-id="1584a-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="1584a-112">String</span></span>|<span data-ttu-id="1584a-113">Valor de hash de archivo.</span><span class="sxs-lookup"><span data-stu-id="1584a-113">Value of the file hash.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="1584a-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1584a-114">JSON representation</span></span>

<span data-ttu-id="1584a-115">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="1584a-115">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.fileHash"
}-->

```json
{
  "hashType": "@odata.type: microsoft.graph.fileHashType",
  "hashValue": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "fileHash resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->