# <a name="organization-resource-type"></a><span data-ttu-id="2384a-101">Tipo de recurso organization</span><span class="sxs-lookup"><span data-stu-id="2384a-101">organization resource type</span></span>

> <span data-ttu-id="2384a-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2384a-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2384a-103">El recurso organization representa una instancia de la configuración global y los recursos que funcionan y se aprovisionan en el nivel del espacio empresarial.</span><span class="sxs-lookup"><span data-stu-id="2384a-103">The organization resource represents an instance of global settings and resources which operate and are provisioned at the tenant-level.</span></span>
## <a name="methods"></a><span data-ttu-id="2384a-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="2384a-104">Methods</span></span>
|<span data-ttu-id="2384a-105">Método</span><span class="sxs-lookup"><span data-stu-id="2384a-105">Method</span></span>|<span data-ttu-id="2384a-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2384a-106">Return Type</span></span>|<span data-ttu-id="2384a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="2384a-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="2384a-108">Enumerar organizaciones</span><span class="sxs-lookup"><span data-stu-id="2384a-108">List organizations</span></span>](../api/intune_onboarding_organization_list.md)|<span data-ttu-id="2384a-109">Colección [organization](../resources/intune_onboarding_organization.md)</span><span class="sxs-lookup"><span data-stu-id="2384a-109">[organization](../resources/intune_onboarding_organization.md) collection</span></span>|<span data-ttu-id="2384a-110">Lea las propiedades y las relaciones de los objetos [organization](../resources/intune_onboarding_organization.md).</span><span class="sxs-lookup"><span data-stu-id="2384a-110">List properties and relationships of the [organization](../resources/intune_onboarding_organization.md) objects.</span></span>|
|[<span data-ttu-id="2384a-111">Obtener organización</span><span class="sxs-lookup"><span data-stu-id="2384a-111">Get organization</span></span>](../api/intune_onboarding_organization_get.md)|[<span data-ttu-id="2384a-112">organization</span><span class="sxs-lookup"><span data-stu-id="2384a-112">organization</span></span>](../resources/intune_onboarding_organization.md)|<span data-ttu-id="2384a-113">Lea las propiedades y las relaciones del objeto [organization](../resources/intune_onboarding_organization.md).</span><span class="sxs-lookup"><span data-stu-id="2384a-113">Read properties and relationships of organization object.</span></span>|
|[<span data-ttu-id="2384a-114">Actualizar organization</span><span class="sxs-lookup"><span data-stu-id="2384a-114">Update organization</span></span>](../api/intune_onboarding_organization_update.md)|[<span data-ttu-id="2384a-115">organization</span><span class="sxs-lookup"><span data-stu-id="2384a-115">organization</span></span>](../resources/intune_onboarding_organization.md)|<span data-ttu-id="2384a-116">Actualice las propiedades de un objeto [organization](../resources/intune_onboarding_organization.md).</span><span class="sxs-lookup"><span data-stu-id="2384a-116">Update the properties of a [calendar](../resources/intune_onboarding_organization.md) object.</span></span>|
|[<span data-ttu-id="2384a-117">Acción setMobileDeviceManagementAuthority</span><span class="sxs-lookup"><span data-stu-id="2384a-117">setMobileDeviceManagementAuthority action</span></span>](../api/intune_onboarding_organization_setmobiledevicemanagementauthority.md)|<span data-ttu-id="2384a-118">Int32</span><span class="sxs-lookup"><span data-stu-id="2384a-118">Int32</span></span>|<span data-ttu-id="2384a-119">Establecer la entidad de administración de dispositivos móviles</span><span class="sxs-lookup"><span data-stu-id="2384a-119">Set mobile device management authority</span></span>|

## <a name="properties"></a><span data-ttu-id="2384a-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2384a-120">Properties</span></span>
|<span data-ttu-id="2384a-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2384a-121">Property</span></span>|<span data-ttu-id="2384a-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="2384a-122">Type</span></span>|<span data-ttu-id="2384a-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="2384a-123">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2384a-124">id</span><span class="sxs-lookup"><span data-stu-id="2384a-124">id</span></span>|<span data-ttu-id="2384a-125">cadena</span><span class="sxs-lookup"><span data-stu-id="2384a-125">String</span></span>|<span data-ttu-id="2384a-126">El GUID para el objeto.</span><span class="sxs-lookup"><span data-stu-id="2384a-126">The resource GUID for the security object is not valid.</span></span>|
|<span data-ttu-id="2384a-127">mobileDeviceManagementAuthority</span><span class="sxs-lookup"><span data-stu-id="2384a-127">mobileDeviceManagementAuthority</span></span>|<span data-ttu-id="2384a-128">cadena</span><span class="sxs-lookup"><span data-stu-id="2384a-128">String</span></span>|<span data-ttu-id="2384a-129">Entidad de administración de dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="2384a-129">Mobile device management authority.</span></span> <span data-ttu-id="2384a-130">Los valores posibles son: `unknown`, `intune`, `sccm` y `office365`.</span><span class="sxs-lookup"><span data-stu-id="2384a-130">Possible values are: `unknown`, `intune`, `sccm`, `office365`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="2384a-131">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2384a-131">Relationships</span></span>
<span data-ttu-id="2384a-132">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2384a-132">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="2384a-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2384a-133">JSON Representation</span></span>
<span data-ttu-id="2384a-134">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2384a-134">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.organization"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.organization",
  "id": "String (identifier)",
  "mobileDeviceManagementAuthority": "String"
}
```



