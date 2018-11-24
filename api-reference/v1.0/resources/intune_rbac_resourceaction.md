# <a name="resourceaction-resource-type"></a><span data-ttu-id="3656a-101">Tipo de recurso resourceAction</span><span class="sxs-lookup"><span data-stu-id="3656a-101">resourceAction resource type</span></span>

> <span data-ttu-id="3656a-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3656a-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3656a-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="3656a-103">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="3656a-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3656a-104">Properties</span></span>
|<span data-ttu-id="3656a-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3656a-105">Property</span></span>|<span data-ttu-id="3656a-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="3656a-106">Type</span></span>|<span data-ttu-id="3656a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="3656a-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3656a-108">allowedResourceActions</span><span class="sxs-lookup"><span data-stu-id="3656a-108">allowedResourceActions</span></span>|<span data-ttu-id="3656a-109">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="3656a-109">String collection</span></span>|<span data-ttu-id="3656a-110">Acciones permitidas</span><span class="sxs-lookup"><span data-stu-id="3656a-110">Allowed Actions</span></span>|
|<span data-ttu-id="3656a-111">notAllowedResourceActions</span><span class="sxs-lookup"><span data-stu-id="3656a-111">notAllowedResourceActions</span></span>|<span data-ttu-id="3656a-112">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="3656a-112">String collection</span></span>|<span data-ttu-id="3656a-113">Acciones no permitidas</span><span class="sxs-lookup"><span data-stu-id="3656a-113">Not Allowed Actions</span></span>|

## <a name="relationships"></a><span data-ttu-id="3656a-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="3656a-114">Relationships</span></span>
<span data-ttu-id="3656a-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="3656a-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="3656a-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3656a-116">JSON Representation</span></span>
<span data-ttu-id="3656a-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3656a-117">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.resourceAction"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.resourceAction",
  "allowedResourceActions": [
    "String"
  ],
  "notAllowedResourceActions": [
    "String"
  ]
}
```



