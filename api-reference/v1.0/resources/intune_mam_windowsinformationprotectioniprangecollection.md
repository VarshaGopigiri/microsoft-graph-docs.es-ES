# <a name="windowsinformationprotectioniprangecollection-resource-type"></a><span data-ttu-id="2fe1f-101">Tipo de recurso windowsInformationProtectionIPRangeCollection</span><span class="sxs-lookup"><span data-stu-id="2fe1f-101">windowsInformationProtectionIPRangeCollection resource type</span></span>

> <span data-ttu-id="2fe1f-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2fe1f-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2fe1f-103">Colección de intervalos IP de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="2fe1f-103">Windows Information Protection IP Range Collection</span></span>
## <a name="properties"></a><span data-ttu-id="2fe1f-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2fe1f-104">Properties</span></span>
|<span data-ttu-id="2fe1f-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2fe1f-105">Property</span></span>|<span data-ttu-id="2fe1f-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fe1f-106">Type</span></span>|<span data-ttu-id="2fe1f-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="2fe1f-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2fe1f-108">displayName</span><span class="sxs-lookup"><span data-stu-id="2fe1f-108">displayName</span></span>|<span data-ttu-id="2fe1f-109">cadena</span><span class="sxs-lookup"><span data-stu-id="2fe1f-109">String</span></span>|<span data-ttu-id="2fe1f-110">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="2fe1f-110">Display name</span></span>|
|<span data-ttu-id="2fe1f-111">rangos</span><span class="sxs-lookup"><span data-stu-id="2fe1f-111">ranges</span></span>|<span data-ttu-id="2fe1f-112">Colección [ipRange](../resources/intune_mam_iprange.md)</span><span class="sxs-lookup"><span data-stu-id="2fe1f-112">[ipRange](../resources/intune_mam_iprange.md) collection</span></span>|<span data-ttu-id="2fe1f-113">Conjunto de intervalos IP</span><span class="sxs-lookup"><span data-stu-id="2fe1f-113">Collection of ip ranges</span></span>|

## <a name="relationships"></a><span data-ttu-id="2fe1f-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2fe1f-114">Relationships</span></span>
<span data-ttu-id="2fe1f-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2fe1f-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="2fe1f-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2fe1f-116">JSON Representation</span></span>
<span data-ttu-id="2fe1f-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2fe1f-117">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsInformationProtectionIPRangeCollection"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionIPRangeCollection",
  "displayName": "String",
  "ranges": [
    {
      "@odata.type": "microsoft.graph.ipRange",
      "lowerAddress": "String",
      "upperAddress": "String"
    }
  ]
}
```



