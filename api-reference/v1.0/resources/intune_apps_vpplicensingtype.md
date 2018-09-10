# <a name="vpplicensingtype-resource-type"></a><span data-ttu-id="a931c-101">Tipo de recurso vppLicensingType</span><span class="sxs-lookup"><span data-stu-id="a931c-101">vppLicensingType resource type</span></span>

> <span data-ttu-id="a931c-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a931c-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a931c-103">Contiene las propiedades del tipo de licencia del Programa de Compras por Volumen (VPP) de iOS.</span><span class="sxs-lookup"><span data-stu-id="a931c-103">Contains properties for iOS Volume-Purchased Program (Vpp) Licensing Type.</span></span>
## <a name="properties"></a><span data-ttu-id="a931c-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a931c-104">Properties</span></span>
|<span data-ttu-id="a931c-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a931c-105">Property</span></span>|<span data-ttu-id="a931c-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="a931c-106">Type</span></span>|<span data-ttu-id="a931c-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a931c-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a931c-108">supportsUserLicensing</span><span class="sxs-lookup"><span data-stu-id="a931c-108">supportsUserLicensing</span></span>|<span data-ttu-id="a931c-109">Booleano</span><span class="sxs-lookup"><span data-stu-id="a931c-109">Boolean</span></span>|<span data-ttu-id="a931c-110">Si el programa es compatible con el tipo de licencia de usuario.</span><span class="sxs-lookup"><span data-stu-id="a931c-110">Whether the program supports the user licensing type.</span></span>|
|<span data-ttu-id="a931c-111">supportsDeviceLicensing</span><span class="sxs-lookup"><span data-stu-id="a931c-111">supportsDeviceLicensing</span></span>|<span data-ttu-id="a931c-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="a931c-112">Boolean</span></span>|<span data-ttu-id="a931c-113">Si el programa es compatible con el tipo de licencia de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a931c-113">Whether the program supports the device licensing type.</span></span>|

## <a name="relationships"></a><span data-ttu-id="a931c-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a931c-114">Relationships</span></span>
<span data-ttu-id="a931c-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="a931c-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="a931c-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a931c-116">JSON Representation</span></span>
<span data-ttu-id="a931c-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a931c-117">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.vppLicensingType"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.vppLicensingType",
  "supportsUserLicensing": true,
  "supportsDeviceLicensing": true
}
```








