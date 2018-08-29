# <a name="groupsettingtemplate-resource-type"></a><span data-ttu-id="9bcea-101">Tipo de recurso groupSettingTemplate</span><span class="sxs-lookup"><span data-stu-id="9bcea-101">groupSettingTemplate resource type</span></span>

<span data-ttu-id="9bcea-p101">Las plantillas de configuración de grupo representan configuraciones definidas por el sistema disponibles para el inquilino. La [configuración de grupo](groupsetting.md) se puede crear según las plantillas de **groupSettingTemplates** disponibles y se pueden cambiar los valores predeterminados. Las plantillas de configuración de grupo no se pueden crear, actualizar ni eliminar. Esta configuración puede representar configuración para todo el inquilino o una para un grupo específico. Actualmente, las únicas plantillas disponibles se aplican a grupos de Office 365 e incluyen opciones como las que establecen si los usuarios pueden crear grupos o no, o si pueden invitar a usuarios de fuera de la organización para convertirse en miembros de un grupo.</span><span class="sxs-lookup"><span data-stu-id="9bcea-p101">Group setting templates represent system-defined settings available to the tenant. [Group settings](groupsetting.md) can be created based on the available **groupSettingTemplates**, and values changed from their preset defaults. Group setting templates cannot be created, updated or deleted. These settings can represent tenant-wide settings, or can represent specific group settings. Currently, the only templates available apply to Office 365 groups, and include settings such as whether users can create groups or invite guests from outside the organization to become members of a group.</span></span>

## <a name="methods"></a><span data-ttu-id="9bcea-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="9bcea-107">Methods</span></span>

| <span data-ttu-id="9bcea-108">Método</span><span class="sxs-lookup"><span data-stu-id="9bcea-108">Method</span></span> | <span data-ttu-id="9bcea-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9bcea-109">Return Type</span></span> | <span data-ttu-id="9bcea-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9bcea-110">Description</span></span> |
|:---------------|:--------|:----------|
|[<span data-ttu-id="9bcea-111">Get groupSettingTemplate</span><span class="sxs-lookup"><span data-stu-id="9bcea-111">Get groupSettingTemplate</span></span>](../api/groupsettingtemplate_get.md) | [<span data-ttu-id="9bcea-112">groupSettingTemplate</span><span class="sxs-lookup"><span data-stu-id="9bcea-112">groupSettingTemplate</span></span>](groupsettingtemplate.md) | <span data-ttu-id="9bcea-113">Lee las propiedades específicas de uno de los objetos groupSettingTemplate definido por el sistema.</span><span class="sxs-lookup"><span data-stu-id="9bcea-113">Read the specific properties of one of the system defined groupSettingTemplate objects.</span></span> |
|[<span data-ttu-id="9bcea-114">List groupSettingTemplate</span><span class="sxs-lookup"><span data-stu-id="9bcea-114">List groupSettingTemplate</span></span>](../api/groupsettingtemplate_list.md) | [<span data-ttu-id="9bcea-115">Colección de groupSettingTemplate</span><span class="sxs-lookup"><span data-stu-id="9bcea-115">Collection of groupSettingTemplate</span></span>](groupsettingtemplate.md) |<span data-ttu-id="9bcea-116">Enumera todos los objetos groupSettingTemplate definidos por el sistema.</span><span class="sxs-lookup"><span data-stu-id="9bcea-116">List all of the system defined groupSettingTemplate objects.</span></span>|

## <a name="properties"></a><span data-ttu-id="9bcea-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9bcea-117">Properties</span></span>

| <span data-ttu-id="9bcea-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9bcea-118">Property</span></span> | <span data-ttu-id="9bcea-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="9bcea-119">Type</span></span> | <span data-ttu-id="9bcea-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="9bcea-120">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="9bcea-121">description</span><span class="sxs-lookup"><span data-stu-id="9bcea-121">description</span></span>|<span data-ttu-id="9bcea-122">String</span><span class="sxs-lookup"><span data-stu-id="9bcea-122">String</span></span>| <span data-ttu-id="9bcea-123">Descripción de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="9bcea-123">Description of the template.</span></span> |
|<span data-ttu-id="9bcea-124">displayName</span><span class="sxs-lookup"><span data-stu-id="9bcea-124">displayName</span></span>|<span data-ttu-id="9bcea-125">String</span><span class="sxs-lookup"><span data-stu-id="9bcea-125">String</span></span>| <span data-ttu-id="9bcea-126">Muestra el nombre de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="9bcea-126">Display name of the template.</span></span> |
|<span data-ttu-id="9bcea-127">id</span><span class="sxs-lookup"><span data-stu-id="9bcea-127">id</span></span>|<span data-ttu-id="9bcea-128">String</span><span class="sxs-lookup"><span data-stu-id="9bcea-128">String</span></span>| <span data-ttu-id="9bcea-p102">Identificador único de la plantilla. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9bcea-p102">Unique identifier for the template. Read-only.</span></span>|
|<span data-ttu-id="9bcea-131">values</span><span class="sxs-lookup"><span data-stu-id="9bcea-131">values</span></span>|<span data-ttu-id="9bcea-132">Colección de [settingTemplateValue](settingtemplatevalue.md)</span><span class="sxs-lookup"><span data-stu-id="9bcea-132">[settingTemplateValue](settingtemplatevalue.md) collection</span></span>| <span data-ttu-id="9bcea-133">Colección de settingTemplateValues que enumera el conjunto de opciones disponibles, los valores predeterminados y los tipos que forman esta plantilla.</span><span class="sxs-lookup"><span data-stu-id="9bcea-133">Collection of settingTemplateValues that list the set of available settings, defaults and types that make up this template.</span></span> |

## <a name="relationships"></a><span data-ttu-id="9bcea-134">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9bcea-134">Relationships</span></span>

<span data-ttu-id="9bcea-135">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="9bcea-135">None.</span></span>


## <a name="json-representation"></a><span data-ttu-id="9bcea-136">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9bcea-136">JSON representation</span></span>

<span data-ttu-id="9bcea-137">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9bcea-137">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "openType": true,
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.directoryObject",
  "@odata.type": "microsoft.graph.groupSettingTemplate"
}-->

```json
{
  "description": "String",
  "displayName": "String",
  "id": "String (identifier)",
  "values": [{"@odata.type": "microsoft.graph.settingTemplateValue"}]
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "groupSettingTemplate resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->