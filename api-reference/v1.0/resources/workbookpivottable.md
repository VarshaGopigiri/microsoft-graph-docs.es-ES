# <a name="pivottable-resource-type"></a><span data-ttu-id="c170d-101">Tipo de recurso PivotTable</span><span class="sxs-lookup"><span data-stu-id="c170d-101">pivotTable resource type</span></span>

<span data-ttu-id="c170d-102">Representa una tabla dinámica de Excel.</span><span class="sxs-lookup"><span data-stu-id="c170d-102">Represents an Excel PivotTable.</span></span>

## <a name="methods"></a><span data-ttu-id="c170d-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="c170d-103">Methods</span></span>

| <span data-ttu-id="c170d-104">Método</span><span class="sxs-lookup"><span data-stu-id="c170d-104">Method</span></span>           | <span data-ttu-id="c170d-105">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c170d-105">Return Type</span></span>    |<span data-ttu-id="c170d-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="c170d-106">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="c170d-107">Get workbookPivotTable</span><span class="sxs-lookup"><span data-stu-id="c170d-107">Get workbookPivotTable</span></span>](../api/workbookpivottable_get.md) | [<span data-ttu-id="c170d-108">workbookPivotTable</span><span class="sxs-lookup"><span data-stu-id="c170d-108">workbookPivotTable</span></span>](workbookpivottable.md) |<span data-ttu-id="c170d-109">Lee las propiedades y relaciones del objeto workbookPivotTable.</span><span class="sxs-lookup"><span data-stu-id="c170d-109">Read properties and relationships of workbookPivotTable object.</span></span>|
|[<span data-ttu-id="c170d-110">Refresh</span><span class="sxs-lookup"><span data-stu-id="c170d-110">Refresh</span></span>](../api/workbookpivottable_refresh.md)|<span data-ttu-id="c170d-111">Ninguno</span><span class="sxs-lookup"><span data-stu-id="c170d-111">None</span></span>|<span data-ttu-id="c170d-112">Actualiza la tabla dinámica.</span><span class="sxs-lookup"><span data-stu-id="c170d-112">Refreshes the PivotTable.</span></span> |
|[<span data-ttu-id="c170d-113">Refreshall</span><span class="sxs-lookup"><span data-stu-id="c170d-113">Refreshall</span></span>](../api/workbookpivottable_refreshall.md)|<span data-ttu-id="c170d-114">Ninguno</span><span class="sxs-lookup"><span data-stu-id="c170d-114">None</span></span>|<span data-ttu-id="c170d-p101">Actualizar todas las tablas de una hoja de cálculo. Tenga en cuenta que esta acción sólo está disponible en la colección de tabla dinámica.</span><span class="sxs-lookup"><span data-stu-id="c170d-p101">Refresh all tables within given worksheet. Note that this action is available only on the pivot table collection.</span></span>|

## <a name="properties"></a><span data-ttu-id="c170d-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c170d-117">Properties</span></span>
| <span data-ttu-id="c170d-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c170d-118">Property</span></span>     | <span data-ttu-id="c170d-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="c170d-119">Type</span></span>   |<span data-ttu-id="c170d-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="c170d-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c170d-121">id</span><span class="sxs-lookup"><span data-stu-id="c170d-121">id</span></span>|<span data-ttu-id="c170d-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="c170d-122">String</span></span>| <span data-ttu-id="c170d-p102">ID la tabla dinámica.   Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c170d-p102">Id of the PivotTable.   Read-only.</span></span>|
|<span data-ttu-id="c170d-125">name</span><span class="sxs-lookup"><span data-stu-id="c170d-125">name</span></span>|<span data-ttu-id="c170d-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="c170d-126">String</span></span>|<span data-ttu-id="c170d-127">Nombre de la tabla dinámica.</span><span class="sxs-lookup"><span data-stu-id="c170d-127">Name of the PivotTable.</span></span>    |

## <a name="relationships"></a><span data-ttu-id="c170d-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c170d-128">Relationships</span></span>
| <span data-ttu-id="c170d-129">Relación</span><span class="sxs-lookup"><span data-stu-id="c170d-129">Relationship</span></span> | <span data-ttu-id="c170d-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="c170d-130">Type</span></span>   |<span data-ttu-id="c170d-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="c170d-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c170d-132">worksheet</span><span class="sxs-lookup"><span data-stu-id="c170d-132">worksheet</span></span>|[<span data-ttu-id="c170d-133">WorkbookWorksheet</span><span class="sxs-lookup"><span data-stu-id="c170d-133">WorkbookWorksheet</span></span>](worksheet.md)| <span data-ttu-id="c170d-p103">La hoja de cálculo que contiene la tabla dinámica actual. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c170d-p103">The worksheet containing the current PivotTable. Read-only.</span></span>   |

## <a name="json-representation"></a><span data-ttu-id="c170d-136">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c170d-136">JSON representation</span></span>
<span data-ttu-id="c170d-137">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c170d-137">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookPivotTable"
}-->

```json
{
  "id": "String (identifier)",
  "name": "String"
}

```
