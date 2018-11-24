# <a name="keyvaluepair-resource-type"></a><span data-ttu-id="17fb6-101">Tipo de recurso keyValuePair</span><span class="sxs-lookup"><span data-stu-id="17fb6-101">keyValuePair resource type</span></span>

> <span data-ttu-id="17fb6-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="17fb6-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="17fb6-103">Par clave-valor para almacenar la configuración personalizada</span><span class="sxs-lookup"><span data-stu-id="17fb6-103">Key value pair for storing custom settings</span></span>
## <a name="properties"></a><span data-ttu-id="17fb6-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="17fb6-104">Properties</span></span>
|<span data-ttu-id="17fb6-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="17fb6-105">Property</span></span>|<span data-ttu-id="17fb6-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="17fb6-106">Type</span></span>|<span data-ttu-id="17fb6-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="17fb6-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="17fb6-108">name</span><span class="sxs-lookup"><span data-stu-id="17fb6-108">name</span></span>|<span data-ttu-id="17fb6-109">cadena</span><span class="sxs-lookup"><span data-stu-id="17fb6-109">String</span></span>|<span data-ttu-id="17fb6-110">Nombre de este par clave-valor</span><span class="sxs-lookup"><span data-stu-id="17fb6-110">Name for this key-value pair</span></span>|
|<span data-ttu-id="17fb6-111">value</span><span class="sxs-lookup"><span data-stu-id="17fb6-111">value</span></span>|<span data-ttu-id="17fb6-112">cadena</span><span class="sxs-lookup"><span data-stu-id="17fb6-112">String</span></span>|<span data-ttu-id="17fb6-113">Valor de este par clave-valor</span><span class="sxs-lookup"><span data-stu-id="17fb6-113">Value for this key-value pair</span></span>|

## <a name="relationships"></a><span data-ttu-id="17fb6-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="17fb6-114">Relationships</span></span>
<span data-ttu-id="17fb6-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="17fb6-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="17fb6-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="17fb6-116">JSON Representation</span></span>
<span data-ttu-id="17fb6-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="17fb6-117">Here is a JSON representation of the resource.</span></span>
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



