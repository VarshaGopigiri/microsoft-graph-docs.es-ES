# <a name="settingtemplatevalue-resource-type"></a><span data-ttu-id="68f71-101">Tipo de recurso settingTemplateValue</span><span class="sxs-lookup"><span data-stu-id="68f71-101">settingTemplateValue resource type</span></span>

<span data-ttu-id="68f71-102">Representa una definición de configuración de plantilla individual, incluido el valor predeterminado de la configuración, en caso de que la configuración no tenga instancias.</span><span class="sxs-lookup"><span data-stu-id="68f71-102">Represents an individual template setting definition, including the default value for the setting, if the setting is not instantiated.</span></span>

### <a name="properties"></a><span data-ttu-id="68f71-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="68f71-103">Properties</span></span>

| <span data-ttu-id="68f71-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="68f71-104">Property</span></span> | <span data-ttu-id="68f71-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="68f71-105">Type</span></span> | <span data-ttu-id="68f71-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="68f71-106">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="68f71-107">defaultValue</span><span class="sxs-lookup"><span data-stu-id="68f71-107">DefaultValue</span></span>|<span data-ttu-id="68f71-108">String</span><span class="sxs-lookup"><span data-stu-id="68f71-108">String</span></span>| <span data-ttu-id="68f71-109">Valor predeterminado para la configuración.</span><span class="sxs-lookup"><span data-stu-id="68f71-109">Default value for the setting.</span></span> |
|<span data-ttu-id="68f71-110">description</span><span class="sxs-lookup"><span data-stu-id="68f71-110">description</span></span>|<span data-ttu-id="68f71-111">String</span><span class="sxs-lookup"><span data-stu-id="68f71-111">String</span></span>| <span data-ttu-id="68f71-112">Descripción de la configuración.</span><span class="sxs-lookup"><span data-stu-id="68f71-112">Description of the component.</span></span> |
|<span data-ttu-id="68f71-113">nombre</span><span class="sxs-lookup"><span data-stu-id="68f71-113">name</span></span>|<span data-ttu-id="68f71-114">String</span><span class="sxs-lookup"><span data-stu-id="68f71-114">String</span></span>| <span data-ttu-id="68f71-115">Nombre de la configuración.</span><span class="sxs-lookup"><span data-stu-id="68f71-115">Name of the setting.</span></span> |
|<span data-ttu-id="68f71-116">tipo</span><span class="sxs-lookup"><span data-stu-id="68f71-116">type</span></span>|<span data-ttu-id="68f71-117">String</span><span class="sxs-lookup"><span data-stu-id="68f71-117">String</span></span>| <span data-ttu-id="68f71-118">Tipo de la configuración.</span><span class="sxs-lookup"><span data-stu-id="68f71-118">Key of the setting.</span></span> |

### <a name="json-representation"></a><span data-ttu-id="68f71-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="68f71-119">JSON representation</span></span>

<span data-ttu-id="68f71-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="68f71-120">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.settingTemplateValue"
}-->

```json
{
  "defaultValue": "String",
  "description": "String",
  "name": "String",
  "type": "String"
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "settingTemplateValue resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->