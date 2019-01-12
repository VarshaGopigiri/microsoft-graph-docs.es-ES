---
title: Actualizar notificationMessageTemplate
description: Actualice las propiedades de un objeto notificationMessageTemplate.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 083391a2d3d18cc23b1419b5586bb1c72d35e3dc
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27917569"
---
# <a name="update-notificationmessagetemplate"></a><span data-ttu-id="b4693-103">Actualizar notificationMessageTemplate</span><span class="sxs-lookup"><span data-stu-id="b4693-103">Update notificationMessageTemplate</span></span>

> <span data-ttu-id="b4693-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b4693-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b4693-105">Actualice las propiedades de un objeto [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md).</span><span class="sxs-lookup"><span data-stu-id="b4693-105">Update the properties of a [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b4693-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b4693-106">Prerequisites</span></span>
<span data-ttu-id="b4693-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b4693-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b4693-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b4693-109">Permission type</span></span>|<span data-ttu-id="b4693-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b4693-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b4693-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b4693-111">Delegated (work or school account)</span></span>|<span data-ttu-id="b4693-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b4693-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="b4693-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b4693-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b4693-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b4693-114">Not supported.</span></span>|
|<span data-ttu-id="b4693-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b4693-115">Application</span></span>|<span data-ttu-id="b4693-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b4693-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b4693-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b4693-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/notificationMessageTemplates/{notificationMessageTemplateId}
```

## <a name="request-headers"></a><span data-ttu-id="b4693-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b4693-118">Request headers</span></span>
|<span data-ttu-id="b4693-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4693-119">Header</span></span>|<span data-ttu-id="b4693-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b4693-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b4693-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="b4693-121">Authorization</span></span>|<span data-ttu-id="b4693-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b4693-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b4693-123">Accept</span><span class="sxs-lookup"><span data-stu-id="b4693-123">Accept</span></span>|<span data-ttu-id="b4693-124">application/json</span><span class="sxs-lookup"><span data-stu-id="b4693-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b4693-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b4693-125">Request body</span></span>
<span data-ttu-id="b4693-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md).</span><span class="sxs-lookup"><span data-stu-id="b4693-126">In the request body, supply a JSON representation for the [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md) object.</span></span>

<span data-ttu-id="b4693-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md).</span><span class="sxs-lookup"><span data-stu-id="b4693-127">The following table shows the properties that are required when you create the [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md).</span></span>

|<span data-ttu-id="b4693-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b4693-128">Property</span></span>|<span data-ttu-id="b4693-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="b4693-129">Type</span></span>|<span data-ttu-id="b4693-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4693-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b4693-131">id</span><span class="sxs-lookup"><span data-stu-id="b4693-131">id</span></span>|<span data-ttu-id="b4693-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="b4693-132">String</span></span>|<span data-ttu-id="b4693-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b4693-133">Key of the entity.</span></span>|
|<span data-ttu-id="b4693-134">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="b4693-134">lastModifiedDateTime</span></span>|<span data-ttu-id="b4693-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b4693-135">DateTimeOffset</span></span>|<span data-ttu-id="b4693-136">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="b4693-136">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="b4693-137">displayName</span><span class="sxs-lookup"><span data-stu-id="b4693-137">displayName</span></span>|<span data-ttu-id="b4693-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="b4693-138">String</span></span>|<span data-ttu-id="b4693-139">Nombre para mostrar de la plantilla de mensajes de notificación.</span><span class="sxs-lookup"><span data-stu-id="b4693-139">Display name for the Notification Message Template.</span></span>|
|<span data-ttu-id="b4693-140">defaultLocale</span><span class="sxs-lookup"><span data-stu-id="b4693-140">defaultLocale</span></span>|<span data-ttu-id="b4693-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="b4693-141">String</span></span>|<span data-ttu-id="b4693-142">La configuración regional predeterminada de reserva para los casos en que la configuración regional solicitada no está disponible.</span><span class="sxs-lookup"><span data-stu-id="b4693-142">The default locale to fallback onto when the requested locale is not available.</span></span>|
|<span data-ttu-id="b4693-143">brandingOptions</span><span class="sxs-lookup"><span data-stu-id="b4693-143">brandingOptions</span></span>|[<span data-ttu-id="b4693-144">notificationTemplateBrandingOptions</span><span class="sxs-lookup"><span data-stu-id="b4693-144">notificationTemplateBrandingOptions</span></span>](../resources/intune-notification-notificationtemplatebrandingoptions.md)|<span data-ttu-id="b4693-145">Las opciones de personalización de marca de la plantilla de mensaje.</span><span class="sxs-lookup"><span data-stu-id="b4693-145">The Message Template Branding Options.</span></span> <span data-ttu-id="b4693-146">La personalización de marca está definida en la consola de administración de Intune.</span><span class="sxs-lookup"><span data-stu-id="b4693-146">Branding is defined in the Intune Admin Console.</span></span> <span data-ttu-id="b4693-147">Los valores posibles son: `none`, `includeCompanyLogo`, `includeCompanyName` y `includeContactInformation`.</span><span class="sxs-lookup"><span data-stu-id="b4693-147">Possible values are: `none`, `includeCompanyLogo`, `includeCompanyName`, `includeContactInformation`.</span></span>|



## <a name="response"></a><span data-ttu-id="b4693-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b4693-148">Response</span></span>
<span data-ttu-id="b4693-149">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b4693-149">If successful, this method returns a `200 OK` response code and an updated [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b4693-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b4693-150">Example</span></span>
### <a name="request"></a><span data-ttu-id="b4693-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b4693-151">Request</span></span>
<span data-ttu-id="b4693-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b4693-152">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/notificationMessageTemplates/{notificationMessageTemplateId}
Content-type: application/json
Content-length: 197

{
  "@odata.type": "#microsoft.graph.notificationMessageTemplate",
  "displayName": "Display Name value",
  "defaultLocale": "Default Locale value",
  "brandingOptions": "includeCompanyLogo"
}
```

### <a name="response"></a><span data-ttu-id="b4693-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b4693-153">Response</span></span>
<span data-ttu-id="b4693-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b4693-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 310

{
  "@odata.type": "#microsoft.graph.notificationMessageTemplate",
  "id": "e1db399b-399b-e1db-9b39-dbe19b39dbe1",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "defaultLocale": "Default Locale value",
  "brandingOptions": "includeCompanyLogo"
}
```



