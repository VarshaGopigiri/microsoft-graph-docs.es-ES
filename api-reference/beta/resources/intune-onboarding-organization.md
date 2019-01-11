---
title: Tipo de recurso organization
description: El recurso organization representa una instancia de la configuración global y los recursos que funcionan y se aprovisionan en el nivel del espacio empresarial.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 7c6f99c378bc7fd53f473419a5ca4f4350f7c57b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27812050"
---
# <a name="organization-resource-type"></a><span data-ttu-id="1e3ba-103">Tipo de recurso organization</span><span class="sxs-lookup"><span data-stu-id="1e3ba-103">organization resource type</span></span>

> <span data-ttu-id="1e3ba-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1e3ba-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1e3ba-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1e3ba-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1e3ba-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1e3ba-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1e3ba-107">El recurso organization representa una instancia de la configuración global y los recursos que funcionan y se aprovisionan en el nivel del espacio empresarial.</span><span class="sxs-lookup"><span data-stu-id="1e3ba-107">The organization resource represents an instance of global settings and resources which operate and are provisioned at the tenant-level.</span></span>
## <a name="methods"></a><span data-ttu-id="1e3ba-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="1e3ba-108">Methods</span></span>
|<span data-ttu-id="1e3ba-109">Método</span><span class="sxs-lookup"><span data-stu-id="1e3ba-109">Method</span></span>|<span data-ttu-id="1e3ba-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e3ba-110">Return Type</span></span>|<span data-ttu-id="1e3ba-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e3ba-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="1e3ba-112">Enumerar organizaciones</span><span class="sxs-lookup"><span data-stu-id="1e3ba-112">List organizations</span></span>](../api/intune-onboarding-organization-list.md)|<span data-ttu-id="1e3ba-113">Colección [organization](../resources/intune-onboarding-organization.md)</span><span class="sxs-lookup"><span data-stu-id="1e3ba-113">[organization](../resources/intune-onboarding-organization.md) collection</span></span>|<span data-ttu-id="1e3ba-114">Lea las propiedades y las relaciones de los objetos [organization](../resources/intune-onboarding-organization.md).</span><span class="sxs-lookup"><span data-stu-id="1e3ba-114">List properties and relationships of the [organization](../resources/intune-onboarding-organization.md) objects.</span></span>|
|[<span data-ttu-id="1e3ba-115">Obtener organización</span><span class="sxs-lookup"><span data-stu-id="1e3ba-115">Get organization</span></span>](../api/intune-onboarding-organization-get.md)|[<span data-ttu-id="1e3ba-116">organization</span><span class="sxs-lookup"><span data-stu-id="1e3ba-116">organization</span></span>](../resources/intune-onboarding-organization.md)|<span data-ttu-id="1e3ba-117">Lea las propiedades y las relaciones del objeto [organization](../resources/intune-onboarding-organization.md).</span><span class="sxs-lookup"><span data-stu-id="1e3ba-117">Read properties and relationships of the [organization](../resources/intune-onboarding-organization.md) object.</span></span>|
|[<span data-ttu-id="1e3ba-118">Actualizar organization</span><span class="sxs-lookup"><span data-stu-id="1e3ba-118">Update organization</span></span>](../api/intune-onboarding-organization-update.md)|[<span data-ttu-id="1e3ba-119">organization</span><span class="sxs-lookup"><span data-stu-id="1e3ba-119">organization</span></span>](../resources/intune-onboarding-organization.md)|<span data-ttu-id="1e3ba-120">Actualice las propiedades de un objeto [organization](../resources/intune-onboarding-organization.md).</span><span class="sxs-lookup"><span data-stu-id="1e3ba-120">Update the properties of a [organization](../resources/intune-onboarding-organization.md) object.</span></span>|
|[<span data-ttu-id="1e3ba-121">Acción setMobileDeviceManagementAuthority</span><span class="sxs-lookup"><span data-stu-id="1e3ba-121">setMobileDeviceManagementAuthority action</span></span>](../api/intune-onboarding-organization-setmobiledevicemanagementauthority.md)|<span data-ttu-id="1e3ba-122">Int32</span><span class="sxs-lookup"><span data-stu-id="1e3ba-122">Int32</span></span>|<span data-ttu-id="1e3ba-123">Establecer la entidad de administración de dispositivos móviles</span><span class="sxs-lookup"><span data-stu-id="1e3ba-123">Set mobile device management authority</span></span>|

## <a name="properties"></a><span data-ttu-id="1e3ba-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1e3ba-124">Properties</span></span>
|<span data-ttu-id="1e3ba-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1e3ba-125">Property</span></span>|<span data-ttu-id="1e3ba-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="1e3ba-126">Type</span></span>|<span data-ttu-id="1e3ba-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e3ba-127">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1e3ba-128">id</span><span class="sxs-lookup"><span data-stu-id="1e3ba-128">id</span></span>|<span data-ttu-id="1e3ba-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="1e3ba-129">String</span></span>|<span data-ttu-id="1e3ba-130">El GUID para el objeto.</span><span class="sxs-lookup"><span data-stu-id="1e3ba-130">The GUID for the object.</span></span>|
|<span data-ttu-id="1e3ba-131">mobileDeviceManagementAuthority</span><span class="sxs-lookup"><span data-stu-id="1e3ba-131">mobileDeviceManagementAuthority</span></span>|[<span data-ttu-id="1e3ba-132">mdmAuthority</span><span class="sxs-lookup"><span data-stu-id="1e3ba-132">mdmAuthority</span></span>](../resources/intune-onboarding-mdmauthority.md)|<span data-ttu-id="1e3ba-133">Entidad de administración de dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="1e3ba-133">Mobile device management authority.</span></span> <span data-ttu-id="1e3ba-134">Los valores posibles son: `unknown`, `intune`, `sccm` y `office365`.</span><span class="sxs-lookup"><span data-stu-id="1e3ba-134">Possible values are: `unknown`, `intune`, `sccm`, `office365`.</span></span>|
|<span data-ttu-id="1e3ba-135">certificateConnectorSetting</span><span class="sxs-lookup"><span data-stu-id="1e3ba-135">certificateConnectorSetting</span></span>|[<span data-ttu-id="1e3ba-136">certificateConnectorSetting</span><span class="sxs-lookup"><span data-stu-id="1e3ba-136">certificateConnectorSetting</span></span>](../resources/intune-onboarding-certificateconnectorsetting.md)|<span data-ttu-id="1e3ba-137">Configuración del conector del certificado.</span><span class="sxs-lookup"><span data-stu-id="1e3ba-137">Certificate connector setting.</span></span>|

## <a name="relationships"></a><span data-ttu-id="1e3ba-138">Relaciones</span><span class="sxs-lookup"><span data-stu-id="1e3ba-138">Relationships</span></span>
<span data-ttu-id="1e3ba-139">Ninguna</span><span class="sxs-lookup"><span data-stu-id="1e3ba-139">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="1e3ba-140">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1e3ba-140">JSON Representation</span></span>
<span data-ttu-id="1e3ba-141">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1e3ba-141">Here is a JSON representation of the resource.</span></span>
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





