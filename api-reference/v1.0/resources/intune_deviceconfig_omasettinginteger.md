# <a name="omasettinginteger-resource-type"></a><span data-ttu-id="fbe75-101">Tipo de recurso omaSettingInteger</span><span class="sxs-lookup"><span data-stu-id="fbe75-101">omaSettingInteger resource type</span></span>

> <span data-ttu-id="fbe75-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fbe75-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fbe75-103">Definición del entero de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="fbe75-103">OMA Settings Integer definition.</span></span>

<span data-ttu-id="fbe75-104">Hereda de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="fbe75-104">Inherits from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="fbe75-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fbe75-105">Properties</span></span>
|<span data-ttu-id="fbe75-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fbe75-106">Property</span></span>|<span data-ttu-id="fbe75-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="fbe75-107">Type</span></span>|<span data-ttu-id="fbe75-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="fbe75-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fbe75-109">displayName</span><span class="sxs-lookup"><span data-stu-id="fbe75-109">displayName</span></span>|<span data-ttu-id="fbe75-110">cadena</span><span class="sxs-lookup"><span data-stu-id="fbe75-110">String</span></span>|<span data-ttu-id="fbe75-111">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="fbe75-111">Display Name</span></span> <span data-ttu-id="fbe75-112">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="fbe75-112">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="fbe75-113">descripción</span><span class="sxs-lookup"><span data-stu-id="fbe75-113">description</span></span>|<span data-ttu-id="fbe75-114">cadena</span><span class="sxs-lookup"><span data-stu-id="fbe75-114">String</span></span>|<span data-ttu-id="fbe75-115">Descripción.</span><span class="sxs-lookup"><span data-stu-id="fbe75-115">Description.</span></span> <span data-ttu-id="fbe75-116">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="fbe75-116">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="fbe75-117">omaUri</span><span class="sxs-lookup"><span data-stu-id="fbe75-117">omaUri</span></span>|<span data-ttu-id="fbe75-118">cadena</span><span class="sxs-lookup"><span data-stu-id="fbe75-118">String</span></span>|<span data-ttu-id="fbe75-119">OMA.</span><span class="sxs-lookup"><span data-stu-id="fbe75-119">OMA.</span></span> <span data-ttu-id="fbe75-120">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="fbe75-120">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="fbe75-121">valor</span><span class="sxs-lookup"><span data-stu-id="fbe75-121">value</span></span>|<span data-ttu-id="fbe75-122">Int32</span><span class="sxs-lookup"><span data-stu-id="fbe75-122">Int32</span></span>|<span data-ttu-id="fbe75-123">Valor.</span><span class="sxs-lookup"><span data-stu-id="fbe75-123">Value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="fbe75-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="fbe75-124">Relationships</span></span>
<span data-ttu-id="fbe75-125">Ninguna</span><span class="sxs-lookup"><span data-stu-id="fbe75-125">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="fbe75-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fbe75-126">JSON Representation</span></span>
<span data-ttu-id="fbe75-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="fbe75-127">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.omaSettingInteger"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSettingInteger",
  "displayName": "String",
  "description": "String",
  "omaUri": "String",
  "value": 1024
}
```



