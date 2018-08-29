# <a name="keyvaluepair-resource-type"></a><span data-ttu-id="8212d-101">Tipo de recurso keyValuePair</span><span class="sxs-lookup"><span data-stu-id="8212d-101">keyValuePair resource type</span></span>

> <span data-ttu-id="8212d-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8212d-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8212d-103">Par clave-valor para almacenar la configuración personalizada</span><span class="sxs-lookup"><span data-stu-id="8212d-103">Key value pair for storing custom settings</span></span>
## <a name="properties"></a><span data-ttu-id="8212d-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8212d-104">Properties</span></span>
|<span data-ttu-id="8212d-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8212d-105">Property</span></span>|<span data-ttu-id="8212d-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="8212d-106">Type</span></span>|<span data-ttu-id="8212d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="8212d-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8212d-108">name</span><span class="sxs-lookup"><span data-stu-id="8212d-108">name</span></span>|<span data-ttu-id="8212d-109">cadena</span><span class="sxs-lookup"><span data-stu-id="8212d-109">String</span></span>|<span data-ttu-id="8212d-110">Nombre de este par clave-valor</span><span class="sxs-lookup"><span data-stu-id="8212d-110">Name for this key-value pair</span></span>|
|<span data-ttu-id="8212d-111">valor</span><span class="sxs-lookup"><span data-stu-id="8212d-111">value</span></span>|<span data-ttu-id="8212d-112">cadena</span><span class="sxs-lookup"><span data-stu-id="8212d-112">String</span></span>|<span data-ttu-id="8212d-113">Valor de este par clave-valor</span><span class="sxs-lookup"><span data-stu-id="8212d-113">Value for this key-value pair</span></span>|

## <a name="relationships"></a><span data-ttu-id="8212d-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8212d-114">Relationships</span></span>
<span data-ttu-id="8212d-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8212d-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8212d-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8212d-116">JSON Representation</span></span>
<span data-ttu-id="8212d-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8212d-117">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.keyValuePair"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.keyValuePair",
  "name": "String",
  "value": "String"
}
```



