# <a name="omasettingstring-resource-type"></a><span data-ttu-id="4c304-101">Tipo de recurso omaSettingString</span><span class="sxs-lookup"><span data-stu-id="4c304-101">omaSettingString resource type</span></span>

> <span data-ttu-id="4c304-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4c304-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4c304-103">Definición de la cadena de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="4c304-103">OMA Settings String definition.</span></span>

<span data-ttu-id="4c304-104">Hereda de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="4c304-104">Inherits from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="4c304-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4c304-105">Properties</span></span>
|<span data-ttu-id="4c304-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4c304-106">Property</span></span>|<span data-ttu-id="4c304-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="4c304-107">Type</span></span>|<span data-ttu-id="4c304-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c304-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4c304-109">displayName</span><span class="sxs-lookup"><span data-stu-id="4c304-109">displayName</span></span>|<span data-ttu-id="4c304-110">cadena</span><span class="sxs-lookup"><span data-stu-id="4c304-110">String</span></span>|<span data-ttu-id="4c304-111">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="4c304-111">Display Name.</span></span> <span data-ttu-id="4c304-112">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="4c304-112">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="4c304-113">descripción</span><span class="sxs-lookup"><span data-stu-id="4c304-113">description</span></span>|<span data-ttu-id="4c304-114">String</span><span class="sxs-lookup"><span data-stu-id="4c304-114">String</span></span>|<span data-ttu-id="4c304-115">Descripción.</span><span class="sxs-lookup"><span data-stu-id="4c304-115">Description.</span></span> <span data-ttu-id="4c304-116">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="4c304-116">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="4c304-117">omaUri</span><span class="sxs-lookup"><span data-stu-id="4c304-117">omaUri</span></span>|<span data-ttu-id="4c304-118">cadena</span><span class="sxs-lookup"><span data-stu-id="4c304-118">String</span></span>|<span data-ttu-id="4c304-119">OMA.</span><span class="sxs-lookup"><span data-stu-id="4c304-119">OMA.</span></span> <span data-ttu-id="4c304-120">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="4c304-120">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="4c304-121">valor</span><span class="sxs-lookup"><span data-stu-id="4c304-121">value</span></span>|<span data-ttu-id="4c304-122">cadena</span><span class="sxs-lookup"><span data-stu-id="4c304-122">String</span></span>|<span data-ttu-id="4c304-123">Valor.</span><span class="sxs-lookup"><span data-stu-id="4c304-123">Value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="4c304-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4c304-124">Relationships</span></span>
<span data-ttu-id="4c304-125">Ninguna</span><span class="sxs-lookup"><span data-stu-id="4c304-125">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="4c304-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4c304-126">JSON Representation</span></span>
<span data-ttu-id="4c304-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4c304-127">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.omaSettingString"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSettingString",
  "displayName": "String",
  "description": "String",
  "omaUri": "String",
  "value": "String"
}
```








