# <a name="onpremisesconditionalaccesssettings-resource-type"></a><span data-ttu-id="75c64-101">Tipo de recurso onPremisesConditionalAccessSettings</span><span class="sxs-lookup"><span data-stu-id="75c64-101">onPremisesConditionalAccessSettings resource type</span></span>

> <span data-ttu-id="75c64-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="75c64-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="75c64-103">Entidad singleton que representa la configuración de acceso condicional de Exchange local de un espacio empresarial.</span><span class="sxs-lookup"><span data-stu-id="75c64-103">Singleton entity which represents the Exchange OnPremises Conditional Access Settings for a tenant.</span></span>
## <a name="methods"></a><span data-ttu-id="75c64-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="75c64-104">Methods</span></span>
|<span data-ttu-id="75c64-105">Método</span><span class="sxs-lookup"><span data-stu-id="75c64-105">Method</span></span>|<span data-ttu-id="75c64-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75c64-106">Return Type</span></span>|<span data-ttu-id="75c64-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="75c64-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="75c64-108">Obtener onPremisesConditionalAccessSettings</span><span class="sxs-lookup"><span data-stu-id="75c64-108">Get onPremisesConditionalAccessSettings</span></span>](../api/intune_onboarding_onpremisesconditionalaccesssettings_get.md)|[<span data-ttu-id="75c64-109">onPremisesConditionalAccessSettings</span><span class="sxs-lookup"><span data-stu-id="75c64-109">onPremisesConditionalAccessSettings</span></span>](../resources/intune_onboarding_onpremisesconditionalaccesssettings.md)|<span data-ttu-id="75c64-110">Lea las propiedades y las relaciones del objeto [onPremisesConditionalAccessSettings](../resources/intune_onboarding_onpremisesconditionalaccesssettings.md).</span><span class="sxs-lookup"><span data-stu-id="75c64-110">Read properties and relationships of the [onPremisesConditionalAccessSettings](../resources/intune_onboarding_onpremisesconditionalaccesssettings.md) object.</span></span>|
|[<span data-ttu-id="75c64-111">Actualizar onPremisesConditionalAccessSettings</span><span class="sxs-lookup"><span data-stu-id="75c64-111">Update onPremisesConditionalAccessSettings</span></span>](../api/intune_onboarding_onpremisesconditionalaccesssettings_update.md)|[<span data-ttu-id="75c64-112">onPremisesConditionalAccessSettings</span><span class="sxs-lookup"><span data-stu-id="75c64-112">onPremisesConditionalAccessSettings</span></span>](../resources/intune_onboarding_onpremisesconditionalaccesssettings.md)|<span data-ttu-id="75c64-113">Actualice las propiedades de un objeto [onPremisesConditionalAccessSettings](../resources/intune_onboarding_onpremisesconditionalaccesssettings.md).</span><span class="sxs-lookup"><span data-stu-id="75c64-113">Update the properties of a [onPremisesConditionalAccessSettings](../resources/intune_onboarding_onpremisesconditionalaccesssettings.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="75c64-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="75c64-114">Properties</span></span>
|<span data-ttu-id="75c64-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="75c64-115">Property</span></span>|<span data-ttu-id="75c64-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="75c64-116">Type</span></span>|<span data-ttu-id="75c64-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="75c64-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="75c64-118">id</span><span class="sxs-lookup"><span data-stu-id="75c64-118">id</span></span>|<span data-ttu-id="75c64-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="75c64-119">String</span></span>|<span data-ttu-id="75c64-120">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="75c64-120">Not yet documented</span></span>|
|<span data-ttu-id="75c64-121">enabled</span><span class="sxs-lookup"><span data-stu-id="75c64-121">enabled</span></span>|<span data-ttu-id="75c64-122">Booleano</span><span class="sxs-lookup"><span data-stu-id="75c64-122">Boolean</span></span>|<span data-ttu-id="75c64-123">Indica si está habilitado el acceso condicional local para esta organización</span><span class="sxs-lookup"><span data-stu-id="75c64-123">Indicates if on premises conditional access is enabled for this organization</span></span>|
|<span data-ttu-id="75c64-124">includedGroups</span><span class="sxs-lookup"><span data-stu-id="75c64-124">includedGroups</span></span>|<span data-ttu-id="75c64-125">Colección Guid</span><span class="sxs-lookup"><span data-stu-id="75c64-125">Guid collection</span></span>|<span data-ttu-id="75c64-126">Grupos de usuarios a los que se dirigirá el acceso condicional local.</span><span class="sxs-lookup"><span data-stu-id="75c64-126">User groups that will be targeted by on premises conditional access.</span></span> <span data-ttu-id="75c64-127">Todos los usuarios de estos grupos deberán tener dispositivos móviles administrados y compatibles para tener acceso al correo.</span><span class="sxs-lookup"><span data-stu-id="75c64-127">All users in these groups will be required to have mobile device managed and compliant for mail access.</span></span>|
|<span data-ttu-id="75c64-128">excludedGroups</span><span class="sxs-lookup"><span data-stu-id="75c64-128">excludedGroups</span></span>|<span data-ttu-id="75c64-129">Colección Guid</span><span class="sxs-lookup"><span data-stu-id="75c64-129">Guid collection</span></span>|<span data-ttu-id="75c64-130">Grupos de usuarios que estarán exentos del acceso condicional local.</span><span class="sxs-lookup"><span data-stu-id="75c64-130">User groups that will be exempt by on premises conditional access.</span></span> <span data-ttu-id="75c64-131">Todos los usuarios de estos grupos estarán exentos de la directiva de acceso condicional.</span><span class="sxs-lookup"><span data-stu-id="75c64-131">All users in these groups will be exempt from the conditional access policy.</span></span>|
|<span data-ttu-id="75c64-132">overrideDefaultRule</span><span class="sxs-lookup"><span data-stu-id="75c64-132">overrideDefaultRule</span></span>|<span data-ttu-id="75c64-133">Booleano</span><span class="sxs-lookup"><span data-stu-id="75c64-133">Boolean</span></span>|<span data-ttu-id="75c64-134">Anular la regla de acceso predeterminada al permitir que un dispositivo garantice que se concede el acceso.</span><span class="sxs-lookup"><span data-stu-id="75c64-134">Override the default access rule when allowing a device to ensure access is granted.</span></span>|

## <a name="relationships"></a><span data-ttu-id="75c64-135">Relaciones</span><span class="sxs-lookup"><span data-stu-id="75c64-135">Relationships</span></span>
<span data-ttu-id="75c64-136">Ninguna</span><span class="sxs-lookup"><span data-stu-id="75c64-136">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="75c64-137">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="75c64-137">JSON Representation</span></span>
<span data-ttu-id="75c64-138">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="75c64-138">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.onPremisesConditionalAccessSettings"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.onPremisesConditionalAccessSettings",
  "id": "String (identifier)",
  "enabled": true,
  "includedGroups": [
    "Guid"
  ],
  "excludedGroups": [
    "Guid"
  ],
  "overrideDefaultRule": true
}
```








