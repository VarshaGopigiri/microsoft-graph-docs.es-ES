# <a name="appconfigurationsettingitem-resource-type"></a><span data-ttu-id="b609d-101">Tipo de recurso appConfigurationSettingItem</span><span class="sxs-lookup"><span data-stu-id="b609d-101">appConfigurationSettingItem resource type</span></span>

> <span data-ttu-id="b609d-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b609d-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b609d-103">Contiene las propiedades del elemento de configuración de la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b609d-103">Contains properties for App configuration setting item.</span></span>
## <a name="properties"></a><span data-ttu-id="b609d-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b609d-104">Properties</span></span>
|<span data-ttu-id="b609d-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b609d-105">Property</span></span>|<span data-ttu-id="b609d-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="b609d-106">Type</span></span>|<span data-ttu-id="b609d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="b609d-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b609d-108">appConfigKey</span><span class="sxs-lookup"><span data-stu-id="b609d-108">appConfigKey</span></span>|<span data-ttu-id="b609d-109">Cadena</span><span class="sxs-lookup"><span data-stu-id="b609d-109">String</span></span>|<span data-ttu-id="b609d-110">Clave de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b609d-110">app configuration key.</span></span>|
|<span data-ttu-id="b609d-111">appConfigKeyType</span><span class="sxs-lookup"><span data-stu-id="b609d-111">appConfigKeyType</span></span>|[<span data-ttu-id="b609d-112">mdmAppConfigKeyType</span><span class="sxs-lookup"><span data-stu-id="b609d-112">mdmAppConfigKeyType</span></span>](../resources/intune_apps_mdmappconfigkeytype.md)|<span data-ttu-id="b609d-113">Tipo de clave de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b609d-113">app configuration key type.</span></span> <span data-ttu-id="b609d-114">Los valores posibles son: `stringType`, `integerType`, `realType`, `booleanType` y `tokenType`.</span><span class="sxs-lookup"><span data-stu-id="b609d-114">Possible values are: `stringType`, `integerType`, `realType`, `booleanType`, `tokenType`.</span></span>|
|<span data-ttu-id="b609d-115">appConfigKeyValue</span><span class="sxs-lookup"><span data-stu-id="b609d-115">appConfigKeyValue</span></span>|<span data-ttu-id="b609d-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="b609d-116">String</span></span>|<span data-ttu-id="b609d-117">Valor de clave de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b609d-117">app configuration key value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="b609d-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b609d-118">Relationships</span></span>
<span data-ttu-id="b609d-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="b609d-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="b609d-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b609d-120">JSON Representation</span></span>
<span data-ttu-id="b609d-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b609d-121">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.appConfigurationSettingItem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.appConfigurationSettingItem",
  "appConfigKey": "String",
  "appConfigKeyType": "String",
  "appConfigKeyValue": "String"
}
```



