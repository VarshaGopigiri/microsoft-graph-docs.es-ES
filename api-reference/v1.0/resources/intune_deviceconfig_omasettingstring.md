# <a name="omasettingstring-resource-type"></a><span data-ttu-id="805f3-101">Tipo de recurso omaSettingString</span><span class="sxs-lookup"><span data-stu-id="805f3-101">omaSettingString resource type</span></span>

> <span data-ttu-id="805f3-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="805f3-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="805f3-103">Definición de la cadena de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="805f3-103">OMA Settings String definition.</span></span>

<span data-ttu-id="805f3-104">Hereda de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="805f3-104">Inherits from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="805f3-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="805f3-105">Properties</span></span>
|<span data-ttu-id="805f3-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="805f3-106">Property</span></span>|<span data-ttu-id="805f3-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="805f3-107">Type</span></span>|<span data-ttu-id="805f3-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="805f3-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="805f3-109">displayName</span><span class="sxs-lookup"><span data-stu-id="805f3-109">displayName</span></span>|<span data-ttu-id="805f3-110">cadena</span><span class="sxs-lookup"><span data-stu-id="805f3-110">String</span></span>|<span data-ttu-id="805f3-111">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="805f3-111">Display Name.</span></span> <span data-ttu-id="805f3-112">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="805f3-112">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="805f3-113">description</span><span class="sxs-lookup"><span data-stu-id="805f3-113">description</span></span>|<span data-ttu-id="805f3-114">cadena</span><span class="sxs-lookup"><span data-stu-id="805f3-114">String</span></span>|<span data-ttu-id="805f3-115">Descripción.</span><span class="sxs-lookup"><span data-stu-id="805f3-115">Description.</span></span> <span data-ttu-id="805f3-116">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="805f3-116">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="805f3-117">omaUri</span><span class="sxs-lookup"><span data-stu-id="805f3-117">omaUri</span></span>|<span data-ttu-id="805f3-118">cadena</span><span class="sxs-lookup"><span data-stu-id="805f3-118">String</span></span>|<span data-ttu-id="805f3-119">OMA.</span><span class="sxs-lookup"><span data-stu-id="805f3-119">OMA.</span></span> <span data-ttu-id="805f3-120">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="805f3-120">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="805f3-121">value</span><span class="sxs-lookup"><span data-stu-id="805f3-121">value</span></span>|<span data-ttu-id="805f3-122">cadena</span><span class="sxs-lookup"><span data-stu-id="805f3-122">String</span></span>|<span data-ttu-id="805f3-123">Valor.</span><span class="sxs-lookup"><span data-stu-id="805f3-123">Value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="805f3-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="805f3-124">Relationships</span></span>
<span data-ttu-id="805f3-125">Ninguna</span><span class="sxs-lookup"><span data-stu-id="805f3-125">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="805f3-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="805f3-126">JSON Representation</span></span>
<span data-ttu-id="805f3-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="805f3-127">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.omaSettingString"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSettingString",
  "displayName": "String",
  "description": "String",
  "omaUri": "String",
  "value": "String"
}
```



