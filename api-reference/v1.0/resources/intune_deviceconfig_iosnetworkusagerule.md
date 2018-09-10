# <a name="iosnetworkusagerule-resource-type"></a><span data-ttu-id="f9b44-101">Tipo de recurso iosNetworkUsageRule</span><span class="sxs-lookup"><span data-stu-id="f9b44-101">iosNetworkUsageRule resource type</span></span>

> <span data-ttu-id="f9b44-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f9b44-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f9b44-103">Las reglas de uso de red permiten a las empresas especificar cómo las aplicaciones administradas usan las redes, como las redes de datos de telefonía móvil.</span><span class="sxs-lookup"><span data-stu-id="f9b44-103">Network Usage Rules allow enterprises to specify how managed apps use networks, such as cellular data networks.</span></span>
## <a name="properties"></a><span data-ttu-id="f9b44-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f9b44-104">Properties</span></span>
|<span data-ttu-id="f9b44-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f9b44-105">Property</span></span>|<span data-ttu-id="f9b44-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="f9b44-106">Type</span></span>|<span data-ttu-id="f9b44-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9b44-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f9b44-108">managedApps</span><span class="sxs-lookup"><span data-stu-id="f9b44-108">managedApps</span></span>|<span data-ttu-id="f9b44-109">Colección [appListItem](../resources/intune_deviceconfig_applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="f9b44-109">[appListItem](../resources/intune_deviceconfig_applistitem.md) collection</span></span>|<span data-ttu-id="f9b44-110">Información sobre las aplicaciones administradas a las que se va a aplicar esta regla.</span><span class="sxs-lookup"><span data-stu-id="f9b44-110">Information about the managed apps that this rule is going to apply to.</span></span> <span data-ttu-id="f9b44-111">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="f9b44-111">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="f9b44-112">cellularDataBlockWhenRoaming</span><span class="sxs-lookup"><span data-stu-id="f9b44-112">cellularDataBlockWhenRoaming</span></span>|<span data-ttu-id="f9b44-113">Booleano</span><span class="sxs-lookup"><span data-stu-id="f9b44-113">Boolean</span></span>|<span data-ttu-id="f9b44-114">Si se establece en true, las aplicaciones administradas correspondientes no podrán usar los datos de telefonía móvil en itinerancia.</span><span class="sxs-lookup"><span data-stu-id="f9b44-114">If set to true, corresponding managed apps will not be allowed to use cellular data when roaming.</span></span>|
|<span data-ttu-id="f9b44-115">cellularDataBlocked</span><span class="sxs-lookup"><span data-stu-id="f9b44-115">cellularDataBlocked</span></span>|<span data-ttu-id="f9b44-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="f9b44-116">Boolean</span></span>|<span data-ttu-id="f9b44-117">Si se establece en true, las aplicaciones administradas correspondientes no podrán usar los datos de telefonía móvil en ningún momento.</span><span class="sxs-lookup"><span data-stu-id="f9b44-117">If set to true, corresponding managed apps will not be allowed to use cellular data at any time.</span></span>|

## <a name="relationships"></a><span data-ttu-id="f9b44-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f9b44-118">Relationships</span></span>
<span data-ttu-id="f9b44-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f9b44-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f9b44-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f9b44-120">JSON Representation</span></span>
<span data-ttu-id="f9b44-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f9b44-121">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosNetworkUsageRule"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.iosNetworkUsageRule",
  "managedApps": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "String",
      "publisher": "String",
      "appStoreUrl": "String",
      "appId": "String"
    }
  ],
  "cellularDataBlockWhenRoaming": true,
  "cellularDataBlocked": true
}
```








