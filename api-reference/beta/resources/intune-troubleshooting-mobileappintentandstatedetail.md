---
title: tipo de recurso mobileAppIntentAndStateDetail
description: La intención de aplicación móvil y el estado de instalación para un dispositivo dado.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: ad20ef00cbc8e5295a96107fbce2f5e7f1cb978a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805813"
---
# <a name="mobileappintentandstatedetail-resource-type"></a><span data-ttu-id="315a0-103">tipo de recurso mobileAppIntentAndStateDetail</span><span class="sxs-lookup"><span data-stu-id="315a0-103">mobileAppIntentAndStateDetail resource type</span></span>

> <span data-ttu-id="315a0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="315a0-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="315a0-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="315a0-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="315a0-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="315a0-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="315a0-107">La intención de aplicación móvil y el estado de instalación para un dispositivo dado.</span><span class="sxs-lookup"><span data-stu-id="315a0-107">Mobile App Intent and Install State for a given device.</span></span>
## <a name="properties"></a><span data-ttu-id="315a0-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="315a0-108">Properties</span></span>
|<span data-ttu-id="315a0-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="315a0-109">Property</span></span>|<span data-ttu-id="315a0-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="315a0-110">Type</span></span>|<span data-ttu-id="315a0-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="315a0-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="315a0-112">applicationId</span><span class="sxs-lookup"><span data-stu-id="315a0-112">applicationId</span></span>|<span data-ttu-id="315a0-113">cadena</span><span class="sxs-lookup"><span data-stu-id="315a0-113">String</span></span>|<span data-ttu-id="315a0-114">Identificador de MobieApp.</span><span class="sxs-lookup"><span data-stu-id="315a0-114">MobieApp identifier.</span></span>|
|<span data-ttu-id="315a0-115">displayName</span><span class="sxs-lookup"><span data-stu-id="315a0-115">displayName</span></span>|<span data-ttu-id="315a0-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="315a0-116">String</span></span>|<span data-ttu-id="315a0-117">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="315a0-117">The admin provided or imported title of the app.</span></span>|
|<span data-ttu-id="315a0-118">mobileAppIntent</span><span class="sxs-lookup"><span data-stu-id="315a0-118">mobileAppIntent</span></span>|[<span data-ttu-id="315a0-119">mobileAppIntent</span><span class="sxs-lookup"><span data-stu-id="315a0-119">mobileAppIntent</span></span>](../resources/intune-troubleshooting-mobileappintent.md)|<span data-ttu-id="315a0-120">Intención de aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="315a0-120">Mobile App Intent.</span></span> <span data-ttu-id="315a0-121">Los valores posibles son: `available`, `notAvailable`, `requiredInstall`, `requiredUninstall`, `requiredAndAvailableInstall`, `availableInstallWithoutEnrollment` y `exclude`.</span><span class="sxs-lookup"><span data-stu-id="315a0-121">Possible values are: `available`, `notAvailable`, `requiredInstall`, `requiredUninstall`, `requiredAndAvailableInstall`, `availableInstallWithoutEnrollment`, `exclude`.</span></span>|
|<span data-ttu-id="315a0-122">displayVersion</span><span class="sxs-lookup"><span data-stu-id="315a0-122">displayVersion</span></span>|<span data-ttu-id="315a0-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="315a0-123">String</span></span>|<span data-ttu-id="315a0-124">Versión legible humano de la aplicación</span><span class="sxs-lookup"><span data-stu-id="315a0-124">Human readable version of the application</span></span>|
|<span data-ttu-id="315a0-125">installState</span><span class="sxs-lookup"><span data-stu-id="315a0-125">installState</span></span>|[<span data-ttu-id="315a0-126">resultantAppState</span><span class="sxs-lookup"><span data-stu-id="315a0-126">resultantAppState</span></span>](../resources/intune-shared-resultantappstate.md)|<span data-ttu-id="315a0-127">El estado de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="315a0-127">The install state of the app.</span></span> <span data-ttu-id="315a0-128">Los valores posibles son: `installed`, `failed`, `notInstalled`, `uninstallFailed`, `pendingInstall`, `unknown` y `notApplicable`.</span><span class="sxs-lookup"><span data-stu-id="315a0-128">Possible values are: `installed`, `failed`, `notInstalled`, `uninstallFailed`, `pendingInstall`, `unknown`, `notApplicable`.</span></span>|
|<span data-ttu-id="315a0-129">supportedDeviceTypes</span><span class="sxs-lookup"><span data-stu-id="315a0-129">supportedDeviceTypes</span></span>|<span data-ttu-id="315a0-130">colección de [mobileAppSupportedDeviceType](../resources/intune-troubleshooting-mobileappsupporteddevicetype.md)</span><span class="sxs-lookup"><span data-stu-id="315a0-130">[mobileAppSupportedDeviceType](../resources/intune-troubleshooting-mobileappsupporteddevicetype.md) collection</span></span>|<span data-ttu-id="315a0-131">Las plataformas compatibles para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="315a0-131">The supported platforms for the app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="315a0-132">Relaciones</span><span class="sxs-lookup"><span data-stu-id="315a0-132">Relationships</span></span>
<span data-ttu-id="315a0-133">Ninguna</span><span class="sxs-lookup"><span data-stu-id="315a0-133">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="315a0-134">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="315a0-134">JSON Representation</span></span>
<span data-ttu-id="315a0-135">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="315a0-135">Here is a JSON representation of the resource.</span></span>
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





