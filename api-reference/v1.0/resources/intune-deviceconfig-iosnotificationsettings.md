---
title: Tipo de recurso iosNotificationSettings
description: Un elemento que describe la configuración de notificaciones.
ms.openlocfilehash: 40f23c228bf10cfb7f273efbe343c1ff773ac280
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031698"
---
# <a name="iosnotificationsettings-resource-type"></a><span data-ttu-id="868f5-103">Tipo de recurso iosNotificationSettings</span><span class="sxs-lookup"><span data-stu-id="868f5-103">iosNotificationSettings resource type</span></span>

> <span data-ttu-id="868f5-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="868f5-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="868f5-105">Un elemento que describe la configuración de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="868f5-105">An item describing notification setting.</span></span>
## <a name="properties"></a><span data-ttu-id="868f5-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="868f5-106">Properties</span></span>
|<span data-ttu-id="868f5-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="868f5-107">Property</span></span>|<span data-ttu-id="868f5-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="868f5-108">Type</span></span>|<span data-ttu-id="868f5-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="868f5-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="868f5-110">bundleID</span><span class="sxs-lookup"><span data-stu-id="868f5-110">bundleID</span></span>|<span data-ttu-id="868f5-111">Cadena</span><span class="sxs-lookup"><span data-stu-id="868f5-111">String</span></span>|<span data-ttu-id="868f5-112">Id. de paquete de la aplicación en el que aplicar esa configuración de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="868f5-112">Bundle id of app to which to apply these notification settings.</span></span>|
|<span data-ttu-id="868f5-113">appName</span><span class="sxs-lookup"><span data-stu-id="868f5-113">appName</span></span>|<span data-ttu-id="868f5-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="868f5-114">String</span></span>|<span data-ttu-id="868f5-115">Nombre de la aplicación que se asociará con el bundleID.</span><span class="sxs-lookup"><span data-stu-id="868f5-115">Application name to be associated with the bundleID.</span></span>|
|<span data-ttu-id="868f5-116">publicador</span><span class="sxs-lookup"><span data-stu-id="868f5-116">publisher</span></span>|<span data-ttu-id="868f5-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="868f5-117">String</span></span>|<span data-ttu-id="868f5-118">Publicador que se asociará con el bundleID.</span><span class="sxs-lookup"><span data-stu-id="868f5-118">Publisher to be associated with the bundleID.</span></span>|
|<span data-ttu-id="868f5-119">habilitado</span><span class="sxs-lookup"><span data-stu-id="868f5-119">enabled</span></span>|<span data-ttu-id="868f5-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="868f5-120">Boolean</span></span>|<span data-ttu-id="868f5-121">Indica si se permiten las notificaciones para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="868f5-121">Indicates whether notifications are allowed for this app.</span></span>|
|<span data-ttu-id="868f5-122">showInNotificationCenter</span><span class="sxs-lookup"><span data-stu-id="868f5-122">showInNotificationCenter</span></span>|<span data-ttu-id="868f5-123">Booleano</span><span class="sxs-lookup"><span data-stu-id="868f5-123">Boolean</span></span>|<span data-ttu-id="868f5-124">Indica si se pueden mostrar notificaciones en el centro de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="868f5-124">Indicates whether notifications can be shown in notification center.</span></span>|
|<span data-ttu-id="868f5-125">showOnLockScreen</span><span class="sxs-lookup"><span data-stu-id="868f5-125">showOnLockScreen</span></span>|<span data-ttu-id="868f5-126">Booleano</span><span class="sxs-lookup"><span data-stu-id="868f5-126">Boolean</span></span>|<span data-ttu-id="868f5-127">Indica si se pueden mostrar notificaciones en la pantalla de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="868f5-127">Indicates whether notifications can be shown on the lock screen.</span></span>|
|<span data-ttu-id="868f5-128">alertType</span><span class="sxs-lookup"><span data-stu-id="868f5-128">alertType</span></span>|[<span data-ttu-id="868f5-129">iosNotificationAlertType</span><span class="sxs-lookup"><span data-stu-id="868f5-129">iosNotificationAlertType</span></span>](../resources/intune-deviceconfig-iosnotificationalerttype.md)|<span data-ttu-id="868f5-130">Indica el tipo de alerta para las notificaciones de esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="868f5-130">Indicates the type of alert for notifications for this app.</span></span> <span data-ttu-id="868f5-131">Los valores posibles son: `deviceDefault`, `banner`, `modal` y `none`.</span><span class="sxs-lookup"><span data-stu-id="868f5-131">Possible values are: `deviceDefault`, `banner`, `modal`, `none`.</span></span>|
|<span data-ttu-id="868f5-132">badgesEnabled</span><span class="sxs-lookup"><span data-stu-id="868f5-132">badgesEnabled</span></span>|<span data-ttu-id="868f5-133">Booleano</span><span class="sxs-lookup"><span data-stu-id="868f5-133">Boolean</span></span>|<span data-ttu-id="868f5-134">Indica si se permiten los distintivos para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="868f5-134">Indicates whether badges are allowed for this app.</span></span>|
|<span data-ttu-id="868f5-135">soundsEnabled</span><span class="sxs-lookup"><span data-stu-id="868f5-135">soundsEnabled</span></span>|<span data-ttu-id="868f5-136">Booleano</span><span class="sxs-lookup"><span data-stu-id="868f5-136">Boolean</span></span>|<span data-ttu-id="868f5-137">Indica si se permiten los sonidos para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="868f5-137">Indicates whether sounds are allowed for this app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="868f5-138">Relaciones</span><span class="sxs-lookup"><span data-stu-id="868f5-138">Relationships</span></span>
<span data-ttu-id="868f5-139">Ninguna</span><span class="sxs-lookup"><span data-stu-id="868f5-139">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="868f5-140">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="868f5-140">JSON Representation</span></span>
<span data-ttu-id="868f5-141">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="868f5-141">Here is a JSON representation of the resource.</span></span>
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



