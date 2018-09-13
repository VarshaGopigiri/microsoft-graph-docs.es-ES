# <a name="filesecuritystate-resource-type"></a><span data-ttu-id="26a84-101">Tipo de recurso fileSecurityState</span><span class="sxs-lookup"><span data-stu-id="26a84-101">fileSecurityState resource type</span></span>

<span data-ttu-id="26a84-102">Contiene información sobre el archivo (no proceso) relacionado con la alerta.</span><span class="sxs-lookup"><span data-stu-id="26a84-102">Contains information about the file (not process) related to the alert.</span></span>

## <a name="properties"></a><span data-ttu-id="26a84-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="26a84-103">Properties</span></span>

| <span data-ttu-id="26a84-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="26a84-104">Property</span></span>   | <span data-ttu-id="26a84-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="26a84-105">Type</span></span>|<span data-ttu-id="26a84-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="26a84-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="26a84-107">fileHash</span><span class="sxs-lookup"><span data-stu-id="26a84-107">fileHash</span></span>|[<span data-ttu-id="26a84-108">fileHash</span><span class="sxs-lookup"><span data-stu-id="26a84-108">fileHash</span></span>](filehash.md)|<span data-ttu-id="26a84-109">Tipo complejo que contiene los valores de hash de archivo (criptográficos y dependientes de la ubicación).</span><span class="sxs-lookup"><span data-stu-id="26a84-109">Complex type containing file hashes (cryptographic and location-sensitive).</span></span>|
|<span data-ttu-id="26a84-110">name</span><span class="sxs-lookup"><span data-stu-id="26a84-110">name</span></span>|<span data-ttu-id="26a84-111">Cadena</span><span class="sxs-lookup"><span data-stu-id="26a84-111">String</span></span>|<span data-ttu-id="26a84-112">Nombre de archivo (sin ruta de acceso).</span><span class="sxs-lookup"><span data-stu-id="26a84-112">File name (without path).</span></span>|
|<span data-ttu-id="26a84-113">path</span><span class="sxs-lookup"><span data-stu-id="26a84-113">path</span></span>|<span data-ttu-id="26a84-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="26a84-114">String</span></span>|<span data-ttu-id="26a84-115">Ruta de acceso completa al archivo del archivo/imageFile.</span><span class="sxs-lookup"><span data-stu-id="26a84-115">Full file path of the stencil file</span></span>|
|<span data-ttu-id="26a84-116">riskScore</span><span class="sxs-lookup"><span data-stu-id="26a84-116">riskScore</span></span>|<span data-ttu-id="26a84-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="26a84-117">String</span></span>|<span data-ttu-id="26a84-118">Puntuación de riesgo calculado/generado por el proveedor del archivo de alerta.</span><span class="sxs-lookup"><span data-stu-id="26a84-118">Provider generated/calculated risk score of the alert file.</span></span> <span data-ttu-id="26a84-119">Intervalo de valores recomendados de 0 a 1, que equivale a un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="26a84-119">Recommended value range of 0-1, which equates to a percentage.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="26a84-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="26a84-120">JSON representation</span></span>

<span data-ttu-id="26a84-121">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="26a84-121">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.fileSecurityState"
}-->

```json
{
  "fileHash": {"@odata.type": "microsoft.graph.fileHash"},
  "name": "String",
  "path": "String",
  "riskScore": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "fileSecurityState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->