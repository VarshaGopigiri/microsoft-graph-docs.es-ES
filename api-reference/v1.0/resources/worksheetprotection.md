# <a name="worksheetprotection-resource-type"></a><span data-ttu-id="4d809-101">Tipo de recurso WorksheetProtection</span><span class="sxs-lookup"><span data-stu-id="4d809-101">WorksheetProtection resource type</span></span>

<span data-ttu-id="4d809-102">Representa la protección de un objeto de hoja.</span><span class="sxs-lookup"><span data-stu-id="4d809-102">Represents the protection of a sheet object.</span></span>


## <a name="methods"></a><span data-ttu-id="4d809-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="4d809-103">Methods</span></span>

| <span data-ttu-id="4d809-104">Método</span><span class="sxs-lookup"><span data-stu-id="4d809-104">Method</span></span>           | <span data-ttu-id="4d809-105">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4d809-105">Return Type</span></span>    |<span data-ttu-id="4d809-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d809-106">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="4d809-107">Get WorksheetProtection</span><span class="sxs-lookup"><span data-stu-id="4d809-107">Get WorksheetProtection</span></span>](../api/worksheetprotection_get.md) | [<span data-ttu-id="4d809-108">WorkbookWorksheetProtection</span><span class="sxs-lookup"><span data-stu-id="4d809-108">WorkbookWorksheetProtection</span></span>](worksheetprotection.md) |<span data-ttu-id="4d809-109">Lee las propiedades y relaciones del objeto worksheetProtection.</span><span class="sxs-lookup"><span data-stu-id="4d809-109">Read properties and relationships of worksheetProtection object.</span></span>|
|[<span data-ttu-id="4d809-110">Protect</span><span class="sxs-lookup"><span data-stu-id="4d809-110">Protect</span></span>](../api/worksheetprotection_protect.md)|<span data-ttu-id="4d809-111">Ninguno</span><span class="sxs-lookup"><span data-stu-id="4d809-111">None</span></span>|<span data-ttu-id="4d809-p101">Proteger una hoja de cálculo. Produce una excepción si se ha protegido la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="4d809-p101">Protect a worksheet. It throws if the worksheet has been protected.</span></span>|
|[<span data-ttu-id="4d809-114">Unprotect</span><span class="sxs-lookup"><span data-stu-id="4d809-114">Unprotect</span></span>](../api/worksheetprotection_unprotect.md)|<span data-ttu-id="4d809-115">Ninguno</span><span class="sxs-lookup"><span data-stu-id="4d809-115">None</span></span>|<span data-ttu-id="4d809-116">Desprotege una hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="4d809-116">Unprotect a worksheet</span></span>|

## <a name="properties"></a><span data-ttu-id="4d809-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4d809-117">Properties</span></span>
| <span data-ttu-id="4d809-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4d809-118">Property</span></span>     | <span data-ttu-id="4d809-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="4d809-119">Type</span></span>   |<span data-ttu-id="4d809-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d809-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4d809-121">options</span><span class="sxs-lookup"><span data-stu-id="4d809-121">options</span></span>|[<span data-ttu-id="4d809-122">WorkbookWorksheetProtectionOptions</span><span class="sxs-lookup"><span data-stu-id="4d809-122">WorkbookWorksheetProtectionOptions</span></span>](worksheetprotectionoptions.md)|<span data-ttu-id="4d809-p102">Opciones de protección de la hoja. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4d809-p102">Sheet protection options. Read-only.</span></span>|
|<span data-ttu-id="4d809-125">protected</span><span class="sxs-lookup"><span data-stu-id="4d809-125">protected</span></span>|<span data-ttu-id="4d809-126">booleano</span><span class="sxs-lookup"><span data-stu-id="4d809-126">boolean</span></span>|<span data-ttu-id="4d809-p103">Indica si la hoja de cálculo está protegida.  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4d809-p103">Indicates if the worksheet is protected.  Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="4d809-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4d809-129">JSON representation</span></span>

<span data-ttu-id="4d809-130">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4d809-130">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookWorksheetProtection"
}-->

```json
{
  "protected": true,
  "options": { "@odata.type": "microsoft.graph.workbookWorksheetProtectionOptions" }
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "WorksheetProtection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->