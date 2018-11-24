# <a name="onpremisesconditionalaccesssettings-resource-type"></a><span data-ttu-id="89b72-101">Tipo de recurso onPremisesConditionalAccessSettings</span><span class="sxs-lookup"><span data-stu-id="89b72-101">onPremisesConditionalAccessSettings resource type</span></span>

> <span data-ttu-id="89b72-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="89b72-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="89b72-103">Entidad singleton que representa la configuración de acceso condicional de Exchange local de un espacio empresarial.</span><span class="sxs-lookup"><span data-stu-id="89b72-103">Singleton entity which represents the Exchange OnPremises Conditional Access Settings for a tenant.</span></span>
## <a name="methods"></a><span data-ttu-id="89b72-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="89b72-104">Methods</span></span>
|<span data-ttu-id="89b72-105">Método</span><span class="sxs-lookup"><span data-stu-id="89b72-105">Method</span></span>|<span data-ttu-id="89b72-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89b72-106">Return Type</span></span>|<span data-ttu-id="89b72-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="89b72-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="89b72-108">Obtener onPremisesConditionalAccessSettings</span><span class="sxs-lookup"><span data-stu-id="89b72-108">Get onPremisesConditionalAccessSettings</span></span>](../api/intune_onboarding_onpremisesconditionalaccesssettings_get.md)|[<span data-ttu-id="89b72-109">onPremisesConditionalAccessSettings</span><span class="sxs-lookup"><span data-stu-id="89b72-109">onPremisesConditionalAccessSettings</span></span>](../resources/intune_onboarding_onpremisesconditionalaccesssettings.md)|<span data-ttu-id="89b72-110">Lea las propiedades y las relaciones del objeto [onPremisesConditionalAccessSettings](../resources/intune_onboarding_onpremisesconditionalaccesssettings.md).</span><span class="sxs-lookup"><span data-stu-id="89b72-110">Read properties and relationships of the [onPremisesConditionalAccessSettings](../resources/intune_onboarding_onpremisesconditionalaccesssettings.md) object.</span></span>|
|[<span data-ttu-id="89b72-111">Actualizar onPremisesConditionalAccessSettings</span><span class="sxs-lookup"><span data-stu-id="89b72-111">Update onPremisesConditionalAccessSettings</span></span>](../api/intune_onboarding_onpremisesconditionalaccesssettings_update.md)|[<span data-ttu-id="89b72-112">onPremisesConditionalAccessSettings</span><span class="sxs-lookup"><span data-stu-id="89b72-112">onPremisesConditionalAccessSettings</span></span>](../resources/intune_onboarding_onpremisesconditionalaccesssettings.md)|<span data-ttu-id="89b72-113">Actualice las propiedades de un objeto [onPremisesConditionalAccessSettings](../resources/intune_onboarding_onpremisesconditionalaccesssettings.md).</span><span class="sxs-lookup"><span data-stu-id="89b72-113">Update the properties of a [onPremisesConditionalAccessSettings](../resources/intune_onboarding_onpremisesconditionalaccesssettings.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="89b72-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="89b72-114">Properties</span></span>
|<span data-ttu-id="89b72-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="89b72-115">Property</span></span>|<span data-ttu-id="89b72-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="89b72-116">Type</span></span>|<span data-ttu-id="89b72-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="89b72-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="89b72-118">id</span><span class="sxs-lookup"><span data-stu-id="89b72-118">id</span></span>|<span data-ttu-id="89b72-119">cadena</span><span class="sxs-lookup"><span data-stu-id="89b72-119">String</span></span>|<span data-ttu-id="89b72-120">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="89b72-120">Not yet documented</span></span>|
|<span data-ttu-id="89b72-121">enabled</span><span class="sxs-lookup"><span data-stu-id="89b72-121">enabled</span></span>|<span data-ttu-id="89b72-122">Booleano</span><span class="sxs-lookup"><span data-stu-id="89b72-122">Boolean</span></span>|<span data-ttu-id="89b72-123">Indica si está habilitado el acceso condicional local para esta organización</span><span class="sxs-lookup"><span data-stu-id="89b72-123">Indicates if on premises conditional access is enabled for this organization</span></span>|
|<span data-ttu-id="89b72-124">includedGroups</span><span class="sxs-lookup"><span data-stu-id="89b72-124">includedGroups</span></span>|<span data-ttu-id="89b72-125">Colección Guid</span><span class="sxs-lookup"><span data-stu-id="89b72-125">Guid collection</span></span>|<span data-ttu-id="89b72-126">Grupos de usuarios a los que se dirigirá el acceso condicional local.</span><span class="sxs-lookup"><span data-stu-id="89b72-126">User groups that will be targeted by on premises conditional access.</span></span> <span data-ttu-id="89b72-127">Todos los usuarios de estos grupos deberán tener dispositivos móviles administrados y compatibles para tener acceso al correo.</span><span class="sxs-lookup"><span data-stu-id="89b72-127">All users in these groups will be required to have mobile device managed and compliant for mail access.</span></span>|
|<span data-ttu-id="89b72-128">excludedGroups</span><span class="sxs-lookup"><span data-stu-id="89b72-128">excludedGroups</span></span>|<span data-ttu-id="89b72-129">Colección Guid</span><span class="sxs-lookup"><span data-stu-id="89b72-129">Guid collection</span></span>|<span data-ttu-id="89b72-130">Grupos de usuarios que estarán exentos del acceso condicional local.</span><span class="sxs-lookup"><span data-stu-id="89b72-130">User groups that will be exempt by on premises conditional access.</span></span> <span data-ttu-id="89b72-131">Todos los usuarios de estos grupos estarán exentos de la directiva de acceso condicional.</span><span class="sxs-lookup"><span data-stu-id="89b72-131">All users in these groups will be exempt from the conditional access policy.</span></span>|
|<span data-ttu-id="89b72-132">overrideDefaultRule</span><span class="sxs-lookup"><span data-stu-id="89b72-132">overrideDefaultRule</span></span>|<span data-ttu-id="89b72-133">Booleano</span><span class="sxs-lookup"><span data-stu-id="89b72-133">Boolean</span></span>|<span data-ttu-id="89b72-134">Anular la regla de acceso predeterminada al permitir que un dispositivo garantice que se concede el acceso.</span><span class="sxs-lookup"><span data-stu-id="89b72-134">Override the default access rule when allowing a device to ensure access is granted.</span></span>|

## <a name="relationships"></a><span data-ttu-id="89b72-135">Relaciones</span><span class="sxs-lookup"><span data-stu-id="89b72-135">Relationships</span></span>
<span data-ttu-id="89b72-136">Ninguna</span><span class="sxs-lookup"><span data-stu-id="89b72-136">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="89b72-137">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="89b72-137">JSON Representation</span></span>
<span data-ttu-id="89b72-138">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="89b72-138">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.onPremisesConditionalAccessSettings"
}
-->
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



