# <a name="auditproperty-resource-type"></a><span data-ttu-id="25f7f-101">Tipo de recurso auditProperty</span><span class="sxs-lookup"><span data-stu-id="25f7f-101">auditProperty resource type</span></span>

> <span data-ttu-id="25f7f-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="25f7f-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="25f7f-103">Una clase que contiene las propiedades de la propiedad de auditoría.</span><span class="sxs-lookup"><span data-stu-id="25f7f-103">A class containing the properties for Audit Property.</span></span>
## <a name="properties"></a><span data-ttu-id="25f7f-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="25f7f-104">Properties</span></span>
|<span data-ttu-id="25f7f-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="25f7f-105">Property</span></span>|<span data-ttu-id="25f7f-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="25f7f-106">Type</span></span>|<span data-ttu-id="25f7f-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="25f7f-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="25f7f-108">displayName</span><span class="sxs-lookup"><span data-stu-id="25f7f-108">displayName</span></span>|<span data-ttu-id="25f7f-109">cadena</span><span class="sxs-lookup"><span data-stu-id="25f7f-109">String</span></span>|<span data-ttu-id="25f7f-110">Nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="25f7f-110">Display name.</span></span>|
|<span data-ttu-id="25f7f-111">oldValue</span><span class="sxs-lookup"><span data-stu-id="25f7f-111">oldValue</span></span>|<span data-ttu-id="25f7f-112">cadena</span><span class="sxs-lookup"><span data-stu-id="25f7f-112">String</span></span>|<span data-ttu-id="25f7f-113">Valor antiguo.</span><span class="sxs-lookup"><span data-stu-id="25f7f-113">Old value.</span></span>|
|<span data-ttu-id="25f7f-114">newValue</span><span class="sxs-lookup"><span data-stu-id="25f7f-114">newValue</span></span>|<span data-ttu-id="25f7f-115">cadena</span><span class="sxs-lookup"><span data-stu-id="25f7f-115">String</span></span>|<span data-ttu-id="25f7f-116">Valor nuevo.</span><span class="sxs-lookup"><span data-stu-id="25f7f-116">New value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="25f7f-117">Relaciones</span><span class="sxs-lookup"><span data-stu-id="25f7f-117">Relationships</span></span>
<span data-ttu-id="25f7f-118">Ninguna</span><span class="sxs-lookup"><span data-stu-id="25f7f-118">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="25f7f-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="25f7f-119">JSON Representation</span></span>
<span data-ttu-id="25f7f-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="25f7f-120">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.auditProperty"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.auditProperty",
  "displayName": "String",
  "oldValue": "String",
  "newValue": "String"
}
```



