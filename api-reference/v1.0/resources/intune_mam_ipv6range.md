# <a name="ipv6range-resource-type"></a><span data-ttu-id="ca202-101">Tipo de recurso iPv6Range</span><span class="sxs-lookup"><span data-stu-id="ca202-101">iPv6Range resource type</span></span>

> <span data-ttu-id="ca202-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ca202-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ca202-103">Intervalo IPv6</span><span class="sxs-lookup"><span data-stu-id="ca202-103">IP V6 range</span></span>

<span data-ttu-id="ca202-104">Hereda de [ipRange](../resources/intune_mam_iprange.md)</span><span class="sxs-lookup"><span data-stu-id="ca202-104">Inherits from [ipRange](../resources/intune_mam_iprange.md)</span></span>

## <a name="properties"></a><span data-ttu-id="ca202-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ca202-105">Properties</span></span>
|<span data-ttu-id="ca202-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ca202-106">Property</span></span>|<span data-ttu-id="ca202-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="ca202-107">Type</span></span>|<span data-ttu-id="ca202-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ca202-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ca202-109">lowerAddress</span><span class="sxs-lookup"><span data-stu-id="ca202-109">lowerAddress</span></span>|<span data-ttu-id="ca202-110">cadena</span><span class="sxs-lookup"><span data-stu-id="ca202-110">String</span></span>|<span data-ttu-id="ca202-111">Dirección IP inferior</span><span class="sxs-lookup"><span data-stu-id="ca202-111">Lower IP Address</span></span>|
|<span data-ttu-id="ca202-112">upperAddress</span><span class="sxs-lookup"><span data-stu-id="ca202-112">upperAddress</span></span>|<span data-ttu-id="ca202-113">cadena</span><span class="sxs-lookup"><span data-stu-id="ca202-113">String</span></span>|<span data-ttu-id="ca202-114">Dirección IP superior</span><span class="sxs-lookup"><span data-stu-id="ca202-114">Upper IP Address</span></span>|

## <a name="relationships"></a><span data-ttu-id="ca202-115">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ca202-115">Relationships</span></span>
<span data-ttu-id="ca202-116">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ca202-116">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ca202-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ca202-117">JSON Representation</span></span>
<span data-ttu-id="ca202-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ca202-118">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iPv6Range"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.iPv6Range",
  "lowerAddress": "String",
  "upperAddress": "String"
}
```








