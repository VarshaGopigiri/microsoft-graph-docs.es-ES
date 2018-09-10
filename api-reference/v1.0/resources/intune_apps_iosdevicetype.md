# <a name="iosdevicetype-resource-type"></a><span data-ttu-id="a4a15-101">Tipo de recurso iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="a4a15-101">iosDeviceType resource type</span></span>

> <span data-ttu-id="a4a15-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a4a15-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a4a15-103">Contiene las propiedades de los posibles tipos de dispositivo iOS en los que se puede ejecutar la aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="a4a15-103">Contains properties of the possible iOS device types the mobile app can run on.</span></span>
## <a name="properties"></a><span data-ttu-id="a4a15-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a4a15-104">Properties</span></span>
|<span data-ttu-id="a4a15-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a4a15-105">Property</span></span>|<span data-ttu-id="a4a15-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="a4a15-106">Type</span></span>|<span data-ttu-id="a4a15-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4a15-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a4a15-108">iPad</span><span class="sxs-lookup"><span data-stu-id="a4a15-108">iPad</span></span>|<span data-ttu-id="a4a15-109">Booleano</span><span class="sxs-lookup"><span data-stu-id="a4a15-109">Boolean</span></span>|<span data-ttu-id="a4a15-110">Si la aplicación debe ejecutarse en iPad.</span><span class="sxs-lookup"><span data-stu-id="a4a15-110">Whether the app should run on iPads.</span></span>|
|<span data-ttu-id="a4a15-111">iPhoneAndIPod</span><span class="sxs-lookup"><span data-stu-id="a4a15-111">iPhoneAndIPod</span></span>|<span data-ttu-id="a4a15-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="a4a15-112">Boolean</span></span>|<span data-ttu-id="a4a15-113">Si la aplicación debe ejecutarse en iPhone y iPod.</span><span class="sxs-lookup"><span data-stu-id="a4a15-113">Whether the app should run on iPhones and iPods.</span></span>|

## <a name="relationships"></a><span data-ttu-id="a4a15-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a4a15-114">Relationships</span></span>
<span data-ttu-id="a4a15-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="a4a15-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="a4a15-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a4a15-116">JSON Representation</span></span>
<span data-ttu-id="a4a15-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a4a15-117">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosDeviceType"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.iosDeviceType",
  "iPad": true,
  "iPhoneAndIPod": true
}
```








