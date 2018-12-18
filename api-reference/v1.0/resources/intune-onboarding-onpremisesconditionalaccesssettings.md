---
title: Tipo de recurso onPremisesConditionalAccessSettings
description: Entidad singleton que representa la configuración de acceso condicional de Exchange local de un espacio empresarial.
author: tfitzmac
ms.openlocfilehash: 534d76b00246763c6dec49149920a1f296148596
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27353931"
---
# <a name="onpremisesconditionalaccesssettings-resource-type"></a><span data-ttu-id="e3fc6-103">Tipo de recurso onPremisesConditionalAccessSettings</span><span class="sxs-lookup"><span data-stu-id="e3fc6-103">onPremisesConditionalAccessSettings resource type</span></span>

> <span data-ttu-id="e3fc6-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e3fc6-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e3fc6-105">Entidad singleton que representa la configuración de acceso condicional de Exchange local de un espacio empresarial.</span><span class="sxs-lookup"><span data-stu-id="e3fc6-105">Singleton entity which represents the Exchange OnPremises Conditional Access Settings for a tenant.</span></span>
## <a name="methods"></a><span data-ttu-id="e3fc6-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="e3fc6-106">Methods</span></span>
|<span data-ttu-id="e3fc6-107">Método</span><span class="sxs-lookup"><span data-stu-id="e3fc6-107">Method</span></span>|<span data-ttu-id="e3fc6-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3fc6-108">Return Type</span></span>|<span data-ttu-id="e3fc6-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3fc6-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="e3fc6-110">Obtener onPremisesConditionalAccessSettings</span><span class="sxs-lookup"><span data-stu-id="e3fc6-110">Get onPremisesConditionalAccessSettings</span></span>](../api/intune-onboarding-onpremisesconditionalaccesssettings-get.md)|[<span data-ttu-id="e3fc6-111">onPremisesConditionalAccessSettings</span><span class="sxs-lookup"><span data-stu-id="e3fc6-111">onPremisesConditionalAccessSettings</span></span>](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md)|<span data-ttu-id="e3fc6-112">Lea las propiedades y las relaciones del objeto [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md).</span><span class="sxs-lookup"><span data-stu-id="e3fc6-112">Read properties and relationships of the [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md) object.</span></span>|
|[<span data-ttu-id="e3fc6-113">Actualizar onPremisesConditionalAccessSettings</span><span class="sxs-lookup"><span data-stu-id="e3fc6-113">Update onPremisesConditionalAccessSettings</span></span>](../api/intune-onboarding-onpremisesconditionalaccesssettings-update.md)|[<span data-ttu-id="e3fc6-114">onPremisesConditionalAccessSettings</span><span class="sxs-lookup"><span data-stu-id="e3fc6-114">onPremisesConditionalAccessSettings</span></span>](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md)|<span data-ttu-id="e3fc6-115">Actualice las propiedades de un objeto [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md).</span><span class="sxs-lookup"><span data-stu-id="e3fc6-115">Update the properties of a [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="e3fc6-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e3fc6-116">Properties</span></span>
|<span data-ttu-id="e3fc6-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e3fc6-117">Property</span></span>|<span data-ttu-id="e3fc6-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3fc6-118">Type</span></span>|<span data-ttu-id="e3fc6-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3fc6-119">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e3fc6-120">id</span><span class="sxs-lookup"><span data-stu-id="e3fc6-120">id</span></span>|<span data-ttu-id="e3fc6-121">String</span><span class="sxs-lookup"><span data-stu-id="e3fc6-121">String</span></span>|<span data-ttu-id="e3fc6-122">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="e3fc6-122">Not yet documented</span></span>|
|<span data-ttu-id="e3fc6-123">enabled</span><span class="sxs-lookup"><span data-stu-id="e3fc6-123">enabled</span></span>|<span data-ttu-id="e3fc6-124">Booleano</span><span class="sxs-lookup"><span data-stu-id="e3fc6-124">Boolean</span></span>|<span data-ttu-id="e3fc6-125">Indica si está habilitado el acceso condicional local para esta organización</span><span class="sxs-lookup"><span data-stu-id="e3fc6-125">Indicates if on premises conditional access is enabled for this organization</span></span>|
|<span data-ttu-id="e3fc6-126">includedGroups</span><span class="sxs-lookup"><span data-stu-id="e3fc6-126">includedGroups</span></span>|<span data-ttu-id="e3fc6-127">Colección Guid</span><span class="sxs-lookup"><span data-stu-id="e3fc6-127">Guid collection</span></span>|<span data-ttu-id="e3fc6-128">Grupos de usuarios a los que se dirigirá el acceso condicional local.</span><span class="sxs-lookup"><span data-stu-id="e3fc6-128">User groups that will be targeted by on premises conditional access.</span></span> <span data-ttu-id="e3fc6-129">Todos los usuarios de estos grupos deberán tener dispositivos móviles administrados y compatibles para tener acceso al correo.</span><span class="sxs-lookup"><span data-stu-id="e3fc6-129">All users in these groups will be required to have mobile device managed and compliant for mail access.</span></span>|
|<span data-ttu-id="e3fc6-130">excludedGroups</span><span class="sxs-lookup"><span data-stu-id="e3fc6-130">excludedGroups</span></span>|<span data-ttu-id="e3fc6-131">Colección Guid</span><span class="sxs-lookup"><span data-stu-id="e3fc6-131">Guid collection</span></span>|<span data-ttu-id="e3fc6-132">Grupos de usuarios que estarán exentos del acceso condicional local.</span><span class="sxs-lookup"><span data-stu-id="e3fc6-132">User groups that will be exempt by on premises conditional access.</span></span> <span data-ttu-id="e3fc6-133">Todos los usuarios de estos grupos estarán exentos de la directiva de acceso condicional.</span><span class="sxs-lookup"><span data-stu-id="e3fc6-133">All users in these groups will be exempt from the conditional access policy.</span></span>|
|<span data-ttu-id="e3fc6-134">overrideDefaultRule</span><span class="sxs-lookup"><span data-stu-id="e3fc6-134">overrideDefaultRule</span></span>|<span data-ttu-id="e3fc6-135">Booleano</span><span class="sxs-lookup"><span data-stu-id="e3fc6-135">Boolean</span></span>|<span data-ttu-id="e3fc6-136">Anular la regla de acceso predeterminada al permitir que un dispositivo garantice que se concede el acceso.</span><span class="sxs-lookup"><span data-stu-id="e3fc6-136">Override the default access rule when allowing a device to ensure access is granted.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e3fc6-137">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e3fc6-137">Relationships</span></span>
<span data-ttu-id="e3fc6-138">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e3fc6-138">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="e3fc6-139">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e3fc6-139">JSON Representation</span></span>
<span data-ttu-id="e3fc6-140">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e3fc6-140">Here is a JSON representation of the resource.</span></span>
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



