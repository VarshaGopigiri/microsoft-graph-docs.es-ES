# <a name="securityvendorinformation-resource-type"></a><span data-ttu-id="7ccfe-101">tipo de recurso securityVendorInformation</span><span class="sxs-lookup"><span data-stu-id="7ccfe-101">securityVendorInformation resource type</span></span>

<span data-ttu-id="7ccfe-102">Contiene detalles sobre el proveedor del producto o servicio de seguridad, el proveedor y la subprovider (por ejemplo, proveedor = Microsoft; proveedor = Windows Defender ATP; subProvider = AppLocker).</span><span class="sxs-lookup"><span data-stu-id="7ccfe-102">Contains details about the security product/service vendor, provider, and subprovider (for example, vendor=Microsoft; provider=Windows Defender ATP; subProvider=AppLocker).</span></span>

## <a name="properties"></a><span data-ttu-id="7ccfe-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7ccfe-103">Properties</span></span>

| <span data-ttu-id="7ccfe-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7ccfe-104">Property</span></span>   | <span data-ttu-id="7ccfe-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="7ccfe-105">Type</span></span>|<span data-ttu-id="7ccfe-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ccfe-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7ccfe-107">proveedor</span><span class="sxs-lookup"><span data-stu-id="7ccfe-107">provider</span></span> |<span data-ttu-id="7ccfe-108">String</span><span class="sxs-lookup"><span data-stu-id="7ccfe-108">String</span></span>|<span data-ttu-id="7ccfe-109">Proveedor específico (producto o servicio - empresa del proveedor no); Por ejemplo, WindowsDefenderATP.</span><span class="sxs-lookup"><span data-stu-id="7ccfe-109">Specific provider (product/service - not vendor company); for example, WindowsDefenderATP.</span></span>|
|<span data-ttu-id="7ccfe-110">providerVersion</span><span class="sxs-lookup"><span data-stu-id="7ccfe-110">providerVersion</span></span>|<span data-ttu-id="7ccfe-111">String</span><span class="sxs-lookup"><span data-stu-id="7ccfe-111">String</span></span>|<span data-ttu-id="7ccfe-112">Versión del proveedor o subprovider, si existe, que generó la alerta.</span><span class="sxs-lookup"><span data-stu-id="7ccfe-112">Version of the provider or subprovider, if it exists, that generated the alert.</span></span> <span data-ttu-id="7ccfe-113">*Required*</span><span class="sxs-lookup"><span data-stu-id="7ccfe-113">*Required*</span></span>|
|<span data-ttu-id="7ccfe-114">subProvider</span><span class="sxs-lookup"><span data-stu-id="7ccfe-114">subProvider</span></span>|<span data-ttu-id="7ccfe-115">String</span><span class="sxs-lookup"><span data-stu-id="7ccfe-115">String</span></span>|<span data-ttu-id="7ccfe-116">Subprovider específico (debajo de agregación de proveedor); Por ejemplo, WindowsDefenderATP.SmartScreen.</span><span class="sxs-lookup"><span data-stu-id="7ccfe-116">Specific subprovider (under aggregating provider); for example, WindowsDefenderATP.SmartScreen.</span></span>|
|<span data-ttu-id="7ccfe-117">proveedor</span><span class="sxs-lookup"><span data-stu-id="7ccfe-117">vendor</span></span> |<span data-ttu-id="7ccfe-118">String</span><span class="sxs-lookup"><span data-stu-id="7ccfe-118">String</span></span>|<span data-ttu-id="7ccfe-119">Nombre del proveedor de alerta (por ejemplo, Microsoft, Dell, FireEye).</span><span class="sxs-lookup"><span data-stu-id="7ccfe-119">Name of the alert vendor (for example, Microsoft, Dell, FireEye).</span></span> <span data-ttu-id="7ccfe-120">*Required*</span><span class="sxs-lookup"><span data-stu-id="7ccfe-120">*Required*</span></span>|


## <a name="json-representation"></a><span data-ttu-id="7ccfe-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7ccfe-121">JSON representation</span></span>

<span data-ttu-id="7ccfe-122">La siguiente es una representación de JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7ccfe-122">The folllowing is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.securityVendorInformation"
}-->

```json
{
  "provider": "String",
  "providerVersion": "String",
  "subProvider": "String",
  "vendor": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "securityVendorInformation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
