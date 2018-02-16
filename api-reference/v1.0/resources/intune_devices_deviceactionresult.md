# <a name="deviceactionresult-resource-type"></a><span data-ttu-id="66dfd-101">Tipo de recurso deviceActionResult</span><span class="sxs-lookup"><span data-stu-id="66dfd-101">deviceActionResult resource type</span></span>

> <span data-ttu-id="66dfd-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="66dfd-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="66dfd-103">Resultado de la acción de dispositivo</span><span class="sxs-lookup"><span data-stu-id="66dfd-103">Device action result</span></span>
## <a name="properties"></a><span data-ttu-id="66dfd-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="66dfd-104">Properties</span></span>
|<span data-ttu-id="66dfd-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="66dfd-105">Property</span></span>|<span data-ttu-id="66dfd-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="66dfd-106">Type</span></span>|<span data-ttu-id="66dfd-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="66dfd-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="66dfd-108">actionName</span><span class="sxs-lookup"><span data-stu-id="66dfd-108">actionName</span></span>|<span data-ttu-id="66dfd-109">cadena</span><span class="sxs-lookup"><span data-stu-id="66dfd-109">String</span></span>|<span data-ttu-id="66dfd-110">Nombre de acción</span><span class="sxs-lookup"><span data-stu-id="66dfd-110">Action name</span></span>|
|<span data-ttu-id="66dfd-111">actionState</span><span class="sxs-lookup"><span data-stu-id="66dfd-111">actionState</span></span>|<span data-ttu-id="66dfd-112">cadena</span><span class="sxs-lookup"><span data-stu-id="66dfd-112">String</span></span>|<span data-ttu-id="66dfd-113">Estado de la acción. Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="66dfd-113">State of the action Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="66dfd-114">startDateTime</span><span class="sxs-lookup"><span data-stu-id="66dfd-114">startDateTime</span></span>|<span data-ttu-id="66dfd-115">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="66dfd-115">DateTimeOffset</span></span>|<span data-ttu-id="66dfd-116">Hora a la que se inició la acción</span><span class="sxs-lookup"><span data-stu-id="66dfd-116">Time the action was initiated</span></span>|
|<span data-ttu-id="66dfd-117">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="66dfd-117">lastUpdatedDateTime</span></span>|<span data-ttu-id="66dfd-118">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="66dfd-118">DateTimeOffset</span></span>|<span data-ttu-id="66dfd-119">Hora en la que se actualizó por última vez el estado de la acción</span><span class="sxs-lookup"><span data-stu-id="66dfd-119">Time the action state was last updated</span></span>|

## <a name="relationships"></a><span data-ttu-id="66dfd-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="66dfd-120">Relationships</span></span>
<span data-ttu-id="66dfd-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="66dfd-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="66dfd-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="66dfd-122">JSON Representation</span></span>
<span data-ttu-id="66dfd-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="66dfd-123">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceActionResult"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceActionResult",
  "actionName": "String",
  "actionState": "String",
  "startDateTime": "String (timestamp)",
  "lastUpdatedDateTime": "String (timestamp)"
}
```



