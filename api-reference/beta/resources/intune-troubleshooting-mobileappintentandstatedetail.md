---
title: tipo de recurso mobileAppIntentAndStateDetail
description: La intención de aplicación móvil y el estado de instalación para un dispositivo dado.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 169988d8a3a114bbae7a06583565c9abd3414b4f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27946689"
---
# <a name="mobileappintentandstatedetail-resource-type"></a><span data-ttu-id="d326b-103">tipo de recurso mobileAppIntentAndStateDetail</span><span class="sxs-lookup"><span data-stu-id="d326b-103">mobileAppIntentAndStateDetail resource type</span></span>

> <span data-ttu-id="d326b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d326b-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d326b-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d326b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d326b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d326b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d326b-107">La intención de aplicación móvil y el estado de instalación para un dispositivo dado.</span><span class="sxs-lookup"><span data-stu-id="d326b-107">Mobile App Intent and Install State for a given device.</span></span>
## <a name="properties"></a><span data-ttu-id="d326b-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d326b-108">Properties</span></span>
|<span data-ttu-id="d326b-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d326b-109">Property</span></span>|<span data-ttu-id="d326b-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="d326b-110">Type</span></span>|<span data-ttu-id="d326b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d326b-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d326b-112">applicationId</span><span class="sxs-lookup"><span data-stu-id="d326b-112">applicationId</span></span>|<span data-ttu-id="d326b-113">cadena</span><span class="sxs-lookup"><span data-stu-id="d326b-113">String</span></span>|<span data-ttu-id="d326b-114">Identificador de MobieApp.</span><span class="sxs-lookup"><span data-stu-id="d326b-114">MobieApp identifier.</span></span>|
|<span data-ttu-id="d326b-115">displayName</span><span class="sxs-lookup"><span data-stu-id="d326b-115">displayName</span></span>|<span data-ttu-id="d326b-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="d326b-116">String</span></span>|<span data-ttu-id="d326b-117">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="d326b-117">The admin provided or imported title of the app.</span></span>|
|<span data-ttu-id="d326b-118">mobileAppIntent</span><span class="sxs-lookup"><span data-stu-id="d326b-118">mobileAppIntent</span></span>|[<span data-ttu-id="d326b-119">mobileAppIntent</span><span class="sxs-lookup"><span data-stu-id="d326b-119">mobileAppIntent</span></span>](../resources/intune-troubleshooting-mobileappintent.md)|<span data-ttu-id="d326b-120">Intención de aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="d326b-120">Mobile App Intent.</span></span> <span data-ttu-id="d326b-121">Los valores posibles son: `available`, `notAvailable`, `requiredInstall`, `requiredUninstall`, `requiredAndAvailableInstall`, `availableInstallWithoutEnrollment` y `exclude`.</span><span class="sxs-lookup"><span data-stu-id="d326b-121">Possible values are: `available`, `notAvailable`, `requiredInstall`, `requiredUninstall`, `requiredAndAvailableInstall`, `availableInstallWithoutEnrollment`, `exclude`.</span></span>|
|<span data-ttu-id="d326b-122">displayVersion</span><span class="sxs-lookup"><span data-stu-id="d326b-122">displayVersion</span></span>|<span data-ttu-id="d326b-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="d326b-123">String</span></span>|<span data-ttu-id="d326b-124">Versión legible humano de la aplicación</span><span class="sxs-lookup"><span data-stu-id="d326b-124">Human readable version of the application</span></span>|
|<span data-ttu-id="d326b-125">installState</span><span class="sxs-lookup"><span data-stu-id="d326b-125">installState</span></span>|[<span data-ttu-id="d326b-126">resultantAppState</span><span class="sxs-lookup"><span data-stu-id="d326b-126">resultantAppState</span></span>](../resources/intune-shared-resultantappstate.md)|<span data-ttu-id="d326b-127">El estado de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d326b-127">The install state of the app.</span></span> <span data-ttu-id="d326b-128">Los valores posibles son: `installed`, `failed`, `notInstalled`, `uninstallFailed`, `pendingInstall`, `unknown` y `notApplicable`.</span><span class="sxs-lookup"><span data-stu-id="d326b-128">Possible values are: `installed`, `failed`, `notInstalled`, `uninstallFailed`, `pendingInstall`, `unknown`, `notApplicable`.</span></span>|
|<span data-ttu-id="d326b-129">supportedDeviceTypes</span><span class="sxs-lookup"><span data-stu-id="d326b-129">supportedDeviceTypes</span></span>|<span data-ttu-id="d326b-130">colección de [mobileAppSupportedDeviceType](../resources/intune-troubleshooting-mobileappsupporteddevicetype.md)</span><span class="sxs-lookup"><span data-stu-id="d326b-130">[mobileAppSupportedDeviceType](../resources/intune-troubleshooting-mobileappsupporteddevicetype.md) collection</span></span>|<span data-ttu-id="d326b-131">Las plataformas compatibles para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d326b-131">The supported platforms for the app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="d326b-132">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d326b-132">Relationships</span></span>
<span data-ttu-id="d326b-133">Ninguna</span><span class="sxs-lookup"><span data-stu-id="d326b-133">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="d326b-134">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d326b-134">JSON Representation</span></span>
<span data-ttu-id="d326b-135">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d326b-135">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mobileAppIntentAndStateDetail"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppIntentAndStateDetail",
  "applicationId": "String",
  "displayName": "String",
  "mobileAppIntent": "String",
  "displayVersion": "String",
  "installState": "String",
  "supportedDeviceTypes": [
    {
      "@odata.type": "microsoft.graph.mobileAppSupportedDeviceType",
      "type": "String",
      "minimumOperatingSystemVersion": "String",
      "maximumOperatingSystemVersion": "String"
    }
  ]
}
```





