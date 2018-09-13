# <a name="appconfigurationsettingitem-resource-type"></a><span data-ttu-id="35587-101">Tipo de recurso appConfigurationSettingItem</span><span class="sxs-lookup"><span data-stu-id="35587-101">appConfigurationSettingItem resource type</span></span>

> <span data-ttu-id="35587-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="35587-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="35587-103">Contiene las propiedades del elemento de configuración de la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="35587-103">Contains properties for App configuration setting item.</span></span>
## <a name="properties"></a><span data-ttu-id="35587-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="35587-104">Properties</span></span>
|<span data-ttu-id="35587-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="35587-105">Property</span></span>|<span data-ttu-id="35587-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="35587-106">Type</span></span>|<span data-ttu-id="35587-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="35587-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="35587-108">appConfigKey</span><span class="sxs-lookup"><span data-stu-id="35587-108">appConfigKey</span></span>|<span data-ttu-id="35587-109">Cadena</span><span class="sxs-lookup"><span data-stu-id="35587-109">String</span></span>|<span data-ttu-id="35587-110">Clave de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="35587-110">app configuration key.</span></span>|
|<span data-ttu-id="35587-111">appConfigKeyType</span><span class="sxs-lookup"><span data-stu-id="35587-111">appConfigKeyType</span></span>|[<span data-ttu-id="35587-112">mdmAppConfigKeyType</span><span class="sxs-lookup"><span data-stu-id="35587-112">mdmAppConfigKeyType</span></span>](../resources/intune_apps_mdmappconfigkeytype.md)|<span data-ttu-id="35587-p101">Tipo de clave de configuración de aplicación. Los valores posibles son: `stringType`, `integerType`, `realType`, `booleanType`, `tokenType`.</span><span class="sxs-lookup"><span data-stu-id="35587-p101">app configuration key type. The possible values are: `stringType`, `integerType`, `realType`, `booleanType`, `tokenType`.</span></span>|
|<span data-ttu-id="35587-115">appConfigKeyValue</span><span class="sxs-lookup"><span data-stu-id="35587-115">appConfigKeyValue</span></span>|<span data-ttu-id="35587-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="35587-116">String</span></span>|<span data-ttu-id="35587-117">Valor de clave de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="35587-117">app configuration key value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="35587-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="35587-118">Relationships</span></span>
<span data-ttu-id="35587-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="35587-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="35587-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="35587-120">JSON Representation</span></span>
<span data-ttu-id="35587-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="35587-121">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.appConfigurationSettingItem"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.appConfigurationSettingItem",
  "appConfigKey": "String",
  "appConfigKeyType": "String",
  "appConfigKeyValue": "String"
}
```








