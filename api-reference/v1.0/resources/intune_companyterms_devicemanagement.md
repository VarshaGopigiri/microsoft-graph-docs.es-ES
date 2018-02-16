# <a name="devicemanagement-resource-type"></a><span data-ttu-id="50975-101">Tipo de recurso deviceManagement</span><span class="sxs-lookup"><span data-stu-id="50975-101">deviceManagement resource type</span></span>

> <span data-ttu-id="50975-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="50975-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="50975-103">Entidad singleton que actúa como un contenedor para todas las funcionalidades de administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="50975-103">Singleton entity that acts as a container for all device management functionality.</span></span>
## <a name="methods"></a><span data-ttu-id="50975-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="50975-104">Methods</span></span>
|<span data-ttu-id="50975-105">Método</span><span class="sxs-lookup"><span data-stu-id="50975-105">Method</span></span>|<span data-ttu-id="50975-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="50975-106">Return Type</span></span>|<span data-ttu-id="50975-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="50975-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="50975-108">Obtener deviceManagement</span><span class="sxs-lookup"><span data-stu-id="50975-108">Get deviceManagement</span></span>](../api/intune_companyterms_devicemanagement_get.md)|[<span data-ttu-id="50975-109">deviceManagement</span><span class="sxs-lookup"><span data-stu-id="50975-109">deviceManagement</span></span>](../resources/intune_companyterms_devicemanagement.md)|<span data-ttu-id="50975-110">Lea las propiedades y las relaciones del objeto [deviceManagement](../resources/intune_companyterms_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="50975-110">Read properties and relationships of [plannerTaskDetails](../resources/intune_companyterms_devicemanagement.md) object.</span></span>|
|[<span data-ttu-id="50975-111">Actualizar deviceManagement</span><span class="sxs-lookup"><span data-stu-id="50975-111">Update deviceManagement</span></span>](../api/intune_companyterms_devicemanagement_update.md)|[<span data-ttu-id="50975-112">deviceManagement</span><span class="sxs-lookup"><span data-stu-id="50975-112">deviceManagement</span></span>](../resources/intune_companyterms_devicemanagement.md)|<span data-ttu-id="50975-113">Actualice las propiedades de un objeto [deviceManagement](../resources/intune_companyterms_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="50975-113">Update the properties of a [calendar](../resources/intune_companyterms_devicemanagement.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="50975-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="50975-114">Properties</span></span>
|<span data-ttu-id="50975-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="50975-115">Property</span></span>|<span data-ttu-id="50975-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="50975-116">Type</span></span>|<span data-ttu-id="50975-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="50975-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="50975-118">id</span><span class="sxs-lookup"><span data-stu-id="50975-118">id</span></span>|<span data-ttu-id="50975-119">cadena</span><span class="sxs-lookup"><span data-stu-id="50975-119">String</span></span>|<span data-ttu-id="50975-120">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="50975-120">Not yet documented</span></span>|

## <a name="relationships"></a><span data-ttu-id="50975-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="50975-121">Relationships</span></span>
|<span data-ttu-id="50975-122">Relación</span><span class="sxs-lookup"><span data-stu-id="50975-122">Relationship</span></span>|<span data-ttu-id="50975-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="50975-123">Type</span></span>|<span data-ttu-id="50975-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="50975-124">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="50975-125">termsAndConditions</span><span class="sxs-lookup"><span data-stu-id="50975-125">termsAndConditions</span></span>|<span data-ttu-id="50975-126">Colección [termsAndConditions](../resources/intune_companyterms_termsandconditions.md)</span><span class="sxs-lookup"><span data-stu-id="50975-126">[termsAndConditions](../resources/intune_companyterms_termsandconditions.md) collection</span></span>|<span data-ttu-id="50975-127">Los términos y condiciones asociados a la administración de dispositivos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="50975-127">The terms and conditions associated with device management of the company.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="50975-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="50975-128">JSON Representation</span></span>
<span data-ttu-id="50975-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="50975-129">Here is a JSON representation of the resource.</span></span>
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



