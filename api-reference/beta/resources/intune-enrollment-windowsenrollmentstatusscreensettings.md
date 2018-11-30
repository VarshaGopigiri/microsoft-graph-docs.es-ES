---
title: tipo de recurso windowsEnrollmentStatusScreenSettings
description: Configuración de pantalla de estado de inscripción
ms.openlocfilehash: 5ec77e41634a2db9f44fd4146cb5266ca00923e4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084252"
---
# <a name="windowsenrollmentstatusscreensettings-resource-type"></a><span data-ttu-id="d100c-103">tipo de recurso windowsEnrollmentStatusScreenSettings</span><span class="sxs-lookup"><span data-stu-id="d100c-103">windowsEnrollmentStatusScreenSettings resource type</span></span>

> <span data-ttu-id="d100c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d100c-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d100c-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d100c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d100c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d100c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d100c-107">Configuración de pantalla de estado de inscripción</span><span class="sxs-lookup"><span data-stu-id="d100c-107">Enrollment status screen setting</span></span>
## <a name="properties"></a><span data-ttu-id="d100c-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d100c-108">Properties</span></span>
|<span data-ttu-id="d100c-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d100c-109">Property</span></span>|<span data-ttu-id="d100c-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="d100c-110">Type</span></span>|<span data-ttu-id="d100c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d100c-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d100c-112">hideInstallationProgress</span><span class="sxs-lookup"><span data-stu-id="d100c-112">hideInstallationProgress</span></span>|<span data-ttu-id="d100c-113">Booleano</span><span class="sxs-lookup"><span data-stu-id="d100c-113">Boolean</span></span>|<span data-ttu-id="d100c-114">Mostrar u ocultar el progreso de la instalación para el usuario</span><span class="sxs-lookup"><span data-stu-id="d100c-114">Show or hide installation progress to user</span></span>|
|<span data-ttu-id="d100c-115">allowDeviceUseBeforeProfileAndAppInstallComplete</span><span class="sxs-lookup"><span data-stu-id="d100c-115">allowDeviceUseBeforeProfileAndAppInstallComplete</span></span>|<span data-ttu-id="d100c-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="d100c-116">Boolean</span></span>|<span data-ttu-id="d100c-117">Permitir o bloquear al usuario que utilice el dispositivo antes de la instalación de perfiles y la aplicación completa</span><span class="sxs-lookup"><span data-stu-id="d100c-117">Allow or block user to use device before profile and app installation complete</span></span>|
|<span data-ttu-id="d100c-118">blockDeviceSetupRetryByUser</span><span class="sxs-lookup"><span data-stu-id="d100c-118">blockDeviceSetupRetryByUser</span></span>|<span data-ttu-id="d100c-119">Booleano</span><span class="sxs-lookup"><span data-stu-id="d100c-119">Boolean</span></span>|<span data-ttu-id="d100c-120">Permitir al usuario que vuelva a intentar la instalación en caso de error de instalación</span><span class="sxs-lookup"><span data-stu-id="d100c-120">Allow the user to retry the setup on installation failure</span></span>|
|<span data-ttu-id="d100c-121">allowLogCollectionOnInstallFailure</span><span class="sxs-lookup"><span data-stu-id="d100c-121">allowLogCollectionOnInstallFailure</span></span>|<span data-ttu-id="d100c-122">Booleano</span><span class="sxs-lookup"><span data-stu-id="d100c-122">Boolean</span></span>|<span data-ttu-id="d100c-123">Permitir o bloquear registro colección en caso de error de instalación</span><span class="sxs-lookup"><span data-stu-id="d100c-123">Allow or block log collection on installation failure</span></span>|
|<span data-ttu-id="d100c-124">customErrorMessage</span><span class="sxs-lookup"><span data-stu-id="d100c-124">customErrorMessage</span></span>|<span data-ttu-id="d100c-125">String</span><span class="sxs-lookup"><span data-stu-id="d100c-125">String</span></span>|<span data-ttu-id="d100c-126">Establecer el mensaje de error personalizado para mostrar al producirse un error de instalación</span><span class="sxs-lookup"><span data-stu-id="d100c-126">Set custom error message to show upon installation failure</span></span>|
|<span data-ttu-id="d100c-127">installProgressTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="d100c-127">installProgressTimeoutInMinutes</span></span>|<span data-ttu-id="d100c-128">Int32</span><span class="sxs-lookup"><span data-stu-id="d100c-128">Int32</span></span>|<span data-ttu-id="d100c-129">Establecer tiempo de espera de progreso de la instalación en minutos</span><span class="sxs-lookup"><span data-stu-id="d100c-129">Set installation progress timeout in minutes</span></span>|
|<span data-ttu-id="d100c-130">allowDeviceUseOnInstallFailure</span><span class="sxs-lookup"><span data-stu-id="d100c-130">allowDeviceUseOnInstallFailure</span></span>|<span data-ttu-id="d100c-131">Booleano</span><span class="sxs-lookup"><span data-stu-id="d100c-131">Boolean</span></span>|<span data-ttu-id="d100c-132">Permitir que el usuario continuar utilizando el dispositivo en caso de error de instalación</span><span class="sxs-lookup"><span data-stu-id="d100c-132">Allow the user to continue using the device on installation failure</span></span>|

## <a name="relationships"></a><span data-ttu-id="d100c-133">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d100c-133">Relationships</span></span>
<span data-ttu-id="d100c-134">Ninguna</span><span class="sxs-lookup"><span data-stu-id="d100c-134">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="d100c-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d100c-135">JSON Representation</span></span>
<span data-ttu-id="d100c-136">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d100c-136">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsEnrollmentStatusScreenSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsEnrollmentStatusScreenSettings",
  "hideInstallationProgress": true,
  "allowDeviceUseBeforeProfileAndAppInstallComplete": true,
  "blockDeviceSetupRetryByUser": true,
  "allowLogCollectionOnInstallFailure": true,
  "customErrorMessage": "String",
  "installProgressTimeoutInMinutes": 1024,
  "allowDeviceUseOnInstallFailure": true
}
```





