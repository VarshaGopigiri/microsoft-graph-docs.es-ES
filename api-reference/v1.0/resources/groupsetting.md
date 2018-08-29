# <a name="groupsetting-resource-type"></a><span data-ttu-id="90a0b-101">Tipo de recurso groupSetting</span><span class="sxs-lookup"><span data-stu-id="90a0b-101">groupSetting resource type</span></span>

<span data-ttu-id="90a0b-102">Comportamientos del control de configuración de grupo, como listas de palabras bloqueadas para los nombres para mostrar del grupo o si los usuarios invitados pueden ser propietarios del grupo.</span><span class="sxs-lookup"><span data-stu-id="90a0b-102">Group settings control behaviors such as blocked word lists for group display names or whether guest users are allowed to be group owners.</span></span>

<span data-ttu-id="90a0b-p101">La configuración de grupo se puede crear según las plantillas de [groupSettingTemplates](groupSettingTemplate.md) disponibles y se pueden cambiar los valores predeterminados. Esta configuración controla el comportamiento del grupo a nivel de todo el inquilino o en un grupo específico. Cuando se establece la misma configuración a nivel de todo el inquilino y en un grupo específico, la configuración de nivel de grupo reemplaza la configuración a nivel de inquilino.  Por ejemplo, puede que una configuración a nivel de todo el inquilino permite que los miembros existentes inviten a otros usuarios, pero la configuración de un grupo concreto puede reemplazarla y no permitir que los miembros del grupo puedan invitar a otros usuarios como invitados. La configuración de grupo solo controla el comportamiento de los grupos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="90a0b-p101">Group settings can be created based on the available [groupSettingTemplates](groupSettingTemplate.md), and changed from their preset defaults. These settings govern group behaviors at a tenant-wide level or to a specific group. When the same setting is defined at both the tenant-wide and to a specific group, the group-level setting overrides the tenant-wide setting.  For example, the tenant-wide setting may allow guests to be invited by existing members of groups, but an individual group setting can override and not allow guests to be invited by members of the group. Group settings only govern Office 365 groups behavior.</span></span>

## <a name="methods"></a><span data-ttu-id="90a0b-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="90a0b-108">Methods</span></span>

| <span data-ttu-id="90a0b-109">Método</span><span class="sxs-lookup"><span data-stu-id="90a0b-109">Method</span></span> | <span data-ttu-id="90a0b-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90a0b-110">Return Type</span></span> | <span data-ttu-id="90a0b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="90a0b-111">Description</span></span> |
|:---------------|:--------|:----------|
|[<span data-ttu-id="90a0b-112">Create setting</span><span class="sxs-lookup"><span data-stu-id="90a0b-112">Create setting</span></span>](../api/groupsetting_post_groupsettings.md) | [<span data-ttu-id="90a0b-113">groupSetting</span><span class="sxs-lookup"><span data-stu-id="90a0b-113">groupSetting</span></span>](groupsetting.md) |<span data-ttu-id="90a0b-p102">Crea un objeto de configuración según una plantilla de groupSettingTemplate. La solicitud POST debe proporcionar settingValues para toda la configuración establecida en la plantilla.</span><span class="sxs-lookup"><span data-stu-id="90a0b-p102">Create a setting object based on a groupSettingTemplate. The POST request must provide settingValues for all the settings defined in the template.</span></span> |
|[<span data-ttu-id="90a0b-116">Get setting</span><span class="sxs-lookup"><span data-stu-id="90a0b-116">Get setting</span></span>](../api/groupsetting_get.md) | [<span data-ttu-id="90a0b-117">groupSetting</span><span class="sxs-lookup"><span data-stu-id="90a0b-117">groupSetting</span></span>](groupsetting.md) | <span data-ttu-id="90a0b-118">Lee las propiedades de un objeto de configuración específico.</span><span class="sxs-lookup"><span data-stu-id="90a0b-118">Read properties of a specific setting object.</span></span> |
|[<span data-ttu-id="90a0b-119">List settings</span><span class="sxs-lookup"><span data-stu-id="90a0b-119">List settings</span></span>](../api/groupsetting_list.md) | <span data-ttu-id="90a0b-120">Colección de [groupSetting](groupsetting.md)</span><span class="sxs-lookup"><span data-stu-id="90a0b-120">[groupSetting](groupsetting.md) collection</span></span> | <span data-ttu-id="90a0b-121">Enumera las propiedades de todos los objetos de configuración.</span><span class="sxs-lookup"><span data-stu-id="90a0b-121">List properties of all setting objects.</span></span> |
|[<span data-ttu-id="90a0b-122">Update setting</span><span class="sxs-lookup"><span data-stu-id="90a0b-122">Update setting</span></span>](../api/groupsetting_update.md) | [<span data-ttu-id="90a0b-123">groupSetting</span><span class="sxs-lookup"><span data-stu-id="90a0b-123">groupSetting</span></span>](groupsetting.md) | <span data-ttu-id="90a0b-124">Actualiza el objeto groupSetting.</span><span class="sxs-lookup"><span data-stu-id="90a0b-124">Update groupsetting object.</span></span> |
|[<span data-ttu-id="90a0b-125">Delete setting</span><span class="sxs-lookup"><span data-stu-id="90a0b-125">Delete setting</span></span>](../api/groupsetting_delete.md) | <span data-ttu-id="90a0b-126">Ninguno</span><span class="sxs-lookup"><span data-stu-id="90a0b-126">None</span></span> | <span data-ttu-id="90a0b-127">Elimina un objeto de configuración.</span><span class="sxs-lookup"><span data-stu-id="90a0b-127">Delete a setting object.</span></span> |

## <a name="properties"></a><span data-ttu-id="90a0b-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="90a0b-128">Properties</span></span>

| <span data-ttu-id="90a0b-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="90a0b-129">Property</span></span> | <span data-ttu-id="90a0b-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="90a0b-130">Type</span></span> | <span data-ttu-id="90a0b-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="90a0b-131">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="90a0b-132">displayName</span><span class="sxs-lookup"><span data-stu-id="90a0b-132">displayName</span></span>|<span data-ttu-id="90a0b-133">String</span><span class="sxs-lookup"><span data-stu-id="90a0b-133">String</span></span>| <span data-ttu-id="90a0b-134">El nombre para mostrar de este grupo de configuraciones, que proviene de la plantilla asociada.</span><span class="sxs-lookup"><span data-stu-id="90a0b-134">Display name of this group of settings, which comes from the associated template.</span></span> |
|<span data-ttu-id="90a0b-135">id</span><span class="sxs-lookup"><span data-stu-id="90a0b-135">id</span></span>|<span data-ttu-id="90a0b-136">String</span><span class="sxs-lookup"><span data-stu-id="90a0b-136">String</span></span>| <span data-ttu-id="90a0b-p103">Identificador único de esta configuración. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="90a0b-p103">Unique identifier for these settings. Read-only.</span></span> |
|<span data-ttu-id="90a0b-139">templateId</span><span class="sxs-lookup"><span data-stu-id="90a0b-139">templateId</span></span>|<span data-ttu-id="90a0b-140">String</span><span class="sxs-lookup"><span data-stu-id="90a0b-140">String</span></span>| <span data-ttu-id="90a0b-p104">Identificador único para la plantilla que se usa para crear este grupo de configuraciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="90a0b-p104">Unique identifier for the template used to create this group of settings. Read-only.</span></span> |
|<span data-ttu-id="90a0b-143">values</span><span class="sxs-lookup"><span data-stu-id="90a0b-143">values</span></span>|<span data-ttu-id="90a0b-144">Colección de [settingValue](settingvalue.md)</span><span class="sxs-lookup"><span data-stu-id="90a0b-144">[settingValue](settingvalue.md) collection</span></span>| <span data-ttu-id="90a0b-p105">Colección de pares de nombre y valor. Debe contener y establecer todas las configuraciones definidas en la plantilla.</span><span class="sxs-lookup"><span data-stu-id="90a0b-p105">Collection of name value pairs. Must contain and set all the settings defined in the template.</span></span> |

## <a name="relationships"></a><span data-ttu-id="90a0b-147">Relaciones</span><span class="sxs-lookup"><span data-stu-id="90a0b-147">Relationships</span></span>

<span data-ttu-id="90a0b-148">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="90a0b-148">None.</span></span>

## <a name="json-representation"></a><span data-ttu-id="90a0b-149">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="90a0b-149">JSON representation</span></span>

<span data-ttu-id="90a0b-150">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="90a0b-150">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "openType": true,
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.groupSetting"
}-->

```json
{
  "displayName": "String",
  "id": "String (identifier)",
  "templateId": "String",
  "values": [{"@odata.type": "microsoft.graph.settingValue"}]
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "groupSetting resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->