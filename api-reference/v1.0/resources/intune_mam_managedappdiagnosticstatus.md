# <a name="managedappdiagnosticstatus-resource-type"></a><span data-ttu-id="a8c32-101">Tipo de recurso managedAppDiagnosticStatus</span><span class="sxs-lookup"><span data-stu-id="a8c32-101">managedAppDiagnosticStatus resource type</span></span>

> <span data-ttu-id="a8c32-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a8c32-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a8c32-103">Representa el estado de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="a8c32-103">Represents diagnostics status.</span></span>
## <a name="properties"></a><span data-ttu-id="a8c32-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a8c32-104">Properties</span></span>
|<span data-ttu-id="a8c32-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a8c32-105">Property</span></span>|<span data-ttu-id="a8c32-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="a8c32-106">Type</span></span>|<span data-ttu-id="a8c32-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8c32-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a8c32-108">validationName</span><span class="sxs-lookup"><span data-stu-id="a8c32-108">validationName</span></span>|<span data-ttu-id="a8c32-109">cadena</span><span class="sxs-lookup"><span data-stu-id="a8c32-109">String</span></span>|<span data-ttu-id="a8c32-110">El nombre descriptivo de validación</span><span class="sxs-lookup"><span data-stu-id="a8c32-110">The validation friendly name</span></span>|
|<span data-ttu-id="a8c32-111">estado</span><span class="sxs-lookup"><span data-stu-id="a8c32-111">state</span></span>|<span data-ttu-id="a8c32-112">cadena</span><span class="sxs-lookup"><span data-stu-id="a8c32-112">String</span></span>|<span data-ttu-id="a8c32-113">El estado actual de la operación.</span><span class="sxs-lookup"><span data-stu-id="a8c32-113">The state of the operation</span></span>|
|<span data-ttu-id="a8c32-114">mitigationInstruction</span><span class="sxs-lookup"><span data-stu-id="a8c32-114">mitigationInstruction</span></span>|<span data-ttu-id="a8c32-115">cadena</span><span class="sxs-lookup"><span data-stu-id="a8c32-115">String</span></span>|<span data-ttu-id="a8c32-116">Instrucciones sobre cómo reducir un error de validación</span><span class="sxs-lookup"><span data-stu-id="a8c32-116">Instruction on how to mitigate a failed validation</span></span>|

## <a name="relationships"></a><span data-ttu-id="a8c32-117">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a8c32-117">Relationships</span></span>
<span data-ttu-id="a8c32-118">Ninguna</span><span class="sxs-lookup"><span data-stu-id="a8c32-118">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="a8c32-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a8c32-119">JSON Representation</span></span>
<span data-ttu-id="a8c32-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a8c32-120">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.managedAppDiagnosticStatus"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppDiagnosticStatus",
  "validationName": "String",
  "state": "String",
  "mitigationInstruction": "String"
}
```



