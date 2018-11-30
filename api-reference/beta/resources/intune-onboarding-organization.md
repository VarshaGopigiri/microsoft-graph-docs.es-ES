---
title: Tipo de recurso organization
description: El recurso organization representa una instancia de la configuración global y los recursos que funcionan y se aprovisionan en el nivel del espacio empresarial.
ms.openlocfilehash: e7e49e5676e412ea0e174b2e158b98efea8e0c7c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086783"
---
# <a name="organization-resource-type"></a><span data-ttu-id="a78b5-103">Tipo de recurso organization</span><span class="sxs-lookup"><span data-stu-id="a78b5-103">organization resource type</span></span>

> <span data-ttu-id="a78b5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a78b5-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a78b5-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a78b5-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a78b5-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a78b5-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a78b5-107">El recurso organization representa una instancia de la configuración global y los recursos que funcionan y se aprovisionan en el nivel del espacio empresarial.</span><span class="sxs-lookup"><span data-stu-id="a78b5-107">The organization resource represents an instance of global settings and resources which operate and are provisioned at the tenant-level.</span></span>
## <a name="methods"></a><span data-ttu-id="a78b5-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="a78b5-108">Methods</span></span>
|<span data-ttu-id="a78b5-109">Método</span><span class="sxs-lookup"><span data-stu-id="a78b5-109">Method</span></span>|<span data-ttu-id="a78b5-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a78b5-110">Return Type</span></span>|<span data-ttu-id="a78b5-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a78b5-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="a78b5-112">Enumerar organizaciones</span><span class="sxs-lookup"><span data-stu-id="a78b5-112">List organizations</span></span>](../api/intune-onboarding-organization-list.md)|<span data-ttu-id="a78b5-113">Colección [organization](../resources/intune-onboarding-organization.md)</span><span class="sxs-lookup"><span data-stu-id="a78b5-113">[organization](../resources/intune-onboarding-organization.md) collection</span></span>|<span data-ttu-id="a78b5-114">Lea las propiedades y las relaciones de los objetos [organization](../resources/intune-onboarding-organization.md).</span><span class="sxs-lookup"><span data-stu-id="a78b5-114">List properties and relationships of the [organization](../resources/intune-onboarding-organization.md) objects.</span></span>|
|[<span data-ttu-id="a78b5-115">Obtener organización</span><span class="sxs-lookup"><span data-stu-id="a78b5-115">Get organization</span></span>](../api/intune-onboarding-organization-get.md)|[<span data-ttu-id="a78b5-116">organization</span><span class="sxs-lookup"><span data-stu-id="a78b5-116">organization</span></span>](../resources/intune-onboarding-organization.md)|<span data-ttu-id="a78b5-117">Lea las propiedades y las relaciones del objeto [organization](../resources/intune-onboarding-organization.md).</span><span class="sxs-lookup"><span data-stu-id="a78b5-117">Read properties and relationships of the [organization](../resources/intune-onboarding-organization.md) object.</span></span>|
|[<span data-ttu-id="a78b5-118">Actualizar organization</span><span class="sxs-lookup"><span data-stu-id="a78b5-118">Update organization</span></span>](../api/intune-onboarding-organization-update.md)|[<span data-ttu-id="a78b5-119">organization</span><span class="sxs-lookup"><span data-stu-id="a78b5-119">organization</span></span>](../resources/intune-onboarding-organization.md)|<span data-ttu-id="a78b5-120">Actualice las propiedades de un objeto [organization](../resources/intune-onboarding-organization.md).</span><span class="sxs-lookup"><span data-stu-id="a78b5-120">Update the properties of a [organization](../resources/intune-onboarding-organization.md) object.</span></span>|
|[<span data-ttu-id="a78b5-121">Acción setMobileDeviceManagementAuthority</span><span class="sxs-lookup"><span data-stu-id="a78b5-121">setMobileDeviceManagementAuthority action</span></span>](../api/intune-onboarding-organization-setmobiledevicemanagementauthority.md)|<span data-ttu-id="a78b5-122">Int32</span><span class="sxs-lookup"><span data-stu-id="a78b5-122">Int32</span></span>|<span data-ttu-id="a78b5-123">Establecer la entidad de administración de dispositivos móviles</span><span class="sxs-lookup"><span data-stu-id="a78b5-123">Set mobile device management authority</span></span>|

## <a name="properties"></a><span data-ttu-id="a78b5-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a78b5-124">Properties</span></span>
|<span data-ttu-id="a78b5-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a78b5-125">Property</span></span>|<span data-ttu-id="a78b5-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="a78b5-126">Type</span></span>|<span data-ttu-id="a78b5-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="a78b5-127">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a78b5-128">id</span><span class="sxs-lookup"><span data-stu-id="a78b5-128">id</span></span>|<span data-ttu-id="a78b5-129">String</span><span class="sxs-lookup"><span data-stu-id="a78b5-129">String</span></span>|<span data-ttu-id="a78b5-130">El GUID para el objeto.</span><span class="sxs-lookup"><span data-stu-id="a78b5-130">The GUID for the object.</span></span>|
|<span data-ttu-id="a78b5-131">mobileDeviceManagementAuthority</span><span class="sxs-lookup"><span data-stu-id="a78b5-131">mobileDeviceManagementAuthority</span></span>|[<span data-ttu-id="a78b5-132">mdmAuthority</span><span class="sxs-lookup"><span data-stu-id="a78b5-132">mdmAuthority</span></span>](../resources/intune-onboarding-mdmauthority.md)|<span data-ttu-id="a78b5-133">Entidad de administración de dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="a78b5-133">Mobile device management authority.</span></span> <span data-ttu-id="a78b5-134">Los valores posibles son: `unknown`, `intune`, `sccm` y `office365`.</span><span class="sxs-lookup"><span data-stu-id="a78b5-134">Possible values are: `unknown`, `intune`, `sccm`, `office365`.</span></span>|
|<span data-ttu-id="a78b5-135">certificateConnectorSetting</span><span class="sxs-lookup"><span data-stu-id="a78b5-135">certificateConnectorSetting</span></span>|[<span data-ttu-id="a78b5-136">certificateConnectorSetting</span><span class="sxs-lookup"><span data-stu-id="a78b5-136">certificateConnectorSetting</span></span>](../resources/intune-onboarding-certificateconnectorsetting.md)|<span data-ttu-id="a78b5-137">Configuración del conector del certificado.</span><span class="sxs-lookup"><span data-stu-id="a78b5-137">Certificate connector setting.</span></span>|

## <a name="relationships"></a><span data-ttu-id="a78b5-138">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a78b5-138">Relationships</span></span>
<span data-ttu-id="a78b5-139">Ninguna</span><span class="sxs-lookup"><span data-stu-id="a78b5-139">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="a78b5-140">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a78b5-140">JSON Representation</span></span>
<span data-ttu-id="a78b5-141">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a78b5-141">Here is a JSON representation of the resource.</span></span>
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
  "mobileDeviceManagementAuthority": "String",
  "certificateConnectorSetting": {
    "@odata.type": "microsoft.graph.certificateConnectorSetting",
    "status": 1024,
    "certExpiryTime": "String (timestamp)",
    "enrollmentError": "String",
    "lastConnectorConnectionTime": "String (timestamp)",
    "connectorVersion": "String",
    "lastUploadVersion": 1024
  }
}
```





