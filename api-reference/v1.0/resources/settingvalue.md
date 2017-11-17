# <a name="settingvalue-resource-type"></a><span data-ttu-id="b4b03-101">Tipo de recurso settingValue</span><span class="sxs-lookup"><span data-stu-id="b4b03-101">settingValue resource type</span></span>

<span data-ttu-id="b4b03-102">Una configuración que representa un par nombre-valor.</span><span class="sxs-lookup"><span data-stu-id="b4b03-102">A setting represented by a name/value pair.</span></span>

### <a name="properties"></a><span data-ttu-id="b4b03-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b4b03-103">Properties</span></span>

| <span data-ttu-id="b4b03-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b4b03-104">Property</span></span> | <span data-ttu-id="b4b03-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="b4b03-105">Type</span></span> | <span data-ttu-id="b4b03-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4b03-106">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="b4b03-107">name</span><span class="sxs-lookup"><span data-stu-id="b4b03-107">name</span></span>|<span data-ttu-id="b4b03-108">String</span><span class="sxs-lookup"><span data-stu-id="b4b03-108">String</span></span>| <span data-ttu-id="b4b03-109">Nombre de la configuración (según lo definido por la plantilla [groupSettingTemplate](groupsettingtemplate.md)).</span><span class="sxs-lookup"><span data-stu-id="b4b03-109">Name of the setting (as defined by the [groupSettingTemplate](groupsettingtemplate.md)).</span></span> |
|<span data-ttu-id="b4b03-110">value</span><span class="sxs-lookup"><span data-stu-id="b4b03-110">value</span></span>|<span data-ttu-id="b4b03-111">String</span><span class="sxs-lookup"><span data-stu-id="b4b03-111">String</span></span>| <span data-ttu-id="b4b03-112">Valor de la configuración.</span><span class="sxs-lookup"><span data-stu-id="b4b03-112">Value of the setting.</span></span> |

### <a name="json-representation"></a><span data-ttu-id="b4b03-113">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b4b03-113">JSON representation</span></span>

<span data-ttu-id="b4b03-114">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b4b03-114">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.settingValue"
}-->

```json
{
  "name": "String",
  "value": "String"
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "settingValue resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->