# <a name="ioshomescreenapp-resource-type"></a><span data-ttu-id="a25a2-101">Tipo de recurso iosHomeScreenApp</span><span class="sxs-lookup"><span data-stu-id="a25a2-101">iosHomeScreenApp resource type</span></span>

> <span data-ttu-id="a25a2-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a25a2-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a25a2-103">Representa un icono de una aplicación en la pantalla de inicio</span><span class="sxs-lookup"><span data-stu-id="a25a2-103">Represents an icon for an app on the Home Screen</span></span>

<span data-ttu-id="a25a2-104">Hereda de [iosHomeScreenItem](../resources/intune_deviceconfig_ioshomescreenitem.md)</span><span class="sxs-lookup"><span data-stu-id="a25a2-104">Inherits from [iosHomeScreenItem](../resources/intune_deviceconfig_ioshomescreenitem.md)</span></span>

## <a name="properties"></a><span data-ttu-id="a25a2-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a25a2-105">Properties</span></span>
|<span data-ttu-id="a25a2-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a25a2-106">Property</span></span>|<span data-ttu-id="a25a2-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="a25a2-107">Type</span></span>|<span data-ttu-id="a25a2-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="a25a2-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a25a2-109">displayName</span><span class="sxs-lookup"><span data-stu-id="a25a2-109">displayName</span></span>|<span data-ttu-id="a25a2-110">cadena</span><span class="sxs-lookup"><span data-stu-id="a25a2-110">String</span></span>|<span data-ttu-id="a25a2-111">Nombre de la aplicación heredado de [iosHomeScreenItem](../resources/intune_deviceconfig_ioshomescreenitem.md)</span><span class="sxs-lookup"><span data-stu-id="a25a2-111">Name of the app Inherited from [iosHomeScreenItem](../resources/intune_deviceconfig_ioshomescreenitem.md)</span></span>|
|<span data-ttu-id="a25a2-112">bundleID</span><span class="sxs-lookup"><span data-stu-id="a25a2-112">bundleID</span></span>|<span data-ttu-id="a25a2-113">cadena</span><span class="sxs-lookup"><span data-stu-id="a25a2-113">String</span></span>|<span data-ttu-id="a25a2-114">BundleID de la aplicación</span><span class="sxs-lookup"><span data-stu-id="a25a2-114">BundleID of app</span></span>|

## <a name="relationships"></a><span data-ttu-id="a25a2-115">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a25a2-115">Relationships</span></span>
<span data-ttu-id="a25a2-116">Ninguna</span><span class="sxs-lookup"><span data-stu-id="a25a2-116">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="a25a2-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a25a2-117">JSON Representation</span></span>
<span data-ttu-id="a25a2-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a25a2-118">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosHomeScreenApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosHomeScreenApp",
  "displayName": "String",
  "bundleID": "String"
}
```



