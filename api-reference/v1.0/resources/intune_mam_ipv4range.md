# <a name="ipv4range-resource-type"></a><span data-ttu-id="80038-101">Tipo de recurso iPv4Range</span><span class="sxs-lookup"><span data-stu-id="80038-101">iPv4Range resource type</span></span>

> <span data-ttu-id="80038-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="80038-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="80038-103">Intervalo IPv4</span><span class="sxs-lookup"><span data-stu-id="80038-103">IP V4 range</span></span>

<span data-ttu-id="80038-104">Hereda de [ipRange](../resources/intune_mam_iprange.md)</span><span class="sxs-lookup"><span data-stu-id="80038-104">Inherits from [ipRange](../resources/intune_mam_iprange.md)</span></span>

## <a name="properties"></a><span data-ttu-id="80038-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="80038-105">Properties</span></span>
|<span data-ttu-id="80038-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="80038-106">Property</span></span>|<span data-ttu-id="80038-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="80038-107">Type</span></span>|<span data-ttu-id="80038-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="80038-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="80038-109">lowerAddress</span><span class="sxs-lookup"><span data-stu-id="80038-109">lowerAddress</span></span>|<span data-ttu-id="80038-110">cadena</span><span class="sxs-lookup"><span data-stu-id="80038-110">String</span></span>|<span data-ttu-id="80038-111">Dirección IP inferior</span><span class="sxs-lookup"><span data-stu-id="80038-111">Lower IP Address</span></span>|
|<span data-ttu-id="80038-112">upperAddress</span><span class="sxs-lookup"><span data-stu-id="80038-112">upperAddress</span></span>|<span data-ttu-id="80038-113">cadena</span><span class="sxs-lookup"><span data-stu-id="80038-113">String</span></span>|<span data-ttu-id="80038-114">Dirección IP superior</span><span class="sxs-lookup"><span data-stu-id="80038-114">Upper IP Address</span></span>|

## <a name="relationships"></a><span data-ttu-id="80038-115">Relaciones</span><span class="sxs-lookup"><span data-stu-id="80038-115">Relationships</span></span>
<span data-ttu-id="80038-116">Ninguna</span><span class="sxs-lookup"><span data-stu-id="80038-116">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="80038-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="80038-117">JSON Representation</span></span>
<span data-ttu-id="80038-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="80038-118">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.ipRange",
  "@odata.type": "microsoft.graph.iPv4Range"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iPv4Range",
  "lowerAddress": "String",
  "upperAddress": "String"
}
```



