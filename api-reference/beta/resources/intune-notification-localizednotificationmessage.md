---
title: Tipo de recurso localizedNotificationMessage
description: El contenido de texto de una plantilla de mensaje de notificación para la configuración regional.
author: tfitzmac
ms.openlocfilehash: e04d1d6d98cbbdbbb2b28250305e3b42a20af688
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27327093"
---
# <a name="localizednotificationmessage-resource-type"></a><span data-ttu-id="02060-103">Tipo de recurso localizedNotificationMessage</span><span class="sxs-lookup"><span data-stu-id="02060-103">localizedNotificationMessage resource type</span></span>

> <span data-ttu-id="02060-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="02060-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="02060-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="02060-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="02060-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="02060-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="02060-107">El contenido de texto de una plantilla de mensaje de notificación para la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="02060-107">The text content of a Notification Message Template for the specified locale.</span></span>
## <a name="methods"></a><span data-ttu-id="02060-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="02060-108">Methods</span></span>
|<span data-ttu-id="02060-109">Método</span><span class="sxs-lookup"><span data-stu-id="02060-109">Method</span></span>|<span data-ttu-id="02060-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02060-110">Return Type</span></span>|<span data-ttu-id="02060-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="02060-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="02060-112">Enumerar localizedNotificationMessages</span><span class="sxs-lookup"><span data-stu-id="02060-112">List localizedNotificationMessages</span></span>](../api/intune-notification-localizednotificationmessage-list.md)|<span data-ttu-id="02060-113">Colección [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md)</span><span class="sxs-lookup"><span data-stu-id="02060-113">[localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md) collection</span></span>|<span data-ttu-id="02060-114">Enumere las propiedades y las relaciones de los objetos [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md).</span><span class="sxs-lookup"><span data-stu-id="02060-114">List properties and relationships of the [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md) objects.</span></span>|
|[<span data-ttu-id="02060-115">Obtener localizedNotificationMessage</span><span class="sxs-lookup"><span data-stu-id="02060-115">Get localizedNotificationMessage</span></span>](../api/intune-notification-localizednotificationmessage-get.md)|[<span data-ttu-id="02060-116">localizedNotificationMessage</span><span class="sxs-lookup"><span data-stu-id="02060-116">localizedNotificationMessage</span></span>](../resources/intune-notification-localizednotificationmessage.md)|<span data-ttu-id="02060-117">Lea las propiedades y las relaciones del objeto [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md).</span><span class="sxs-lookup"><span data-stu-id="02060-117">Read properties and relationships of the [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md) object.</span></span>|
|[<span data-ttu-id="02060-118">Crear localizedNotificationMessage</span><span class="sxs-lookup"><span data-stu-id="02060-118">Create localizedNotificationMessage</span></span>](../api/intune-notification-localizednotificationmessage-create.md)|[<span data-ttu-id="02060-119">localizedNotificationMessage</span><span class="sxs-lookup"><span data-stu-id="02060-119">localizedNotificationMessage</span></span>](../resources/intune-notification-localizednotificationmessage.md)|<span data-ttu-id="02060-120">Cree un objeto [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md).</span><span class="sxs-lookup"><span data-stu-id="02060-120">Create a new [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md) object.</span></span>|
|[<span data-ttu-id="02060-121">Eliminar localizedNotificationMessage</span><span class="sxs-lookup"><span data-stu-id="02060-121">Delete localizedNotificationMessage</span></span>](../api/intune-notification-localizednotificationmessage-delete.md)|<span data-ttu-id="02060-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="02060-122">None</span></span>|<span data-ttu-id="02060-123">Elimina un [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md).</span><span class="sxs-lookup"><span data-stu-id="02060-123">Deletes a [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md).</span></span>|
|[<span data-ttu-id="02060-124">Actualizar localizedNotificationMessage</span><span class="sxs-lookup"><span data-stu-id="02060-124">Update localizedNotificationMessage</span></span>](../api/intune-notification-localizednotificationmessage-update.md)|[<span data-ttu-id="02060-125">localizedNotificationMessage</span><span class="sxs-lookup"><span data-stu-id="02060-125">localizedNotificationMessage</span></span>](../resources/intune-notification-localizednotificationmessage.md)|<span data-ttu-id="02060-126">Actualice las propiedades de un objeto [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md).</span><span class="sxs-lookup"><span data-stu-id="02060-126">Update the properties of a [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="02060-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="02060-127">Properties</span></span>
|<span data-ttu-id="02060-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="02060-128">Property</span></span>|<span data-ttu-id="02060-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="02060-129">Type</span></span>|<span data-ttu-id="02060-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="02060-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="02060-131">id</span><span class="sxs-lookup"><span data-stu-id="02060-131">id</span></span>|<span data-ttu-id="02060-132">String</span><span class="sxs-lookup"><span data-stu-id="02060-132">String</span></span>|<span data-ttu-id="02060-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="02060-133">Key of the entity.</span></span>|
|<span data-ttu-id="02060-134">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="02060-134">lastModifiedDateTime</span></span>|<span data-ttu-id="02060-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="02060-135">DateTimeOffset</span></span>|<span data-ttu-id="02060-136">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="02060-136">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="02060-137">configuración regional</span><span class="sxs-lookup"><span data-stu-id="02060-137">locale</span></span>|<span data-ttu-id="02060-138">String</span><span class="sxs-lookup"><span data-stu-id="02060-138">String</span></span>|<span data-ttu-id="02060-139">La configuración regional para la que se destina este mensaje.</span><span class="sxs-lookup"><span data-stu-id="02060-139">The Locale for which this message is destined.</span></span>|
|<span data-ttu-id="02060-140">subject</span><span class="sxs-lookup"><span data-stu-id="02060-140">subject</span></span>|<span data-ttu-id="02060-141">String</span><span class="sxs-lookup"><span data-stu-id="02060-141">String</span></span>|<span data-ttu-id="02060-142">El asunto de la plantilla del mensaje.</span><span class="sxs-lookup"><span data-stu-id="02060-142">The Message Template Subject.</span></span>|
|<span data-ttu-id="02060-143">messageTemplate</span><span class="sxs-lookup"><span data-stu-id="02060-143">messageTemplate</span></span>|<span data-ttu-id="02060-144">String</span><span class="sxs-lookup"><span data-stu-id="02060-144">String</span></span>|<span data-ttu-id="02060-145">El contenido de la plantilla del mensaje.</span><span class="sxs-lookup"><span data-stu-id="02060-145">The Message Template content.</span></span>|
|<span data-ttu-id="02060-146">isDefault</span><span class="sxs-lookup"><span data-stu-id="02060-146">isDefault</span></span>|<span data-ttu-id="02060-147">Boolean</span><span class="sxs-lookup"><span data-stu-id="02060-147">Boolean</span></span>|<span data-ttu-id="02060-148">Marca para indicar si se trata de la configuración regional predeterminada para la reserva del idioma.</span><span class="sxs-lookup"><span data-stu-id="02060-148">Flag to indicate whether or not this is the default locale for language fallback.</span></span> <span data-ttu-id="02060-149">Solo se puede establecer esta marca.</span><span class="sxs-lookup"><span data-stu-id="02060-149">This flag can only be set.</span></span> <span data-ttu-id="02060-150">Para eliminarla, establezca esta propiedad en true en otro mensaje de notificación localizado.</span><span class="sxs-lookup"><span data-stu-id="02060-150">To unset, set this property to true on another Localized Notification Message.</span></span>|

## <a name="relationships"></a><span data-ttu-id="02060-151">Relaciones</span><span class="sxs-lookup"><span data-stu-id="02060-151">Relationships</span></span>
<span data-ttu-id="02060-152">Ninguna</span><span class="sxs-lookup"><span data-stu-id="02060-152">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="02060-153">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="02060-153">JSON Representation</span></span>
<span data-ttu-id="02060-154">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="02060-154">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.localizedNotificationMessage"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.localizedNotificationMessage",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "locale": "String",
  "subject": "String",
  "messageTemplate": "String",
  "isDefault": true
}
```





