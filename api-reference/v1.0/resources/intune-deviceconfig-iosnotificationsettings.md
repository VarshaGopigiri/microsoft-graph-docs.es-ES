---
title: Tipo de recurso iosNotificationSettings
description: Un elemento que describe la configuración de notificaciones.
author: tfitzmac
ms.openlocfilehash: 197de8b9cd59d1f6c998f92460e62aab480ef455
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27307843"
---
# <a name="iosnotificationsettings-resource-type"></a><span data-ttu-id="0e6d6-103">Tipo de recurso iosNotificationSettings</span><span class="sxs-lookup"><span data-stu-id="0e6d6-103">iosNotificationSettings resource type</span></span>

> <span data-ttu-id="0e6d6-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0e6d6-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0e6d6-105">Un elemento que describe la configuración de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="0e6d6-105">An item describing notification setting.</span></span>
## <a name="properties"></a><span data-ttu-id="0e6d6-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0e6d6-106">Properties</span></span>
|<span data-ttu-id="0e6d6-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0e6d6-107">Property</span></span>|<span data-ttu-id="0e6d6-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="0e6d6-108">Type</span></span>|<span data-ttu-id="0e6d6-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e6d6-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0e6d6-110">bundleID</span><span class="sxs-lookup"><span data-stu-id="0e6d6-110">bundleID</span></span>|<span data-ttu-id="0e6d6-111">Cadena</span><span class="sxs-lookup"><span data-stu-id="0e6d6-111">String</span></span>|<span data-ttu-id="0e6d6-112">Id. de paquete de la aplicación en el que aplicar esa configuración de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="0e6d6-112">Bundle id of app to which to apply these notification settings.</span></span>|
|<span data-ttu-id="0e6d6-113">appName</span><span class="sxs-lookup"><span data-stu-id="0e6d6-113">appName</span></span>|<span data-ttu-id="0e6d6-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="0e6d6-114">String</span></span>|<span data-ttu-id="0e6d6-115">Nombre de la aplicación que se asociará con el bundleID.</span><span class="sxs-lookup"><span data-stu-id="0e6d6-115">Application name to be associated with the bundleID.</span></span>|
|<span data-ttu-id="0e6d6-116">publicador</span><span class="sxs-lookup"><span data-stu-id="0e6d6-116">publisher</span></span>|<span data-ttu-id="0e6d6-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="0e6d6-117">String</span></span>|<span data-ttu-id="0e6d6-118">Publicador que se asociará con el bundleID.</span><span class="sxs-lookup"><span data-stu-id="0e6d6-118">Publisher to be associated with the bundleID.</span></span>|
|<span data-ttu-id="0e6d6-119">habilitado</span><span class="sxs-lookup"><span data-stu-id="0e6d6-119">enabled</span></span>|<span data-ttu-id="0e6d6-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e6d6-120">Boolean</span></span>|<span data-ttu-id="0e6d6-121">Indica si se permiten las notificaciones para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="0e6d6-121">Indicates whether notifications are allowed for this app.</span></span>|
|<span data-ttu-id="0e6d6-122">showInNotificationCenter</span><span class="sxs-lookup"><span data-stu-id="0e6d6-122">showInNotificationCenter</span></span>|<span data-ttu-id="0e6d6-123">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e6d6-123">Boolean</span></span>|<span data-ttu-id="0e6d6-124">Indica si se pueden mostrar notificaciones en el centro de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="0e6d6-124">Indicates whether notifications can be shown in notification center.</span></span>|
|<span data-ttu-id="0e6d6-125">showOnLockScreen</span><span class="sxs-lookup"><span data-stu-id="0e6d6-125">showOnLockScreen</span></span>|<span data-ttu-id="0e6d6-126">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e6d6-126">Boolean</span></span>|<span data-ttu-id="0e6d6-127">Indica si se pueden mostrar notificaciones en la pantalla de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="0e6d6-127">Indicates whether notifications can be shown on the lock screen.</span></span>|
|<span data-ttu-id="0e6d6-128">alertType</span><span class="sxs-lookup"><span data-stu-id="0e6d6-128">alertType</span></span>|[<span data-ttu-id="0e6d6-129">iosNotificationAlertType</span><span class="sxs-lookup"><span data-stu-id="0e6d6-129">iosNotificationAlertType</span></span>](../resources/intune-deviceconfig-iosnotificationalerttype.md)|<span data-ttu-id="0e6d6-130">Indica el tipo de alerta para las notificaciones de esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="0e6d6-130">Indicates the type of alert for notifications for this app.</span></span> <span data-ttu-id="0e6d6-131">Los valores posibles son: `deviceDefault`, `banner`, `modal` y `none`.</span><span class="sxs-lookup"><span data-stu-id="0e6d6-131">Possible values are: `deviceDefault`, `banner`, `modal`, `none`.</span></span>|
|<span data-ttu-id="0e6d6-132">badgesEnabled</span><span class="sxs-lookup"><span data-stu-id="0e6d6-132">badgesEnabled</span></span>|<span data-ttu-id="0e6d6-133">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e6d6-133">Boolean</span></span>|<span data-ttu-id="0e6d6-134">Indica si se permiten los distintivos para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="0e6d6-134">Indicates whether badges are allowed for this app.</span></span>|
|<span data-ttu-id="0e6d6-135">soundsEnabled</span><span class="sxs-lookup"><span data-stu-id="0e6d6-135">soundsEnabled</span></span>|<span data-ttu-id="0e6d6-136">Booleano</span><span class="sxs-lookup"><span data-stu-id="0e6d6-136">Boolean</span></span>|<span data-ttu-id="0e6d6-137">Indica si se permiten los sonidos para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="0e6d6-137">Indicates whether sounds are allowed for this app.</span></span>|

## <a name="relationships"></a><span data-ttu-id="0e6d6-138">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0e6d6-138">Relationships</span></span>
<span data-ttu-id="0e6d6-139">Ninguna</span><span class="sxs-lookup"><span data-stu-id="0e6d6-139">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="0e6d6-140">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0e6d6-140">JSON Representation</span></span>
<span data-ttu-id="0e6d6-141">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="0e6d6-141">Here is a JSON representation of the resource.</span></span>
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



