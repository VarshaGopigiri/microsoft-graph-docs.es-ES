# <a name="omasettingbase64-resource-type"></a><span data-ttu-id="c428d-101">Tipo de recurso omaSettingBase64</span><span class="sxs-lookup"><span data-stu-id="c428d-101">omaSettingBase64 resource type</span></span>

> <span data-ttu-id="c428d-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c428d-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c428d-103">Definición de Base64 de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="c428d-103">OMA Settings Base64 definition.</span></span>

<span data-ttu-id="c428d-104">Hereda de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="c428d-104">Inherits from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>

## <a name="properties"></a><span data-ttu-id="c428d-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c428d-105">Properties</span></span>
|<span data-ttu-id="c428d-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c428d-106">Property</span></span>|<span data-ttu-id="c428d-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="c428d-107">Type</span></span>|<span data-ttu-id="c428d-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="c428d-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c428d-109">displayName</span><span class="sxs-lookup"><span data-stu-id="c428d-109">displayName</span></span>|<span data-ttu-id="c428d-110">cadena</span><span class="sxs-lookup"><span data-stu-id="c428d-110">String</span></span>|<span data-ttu-id="c428d-111">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="c428d-111">Display Name</span></span> <span data-ttu-id="c428d-112">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="c428d-112">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="c428d-113">descripción</span><span class="sxs-lookup"><span data-stu-id="c428d-113">description</span></span>|<span data-ttu-id="c428d-114">cadena</span><span class="sxs-lookup"><span data-stu-id="c428d-114">String</span></span>|<span data-ttu-id="c428d-115">Descripción.</span><span class="sxs-lookup"><span data-stu-id="c428d-115">Description.</span></span> <span data-ttu-id="c428d-116">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="c428d-116">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="c428d-117">omaUri</span><span class="sxs-lookup"><span data-stu-id="c428d-117">omaUri</span></span>|<span data-ttu-id="c428d-118">cadena</span><span class="sxs-lookup"><span data-stu-id="c428d-118">String</span></span>|<span data-ttu-id="c428d-119">OMA.</span><span class="sxs-lookup"><span data-stu-id="c428d-119">OMA.</span></span> <span data-ttu-id="c428d-120">Heredado de [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="c428d-120">Inherited from [omaSetting](../resources/intune_deviceconfig_omasetting.md)</span></span>|
|<span data-ttu-id="c428d-121">fileName</span><span class="sxs-lookup"><span data-stu-id="c428d-121">fileName</span></span>|<span data-ttu-id="c428d-122">cadena</span><span class="sxs-lookup"><span data-stu-id="c428d-122">String</span></span>|<span data-ttu-id="c428d-123">Nombre de archivo asociado a la propiedad de valor (\*.cer</span><span class="sxs-lookup"><span data-stu-id="c428d-123">File name associated with the Value property (\*.cer</span></span> | <span data-ttu-id="c428d-124">\*.crt).</span><span class="sxs-lookup"><span data-stu-id="c428d-124">\*.crt ).</span></span>|
|<span data-ttu-id="c428d-125">valor</span><span class="sxs-lookup"><span data-stu-id="c428d-125">value</span></span>|<span data-ttu-id="c428d-126">cadena</span><span class="sxs-lookup"><span data-stu-id="c428d-126">String</span></span>|<span data-ttu-id="c428d-127">Valor.</span><span class="sxs-lookup"><span data-stu-id="c428d-127">Value.</span></span> <span data-ttu-id="c428d-128">(Cadena codificada en Base64)</span><span class="sxs-lookup"><span data-stu-id="c428d-128">(Base64 encoded string)</span></span>|

## <a name="relationships"></a><span data-ttu-id="c428d-129">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c428d-129">Relationships</span></span>
<span data-ttu-id="c428d-130">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c428d-130">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="c428d-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c428d-131">JSON Representation</span></span>
<span data-ttu-id="c428d-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c428d-132">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.omaSettingBase64"
}
-->
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



