# <a name="securityvendorinformation-resource-type"></a><span data-ttu-id="d8112-101">Tipo de recurso securityVendorInformation</span><span class="sxs-lookup"><span data-stu-id="d8112-101">securityVendorInformation resource type</span></span>

<span data-ttu-id="d8112-102">Contiene detalles sobre el proveedor del producto o servicio de seguridad, el proveedor y el subproveedor (por ejemplo, vendor=Microsoft; provider=Windows Defender ATP; subProvider=AppLocker).</span><span class="sxs-lookup"><span data-stu-id="d8112-102">Contains details about the security product/service vendor, provider, and subprovider (for example, vendor=Microsoft; provider=Windows Defender ATP; subProvider=AppLocker).</span></span>

## <a name="properties"></a><span data-ttu-id="d8112-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d8112-103">Properties</span></span>

| <span data-ttu-id="d8112-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d8112-104">Property</span></span>   | <span data-ttu-id="d8112-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="d8112-105">Type</span></span>|<span data-ttu-id="d8112-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8112-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d8112-107">proveedor \*</span><span class="sxs-lookup"><span data-stu-id="d8112-107">provider \*</span></span>|<span data-ttu-id="d8112-108">Cadena</span><span class="sxs-lookup"><span data-stu-id="d8112-108">String</span></span>|<span data-ttu-id="d8112-109">Proveedor específico (producto/servicio - no empresa proveedora); por ejemplo, WindowsDefenderATP.</span><span class="sxs-lookup"><span data-stu-id="d8112-109">Specific provider (product/service - not vendor company); for example, WindowsDefenderATP.</span></span>|
|<span data-ttu-id="d8112-110">providerVersion</span><span class="sxs-lookup"><span data-stu-id="d8112-110">providerVersion</span></span>|<span data-ttu-id="d8112-111">Cadena</span><span class="sxs-lookup"><span data-stu-id="d8112-111">String</span></span>|<span data-ttu-id="d8112-112">Versión del proveedor o subprovider, si existe, que generó la alerta.</span><span class="sxs-lookup"><span data-stu-id="d8112-112">Version of the provider or subprovider, if it exists, that generated the alert.</span></span>|
|<span data-ttu-id="d8112-113">subProvider</span><span class="sxs-lookup"><span data-stu-id="d8112-113">subProvider</span></span>|<span data-ttu-id="d8112-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="d8112-114">String</span></span>|<span data-ttu-id="d8112-115">Subproveedor específico (debajo de agregación de proveedor); Por ejemplo, WindowsDefenderATP.SmartScreen.</span><span class="sxs-lookup"><span data-stu-id="d8112-115">Specific subprovider (under aggregating provider); for example, WindowsDefenderATP.SmartScreen.</span></span>|
|<span data-ttu-id="d8112-116">proveedor \*</span><span class="sxs-lookup"><span data-stu-id="d8112-116">vendor \*</span></span>|<span data-ttu-id="d8112-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="d8112-117">String</span></span>|<span data-ttu-id="d8112-118">Nombre del proveedor de alerta (por ejemplo, Microsoft, Dell, FireEye).</span><span class="sxs-lookup"><span data-stu-id="d8112-118">Name of the alert vendor (for example, Microsoft, Dell, FireEye).</span></span>|
<span data-ttu-id="d8112-119">(\* Indica un campo obligatorio.)</span><span class="sxs-lookup"><span data-stu-id="d8112-119">(\* Indicates a mandatory field.)</span></span>

## <a name="json-representation"></a><span data-ttu-id="d8112-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d8112-120">JSON representation</span></span>

<span data-ttu-id="d8112-121">La siguiente es una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d8112-121">The following is a JSON representation of the resource.</span></span>
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
