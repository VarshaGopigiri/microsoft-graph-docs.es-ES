# <a name="quota-resource-type"></a><span data-ttu-id="58c1e-101">Tipo de recurso Quota</span><span class="sxs-lookup"><span data-stu-id="58c1e-101">Quota resource type</span></span>

<span data-ttu-id="58c1e-102">El recurso **quota** proporciona detalles sobre las limitaciones de espacio en un recurso [Drive](drive.md).</span><span class="sxs-lookup"><span data-stu-id="58c1e-102">The **quota** resource provides details about space constrains on a [Drive](drive.md) resource.</span></span>

## <a name="json-representation"></a><span data-ttu-id="58c1e-103">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="58c1e-103">JSON representation</span></span>

<span data-ttu-id="58c1e-104">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="58c1e-104">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@odata.type": "microsoft.graph.quota"
}-->

```json
{
  "deleted": 1024,
  "remaining": 1024,
  "state": "normal | nearing | critical | exceeded",
  "total": 1024,
  "used": 1024
}
```

## <a name="properties"></a><span data-ttu-id="58c1e-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="58c1e-105">Properties</span></span>

| <span data-ttu-id="58c1e-106">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="58c1e-106">Property name</span></span> | <span data-ttu-id="58c1e-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="58c1e-107">Type</span></span>   | <span data-ttu-id="58c1e-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="58c1e-108">Description</span></span>                                                                 |
|:--------------|:-------|:----------------------------------------------------------------------------|
| <span data-ttu-id="58c1e-109">total</span><span class="sxs-lookup"><span data-stu-id="58c1e-109">total</span></span>         | <span data-ttu-id="58c1e-110">Int64</span><span class="sxs-lookup"><span data-stu-id="58c1e-110">Int64</span></span>  | <span data-ttu-id="58c1e-p101">Espacio total de almacenamiento permitido, en bytes. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="58c1e-p101">Total allowed storage space, in bytes. Read-only.</span></span>                           |
| <span data-ttu-id="58c1e-113">used</span><span class="sxs-lookup"><span data-stu-id="58c1e-113">used</span></span>          | <span data-ttu-id="58c1e-114">Int64</span><span class="sxs-lookup"><span data-stu-id="58c1e-114">Int64</span></span>  | <span data-ttu-id="58c1e-p102">Espacio total usado, en bytes. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="58c1e-p102">Total space used, in bytes. Read-only.</span></span>                                      |
| <span data-ttu-id="58c1e-117">remaining</span><span class="sxs-lookup"><span data-stu-id="58c1e-117">remaining</span></span>     | <span data-ttu-id="58c1e-118">Int64</span><span class="sxs-lookup"><span data-stu-id="58c1e-118">Int64</span></span>  | <span data-ttu-id="58c1e-p103">Espacio total restante antes de alcanzar el límite de cuota, en bytes. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="58c1e-p103">Total space remaining before reaching the quota limit, in bytes. Read-only.</span></span> |
| <span data-ttu-id="58c1e-121">deleted</span><span class="sxs-lookup"><span data-stu-id="58c1e-121">deleted</span></span>       | <span data-ttu-id="58c1e-122">Int64</span><span class="sxs-lookup"><span data-stu-id="58c1e-122">Int64</span></span>  | <span data-ttu-id="58c1e-p104">Espacio total consumido por los archivos de la Papelera de reciclaje, en bytes. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="58c1e-p104">Total space consumed by files in the recycle bin, in bytes. Read-only.</span></span>      |
| <span data-ttu-id="58c1e-125">estado</span><span class="sxs-lookup"><span data-stu-id="58c1e-125">state</span></span>         | <span data-ttu-id="58c1e-126">string</span><span class="sxs-lookup"><span data-stu-id="58c1e-126">string</span></span> | <span data-ttu-id="58c1e-p105">Valor de enumeración que indica el estado del espacio de almacenamiento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="58c1e-p105">Enumeration value that indicates the state of the storage space. Read-only.</span></span> |

## <a name="state-enumeration"></a><span data-ttu-id="58c1e-129">Enumeración de estado</span><span class="sxs-lookup"><span data-stu-id="58c1e-129">State Enumeration</span></span>

| <span data-ttu-id="58c1e-130">Valor</span><span class="sxs-lookup"><span data-stu-id="58c1e-130">Value</span></span>      | <span data-ttu-id="58c1e-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="58c1e-131">Description</span></span>                                                                                                                                                                 |
|:-----------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `normal`   | <span data-ttu-id="58c1e-132">A la unidad le queda mucha cuota restante.</span><span class="sxs-lookup"><span data-stu-id="58c1e-132">The drive has plenty of remaining quota left.</span></span>                                                                                                                               |
| `nearing`  | <span data-ttu-id="58c1e-133">La cuota restante es inferior al 10 % del espacio total de cuota.</span><span class="sxs-lookup"><span data-stu-id="58c1e-133">Remaining quota is less than 10% of total quota space.</span></span>                                                                                                                      |
| `critical` | <span data-ttu-id="58c1e-134">La cuota restante es inferior al 1 % del espacio total de cuota.</span><span class="sxs-lookup"><span data-stu-id="58c1e-134">Remaining quota is less than 1% of total quota space.</span></span>                                                                                                                       |
| `exceeded` | <span data-ttu-id="58c1e-p106">La cuota usada ha superado la cuota total. No se pueden agregar nuevos archivos ni carpetas en la unidad hasta que esté por debajo de la cantidad total de cuota o se adquiera más espacio de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="58c1e-p106">The used quota has exceeded the total quota. New files or folders cannot be added to the drive until it is under the total quota amount or more storage space is purchased.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "quota resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
