# <a name="organization-resource-type"></a><span data-ttu-id="11db3-101">Tipo de recurso organization</span><span class="sxs-lookup"><span data-stu-id="11db3-101">organization resource type</span></span>

> <span data-ttu-id="11db3-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="11db3-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="11db3-103">El recurso organization representa una instancia de la configuración global y los recursos que funcionan y se aprovisionan en el nivel del espacio empresarial.</span><span class="sxs-lookup"><span data-stu-id="11db3-103">The organization resource represents an instance of global settings and resources which operate and are provisioned at the tenant-level.</span></span>
## <a name="methods"></a><span data-ttu-id="11db3-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="11db3-104">Methods</span></span>
|<span data-ttu-id="11db3-105">Método</span><span class="sxs-lookup"><span data-stu-id="11db3-105">Method</span></span>|<span data-ttu-id="11db3-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11db3-106">Return Type</span></span>|<span data-ttu-id="11db3-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="11db3-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="11db3-108">Enumerar organizaciones</span><span class="sxs-lookup"><span data-stu-id="11db3-108">List organizations</span></span>](../api/intune_onboarding_organization_list.md)|<span data-ttu-id="11db3-109">Colección [organization](../resources/intune_onboarding_organization.md)</span><span class="sxs-lookup"><span data-stu-id="11db3-109">[organization](../resources/intune_onboarding_organization.md) collection</span></span>|<span data-ttu-id="11db3-110">Lea las propiedades y las relaciones de los objetos [organization](../resources/intune_onboarding_organization.md).</span><span class="sxs-lookup"><span data-stu-id="11db3-110">List properties and relationships of the [organization](../resources/intune_onboarding_organization.md) objects.</span></span>|
|[<span data-ttu-id="11db3-111">Obtener organización</span><span class="sxs-lookup"><span data-stu-id="11db3-111">Get organization</span></span>](../api/intune_onboarding_organization_get.md)|[<span data-ttu-id="11db3-112">organización</span><span class="sxs-lookup"><span data-stu-id="11db3-112">organization</span></span>](../resources/intune_onboarding_organization.md)|<span data-ttu-id="11db3-113">Lea las propiedades y las relaciones del objeto [organization](../resources/intune_onboarding_organization.md).</span><span class="sxs-lookup"><span data-stu-id="11db3-113">Read properties and relationships of the [organization](../resources/intune_onboarding_organization.md) object.</span></span>|
|[<span data-ttu-id="11db3-114">Actualizar organization</span><span class="sxs-lookup"><span data-stu-id="11db3-114">Update organization</span></span>](../api/intune_onboarding_organization_update.md)|[<span data-ttu-id="11db3-115">organización</span><span class="sxs-lookup"><span data-stu-id="11db3-115">organization</span></span>](../resources/intune_onboarding_organization.md)|<span data-ttu-id="11db3-116">Actualice las propiedades de un objeto [organization](../resources/intune_onboarding_organization.md).</span><span class="sxs-lookup"><span data-stu-id="11db3-116">Update the properties of a [organization](../resources/intune_onboarding_organization.md) object.</span></span>|
|[<span data-ttu-id="11db3-117">Acción setMobileDeviceManagementAuthority</span><span class="sxs-lookup"><span data-stu-id="11db3-117">setMobileDeviceManagementAuthority action</span></span>](../api/intune_onboarding_organization_setmobiledevicemanagementauthority.md)|<span data-ttu-id="11db3-118">Int32</span><span class="sxs-lookup"><span data-stu-id="11db3-118">Int32</span></span>|<span data-ttu-id="11db3-119">Establecer la entidad de administración de dispositivos móviles</span><span class="sxs-lookup"><span data-stu-id="11db3-119">Set mobile device management authority</span></span>|

## <a name="properties"></a><span data-ttu-id="11db3-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="11db3-120">Properties</span></span>
|<span data-ttu-id="11db3-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="11db3-121">Property</span></span>|<span data-ttu-id="11db3-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="11db3-122">Type</span></span>|<span data-ttu-id="11db3-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="11db3-123">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="11db3-124">id</span><span class="sxs-lookup"><span data-stu-id="11db3-124">id</span></span>|<span data-ttu-id="11db3-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="11db3-125">String</span></span>|<span data-ttu-id="11db3-126">El GUID para el objeto.</span><span class="sxs-lookup"><span data-stu-id="11db3-126">The GUID for the object.</span></span>|
|<span data-ttu-id="11db3-127">mobileDeviceManagementAuthority</span><span class="sxs-lookup"><span data-stu-id="11db3-127">mobileDeviceManagementAuthority</span></span>|[<span data-ttu-id="11db3-128">mdmAuthority</span><span class="sxs-lookup"><span data-stu-id="11db3-128">mdmAuthority</span></span>](../resources/intune_onboarding_mdmauthority.md)|<span data-ttu-id="11db3-129">Entidad de administración de dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="11db3-129">Mobile device management authority.</span></span> <span data-ttu-id="11db3-130">Los valores posibles son: `unknown`, `intune`, `sccm` y `office365`.</span><span class="sxs-lookup"><span data-stu-id="11db3-130">The possible values are `unknown`, `intune`, `sccm`, `office365`, , , , , , , , or .</span></span>|

## <a name="relationships"></a><span data-ttu-id="11db3-131">Relaciones</span><span class="sxs-lookup"><span data-stu-id="11db3-131">Relationships</span></span>
<span data-ttu-id="11db3-132">Ninguna</span><span class="sxs-lookup"><span data-stu-id="11db3-132">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="11db3-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="11db3-133">JSON Representation</span></span>
<span data-ttu-id="11db3-134">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="11db3-134">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "openType": true,
  "keyProperty": "id",
  "baseType": "microsoft.graph.directoryObject",
  "@odata.type": "microsoft.graph.organization"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.organization",
  "id": "String (identifier)",
  "mobileDeviceManagementAuthority": "String"
}
```

<!-- {
  "type": "#page.annotation",
  "suppressions": [
    "Warning: Resource microsoft.graph.organization is defined in multiple files: /api-reference/v1.0/resources/intune_onboarding_organization.md, /api-reference/v1.0/resources/organization.md"
  ]
}-->
