# <a name="auditproperty-resource-type"></a><span data-ttu-id="3e7bc-101">Tipo de recurso auditProperty</span><span class="sxs-lookup"><span data-stu-id="3e7bc-101">auditProperty resource type</span></span>

> <span data-ttu-id="3e7bc-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3e7bc-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3e7bc-103">Una clase que contiene las propiedades de la propiedad de auditoría.</span><span class="sxs-lookup"><span data-stu-id="3e7bc-103">A class containing the properties for Audit Property.</span></span>
## <a name="properties"></a><span data-ttu-id="3e7bc-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3e7bc-104">Properties</span></span>
|<span data-ttu-id="3e7bc-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3e7bc-105">Property</span></span>|<span data-ttu-id="3e7bc-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="3e7bc-106">Type</span></span>|<span data-ttu-id="3e7bc-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="3e7bc-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3e7bc-108">displayName</span><span class="sxs-lookup"><span data-stu-id="3e7bc-108">displayName</span></span>|<span data-ttu-id="3e7bc-109">cadena</span><span class="sxs-lookup"><span data-stu-id="3e7bc-109">String</span></span>|<span data-ttu-id="3e7bc-110">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="3e7bc-110">Display name.</span></span>|
|<span data-ttu-id="3e7bc-111">oldValue</span><span class="sxs-lookup"><span data-stu-id="3e7bc-111">oldValue</span></span>|<span data-ttu-id="3e7bc-112">cadena</span><span class="sxs-lookup"><span data-stu-id="3e7bc-112">String</span></span>|<span data-ttu-id="3e7bc-113">Valor antiguo.</span><span class="sxs-lookup"><span data-stu-id="3e7bc-113">Old value.</span></span>|
|<span data-ttu-id="3e7bc-114">newValue</span><span class="sxs-lookup"><span data-stu-id="3e7bc-114">newValue</span></span>|<span data-ttu-id="3e7bc-115">cadena</span><span class="sxs-lookup"><span data-stu-id="3e7bc-115">String</span></span>|<span data-ttu-id="3e7bc-116">Valor nuevo.</span><span class="sxs-lookup"><span data-stu-id="3e7bc-116">New value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="3e7bc-117">Relaciones</span><span class="sxs-lookup"><span data-stu-id="3e7bc-117">Relationships</span></span>
<span data-ttu-id="3e7bc-118">Ninguna</span><span class="sxs-lookup"><span data-stu-id="3e7bc-118">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="3e7bc-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3e7bc-119">JSON Representation</span></span>
<span data-ttu-id="3e7bc-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3e7bc-120">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.auditProperty"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.auditProperty",
  "displayName": "String",
  "oldValue": "String",
  "newValue": "String"
}
```



