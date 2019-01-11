---
title: Tipo de recurso onPremisesConditionalAccessSettings
description: Entidad singleton que representa la configuración de acceso condicional de Exchange local de un espacio empresarial.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 88d513cc59b9570b355e67fa417a9856519cf551
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27875995"
---
# <a name="onpremisesconditionalaccesssettings-resource-type"></a><span data-ttu-id="2af8d-103">Tipo de recurso onPremisesConditionalAccessSettings</span><span class="sxs-lookup"><span data-stu-id="2af8d-103">onPremisesConditionalAccessSettings resource type</span></span>

> <span data-ttu-id="2af8d-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2af8d-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2af8d-105">Entidad singleton que representa la configuración de acceso condicional de Exchange local de un espacio empresarial.</span><span class="sxs-lookup"><span data-stu-id="2af8d-105">Singleton entity which represents the Exchange OnPremises Conditional Access Settings for a tenant.</span></span>
## <a name="methods"></a><span data-ttu-id="2af8d-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="2af8d-106">Methods</span></span>
|<span data-ttu-id="2af8d-107">Método</span><span class="sxs-lookup"><span data-stu-id="2af8d-107">Method</span></span>|<span data-ttu-id="2af8d-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2af8d-108">Return Type</span></span>|<span data-ttu-id="2af8d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="2af8d-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="2af8d-110">Obtener onPremisesConditionalAccessSettings</span><span class="sxs-lookup"><span data-stu-id="2af8d-110">Get onPremisesConditionalAccessSettings</span></span>](../api/intune-onboarding-onpremisesconditionalaccesssettings-get.md)|[<span data-ttu-id="2af8d-111">onPremisesConditionalAccessSettings</span><span class="sxs-lookup"><span data-stu-id="2af8d-111">onPremisesConditionalAccessSettings</span></span>](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md)|<span data-ttu-id="2af8d-112">Lea las propiedades y las relaciones del objeto [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md).</span><span class="sxs-lookup"><span data-stu-id="2af8d-112">Read properties and relationships of the [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md) object.</span></span>|
|[<span data-ttu-id="2af8d-113">Actualizar onPremisesConditionalAccessSettings</span><span class="sxs-lookup"><span data-stu-id="2af8d-113">Update onPremisesConditionalAccessSettings</span></span>](../api/intune-onboarding-onpremisesconditionalaccesssettings-update.md)|[<span data-ttu-id="2af8d-114">onPremisesConditionalAccessSettings</span><span class="sxs-lookup"><span data-stu-id="2af8d-114">onPremisesConditionalAccessSettings</span></span>](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md)|<span data-ttu-id="2af8d-115">Actualice las propiedades de un objeto [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md).</span><span class="sxs-lookup"><span data-stu-id="2af8d-115">Update the properties of a [onPremisesConditionalAccessSettings](../resources/intune-onboarding-onpremisesconditionalaccesssettings.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="2af8d-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2af8d-116">Properties</span></span>
|<span data-ttu-id="2af8d-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2af8d-117">Property</span></span>|<span data-ttu-id="2af8d-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="2af8d-118">Type</span></span>|<span data-ttu-id="2af8d-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="2af8d-119">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2af8d-120">id</span><span class="sxs-lookup"><span data-stu-id="2af8d-120">id</span></span>|<span data-ttu-id="2af8d-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="2af8d-121">String</span></span>|<span data-ttu-id="2af8d-122">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="2af8d-122">Not yet documented</span></span>|
|<span data-ttu-id="2af8d-123">enabled</span><span class="sxs-lookup"><span data-stu-id="2af8d-123">enabled</span></span>|<span data-ttu-id="2af8d-124">Booleano</span><span class="sxs-lookup"><span data-stu-id="2af8d-124">Boolean</span></span>|<span data-ttu-id="2af8d-125">Indica si está habilitado el acceso condicional local para esta organización</span><span class="sxs-lookup"><span data-stu-id="2af8d-125">Indicates if on premises conditional access is enabled for this organization</span></span>|
|<span data-ttu-id="2af8d-126">includedGroups</span><span class="sxs-lookup"><span data-stu-id="2af8d-126">includedGroups</span></span>|<span data-ttu-id="2af8d-127">Colección Guid</span><span class="sxs-lookup"><span data-stu-id="2af8d-127">Guid collection</span></span>|<span data-ttu-id="2af8d-128">Grupos de usuarios a los que se dirigirá el acceso condicional local.</span><span class="sxs-lookup"><span data-stu-id="2af8d-128">User groups that will be targeted by on premises conditional access.</span></span> <span data-ttu-id="2af8d-129">Todos los usuarios de estos grupos deberán tener dispositivos móviles administrados y compatibles para tener acceso al correo.</span><span class="sxs-lookup"><span data-stu-id="2af8d-129">All users in these groups will be required to have mobile device managed and compliant for mail access.</span></span>|
|<span data-ttu-id="2af8d-130">excludedGroups</span><span class="sxs-lookup"><span data-stu-id="2af8d-130">excludedGroups</span></span>|<span data-ttu-id="2af8d-131">Colección Guid</span><span class="sxs-lookup"><span data-stu-id="2af8d-131">Guid collection</span></span>|<span data-ttu-id="2af8d-132">Grupos de usuarios que estarán exentos del acceso condicional local.</span><span class="sxs-lookup"><span data-stu-id="2af8d-132">User groups that will be exempt by on premises conditional access.</span></span> <span data-ttu-id="2af8d-133">Todos los usuarios de estos grupos estarán exentos de la directiva de acceso condicional.</span><span class="sxs-lookup"><span data-stu-id="2af8d-133">All users in these groups will be exempt from the conditional access policy.</span></span>|
|<span data-ttu-id="2af8d-134">overrideDefaultRule</span><span class="sxs-lookup"><span data-stu-id="2af8d-134">overrideDefaultRule</span></span>|<span data-ttu-id="2af8d-135">Booleano</span><span class="sxs-lookup"><span data-stu-id="2af8d-135">Boolean</span></span>|<span data-ttu-id="2af8d-136">Anular la regla de acceso predeterminada al permitir que un dispositivo garantice que se concede el acceso.</span><span class="sxs-lookup"><span data-stu-id="2af8d-136">Override the default access rule when allowing a device to ensure access is granted.</span></span>|

## <a name="relationships"></a><span data-ttu-id="2af8d-137">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2af8d-137">Relationships</span></span>
<span data-ttu-id="2af8d-138">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2af8d-138">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="2af8d-139">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2af8d-139">JSON Representation</span></span>
<span data-ttu-id="2af8d-140">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2af8d-140">Here is a JSON representation of the resource.</span></span>
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



