# <a name="ipv6range-resource-type"></a><span data-ttu-id="9b509-101">Tipo de recurso iPv6Range</span><span class="sxs-lookup"><span data-stu-id="9b509-101">iPv6Range resource type</span></span>

> <span data-ttu-id="9b509-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9b509-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9b509-103">Intervalo IPv6</span><span class="sxs-lookup"><span data-stu-id="9b509-103">IP V6 range</span></span>

<span data-ttu-id="9b509-104">Hereda de [ipRange](../resources/intune_mam_iprange.md)</span><span class="sxs-lookup"><span data-stu-id="9b509-104">Inherits from [ipRange](../resources/intune_mam_iprange.md)</span></span>

## <a name="properties"></a><span data-ttu-id="9b509-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9b509-105">Properties</span></span>
|<span data-ttu-id="9b509-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9b509-106">Property</span></span>|<span data-ttu-id="9b509-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="9b509-107">Type</span></span>|<span data-ttu-id="9b509-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b509-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9b509-109">lowerAddress</span><span class="sxs-lookup"><span data-stu-id="9b509-109">lowerAddress</span></span>|<span data-ttu-id="9b509-110">cadena</span><span class="sxs-lookup"><span data-stu-id="9b509-110">String</span></span>|<span data-ttu-id="9b509-111">Dirección IP inferior</span><span class="sxs-lookup"><span data-stu-id="9b509-111">Lower IP Address</span></span>|
|<span data-ttu-id="9b509-112">upperAddress</span><span class="sxs-lookup"><span data-stu-id="9b509-112">upperAddress</span></span>|<span data-ttu-id="9b509-113">cadena</span><span class="sxs-lookup"><span data-stu-id="9b509-113">String</span></span>|<span data-ttu-id="9b509-114">Dirección IP superior</span><span class="sxs-lookup"><span data-stu-id="9b509-114">Upper IP Address</span></span>|

## <a name="relationships"></a><span data-ttu-id="9b509-115">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9b509-115">Relationships</span></span>
<span data-ttu-id="9b509-116">Ninguna</span><span class="sxs-lookup"><span data-stu-id="9b509-116">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="9b509-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9b509-117">JSON Representation</span></span>
<span data-ttu-id="9b509-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9b509-118">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iPv6Range"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iPv6Range",
  "lowerAddress": "String",
  "upperAddress": "String"
}
```



