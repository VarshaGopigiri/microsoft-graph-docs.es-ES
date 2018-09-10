# <a name="omasettingfloatingpoint-resource-type"></a><span data-ttu-id="c7b68-101">Tipo de recurso omaSettingFloatingPoint</span><span class="sxs-lookup"><span data-stu-id="c7b68-101">omaSettingFloatingPoint resource type</span></span>

> <span data-ttu-id="c7b68-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c7b68-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c7b68-103">Definición de punto flotante de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="c7b68-103">OMA Settings Floating Point definition.</span></span>

<span data-ttu-id="c7b68-104">Hereda de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="c7b68-104">Inherits from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="c7b68-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c7b68-105">Properties</span></span>
|<span data-ttu-id="c7b68-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c7b68-106">Property</span></span>|<span data-ttu-id="c7b68-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="c7b68-107">Type</span></span>|<span data-ttu-id="c7b68-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7b68-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c7b68-109">displayName</span><span class="sxs-lookup"><span data-stu-id="c7b68-109">displayName</span></span>|<span data-ttu-id="c7b68-110">cadena</span><span class="sxs-lookup"><span data-stu-id="c7b68-110">String</span></span>|<span data-ttu-id="c7b68-111">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="c7b68-111">Display Name.</span></span> <span data-ttu-id="c7b68-112">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="c7b68-112">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="c7b68-113">descripción</span><span class="sxs-lookup"><span data-stu-id="c7b68-113">description</span></span>|<span data-ttu-id="c7b68-114">String</span><span class="sxs-lookup"><span data-stu-id="c7b68-114">String</span></span>|<span data-ttu-id="c7b68-115">Descripción.</span><span class="sxs-lookup"><span data-stu-id="c7b68-115">Description.</span></span> <span data-ttu-id="c7b68-116">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="c7b68-116">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="c7b68-117">omaUri</span><span class="sxs-lookup"><span data-stu-id="c7b68-117">omaUri</span></span>|<span data-ttu-id="c7b68-118">cadena</span><span class="sxs-lookup"><span data-stu-id="c7b68-118">String</span></span>|<span data-ttu-id="c7b68-119">OMA.</span><span class="sxs-lookup"><span data-stu-id="c7b68-119">OMA.</span></span> <span data-ttu-id="c7b68-120">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="c7b68-120">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="c7b68-121">value</span><span class="sxs-lookup"><span data-stu-id="c7b68-121">value</span></span>|<span data-ttu-id="c7b68-122">Simple</span><span class="sxs-lookup"><span data-stu-id="c7b68-122">Single</span></span>|<span data-ttu-id="c7b68-123">Valor.</span><span class="sxs-lookup"><span data-stu-id="c7b68-123">Value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="c7b68-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c7b68-124">Relationships</span></span>
<span data-ttu-id="c7b68-125">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c7b68-125">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="c7b68-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c7b68-126">JSON Representation</span></span>
<span data-ttu-id="c7b68-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c7b68-127">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.omaSettingFloatingPoint"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSettingFloatingPoint",
  "displayName": "String",
  "description": "String",
  "omaUri": "String",
  "value": "<Unknown Primitive Type Edm.Single>"
}
```








