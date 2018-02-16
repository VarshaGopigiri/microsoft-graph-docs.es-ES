# <a name="edgesearchengine-resource-type"></a><span data-ttu-id="2882a-101">Tipo de recurso edgeSearchEngine</span><span class="sxs-lookup"><span data-stu-id="2882a-101">edgeSearchEngine resource type</span></span>

> <span data-ttu-id="2882a-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2882a-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2882a-103">Permite a los administradores de TI configurar un motor de búsqueda predeterminado predefinido para dispositivos controlados por MDM.</span><span class="sxs-lookup"><span data-stu-id="2882a-103">Allows IT admins to set a predefined default search engine for MDM-Controlled devices.</span></span>

<span data-ttu-id="2882a-104">Hereda de [edgeSearchEngineBase](../resources/intune_deviceconfig_edgesearchenginebase.md)</span><span class="sxs-lookup"><span data-stu-id="2882a-104">Inherits from [edgeSearchEngineBase](../resources/intune_deviceconfig_edgesearchenginebase.md)</span></span>

## <a name="properties"></a><span data-ttu-id="2882a-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2882a-105">Properties</span></span>
|<span data-ttu-id="2882a-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2882a-106">Property</span></span>|<span data-ttu-id="2882a-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="2882a-107">Type</span></span>|<span data-ttu-id="2882a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="2882a-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2882a-109">edgeSearchEngineType</span><span class="sxs-lookup"><span data-stu-id="2882a-109">edgeSearchEngineType</span></span>|<span data-ttu-id="2882a-110">cadena</span><span class="sxs-lookup"><span data-stu-id="2882a-110">String</span></span>|<span data-ttu-id="2882a-111">Permite a los administradores de TI configurar un motor de búsqueda predeterminado predefinido para dispositivos controlados por MDM.</span><span class="sxs-lookup"><span data-stu-id="2882a-111">Allows IT admins to set a predefined default search engine for MDM-Controlled devices.</span></span> <span data-ttu-id="2882a-112">Los valores posibles son: `default` y `bing`.</span><span class="sxs-lookup"><span data-stu-id="2882a-112">Possible values are: `default`, `bing`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="2882a-113">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2882a-113">Relationships</span></span>
<span data-ttu-id="2882a-114">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2882a-114">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="2882a-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2882a-115">JSON Representation</span></span>
<span data-ttu-id="2882a-116">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2882a-116">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.edgeSearchEngine"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.edgeSearchEngine",
  "edgeSearchEngineType": "String"
}
```



