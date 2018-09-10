# <a name="windowsinformationprotectionresourcecollection-resource-type"></a><span data-ttu-id="b9f53-101">Tipo de recurso windowsInformationProtectionResourceCollection</span><span class="sxs-lookup"><span data-stu-id="b9f53-101">windowsInformationProtectionResourceCollection resource type</span></span>

> <span data-ttu-id="b9f53-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b9f53-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b9f53-103">Colección de recursos de Windows Information Protection</span><span class="sxs-lookup"><span data-stu-id="b9f53-103">Windows Information Protection Resource Collection</span></span>
## <a name="properties"></a><span data-ttu-id="b9f53-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b9f53-104">Properties</span></span>
|<span data-ttu-id="b9f53-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b9f53-105">Property</span></span>|<span data-ttu-id="b9f53-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="b9f53-106">Type</span></span>|<span data-ttu-id="b9f53-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9f53-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b9f53-108">displayName</span><span class="sxs-lookup"><span data-stu-id="b9f53-108">displayName</span></span>|<span data-ttu-id="b9f53-109">cadena</span><span class="sxs-lookup"><span data-stu-id="b9f53-109">String</span></span>|<span data-ttu-id="b9f53-110">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="b9f53-110">Display name</span></span>|
|<span data-ttu-id="b9f53-111">resources</span><span class="sxs-lookup"><span data-stu-id="b9f53-111">resources</span></span>|<span data-ttu-id="b9f53-112">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="b9f53-112">String collection</span></span>|<span data-ttu-id="b9f53-113">Colección de recursos</span><span class="sxs-lookup"><span data-stu-id="b9f53-113">Collection of resources</span></span>|

## <a name="relationships"></a><span data-ttu-id="b9f53-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b9f53-114">Relationships</span></span>
<span data-ttu-id="b9f53-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="b9f53-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="b9f53-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b9f53-116">JSON Representation</span></span>
<span data-ttu-id="b9f53-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b9f53-117">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionResourceCollection",
  "displayName": "String",
  "resources": [
    "String"
  ]
}
```








