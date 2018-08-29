# <a name="omasetting-resource-type"></a><span data-ttu-id="179ad-101">Tipo de recurso omaSetting</span><span class="sxs-lookup"><span data-stu-id="179ad-101">omaSetting resource type</span></span>

> <span data-ttu-id="179ad-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="179ad-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="179ad-103">Definición de la configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="179ad-103">OMA Settings definition.</span></span>
## <a name="properties"></a><span data-ttu-id="179ad-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="179ad-104">Properties</span></span>
|<span data-ttu-id="179ad-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="179ad-105">Property</span></span>|<span data-ttu-id="179ad-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="179ad-106">Type</span></span>|<span data-ttu-id="179ad-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="179ad-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="179ad-108">displayName</span><span class="sxs-lookup"><span data-stu-id="179ad-108">displayName</span></span>|<span data-ttu-id="179ad-109">cadena</span><span class="sxs-lookup"><span data-stu-id="179ad-109">String</span></span>|<span data-ttu-id="179ad-110">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="179ad-110">Display Name.</span></span>|
|<span data-ttu-id="179ad-111">description</span><span class="sxs-lookup"><span data-stu-id="179ad-111">description</span></span>|<span data-ttu-id="179ad-112">String</span><span class="sxs-lookup"><span data-stu-id="179ad-112">String</span></span>|<span data-ttu-id="179ad-113">Descripción.</span><span class="sxs-lookup"><span data-stu-id="179ad-113">Description.</span></span>|
|<span data-ttu-id="179ad-114">omaUri</span><span class="sxs-lookup"><span data-stu-id="179ad-114">omaUri</span></span>|<span data-ttu-id="179ad-115">cadena</span><span class="sxs-lookup"><span data-stu-id="179ad-115">String</span></span>|<span data-ttu-id="179ad-116">OMA.</span><span class="sxs-lookup"><span data-stu-id="179ad-116">OMA.</span></span>|

## <a name="relationships"></a><span data-ttu-id="179ad-117">Relaciones</span><span class="sxs-lookup"><span data-stu-id="179ad-117">Relationships</span></span>
<span data-ttu-id="179ad-118">Ninguna</span><span class="sxs-lookup"><span data-stu-id="179ad-118">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="179ad-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="179ad-119">JSON Representation</span></span>
<span data-ttu-id="179ad-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="179ad-120">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "abstract": true,
  "@odata.type": "microsoft.graph.omaSetting"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.omaSetting",
  "displayName": "String",
  "description": "String",
  "omaUri": "String"
}
```



