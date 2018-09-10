# <a name="omasettingstringxml-resource-type"></a><span data-ttu-id="ada15-101">Tipo de recurso omaSettingStringXml</span><span class="sxs-lookup"><span data-stu-id="ada15-101">omaSettingStringXml resource type</span></span>

> <span data-ttu-id="ada15-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ada15-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ada15-103">Definición de la cadena XML de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="ada15-103">OMA Settings StringXML definition.</span></span>

<span data-ttu-id="ada15-104">Hereda de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="ada15-104">Inherits from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="ada15-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ada15-105">Properties</span></span>
|<span data-ttu-id="ada15-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ada15-106">Property</span></span>|<span data-ttu-id="ada15-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="ada15-107">Type</span></span>|<span data-ttu-id="ada15-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ada15-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ada15-109">displayName</span><span class="sxs-lookup"><span data-stu-id="ada15-109">displayName</span></span>|<span data-ttu-id="ada15-110">cadena</span><span class="sxs-lookup"><span data-stu-id="ada15-110">String</span></span>|<span data-ttu-id="ada15-111">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="ada15-111">Display Name.</span></span> <span data-ttu-id="ada15-112">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="ada15-112">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="ada15-113">descripción</span><span class="sxs-lookup"><span data-stu-id="ada15-113">description</span></span>|<span data-ttu-id="ada15-114">String</span><span class="sxs-lookup"><span data-stu-id="ada15-114">String</span></span>|<span data-ttu-id="ada15-115">Descripción.</span><span class="sxs-lookup"><span data-stu-id="ada15-115">Description.</span></span> <span data-ttu-id="ada15-116">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="ada15-116">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="ada15-117">omaUri</span><span class="sxs-lookup"><span data-stu-id="ada15-117">omaUri</span></span>|<span data-ttu-id="ada15-118">cadena</span><span class="sxs-lookup"><span data-stu-id="ada15-118">String</span></span>|<span data-ttu-id="ada15-119">OMA.</span><span class="sxs-lookup"><span data-stu-id="ada15-119">OMA.</span></span> <span data-ttu-id="ada15-120">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="ada15-120">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="ada15-121">fileName</span><span class="sxs-lookup"><span data-stu-id="ada15-121">fileName</span></span>|<span data-ttu-id="ada15-122">cadena</span><span class="sxs-lookup"><span data-stu-id="ada15-122">String</span></span>|<span data-ttu-id="ada15-123">Nombre de archivo asociado a la propiedad de valor (\*.xml).</span><span class="sxs-lookup"><span data-stu-id="ada15-123">File name associated with the Value property (\*.xml).</span></span>|
|<span data-ttu-id="ada15-124">valor</span><span class="sxs-lookup"><span data-stu-id="ada15-124">value</span></span>|<span data-ttu-id="ada15-125">Binario</span><span class="sxs-lookup"><span data-stu-id="ada15-125">Binary</span></span>|<span data-ttu-id="ada15-126">Valor.</span><span class="sxs-lookup"><span data-stu-id="ada15-126">Value.</span></span> <span data-ttu-id="ada15-127">(Matriz de bytes codificada UTF8)</span><span class="sxs-lookup"><span data-stu-id="ada15-127">(UTF8 encoded byte array)</span></span>|

## <a name="relationships"></a><span data-ttu-id="ada15-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ada15-128">Relationships</span></span>
<span data-ttu-id="ada15-129">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ada15-129">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ada15-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ada15-130">JSON Representation</span></span>
<span data-ttu-id="ada15-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ada15-131">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.omaSettingStringXml"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSettingStringXml",
  "displayName": "String",
  "description": "String",
  "omaUri": "String",
  "fileName": "String",
  "value": "binary"
}
```








