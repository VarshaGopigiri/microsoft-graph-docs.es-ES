# <a name="omasettingfloatingpoint-resource-type"></a><span data-ttu-id="427ba-101">Tipo de recurso omaSettingFloatingPoint</span><span class="sxs-lookup"><span data-stu-id="427ba-101">omaSettingFloatingPoint resource type</span></span>

> <span data-ttu-id="427ba-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="427ba-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="427ba-103">Definición de punto flotante de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="427ba-103">OMA Settings Floating Point definition.</span></span>

<span data-ttu-id="427ba-104">Hereda de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="427ba-104">Inherits from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="427ba-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="427ba-105">Properties</span></span>
|<span data-ttu-id="427ba-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="427ba-106">Property</span></span>|<span data-ttu-id="427ba-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="427ba-107">Type</span></span>|<span data-ttu-id="427ba-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="427ba-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="427ba-109">displayName</span><span class="sxs-lookup"><span data-stu-id="427ba-109">displayName</span></span>|<span data-ttu-id="427ba-110">cadena</span><span class="sxs-lookup"><span data-stu-id="427ba-110">String</span></span>|<span data-ttu-id="427ba-111">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="427ba-111">Display Name.</span></span> <span data-ttu-id="427ba-112">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="427ba-112">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="427ba-113">description</span><span class="sxs-lookup"><span data-stu-id="427ba-113">description</span></span>|<span data-ttu-id="427ba-114">cadena</span><span class="sxs-lookup"><span data-stu-id="427ba-114">String</span></span>|<span data-ttu-id="427ba-115">Descripción.</span><span class="sxs-lookup"><span data-stu-id="427ba-115">Description.</span></span> <span data-ttu-id="427ba-116">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="427ba-116">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="427ba-117">omaUri</span><span class="sxs-lookup"><span data-stu-id="427ba-117">omaUri</span></span>|<span data-ttu-id="427ba-118">cadena</span><span class="sxs-lookup"><span data-stu-id="427ba-118">String</span></span>|<span data-ttu-id="427ba-119">OMA.</span><span class="sxs-lookup"><span data-stu-id="427ba-119">OMA.</span></span> <span data-ttu-id="427ba-120">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="427ba-120">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="427ba-121">value</span><span class="sxs-lookup"><span data-stu-id="427ba-121">value</span></span>|<span data-ttu-id="427ba-122">Simple</span><span class="sxs-lookup"><span data-stu-id="427ba-122">Single</span></span>|<span data-ttu-id="427ba-123">Valor.</span><span class="sxs-lookup"><span data-stu-id="427ba-123">Value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="427ba-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="427ba-124">Relationships</span></span>
<span data-ttu-id="427ba-125">Ninguna</span><span class="sxs-lookup"><span data-stu-id="427ba-125">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="427ba-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="427ba-126">JSON Representation</span></span>
<span data-ttu-id="427ba-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="427ba-127">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.omaSettingFloatingPoint"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSettingFloatingPoint",
  "displayName": "String",
  "description": "String",
  "omaUri": "String",
  "value": "<Unknown Primitive Type Edm.Single>"
}
```



