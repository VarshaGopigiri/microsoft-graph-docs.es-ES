# <a name="keyvaluepair-resource-type"></a><span data-ttu-id="1b64c-101">Tipo de recurso keyValuePair</span><span class="sxs-lookup"><span data-stu-id="1b64c-101">keyValuePair resource type</span></span>

> <span data-ttu-id="1b64c-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1b64c-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1b64c-103">Par clave-valor para almacenar la configuración personalizada</span><span class="sxs-lookup"><span data-stu-id="1b64c-103">Key value pair for storing custom settings</span></span>
## <a name="properties"></a><span data-ttu-id="1b64c-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1b64c-104">Properties</span></span>
|<span data-ttu-id="1b64c-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1b64c-105">Property</span></span>|<span data-ttu-id="1b64c-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="1b64c-106">Type</span></span>|<span data-ttu-id="1b64c-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b64c-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1b64c-108">name</span><span class="sxs-lookup"><span data-stu-id="1b64c-108">name</span></span>|<span data-ttu-id="1b64c-109">cadena</span><span class="sxs-lookup"><span data-stu-id="1b64c-109">String</span></span>|<span data-ttu-id="1b64c-110">Nombre de este par clave-valor</span><span class="sxs-lookup"><span data-stu-id="1b64c-110">Name for this key-value pair</span></span>|
|<span data-ttu-id="1b64c-111">valor</span><span class="sxs-lookup"><span data-stu-id="1b64c-111">value</span></span>|<span data-ttu-id="1b64c-112">cadena</span><span class="sxs-lookup"><span data-stu-id="1b64c-112">String</span></span>|<span data-ttu-id="1b64c-113">Valor de este par clave-valor</span><span class="sxs-lookup"><span data-stu-id="1b64c-113">Value for this key-value pair</span></span>|

## <a name="relationships"></a><span data-ttu-id="1b64c-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="1b64c-114">Relationships</span></span>
<span data-ttu-id="1b64c-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="1b64c-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="1b64c-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1b64c-116">JSON Representation</span></span>
<span data-ttu-id="1b64c-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1b64c-117">Here is a JSON representation of the resource.</span></span>
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



