---
title: Tipo de recurso iosNotificationSettings
description: Un elemento que describe la configuración de notificaciones.
author: tfitzmac
ms.openlocfilehash: c24e0719e634d2939f88280431538b41fb0a1b5f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27359195"
---
# <a name="iosnotificationsettings-resource-type"></a><span data-ttu-id="9fb7c-103">Tipo de recurso iosNotificationSettings</span><span class="sxs-lookup"><span data-stu-id="9fb7c-103">iosNotificationSettings resource type</span></span>

> <span data-ttu-id="9fb7c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9fb7c-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9fb7c-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9fb7c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="9fb7c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9fb7c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9fb7c-107">Un elemento que describe la configuración de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="9fb7c-107">An item describing notification setting.</span></span>
## <a name="properties"></a><span data-ttu-id="9fb7c-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9fb7c-108">Properties</span></span>
|<span data-ttu-id="9fb7c-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9fb7c-109">Property</span></span>|<span data-ttu-id="9fb7c-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="9fb7c-110">Type</span></span>|<span data-ttu-id="9fb7c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fb7c-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9fb7c-112">bundleID</span><span class="sxs-lookup"><span data-stu-id="9fb7c-112">bundleID</span></span>|<span data-ttu-id="9fb7c-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="9fb7c-113">String</span></span>|<span data-ttu-id="9fb7c-114">Id. de paquete de la aplicación en el que aplicar esa configuración de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="9fb7c-114">Bundle id of app to which to apply these notification settings.</span></span>|
|<span data-ttu-id="9fb7c-115">appName</span><span class="sxs-lookup"><span data-stu-id="9fb7c-115">appName</span></span>|<span data-ttu-id="9fb7c-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="9fb7c-116">String</span></span>|<span data-ttu-id="9fb7c-117">Nombre de la aplicación que se asociará con el bundleID.</span><span class="sxs-lookup"><span data-stu-id="9fb7c-117">Application name to be associated with the bundleID.</span></span>|
|<span data-ttu-id="9fb7c-118">publicador</span><span class="sxs-lookup"><span data-stu-id="9fb7c-118">publisher</span></span>|<span data-ttu-id="9fb7c-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="9fb7c-119">String</span></span>|<span data-ttu-id="9fb7c-120">Publicador que se asociará con el bundleID.</span><span class="sxs-lookup"><span data-stu-id="9fb7c-120">Publisher to be associated with the bundleID.</span></span>|
|<span data-ttu-id="9fb7c-121">habilitado</span><span class="sxs-lookup"><span data-stu-id="9fb7c-121">enabled</span></span>|<span data-ttu-id="9fb7c-122">Booleano</span><span class="sxs-lookup"><span data-stu-id="9fb7c-122">Boolean</span></span>|<span data-ttu-id="9fb7c-123">Indica si se permiten las notificaciones para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="9fb7c-123">Indicates whether notifications are allowed for this app.</span></span>|
|<span data-ttu-id="9fb7c-124">showInNotificationCenter</span><span class="sxs-lookup"><span data-stu-id="9fb7c-124">showInNotificationCenter</span></span>|<span data-ttu-id="9fb7c-125">Booleano</span><span class="sxs-lookup"><span data-stu-id="9fb7c-125">Boolean</span></span>|<span data-ttu-id="9fb7c-126">Indica si se pueden mostrar notificaciones en el centro de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="9fb7c-126">Indicates whether notifications can be shown in notification center.</span></span>|
|<span data-ttu-id="9fb7c-127">showOnLockScreen</span><span class="sxs-lookup"><span data-stu-id="9fb7c-127">showOnLockScreen</span></span>|<span data-ttu-id="9fb7c-128">Booleano</span><span class="sxs-lookup"><span data-stu-id="9fb7c-128">Boolean</span></span>|<span data-ttu-id="9fb7c-129">Indica si se pueden mostrar notificaciones en la pantalla de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="9fb7c-129">Indicates whether notifications can be shown on the lock screen.</span></span>|
|<span data-ttu-id="9fb7c-130">alertType</span><span class="sxs-lookup"><span data-stu-id="9fb7c-130">alertType</span></span>|[<span data-ttu-id="9fb7c-131">iosNotificationAlertType</span><span class="sxs-lookup"><span data-stu-id="9fb7c-131">iosNotificationAlertType</span></span>](../resources/intune-deviceconfig-iosnotificationalerttype.md)|<span data-ttu-id="9fb7c-132">Indica el tipo de alerta para las notificaciones de esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="9fb7c-132">Indicates the type of alert for notifications for this app.</span></span> <span data-ttu-id="9fb7c-133">Los valores posibles son: `deviceDefault`, `banner`, `modal` y `none`.</span><span class="sxs-lookup"><span data-stu-id="9fb7c-133">Possible values are: `deviceDefault`, `banner`, `modal`, `none`.</span></span>|
|<span data-ttu-id="9fb7c-134">badgesEnabled</span><span class="sxs-lookup"><span data-stu-id="9fb7c-134">badgesEnabled</span></span>|<span data-ttu-id="9fb7c-135">Booleano</span><span class="sxs-lookup"><span data-stu-id="9fb7c-135">Boolean</span></span>|<span data-ttu-id="9fb7c-136">Indica si se permiten los distintivos para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="9fb7c-136">Indicates whether badges are allowed for this app.</span></span>|
|<span data-ttu-id="9fb7c-137">soundsEnabled</span><span class="sxs-lookup"><span data-stu-id="9fb7c-137">soundsEnabled</span></span>|<span data-ttu-id="9fb7c-138">Booleano</span><span class="sxs-lookup"><span data-stu-id="9fb7c-138">Boolean</span></span>|<span data-ttu-id="9fb7c-139">Indica si se permiten los sonidos para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="9fb7c-139">Indicates whether sounds are allowed for this app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="9fb7c-140">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9fb7c-140">Relationships</span></span>
<span data-ttu-id="9fb7c-141">Ninguna</span><span class="sxs-lookup"><span data-stu-id="9fb7c-141">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="9fb7c-142">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9fb7c-142">JSON Representation</span></span>
<span data-ttu-id="9fb7c-143">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9fb7c-143">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosNotificationSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosNotificationSettings",
  "bundleID": "String",
  "appName": "String",
  "publisher": "String",
  "enabled": true,
  "showInNotificationCenter": true,
  "showOnLockScreen": true,
  "alertType": "String",
  "badgesEnabled": true,
  "soundsEnabled": true
}
```





