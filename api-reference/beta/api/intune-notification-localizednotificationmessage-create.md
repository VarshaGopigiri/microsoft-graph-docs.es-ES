---
title: Crear localizedNotificationMessage
description: Cree un objeto localizedNotificationMessage.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: bf0187177a80428924af6276eaf9df6f6456e2d2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27950798"
---
# <a name="create-localizednotificationmessage"></a><span data-ttu-id="7ea11-103">Crear localizedNotificationMessage</span><span class="sxs-lookup"><span data-stu-id="7ea11-103">Create localizedNotificationMessage</span></span>

> <span data-ttu-id="7ea11-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7ea11-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7ea11-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7ea11-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7ea11-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7ea11-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7ea11-107">Cree un objeto [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md).</span><span class="sxs-lookup"><span data-stu-id="7ea11-107">Create a new [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7ea11-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7ea11-108">Prerequisites</span></span>
<span data-ttu-id="7ea11-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7ea11-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7ea11-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7ea11-111">Permission type</span></span>|<span data-ttu-id="7ea11-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7ea11-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7ea11-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7ea11-113">Delegated (work or school account)</span></span>|<span data-ttu-id="7ea11-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7ea11-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="7ea11-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7ea11-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7ea11-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7ea11-116">Not supported.</span></span>|
|<span data-ttu-id="7ea11-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7ea11-117">Application</span></span>|<span data-ttu-id="7ea11-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7ea11-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7ea11-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7ea11-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/notificationMessageTemplates/{notificationMessageTemplateId}/localizedNotificationMessages
```

## <a name="request-headers"></a><span data-ttu-id="7ea11-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7ea11-120">Request headers</span></span>
|<span data-ttu-id="7ea11-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7ea11-121">Header</span></span>|<span data-ttu-id="7ea11-122">Valor</span><span class="sxs-lookup"><span data-stu-id="7ea11-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7ea11-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="7ea11-123">Authorization</span></span>|<span data-ttu-id="7ea11-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7ea11-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7ea11-125">Accept</span><span class="sxs-lookup"><span data-stu-id="7ea11-125">Accept</span></span>|<span data-ttu-id="7ea11-126">application/json</span><span class="sxs-lookup"><span data-stu-id="7ea11-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7ea11-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7ea11-127">Request body</span></span>
<span data-ttu-id="7ea11-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto localizedNotificationMessage.</span><span class="sxs-lookup"><span data-stu-id="7ea11-128">In the request body, supply a JSON representation for the localizedNotificationMessage object.</span></span>

<span data-ttu-id="7ea11-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto localizedNotificationMessage.</span><span class="sxs-lookup"><span data-stu-id="7ea11-129">The following table shows the properties that are required when you create the localizedNotificationMessage.</span></span>

|<span data-ttu-id="7ea11-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7ea11-130">Property</span></span>|<span data-ttu-id="7ea11-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="7ea11-131">Type</span></span>|<span data-ttu-id="7ea11-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ea11-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7ea11-133">id</span><span class="sxs-lookup"><span data-stu-id="7ea11-133">id</span></span>|<span data-ttu-id="7ea11-134">String</span><span class="sxs-lookup"><span data-stu-id="7ea11-134">String</span></span>|<span data-ttu-id="7ea11-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7ea11-135">Key of the entity.</span></span>|
|<span data-ttu-id="7ea11-136">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="7ea11-136">lastModifiedDateTime</span></span>|<span data-ttu-id="7ea11-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7ea11-137">DateTimeOffset</span></span>|<span data-ttu-id="7ea11-138">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="7ea11-138">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="7ea11-139">configuración regional</span><span class="sxs-lookup"><span data-stu-id="7ea11-139">locale</span></span>|<span data-ttu-id="7ea11-140">String</span><span class="sxs-lookup"><span data-stu-id="7ea11-140">String</span></span>|<span data-ttu-id="7ea11-141">La configuración regional para la que se destina este mensaje.</span><span class="sxs-lookup"><span data-stu-id="7ea11-141">The Locale for which this message is destined.</span></span>|
|<span data-ttu-id="7ea11-142">subject</span><span class="sxs-lookup"><span data-stu-id="7ea11-142">subject</span></span>|<span data-ttu-id="7ea11-143">String</span><span class="sxs-lookup"><span data-stu-id="7ea11-143">String</span></span>|<span data-ttu-id="7ea11-144">El asunto de la plantilla del mensaje.</span><span class="sxs-lookup"><span data-stu-id="7ea11-144">The Message Template Subject.</span></span>|
|<span data-ttu-id="7ea11-145">messageTemplate</span><span class="sxs-lookup"><span data-stu-id="7ea11-145">messageTemplate</span></span>|<span data-ttu-id="7ea11-146">String</span><span class="sxs-lookup"><span data-stu-id="7ea11-146">String</span></span>|<span data-ttu-id="7ea11-147">El contenido de la plantilla del mensaje.</span><span class="sxs-lookup"><span data-stu-id="7ea11-147">The Message Template content.</span></span>|
|<span data-ttu-id="7ea11-148">isDefault</span><span class="sxs-lookup"><span data-stu-id="7ea11-148">isDefault</span></span>|<span data-ttu-id="7ea11-149">Booleano</span><span class="sxs-lookup"><span data-stu-id="7ea11-149">Boolean</span></span>|<span data-ttu-id="7ea11-150">Marca para indicar si se trata de la configuración regional predeterminada para la reserva del idioma.</span><span class="sxs-lookup"><span data-stu-id="7ea11-150">Flag to indicate whether or not this is the default locale for language fallback.</span></span> <span data-ttu-id="7ea11-151">Solo se puede establecer esta marca.</span><span class="sxs-lookup"><span data-stu-id="7ea11-151">This flag can only be set.</span></span> <span data-ttu-id="7ea11-152">Para eliminarla, establezca esta propiedad en true en otro mensaje de notificación localizado.</span><span class="sxs-lookup"><span data-stu-id="7ea11-152">To unset, set this property to true on another Localized Notification Message.</span></span>|



## <a name="response"></a><span data-ttu-id="7ea11-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7ea11-153">Response</span></span>
<span data-ttu-id="7ea11-154">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7ea11-154">If successful, this method returns a `201 Created` response code and a [localizedNotificationMessage](../resources/intune-notification-localizednotificationmessage.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7ea11-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7ea11-155">Example</span></span>
### <a name="request"></a><span data-ttu-id="7ea11-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7ea11-156">Request</span></span>
<span data-ttu-id="7ea11-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7ea11-157">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/notificationMessageTemplates/{notificationMessageTemplateId}/localizedNotificationMessages
Content-type: application/json
Content-length: 264

{
  "@odata.type": "#microsoft.graph.localizedNotificationMessage",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "locale": "Locale value",
  "subject": "Subject value",
  "messageTemplate": "Message Template value",
  "isDefault": true
}
```

### <a name="response"></a><span data-ttu-id="7ea11-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7ea11-158">Response</span></span>
<span data-ttu-id="7ea11-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7ea11-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 313

{
  "@odata.type": "#microsoft.graph.localizedNotificationMessage",
  "id": "7a777708-7708-7a77-0877-777a0877777a",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "locale": "Locale value",
  "subject": "Subject value",
  "messageTemplate": "Message Template value",
  "isDefault": true
}
```





