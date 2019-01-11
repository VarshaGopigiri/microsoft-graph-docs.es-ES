---
title: tipo de recurso officeConfiguration
description: Entidad singleton que actúa como un contenedor para todas las funcionalidades de administración de dispositivos.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 096a54db296181e58020bb9bc694056c0b9e949a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27817264"
---
# <a name="officeconfiguration-resource-type"></a><span data-ttu-id="72157-103">tipo de recurso officeConfiguration</span><span class="sxs-lookup"><span data-stu-id="72157-103">officeConfiguration resource type</span></span>

> <span data-ttu-id="72157-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="72157-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="72157-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="72157-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="72157-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="72157-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="72157-107">Entidad singleton que actúa como un contenedor para todas las funcionalidades de administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="72157-107">Singleton entity that acts as a container for all device management functionality.</span></span>
## <a name="methods"></a><span data-ttu-id="72157-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="72157-108">Methods</span></span>
|<span data-ttu-id="72157-109">Método</span><span class="sxs-lookup"><span data-stu-id="72157-109">Method</span></span>|<span data-ttu-id="72157-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="72157-110">Return Type</span></span>|<span data-ttu-id="72157-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="72157-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="72157-112">Obtener officeConfiguration</span><span class="sxs-lookup"><span data-stu-id="72157-112">Get officeConfiguration</span></span>|[<span data-ttu-id="72157-113">officeConfiguration</span><span class="sxs-lookup"><span data-stu-id="72157-113">officeConfiguration</span></span>](../resources/intune-cirrus-officeconfiguration.md)|<span data-ttu-id="72157-114">Leer las propiedades y las relaciones del objeto [officeConfiguration](../resources/intune-cirrus-officeconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="72157-114">Read properties and relationships of the [officeConfiguration](../resources/intune-cirrus-officeconfiguration.md) object.</span></span>|
|<span data-ttu-id="72157-115">Actualizar officeConfiguration</span><span class="sxs-lookup"><span data-stu-id="72157-115">Update officeConfiguration</span></span>|[<span data-ttu-id="72157-116">officeConfiguration</span><span class="sxs-lookup"><span data-stu-id="72157-116">officeConfiguration</span></span>](../resources/intune-cirrus-officeconfiguration.md)|<span data-ttu-id="72157-117">Actualizar las propiedades de un objeto [officeConfiguration](../resources/intune-cirrus-officeconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="72157-117">Update the properties of a [officeConfiguration](../resources/intune-cirrus-officeconfiguration.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="72157-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="72157-118">Properties</span></span>
|<span data-ttu-id="72157-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="72157-119">Property</span></span>|<span data-ttu-id="72157-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="72157-120">Type</span></span>|<span data-ttu-id="72157-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="72157-121">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="72157-122">id</span><span class="sxs-lookup"><span data-stu-id="72157-122">id</span></span>|<span data-ttu-id="72157-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="72157-123">String</span></span>|<span data-ttu-id="72157-124">Identificador de la configuración de office.</span><span class="sxs-lookup"><span data-stu-id="72157-124">Id of the office configuration.</span></span>|
|<span data-ttu-id="72157-125">tenantCheckinStatuses</span><span class="sxs-lookup"><span data-stu-id="72157-125">tenantCheckinStatuses</span></span>|<span data-ttu-id="72157-126">colección de [officeClientCheckinStatus](../resources/intune-cirrus-officeclientcheckinstatus.md)</span><span class="sxs-lookup"><span data-stu-id="72157-126">[officeClientCheckinStatus](../resources/intune-cirrus-officeclientcheckinstatus.md) collection</span></span>|<span data-ttu-id="72157-127">Lista de comprobación de estado del cliente de office.</span><span class="sxs-lookup"><span data-stu-id="72157-127">List of office Client check-in status.</span></span>|
|<span data-ttu-id="72157-128">tenantUserCheckinSummary</span><span class="sxs-lookup"><span data-stu-id="72157-128">tenantUserCheckinSummary</span></span>|[<span data-ttu-id="72157-129">officeUserCheckinSummary</span><span class="sxs-lookup"><span data-stu-id="72157-129">officeUserCheckinSummary</span></span>](../resources/intune-cirrus-officeusercheckinsummary.md)|<span data-ttu-id="72157-130">Entidad que describe el inquilino de verificación estatuas</span><span class="sxs-lookup"><span data-stu-id="72157-130">Entity that describes tenant check-in statues</span></span>|

## <a name="relationships"></a><span data-ttu-id="72157-131">Relaciones</span><span class="sxs-lookup"><span data-stu-id="72157-131">Relationships</span></span>
|<span data-ttu-id="72157-132">Relación</span><span class="sxs-lookup"><span data-stu-id="72157-132">Relationship</span></span>|<span data-ttu-id="72157-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="72157-133">Type</span></span>|<span data-ttu-id="72157-134">Description</span><span class="sxs-lookup"><span data-stu-id="72157-134">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="72157-135">clientConfigurations</span><span class="sxs-lookup"><span data-stu-id="72157-135">clientConfigurations</span></span>|<span data-ttu-id="72157-136">colección de [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="72157-136">[officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md) collection</span></span>|<span data-ttu-id="72157-137">Lista de configuración de cliente de office.</span><span class="sxs-lookup"><span data-stu-id="72157-137">List of office Client configuration.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="72157-138">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="72157-138">JSON Representation</span></span>
<span data-ttu-id="72157-139">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="72157-139">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.officeConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.officeConfiguration",
  "id": "String (identifier)",
  "tenantCheckinStatuses": [
    {
      "@odata.type": "microsoft.graph.officeClientCheckinStatus",
      "userPrincipalName": "String",
      "deviceName": "String",
      "devicePlatform": "String",
      "devicePlatformVersion": "String",
      "wasSuccessful": true,
      "userId": "String",
      "checkinDateTime": "String (timestamp)",
      "errorMessage": "String",
      "appliedPolicies": [
        "String"
      ]
    }
  ],
  "tenantUserCheckinSummary": {
    "@odata.type": "microsoft.graph.officeUserCheckinSummary",
    "succeededUserCount": 1024,
    "failedUserCount": 1024
  }
}
```



