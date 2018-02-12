# <a name="keyvaluepair-resource-type"></a><span data-ttu-id="4ccd5-101">Tipo de recurso keyValuePair</span><span class="sxs-lookup"><span data-stu-id="4ccd5-101">keyValuePair resource type</span></span>

> <span data-ttu-id="4ccd5-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4ccd5-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4ccd5-103">Par clave-valor para almacenar la configuración personalizada</span><span class="sxs-lookup"><span data-stu-id="4ccd5-103">Key value pair for storing custom settings</span></span>
## <a name="properties"></a><span data-ttu-id="4ccd5-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4ccd5-104">Properties</span></span>
|<span data-ttu-id="4ccd5-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4ccd5-105">Property</span></span>|<span data-ttu-id="4ccd5-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="4ccd5-106">Type</span></span>|<span data-ttu-id="4ccd5-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="4ccd5-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4ccd5-108">name</span><span class="sxs-lookup"><span data-stu-id="4ccd5-108">name</span></span>|<span data-ttu-id="4ccd5-109">cadena</span><span class="sxs-lookup"><span data-stu-id="4ccd5-109">String</span></span>|<span data-ttu-id="4ccd5-110">Nombre de este par clave-valor</span><span class="sxs-lookup"><span data-stu-id="4ccd5-110">Name for this key-value pair</span></span>|
|<span data-ttu-id="4ccd5-111">value</span><span class="sxs-lookup"><span data-stu-id="4ccd5-111">value</span></span>|<span data-ttu-id="4ccd5-112">cadena</span><span class="sxs-lookup"><span data-stu-id="4ccd5-112">String</span></span>|<span data-ttu-id="4ccd5-113">Valor de este par clave-valor</span><span class="sxs-lookup"><span data-stu-id="4ccd5-113">Value for this key-value pair</span></span>|

## <a name="relationships"></a><span data-ttu-id="4ccd5-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4ccd5-114">Relationships</span></span>
<span data-ttu-id="4ccd5-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="4ccd5-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="4ccd5-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4ccd5-116">JSON Representation</span></span>
<span data-ttu-id="4ccd5-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4ccd5-117">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
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



