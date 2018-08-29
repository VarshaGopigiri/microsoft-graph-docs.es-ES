# <a name="omasettingbase64-resource-type"></a><span data-ttu-id="fadec-101">Tipo de recurso omaSettingBase64</span><span class="sxs-lookup"><span data-stu-id="fadec-101">omaSettingBase64 resource type</span></span>

> <span data-ttu-id="fadec-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fadec-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fadec-103">Definición de Base64 de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="fadec-103">OMA Settings Base64 definition.</span></span>

<span data-ttu-id="fadec-104">Hereda de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="fadec-104">Inherits from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="fadec-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fadec-105">Properties</span></span>
|<span data-ttu-id="fadec-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fadec-106">Property</span></span>|<span data-ttu-id="fadec-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="fadec-107">Type</span></span>|<span data-ttu-id="fadec-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="fadec-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fadec-109">displayName</span><span class="sxs-lookup"><span data-stu-id="fadec-109">displayName</span></span>|<span data-ttu-id="fadec-110">cadena</span><span class="sxs-lookup"><span data-stu-id="fadec-110">String</span></span>|<span data-ttu-id="fadec-111">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="fadec-111">Display Name.</span></span> <span data-ttu-id="fadec-112">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="fadec-112">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="fadec-113">descripción</span><span class="sxs-lookup"><span data-stu-id="fadec-113">description</span></span>|<span data-ttu-id="fadec-114">String</span><span class="sxs-lookup"><span data-stu-id="fadec-114">String</span></span>|<span data-ttu-id="fadec-115">Descripción.</span><span class="sxs-lookup"><span data-stu-id="fadec-115">Description.</span></span> <span data-ttu-id="fadec-116">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="fadec-116">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="fadec-117">omaUri</span><span class="sxs-lookup"><span data-stu-id="fadec-117">omaUri</span></span>|<span data-ttu-id="fadec-118">cadena</span><span class="sxs-lookup"><span data-stu-id="fadec-118">String</span></span>|<span data-ttu-id="fadec-119">OMA.</span><span class="sxs-lookup"><span data-stu-id="fadec-119">OMA.</span></span> <span data-ttu-id="fadec-120">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="fadec-120">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="fadec-121">fileName</span><span class="sxs-lookup"><span data-stu-id="fadec-121">fileName</span></span>|<span data-ttu-id="fadec-122">cadena</span><span class="sxs-lookup"><span data-stu-id="fadec-122">String</span></span>|<span data-ttu-id="fadec-123">Nombre de archivo asociado a la propiedad de valor (\*.cer</span><span class="sxs-lookup"><span data-stu-id="fadec-123">File name associated with the Value property (\*.cer</span></span> | <span data-ttu-id="fadec-124">\*.crt).</span><span class="sxs-lookup"><span data-stu-id="fadec-124">\*.crt ).</span></span>|
|<span data-ttu-id="fadec-125">valor</span><span class="sxs-lookup"><span data-stu-id="fadec-125">value</span></span>|<span data-ttu-id="fadec-126">cadena</span><span class="sxs-lookup"><span data-stu-id="fadec-126">String</span></span>|<span data-ttu-id="fadec-127">Valor.</span><span class="sxs-lookup"><span data-stu-id="fadec-127">Value.</span></span> <span data-ttu-id="fadec-128">(Cadena codificada en Base64)</span><span class="sxs-lookup"><span data-stu-id="fadec-128">(Base64 encoded string)</span></span>|

## <a name="relationships"></a><span data-ttu-id="fadec-129">Relaciones</span><span class="sxs-lookup"><span data-stu-id="fadec-129">Relationships</span></span>
<span data-ttu-id="fadec-130">Ninguna</span><span class="sxs-lookup"><span data-stu-id="fadec-130">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="fadec-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fadec-131">JSON Representation</span></span>
<span data-ttu-id="fadec-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="fadec-132">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.omaSetting",
  "@odata.type": "microsoft.graph.omaSettingBase64"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSettingBase64",
  "displayName": "String",
  "description": "String",
  "omaUri": "String",
  "fileName": "String",
  "value": "String"
}
```



