# <a name="omasettingstring-resource-type"></a><span data-ttu-id="3a362-101">Tipo de recurso omaSettingString</span><span class="sxs-lookup"><span data-stu-id="3a362-101">omaSettingString resource type</span></span>

> <span data-ttu-id="3a362-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3a362-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3a362-103">Definición de la cadena de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="3a362-103">OMA Settings String definition.</span></span>

<span data-ttu-id="3a362-104">Hereda de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="3a362-104">Inherits from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="3a362-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3a362-105">Properties</span></span>
|<span data-ttu-id="3a362-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3a362-106">Property</span></span>|<span data-ttu-id="3a362-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="3a362-107">Type</span></span>|<span data-ttu-id="3a362-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a362-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3a362-109">displayName</span><span class="sxs-lookup"><span data-stu-id="3a362-109">displayName</span></span>|<span data-ttu-id="3a362-110">cadena</span><span class="sxs-lookup"><span data-stu-id="3a362-110">String</span></span>|<span data-ttu-id="3a362-111">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="3a362-111">Display Name</span></span> <span data-ttu-id="3a362-112">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="3a362-112">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="3a362-113">description</span><span class="sxs-lookup"><span data-stu-id="3a362-113">description</span></span>|<span data-ttu-id="3a362-114">cadena</span><span class="sxs-lookup"><span data-stu-id="3a362-114">String</span></span>|<span data-ttu-id="3a362-115">Descripción.</span><span class="sxs-lookup"><span data-stu-id="3a362-115">Description.</span></span> <span data-ttu-id="3a362-116">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="3a362-116">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="3a362-117">omaUri</span><span class="sxs-lookup"><span data-stu-id="3a362-117">omaUri</span></span>|<span data-ttu-id="3a362-118">cadena</span><span class="sxs-lookup"><span data-stu-id="3a362-118">String</span></span>|<span data-ttu-id="3a362-119">OMA.</span><span class="sxs-lookup"><span data-stu-id="3a362-119">OMA.</span></span> <span data-ttu-id="3a362-120">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="3a362-120">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="3a362-121">value</span><span class="sxs-lookup"><span data-stu-id="3a362-121">value</span></span>|<span data-ttu-id="3a362-122">cadena</span><span class="sxs-lookup"><span data-stu-id="3a362-122">String</span></span>|<span data-ttu-id="3a362-123">Valor.</span><span class="sxs-lookup"><span data-stu-id="3a362-123">Value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="3a362-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="3a362-124">Relationships</span></span>
<span data-ttu-id="3a362-125">Ninguna</span><span class="sxs-lookup"><span data-stu-id="3a362-125">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="3a362-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3a362-126">JSON Representation</span></span>
<span data-ttu-id="3a362-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3a362-127">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
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



