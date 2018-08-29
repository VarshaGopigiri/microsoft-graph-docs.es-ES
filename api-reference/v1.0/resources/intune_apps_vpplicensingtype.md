# <a name="vpplicensingtype-resource-type"></a><span data-ttu-id="28cf4-101">Tipo de recurso vppLicensingType</span><span class="sxs-lookup"><span data-stu-id="28cf4-101">vppLicensingType resource type</span></span>

> <span data-ttu-id="28cf4-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="28cf4-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="28cf4-103">Contiene las propiedades del tipo de licencia del Programa de Compras por Volumen (VPP) de iOS.</span><span class="sxs-lookup"><span data-stu-id="28cf4-103">Contains properties for iOS Volume-Purchased Program (Vpp) Licensing Type.</span></span>
## <a name="properties"></a><span data-ttu-id="28cf4-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="28cf4-104">Properties</span></span>
|<span data-ttu-id="28cf4-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="28cf4-105">Property</span></span>|<span data-ttu-id="28cf4-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="28cf4-106">Type</span></span>|<span data-ttu-id="28cf4-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="28cf4-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="28cf4-108">supportsUserLicensing</span><span class="sxs-lookup"><span data-stu-id="28cf4-108">supportsUserLicensing</span></span>|<span data-ttu-id="28cf4-109">Booleano</span><span class="sxs-lookup"><span data-stu-id="28cf4-109">Boolean</span></span>|<span data-ttu-id="28cf4-110">Si el programa es compatible con el tipo de licencia de usuario.</span><span class="sxs-lookup"><span data-stu-id="28cf4-110">Whether the program supports the user licensing type.</span></span>|
|<span data-ttu-id="28cf4-111">supportsDeviceLicensing</span><span class="sxs-lookup"><span data-stu-id="28cf4-111">supportsDeviceLicensing</span></span>|<span data-ttu-id="28cf4-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="28cf4-112">Boolean</span></span>|<span data-ttu-id="28cf4-113">Si el programa es compatible con el tipo de licencia de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="28cf4-113">Whether the program supports the device licensing type.</span></span>|

## <a name="relationships"></a><span data-ttu-id="28cf4-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="28cf4-114">Relationships</span></span>
<span data-ttu-id="28cf4-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="28cf4-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="28cf4-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="28cf4-116">JSON Representation</span></span>
<span data-ttu-id="28cf4-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="28cf4-117">Here is a JSON representation of the resource.</span></span>
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



