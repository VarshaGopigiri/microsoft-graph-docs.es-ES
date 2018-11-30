---
title: Tipo de recurso onPremisesConditionalAccessSettings
description: Entidad singleton que representa la configuración de acceso condicional de Exchange local de un espacio empresarial.
ms.openlocfilehash: e67fe43be627d98bd59d760fe1a6d5faa3137acc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090712"
---
# <a name="onpremisesconditionalaccesssettings-resource-type"></a><span data-ttu-id="129ab-103">Tipo de recurso onPremisesConditionalAccessSettings</span><span class="sxs-lookup"><span data-stu-id="129ab-103">onPremisesConditionalAccessSettings resource type</span></span>

> <span data-ttu-id="129ab-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="129ab-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="129ab-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="129ab-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="129ab-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="129ab-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="129ab-107">Entidad singleton que representa la configuración de acceso condicional de Exchange local de un espacio empresarial.</span><span class="sxs-lookup"><span data-stu-id="129ab-107">Singleton entity which represents the Exchange OnPremises Conditional Access Settings for a tenant.</span></span>
## <a name="methods"></a><span data-ttu-id="129ab-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="129ab-108">Methods</span></span>
|<span data-ttu-id="129ab-109">Método</span><span class="sxs-lookup"><span data-stu-id="129ab-109">Method</span></span>|<span data-ttu-id="129ab-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="129ab-110">Return Type</span></span>|<span data-ttu-id="129ab-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="129ab-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="129ab-112">Obtener onPremisesConditionalAccessSettings</span><span class="sxs-lookup"><span data-stu-id="129ab-112">Get onPremisesConditionalAccessSettings</span></span>](../api/intune-onboarding-onpremisesconditionalaccesssettings-get.md)|[<span data-ttu-id="129ab-113">onPremisesConditionalAccessSettings</span><span class="sxs-lookup"><span data-stu-id="129ab-113">onPremisesConditionalAccessSettings</span></span>](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md)|<span data-ttu-id="129ab-114">Lea las propiedades y las relaciones del objeto [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md).</span><span class="sxs-lookup"><span data-stu-id="129ab-114">Read properties and relationships of the [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md) object.</span></span>|
|[<span data-ttu-id="129ab-115">Actualizar onPremisesConditionalAccessSettings</span><span class="sxs-lookup"><span data-stu-id="129ab-115">Update onPremisesConditionalAccessSettings</span></span>](../api/intune-onboarding-onpremisesconditionalaccesssettings-update.md)|[<span data-ttu-id="129ab-116">onPremisesConditionalAccessSettings</span><span class="sxs-lookup"><span data-stu-id="129ab-116">onPremisesConditionalAccessSettings</span></span>](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md)|<span data-ttu-id="129ab-117">Actualice las propiedades de un objeto [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md).</span><span class="sxs-lookup"><span data-stu-id="129ab-117">Update the properties of a [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="129ab-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="129ab-118">Properties</span></span>
|<span data-ttu-id="129ab-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="129ab-119">Property</span></span>|<span data-ttu-id="129ab-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="129ab-120">Type</span></span>|<span data-ttu-id="129ab-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="129ab-121">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="129ab-122">id</span><span class="sxs-lookup"><span data-stu-id="129ab-122">id</span></span>|<span data-ttu-id="129ab-123">String</span><span class="sxs-lookup"><span data-stu-id="129ab-123">String</span></span>|<span data-ttu-id="129ab-124">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="129ab-124">Not yet documented</span></span>|
|<span data-ttu-id="129ab-125">enabled</span><span class="sxs-lookup"><span data-stu-id="129ab-125">enabled</span></span>|<span data-ttu-id="129ab-126">Booleano</span><span class="sxs-lookup"><span data-stu-id="129ab-126">Boolean</span></span>|<span data-ttu-id="129ab-127">Indica si está habilitado el acceso condicional local para esta organización</span><span class="sxs-lookup"><span data-stu-id="129ab-127">Indicates if on premises conditional access is enabled for this organization</span></span>|
|<span data-ttu-id="129ab-128">includedGroups</span><span class="sxs-lookup"><span data-stu-id="129ab-128">includedGroups</span></span>|<span data-ttu-id="129ab-129">Colección Guid</span><span class="sxs-lookup"><span data-stu-id="129ab-129">Guid collection</span></span>|<span data-ttu-id="129ab-130">Grupos de usuarios a los que se dirigirá el acceso condicional local.</span><span class="sxs-lookup"><span data-stu-id="129ab-130">User groups that will be targeted by on premises conditional access.</span></span> <span data-ttu-id="129ab-131">Todos los usuarios de estos grupos deberán tener dispositivos móviles administrados y compatibles para tener acceso al correo.</span><span class="sxs-lookup"><span data-stu-id="129ab-131">All users in these groups will be required to have mobile device managed and compliant for mail access.</span></span>|
|<span data-ttu-id="129ab-132">excludedGroups</span><span class="sxs-lookup"><span data-stu-id="129ab-132">excludedGroups</span></span>|<span data-ttu-id="129ab-133">Colección Guid</span><span class="sxs-lookup"><span data-stu-id="129ab-133">Guid collection</span></span>|<span data-ttu-id="129ab-134">Grupos de usuarios que estarán exentos del acceso condicional local.</span><span class="sxs-lookup"><span data-stu-id="129ab-134">User groups that will be exempt by on premises conditional access.</span></span> <span data-ttu-id="129ab-135">Todos los usuarios de estos grupos estarán exentos de la directiva de acceso condicional.</span><span class="sxs-lookup"><span data-stu-id="129ab-135">All users in these groups will be exempt from the conditional access policy.</span></span>|
|<span data-ttu-id="129ab-136">overrideDefaultRule</span><span class="sxs-lookup"><span data-stu-id="129ab-136">overrideDefaultRule</span></span>|<span data-ttu-id="129ab-137">Booleano</span><span class="sxs-lookup"><span data-stu-id="129ab-137">Boolean</span></span>|<span data-ttu-id="129ab-138">Anular la regla de acceso predeterminada al permitir que un dispositivo garantice que se concede el acceso.</span><span class="sxs-lookup"><span data-stu-id="129ab-138">Override the default access rule when allowing a device to ensure access is granted.</span></span>|

## <a name="relationships"></a><span data-ttu-id="129ab-139">Relaciones</span><span class="sxs-lookup"><span data-stu-id="129ab-139">Relationships</span></span>
<span data-ttu-id="129ab-140">Ninguna</span><span class="sxs-lookup"><span data-stu-id="129ab-140">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="129ab-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="129ab-141">JSON Representation</span></span>
<span data-ttu-id="129ab-142">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="129ab-142">Here is a JSON representation of the resource.</span></span>
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




