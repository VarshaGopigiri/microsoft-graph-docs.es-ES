# <a name="edgesearchenginecustom-resource-type"></a><span data-ttu-id="812c2-101">Tipo de recurso edgeSearchEngineCustom</span><span class="sxs-lookup"><span data-stu-id="812c2-101">edgeSearchEngineCustom resource type</span></span>

> <span data-ttu-id="812c2-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="812c2-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="812c2-103">Permite a los administradores de TI configurar un motor de búsqueda predeterminado personalizado para dispositivos controlados por MDM.</span><span class="sxs-lookup"><span data-stu-id="812c2-103">Allows IT admins to set a custom default search engine for MDM-Controlled devices.</span></span>

<span data-ttu-id="812c2-104">Hereda de [edgeSearchEngineBase](../resources/intune_deviceconfig_edgesearchenginebase.md)</span><span class="sxs-lookup"><span data-stu-id="812c2-104">Inherits from [edgeSearchEngineBase](../resources/intune_deviceconfig_edgesearchenginebase.md)</span></span>

## <a name="properties"></a><span data-ttu-id="812c2-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="812c2-105">Properties</span></span>
|<span data-ttu-id="812c2-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="812c2-106">Property</span></span>|<span data-ttu-id="812c2-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="812c2-107">Type</span></span>|<span data-ttu-id="812c2-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="812c2-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="812c2-109">edgeSearchEngineOpenSearchXmlUrl</span><span class="sxs-lookup"><span data-stu-id="812c2-109">edgeSearchEngineOpenSearchXmlUrl</span></span>|<span data-ttu-id="812c2-110">cadena</span><span class="sxs-lookup"><span data-stu-id="812c2-110">String</span></span>|<span data-ttu-id="812c2-111">Apunta a un vínculo HTTPS que contiene el archivo XML OpenSearch, que incluye, como mínimo, el nombre corto y la dirección URL del motor de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="812c2-111">Points to a https link containing the OpenSearch xml file that contains, at minimum, the short name and the URL to the search Engine.</span></span>|

## <a name="relationships"></a><span data-ttu-id="812c2-112">Relaciones</span><span class="sxs-lookup"><span data-stu-id="812c2-112">Relationships</span></span>
<span data-ttu-id="812c2-113">Ninguna</span><span class="sxs-lookup"><span data-stu-id="812c2-113">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="812c2-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="812c2-114">JSON Representation</span></span>
<span data-ttu-id="812c2-115">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="812c2-115">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.edgeSearchEngineBase",
  "@odata.type": "microsoft.graph.edgeSearchEngineCustom"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.edgeSearchEngineCustom",
  "edgeSearchEngineOpenSearchXmlUrl": "String"
}
```



