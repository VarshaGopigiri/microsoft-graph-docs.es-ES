# <a name="edgesearchengine-resource-type"></a><span data-ttu-id="0a529-101">Tipo de recurso edgeSearchEngine</span><span class="sxs-lookup"><span data-stu-id="0a529-101">edgeSearchEngine resource type</span></span>

> <span data-ttu-id="0a529-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0a529-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0a529-103">Permite a los administradores de TI configurar un motor de búsqueda predeterminado predefinido para dispositivos controlados por MDM.</span><span class="sxs-lookup"><span data-stu-id="0a529-103">Allows IT admins to set a predefined default search engine for MDM-Controlled devices.</span></span>

<span data-ttu-id="0a529-104">Hereda de [edgeSearchEngineBase](../resources/intune_deviceconfig_edgesearchenginebase.md)</span><span class="sxs-lookup"><span data-stu-id="0a529-104">Inherits from [edgeSearchEngineBase](../resources/intune_deviceconfig_edgesearchenginebase.md)</span></span>

## <a name="properties"></a><span data-ttu-id="0a529-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0a529-105">Properties</span></span>
|<span data-ttu-id="0a529-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0a529-106">Property</span></span>|<span data-ttu-id="0a529-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="0a529-107">Type</span></span>|<span data-ttu-id="0a529-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a529-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0a529-109">edgeSearchEngineType</span><span class="sxs-lookup"><span data-stu-id="0a529-109">edgeSearchEngineType</span></span>|[<span data-ttu-id="0a529-110">edgeSearchEngineType</span><span class="sxs-lookup"><span data-stu-id="0a529-110">edgeSearchEngineType</span></span>](../resources/intune_deviceconfig_edgesearchenginetype.md)|<span data-ttu-id="0a529-p101">Permite a los administradores de TI configurar un motor de búsqueda predeterminado predefinido para dispositivos controlados por MDM. Los posibles valores son: `default`, `bing`.</span><span class="sxs-lookup"><span data-stu-id="0a529-p101">Allows IT admins to set a predefined default search engine for MDM-Controlled devices. The possible values are: `default`, `bing`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="0a529-113">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0a529-113">Relationships</span></span>
<span data-ttu-id="0a529-114">Ninguna</span><span class="sxs-lookup"><span data-stu-id="0a529-114">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="0a529-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0a529-115">JSON Representation</span></span>
<span data-ttu-id="0a529-116">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="0a529-116">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.edgeSearchEngine"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.edgeSearchEngine",
  "edgeSearchEngineType": "String"
}
```








