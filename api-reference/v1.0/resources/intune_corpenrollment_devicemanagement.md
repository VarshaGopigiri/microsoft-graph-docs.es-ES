# <a name="devicemanagement-resource-type"></a><span data-ttu-id="16178-101">Tipo de recurso deviceManagement</span><span class="sxs-lookup"><span data-stu-id="16178-101">deviceManagement resource type</span></span>

> <span data-ttu-id="16178-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="16178-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="16178-103">El recurso deviceManagement representa las identidades de dispositivo de colección de un espacio empresarial que se han preconfigurado en Intune y los perfiles de inscripción que se pueden asignar a las identidades de dispositivos compatibles con la configuración de preinscripción.</span><span class="sxs-lookup"><span data-stu-id="16178-103">The deviceManagement resource represents a tenant's collection device identities that have been pre-staged in Intune, and the enrollment profiles that may be assigned to device identities that support pre-enrollment configuration.</span></span>
## <a name="methods"></a><span data-ttu-id="16178-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="16178-104">Methods</span></span>
|<span data-ttu-id="16178-105">Método</span><span class="sxs-lookup"><span data-stu-id="16178-105">Method</span></span>|<span data-ttu-id="16178-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="16178-106">Return Type</span></span>|<span data-ttu-id="16178-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="16178-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="16178-108">Obtener deviceManagement</span><span class="sxs-lookup"><span data-stu-id="16178-108">Get deviceManagement</span></span>](../api/intune_corpenrollment_devicemanagement_get.md)|[<span data-ttu-id="16178-109">deviceManagement</span><span class="sxs-lookup"><span data-stu-id="16178-109">deviceManagement</span></span>](../resources/intune_corpenrollment_devicemanagement.md)|<span data-ttu-id="16178-110">Lea las propiedades y las relaciones del objeto [deviceManagement](../resources/intune_corpenrollment_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="16178-110">Read properties and relationships of [plannerTaskDetails](../resources/intune_corpenrollment_devicemanagement.md) object.</span></span>|
|[<span data-ttu-id="16178-111">Actualizar deviceManagement</span><span class="sxs-lookup"><span data-stu-id="16178-111">Update deviceManagement</span></span>](../api/intune_corpenrollment_devicemanagement_update.md)|[<span data-ttu-id="16178-112">deviceManagement</span><span class="sxs-lookup"><span data-stu-id="16178-112">deviceManagement</span></span>](../resources/intune_corpenrollment_devicemanagement.md)|<span data-ttu-id="16178-113">Actualice las propiedades de un objeto [deviceManagement](../resources/intune_corpenrollment_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="16178-113">Update the properties of a [calendar](../resources/intune_corpenrollment_devicemanagement.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="16178-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="16178-114">Properties</span></span>
|<span data-ttu-id="16178-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="16178-115">Property</span></span>|<span data-ttu-id="16178-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="16178-116">Type</span></span>|<span data-ttu-id="16178-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="16178-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="16178-118">id</span><span class="sxs-lookup"><span data-stu-id="16178-118">id</span></span>|<span data-ttu-id="16178-119">cadena</span><span class="sxs-lookup"><span data-stu-id="16178-119">String</span></span>|<span data-ttu-id="16178-120">El GUID para el objeto.</span><span class="sxs-lookup"><span data-stu-id="16178-120">The resource GUID for the security object is not valid.</span></span>|

## <a name="relationships"></a><span data-ttu-id="16178-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="16178-121">Relationships</span></span>
<span data-ttu-id="16178-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="16178-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="16178-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="16178-123">JSON Representation</span></span>
<span data-ttu-id="16178-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="16178-124">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagement"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagement",
  "id": "String (identifier)"
}
```



