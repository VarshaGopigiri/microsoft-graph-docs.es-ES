# <a name="omasettingboolean-resource-type"></a><span data-ttu-id="e772b-101">Tipo de recurso omaSettingBoolean</span><span class="sxs-lookup"><span data-stu-id="e772b-101">omaSettingBoolean resource type</span></span>

> <span data-ttu-id="e772b-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e772b-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e772b-103">Definición booleana de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="e772b-103">OMA Settings Boolean definition.</span></span>

<span data-ttu-id="e772b-104">Hereda de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="e772b-104">Inherits from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="e772b-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e772b-105">Properties</span></span>
|<span data-ttu-id="e772b-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e772b-106">Property</span></span>|<span data-ttu-id="e772b-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="e772b-107">Type</span></span>|<span data-ttu-id="e772b-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e772b-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e772b-109">displayName</span><span class="sxs-lookup"><span data-stu-id="e772b-109">displayName</span></span>|<span data-ttu-id="e772b-110">cadena</span><span class="sxs-lookup"><span data-stu-id="e772b-110">String</span></span>|<span data-ttu-id="e772b-111">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="e772b-111">Display Name.</span></span> <span data-ttu-id="e772b-112">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="e772b-112">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="e772b-113">descripción</span><span class="sxs-lookup"><span data-stu-id="e772b-113">description</span></span>|<span data-ttu-id="e772b-114">String</span><span class="sxs-lookup"><span data-stu-id="e772b-114">String</span></span>|<span data-ttu-id="e772b-115">Descripción.</span><span class="sxs-lookup"><span data-stu-id="e772b-115">Description.</span></span> <span data-ttu-id="e772b-116">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="e772b-116">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="e772b-117">omaUri</span><span class="sxs-lookup"><span data-stu-id="e772b-117">omaUri</span></span>|<span data-ttu-id="e772b-118">cadena</span><span class="sxs-lookup"><span data-stu-id="e772b-118">String</span></span>|<span data-ttu-id="e772b-119">OMA.</span><span class="sxs-lookup"><span data-stu-id="e772b-119">OMA.</span></span> <span data-ttu-id="e772b-120">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="e772b-120">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="e772b-121">valor</span><span class="sxs-lookup"><span data-stu-id="e772b-121">value</span></span>|<span data-ttu-id="e772b-122">Booleano</span><span class="sxs-lookup"><span data-stu-id="e772b-122">Boolean</span></span>|<span data-ttu-id="e772b-123">Valor.</span><span class="sxs-lookup"><span data-stu-id="e772b-123">Value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e772b-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e772b-124">Relationships</span></span>
<span data-ttu-id="e772b-125">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e772b-125">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="e772b-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e772b-126">JSON Representation</span></span>
<span data-ttu-id="e772b-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e772b-127">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.omaSetting",
  "@odata.type": "microsoft.graph.omaSettingBoolean"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSettingBoolean",
  "displayName": "String",
  "description": "String",
  "omaUri": "String",
  "value": true
}
```



