---
title: Crear notificationMessageTemplate
description: Cree un objeto notificationMessageTemplate.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 4d7e8fb5f7e718ec2ec1c0a0f5b35241ef408aaf
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27912354"
---
# <a name="create-notificationmessagetemplate"></a><span data-ttu-id="ef31f-103">Crear notificationMessageTemplate</span><span class="sxs-lookup"><span data-stu-id="ef31f-103">Create notificationMessageTemplate</span></span>

> <span data-ttu-id="ef31f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ef31f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ef31f-105">Cree un objeto [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md).</span><span class="sxs-lookup"><span data-stu-id="ef31f-105">Create a new [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ef31f-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ef31f-106">Prerequisites</span></span>
<span data-ttu-id="ef31f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ef31f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ef31f-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ef31f-109">Permission type</span></span>|<span data-ttu-id="ef31f-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ef31f-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ef31f-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ef31f-111">Delegated (work or school account)</span></span>|<span data-ttu-id="ef31f-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ef31f-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="ef31f-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ef31f-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ef31f-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ef31f-114">Not supported.</span></span>|
|<span data-ttu-id="ef31f-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ef31f-115">Application</span></span>|<span data-ttu-id="ef31f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ef31f-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ef31f-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ef31f-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/notificationMessageTemplates
```

## <a name="request-headers"></a><span data-ttu-id="ef31f-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ef31f-118">Request headers</span></span>
|<span data-ttu-id="ef31f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef31f-119">Header</span></span>|<span data-ttu-id="ef31f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ef31f-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ef31f-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="ef31f-121">Authorization</span></span>|<span data-ttu-id="ef31f-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ef31f-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ef31f-123">Accept</span><span class="sxs-lookup"><span data-stu-id="ef31f-123">Accept</span></span>|<span data-ttu-id="ef31f-124">application/json</span><span class="sxs-lookup"><span data-stu-id="ef31f-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ef31f-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ef31f-125">Request body</span></span>
<span data-ttu-id="ef31f-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto notificationMessageTemplate.</span><span class="sxs-lookup"><span data-stu-id="ef31f-126">In the request body, supply a JSON representation for the notificationMessageTemplate object.</span></span>

<span data-ttu-id="ef31f-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto notificationMessageTemplate.</span><span class="sxs-lookup"><span data-stu-id="ef31f-127">The following table shows the properties that are required when you create the notificationMessageTemplate.</span></span>

|<span data-ttu-id="ef31f-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ef31f-128">Property</span></span>|<span data-ttu-id="ef31f-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="ef31f-129">Type</span></span>|<span data-ttu-id="ef31f-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef31f-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ef31f-131">id</span><span class="sxs-lookup"><span data-stu-id="ef31f-131">id</span></span>|<span data-ttu-id="ef31f-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="ef31f-132">String</span></span>|<span data-ttu-id="ef31f-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ef31f-133">Key of the entity.</span></span>|
|<span data-ttu-id="ef31f-134">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="ef31f-134">lastModifiedDateTime</span></span>|<span data-ttu-id="ef31f-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ef31f-135">DateTimeOffset</span></span>|<span data-ttu-id="ef31f-136">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="ef31f-136">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="ef31f-137">displayName</span><span class="sxs-lookup"><span data-stu-id="ef31f-137">displayName</span></span>|<span data-ttu-id="ef31f-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="ef31f-138">String</span></span>|<span data-ttu-id="ef31f-139">Nombre para mostrar de la plantilla de mensajes de notificación.</span><span class="sxs-lookup"><span data-stu-id="ef31f-139">Display name for the Notification Message Template.</span></span>|
|<span data-ttu-id="ef31f-140">defaultLocale</span><span class="sxs-lookup"><span data-stu-id="ef31f-140">defaultLocale</span></span>|<span data-ttu-id="ef31f-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="ef31f-141">String</span></span>|<span data-ttu-id="ef31f-142">La configuración regional predeterminada de reserva para los casos en que la configuración regional solicitada no está disponible.</span><span class="sxs-lookup"><span data-stu-id="ef31f-142">The default locale to fallback onto when the requested locale is not available.</span></span>|
|<span data-ttu-id="ef31f-143">brandingOptions</span><span class="sxs-lookup"><span data-stu-id="ef31f-143">brandingOptions</span></span>|[<span data-ttu-id="ef31f-144">notificationTemplateBrandingOptions</span><span class="sxs-lookup"><span data-stu-id="ef31f-144">notificationTemplateBrandingOptions</span></span>](../resources/intune-notification-notificationtemplatebrandingoptions.md)|<span data-ttu-id="ef31f-145">Las opciones de personalización de marca de la plantilla de mensaje.</span><span class="sxs-lookup"><span data-stu-id="ef31f-145">The Message Template Branding Options.</span></span> <span data-ttu-id="ef31f-146">La personalización de marca está definida en la consola de administración de Intune.</span><span class="sxs-lookup"><span data-stu-id="ef31f-146">Branding is defined in the Intune Admin Console.</span></span> <span data-ttu-id="ef31f-147">Los valores posibles son: `none`, `includeCompanyLogo`, `includeCompanyName` y `includeContactInformation`.</span><span class="sxs-lookup"><span data-stu-id="ef31f-147">Possible values are: `none`, `includeCompanyLogo`, `includeCompanyName`, `includeContactInformation`.</span></span>|



## <a name="response"></a><span data-ttu-id="ef31f-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ef31f-148">Response</span></span>
<span data-ttu-id="ef31f-149">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ef31f-149">If successful, this method returns a `201 Created` response code and a [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ef31f-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ef31f-150">Example</span></span>
### <a name="request"></a><span data-ttu-id="ef31f-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ef31f-151">Request</span></span>
<span data-ttu-id="ef31f-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ef31f-152">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/notificationMessageTemplates
Content-type: application/json
Content-length: 197

{
  "@odata.type": "#microsoft.graph.notificationMessageTemplate",
  "displayName": "Display Name value",
  "defaultLocale": "Default Locale value",
  "brandingOptions": "includeCompanyLogo"
}
```

### <a name="response"></a><span data-ttu-id="ef31f-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ef31f-153">Response</span></span>
<span data-ttu-id="ef31f-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ef31f-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



