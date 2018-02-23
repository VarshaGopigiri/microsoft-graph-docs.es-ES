# <a name="androidforworkappconfigurationschemaitem-resource-type"></a><span data-ttu-id="222bc-101">Tipo de recurso androidForWorkAppConfigurationSchemaItem</span><span class="sxs-lookup"><span data-stu-id="222bc-101">androidForWorkAppConfigurationSchemaItem resource type</span></span>

> <span data-ttu-id="222bc-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="222bc-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="222bc-103">Elemento de configuración único dentro del esquema de configuración personalizada de la aplicación de Android for Work.</span><span class="sxs-lookup"><span data-stu-id="222bc-103">Single configuration item inside an Android for Work application's custom configuration schema.</span></span>
## <a name="properties"></a><span data-ttu-id="222bc-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="222bc-104">Properties</span></span>
|<span data-ttu-id="222bc-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="222bc-105">Property</span></span>|<span data-ttu-id="222bc-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="222bc-106">Type</span></span>|<span data-ttu-id="222bc-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="222bc-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="222bc-108">schemaItemKey</span><span class="sxs-lookup"><span data-stu-id="222bc-108">schemaItemKey</span></span>|<span data-ttu-id="222bc-109">Cadena</span><span class="sxs-lookup"><span data-stu-id="222bc-109">String</span></span>|<span data-ttu-id="222bc-110">La clave única que usa la aplicación para identificar el elemento</span><span class="sxs-lookup"><span data-stu-id="222bc-110">Unique key the application uses to identify the item</span></span>|
|<span data-ttu-id="222bc-111">displayName</span><span class="sxs-lookup"><span data-stu-id="222bc-111">displayName</span></span>|<span data-ttu-id="222bc-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="222bc-112">String</span></span>|<span data-ttu-id="222bc-113">Nombre legible</span><span class="sxs-lookup"><span data-stu-id="222bc-113">Human readable name</span></span>|
|<span data-ttu-id="222bc-114">description</span><span class="sxs-lookup"><span data-stu-id="222bc-114">description</span></span>|<span data-ttu-id="222bc-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="222bc-115">String</span></span>|<span data-ttu-id="222bc-116">Descripción de lo que controla el elemento dentro de la aplicación</span><span class="sxs-lookup"><span data-stu-id="222bc-116">Description of what the item controls within the application</span></span>|
|<span data-ttu-id="222bc-117">defaultBoolValue</span><span class="sxs-lookup"><span data-stu-id="222bc-117">defaultBoolValue</span></span>|<span data-ttu-id="222bc-118">Booleano</span><span class="sxs-lookup"><span data-stu-id="222bc-118">Boolean</span></span>|<span data-ttu-id="222bc-119">Valor predeterminado para los elementos de tipo booleano, si lo especifica el desarrollador de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="222bc-119">Default value for boolean type items, if specified by the app developer</span></span>|
|<span data-ttu-id="222bc-120">defaultIntValue</span><span class="sxs-lookup"><span data-stu-id="222bc-120">defaultIntValue</span></span>|<span data-ttu-id="222bc-121">Int32</span><span class="sxs-lookup"><span data-stu-id="222bc-121">Int32</span></span>|<span data-ttu-id="222bc-122">Valor predeterminado para los elementos de tipo entero, si lo especifica el desarrollador de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="222bc-122">Default value for integer type items, if specified by the app developer</span></span>|
|<span data-ttu-id="222bc-123">defaultStringValue</span><span class="sxs-lookup"><span data-stu-id="222bc-123">defaultStringValue</span></span>|<span data-ttu-id="222bc-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="222bc-124">String</span></span>|<span data-ttu-id="222bc-125">Valor predeterminado para los elementos de tipo cadena, si lo especifica el desarrollador de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="222bc-125">Default value for string type items, if specified by the app developer</span></span>|
|<span data-ttu-id="222bc-126">defaultStringArrayValue</span><span class="sxs-lookup"><span data-stu-id="222bc-126">defaultStringArrayValue</span></span>|<span data-ttu-id="222bc-127">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="222bc-127">String collection</span></span>|<span data-ttu-id="222bc-128">Valor predeterminado para los elementos de tipo matriz de cadenas, si lo especifica el desarrollador de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="222bc-128">Default value for string array type items, if specified by the app developer</span></span>|
|<span data-ttu-id="222bc-129">dataType</span><span class="sxs-lookup"><span data-stu-id="222bc-129">DataType</span></span>|<span data-ttu-id="222bc-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="222bc-130">String</span></span>|<span data-ttu-id="222bc-131">El tipo de valor que describe este elemento. Los valores posibles son: `bool`, `integer`, `string`, `choice`, `multiselect`, `bundle`, `bundleArray` y `hidden`.</span><span class="sxs-lookup"><span data-stu-id="222bc-131">The type of value this item describes Possible values are: `bool`, `integer`, `string`, `choice`, `multiselect`, `bundle`, `bundleArray`, `hidden`.</span></span>|
|<span data-ttu-id="222bc-132">selecciones</span><span class="sxs-lookup"><span data-stu-id="222bc-132">selections</span></span>|<span data-ttu-id="222bc-133">Colección [keyValuePair](../resources/intune_androidforwork_keyvaluepair.md)</span><span class="sxs-lookup"><span data-stu-id="222bc-133">[keyValuePair](../resources/intune_androidforwork_keyvaluepair.md) collection</span></span>|<span data-ttu-id="222bc-134">Lista de los pares nombre-valor legibles para los valores válidos que se pueden establecer para este elemento (solo elementos de selección de opciones múltiples)</span><span class="sxs-lookup"><span data-stu-id="222bc-134">List of human readable name/value pairs for the valid values that can be set for this item (Choice and Multiselect items only)</span></span>|

## <a name="relationships"></a><span data-ttu-id="222bc-135">Relaciones</span><span class="sxs-lookup"><span data-stu-id="222bc-135">Relationships</span></span>
<span data-ttu-id="222bc-136">Ninguna</span><span class="sxs-lookup"><span data-stu-id="222bc-136">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="222bc-137">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="222bc-137">JSON Representation</span></span>
<span data-ttu-id="222bc-138">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="222bc-138">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.androidForWorkAppConfigurationSchemaItem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidForWorkAppConfigurationSchemaItem",
  "schemaItemKey": "String",
  "displayName": "String",
  "description": "String",
  "defaultBoolValue": true,
  "defaultIntValue": 1024,
  "defaultStringValue": "String",
  "defaultStringArrayValue": [
    "String"
  ],
  "dataType": "String",
  "selections": [
    {
      "@odata.type": "microsoft.graph.keyValuePair",
      "name": "String",
      "value": "String"
    }
  ]
}
```



