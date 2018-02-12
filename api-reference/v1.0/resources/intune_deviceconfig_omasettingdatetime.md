# <a name="omasettingdatetime-resource-type"></a><span data-ttu-id="84bbf-101">Tipo de recurso omaSettingDateTime</span><span class="sxs-lookup"><span data-stu-id="84bbf-101">omaSettingDateTime resource type</span></span>

> <span data-ttu-id="84bbf-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="84bbf-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="84bbf-103">Definición de DateTime de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="84bbf-103">OMA Settings DateTime definition.</span></span>

<span data-ttu-id="84bbf-104">Hereda de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="84bbf-104">Inherits from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="84bbf-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="84bbf-105">Properties</span></span>
|<span data-ttu-id="84bbf-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="84bbf-106">Property</span></span>|<span data-ttu-id="84bbf-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="84bbf-107">Type</span></span>|<span data-ttu-id="84bbf-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="84bbf-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="84bbf-109">displayName</span><span class="sxs-lookup"><span data-stu-id="84bbf-109">displayName</span></span>|<span data-ttu-id="84bbf-110">cadena</span><span class="sxs-lookup"><span data-stu-id="84bbf-110">String</span></span>|<span data-ttu-id="84bbf-111">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="84bbf-111">Display Name</span></span> <span data-ttu-id="84bbf-112">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="84bbf-112">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="84bbf-113">description</span><span class="sxs-lookup"><span data-stu-id="84bbf-113">description</span></span>|<span data-ttu-id="84bbf-114">cadena</span><span class="sxs-lookup"><span data-stu-id="84bbf-114">String</span></span>|<span data-ttu-id="84bbf-115">Descripción.</span><span class="sxs-lookup"><span data-stu-id="84bbf-115">Description.</span></span> <span data-ttu-id="84bbf-116">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="84bbf-116">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="84bbf-117">omaUri</span><span class="sxs-lookup"><span data-stu-id="84bbf-117">omaUri</span></span>|<span data-ttu-id="84bbf-118">cadena</span><span class="sxs-lookup"><span data-stu-id="84bbf-118">String</span></span>|<span data-ttu-id="84bbf-119">OMA.</span><span class="sxs-lookup"><span data-stu-id="84bbf-119">OMA.</span></span> <span data-ttu-id="84bbf-120">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="84bbf-120">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="84bbf-121">value</span><span class="sxs-lookup"><span data-stu-id="84bbf-121">value</span></span>|<span data-ttu-id="84bbf-122">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="84bbf-122">DateTimeOffset</span></span>|<span data-ttu-id="84bbf-123">Valor.</span><span class="sxs-lookup"><span data-stu-id="84bbf-123">Value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="84bbf-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="84bbf-124">Relationships</span></span>
<span data-ttu-id="84bbf-125">Ninguna</span><span class="sxs-lookup"><span data-stu-id="84bbf-125">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="84bbf-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="84bbf-126">JSON Representation</span></span>
<span data-ttu-id="84bbf-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="84bbf-127">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.omaSettingDateTime"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSettingDateTime",
  "displayName": "String",
  "description": "String",
  "omaUri": "String",
  "value": "String (timestamp)"
}
```



