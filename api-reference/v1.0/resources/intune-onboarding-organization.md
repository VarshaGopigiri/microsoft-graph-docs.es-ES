---
title: Tipo de recurso organization
description: El recurso organization representa una instancia de la configuración global y los recursos que funcionan y se aprovisionan en el nivel del espacio empresarial.
ms.openlocfilehash: ddc3b47777ea586a0f31c0d1d18aaa5727c828e5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030665"
---
# <a name="organization-resource-type"></a><span data-ttu-id="39cca-103">Tipo de recurso organization</span><span class="sxs-lookup"><span data-stu-id="39cca-103">organization resource type</span></span>

> <span data-ttu-id="39cca-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="39cca-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="39cca-105">El recurso organization representa una instancia de la configuración global y los recursos que funcionan y se aprovisionan en el nivel del espacio empresarial.</span><span class="sxs-lookup"><span data-stu-id="39cca-105">The organization resource represents an instance of global settings and resources which operate and are provisioned at the tenant-level.</span></span>
## <a name="methods"></a><span data-ttu-id="39cca-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="39cca-106">Methods</span></span>
|<span data-ttu-id="39cca-107">Método</span><span class="sxs-lookup"><span data-stu-id="39cca-107">Method</span></span>|<span data-ttu-id="39cca-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39cca-108">Return Type</span></span>|<span data-ttu-id="39cca-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="39cca-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="39cca-110">Enumerar organizaciones</span><span class="sxs-lookup"><span data-stu-id="39cca-110">List organizations</span></span>](../api/intune-onboarding-organization-list.md)|<span data-ttu-id="39cca-111">Colección [organization](../resources/intune-onboarding-organization.md)</span><span class="sxs-lookup"><span data-stu-id="39cca-111">[organization](../resources/intune-onboarding-organization.md) collection</span></span>|<span data-ttu-id="39cca-112">Lea las propiedades y las relaciones de los objetos [organization](../resources/intune-onboarding-organization.md).</span><span class="sxs-lookup"><span data-stu-id="39cca-112">List properties and relationships of the [organization](../resources/intune-onboarding-organization.md) objects.</span></span>|
|[<span data-ttu-id="39cca-113">Obtener organización</span><span class="sxs-lookup"><span data-stu-id="39cca-113">Get organization</span></span>](../api/intune-onboarding-organization-get.md)|[<span data-ttu-id="39cca-114">organization</span><span class="sxs-lookup"><span data-stu-id="39cca-114">organization</span></span>](../resources/intune-onboarding-organization.md)|<span data-ttu-id="39cca-115">Lea las propiedades y las relaciones del objeto [organization](../resources/intune-onboarding-organization.md).</span><span class="sxs-lookup"><span data-stu-id="39cca-115">Read properties and relationships of the [organization](../resources/intune-onboarding-organization.md) object.</span></span>|
|[<span data-ttu-id="39cca-116">Actualizar organization</span><span class="sxs-lookup"><span data-stu-id="39cca-116">Update organization</span></span>](../api/intune-onboarding-organization-update.md)|[<span data-ttu-id="39cca-117">organization</span><span class="sxs-lookup"><span data-stu-id="39cca-117">organization</span></span>](../resources/intune-onboarding-organization.md)|<span data-ttu-id="39cca-118">Actualice las propiedades de un objeto [organization](../resources/intune-onboarding-organization.md).</span><span class="sxs-lookup"><span data-stu-id="39cca-118">Update the properties of a [organization](../resources/intune-onboarding-organization.md) object.</span></span>|
|[<span data-ttu-id="39cca-119">Acción setMobileDeviceManagementAuthority</span><span class="sxs-lookup"><span data-stu-id="39cca-119">setMobileDeviceManagementAuthority action</span></span>](../api/intune-onboarding-organization-setmobiledevicemanagementauthority.md)|<span data-ttu-id="39cca-120">Int32</span><span class="sxs-lookup"><span data-stu-id="39cca-120">Int32</span></span>|<span data-ttu-id="39cca-121">Establecer la entidad de administración de dispositivos móviles</span><span class="sxs-lookup"><span data-stu-id="39cca-121">Set mobile device management authority</span></span>|

## <a name="properties"></a><span data-ttu-id="39cca-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="39cca-122">Properties</span></span>
|<span data-ttu-id="39cca-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="39cca-123">Property</span></span>|<span data-ttu-id="39cca-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="39cca-124">Type</span></span>|<span data-ttu-id="39cca-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="39cca-125">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="39cca-126">id</span><span class="sxs-lookup"><span data-stu-id="39cca-126">id</span></span>|<span data-ttu-id="39cca-127">String</span><span class="sxs-lookup"><span data-stu-id="39cca-127">String</span></span>|<span data-ttu-id="39cca-128">El GUID para el objeto.</span><span class="sxs-lookup"><span data-stu-id="39cca-128">The GUID for the object.</span></span>|
|<span data-ttu-id="39cca-129">mobileDeviceManagementAuthority</span><span class="sxs-lookup"><span data-stu-id="39cca-129">mobileDeviceManagementAuthority</span></span>|[<span data-ttu-id="39cca-130">mdmAuthority</span><span class="sxs-lookup"><span data-stu-id="39cca-130">mdmAuthority</span></span>](../resources/intune-onboarding-mdmauthority.md)|<span data-ttu-id="39cca-131">Entidad de administración de dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="39cca-131">Mobile device management authority.</span></span> <span data-ttu-id="39cca-132">Los valores posibles son: `unknown`, `intune`, `sccm` y `office365`.</span><span class="sxs-lookup"><span data-stu-id="39cca-132">Possible values are: `unknown`, `intune`, `sccm`, `office365`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="39cca-133">Relaciones</span><span class="sxs-lookup"><span data-stu-id="39cca-133">Relationships</span></span>
<span data-ttu-id="39cca-134">Ninguna</span><span class="sxs-lookup"><span data-stu-id="39cca-134">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="39cca-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="39cca-135">JSON Representation</span></span>
<span data-ttu-id="39cca-136">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="39cca-136">Here is a JSON representation of the resource.</span></span>
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


<!-- {
  "type": "#page.annotation",
  "suppressions": [

"Warning: Resource microsoft.graph.organization is defined in multiple files: /api-reference/v1.0/resources/intune_onboarding_organization.md, /api-reference/v1.0/resources/organization.md",

"Warning: Schema type organization has a different BaseType value microsoft.graph.directoryObject than the documentation .",

"Warning: Schema type organization has a different OpenType value False than the documentation True.",

"Warning: Resource organization has multiple declarations with mismatched OpenType declarations."

  ],

}
-->
