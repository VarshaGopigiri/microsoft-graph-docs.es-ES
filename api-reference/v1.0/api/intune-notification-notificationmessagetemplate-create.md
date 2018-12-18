---
title: Crear notificationMessageTemplate
description: Cree un objeto notificationMessageTemplate.
author: tfitzmac
ms.openlocfilehash: ac5a91d6a53719eac38f91e402a6f36f63ebdc36
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27315599"
---
# <a name="create-notificationmessagetemplate"></a><span data-ttu-id="184da-103">Crear notificationMessageTemplate</span><span class="sxs-lookup"><span data-stu-id="184da-103">Create notificationMessageTemplate</span></span>

> <span data-ttu-id="184da-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="184da-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="184da-105">Cree un objeto [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md).</span><span class="sxs-lookup"><span data-stu-id="184da-105">Create a new [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="184da-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="184da-106">Prerequisites</span></span>
<span data-ttu-id="184da-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="184da-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="184da-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="184da-109">Permission type</span></span>|<span data-ttu-id="184da-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="184da-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="184da-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="184da-111">Delegated (work or school account)</span></span>|<span data-ttu-id="184da-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="184da-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="184da-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="184da-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="184da-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="184da-114">Not supported.</span></span>|
|<span data-ttu-id="184da-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="184da-115">Application</span></span>|<span data-ttu-id="184da-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="184da-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="184da-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="184da-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/notificationMessageTemplates
```

## <a name="request-headers"></a><span data-ttu-id="184da-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="184da-118">Request headers</span></span>
|<span data-ttu-id="184da-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="184da-119">Header</span></span>|<span data-ttu-id="184da-120">Valor</span><span class="sxs-lookup"><span data-stu-id="184da-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="184da-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="184da-121">Authorization</span></span>|<span data-ttu-id="184da-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="184da-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="184da-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="184da-123">Accept</span></span>|<span data-ttu-id="184da-124">application/json</span><span class="sxs-lookup"><span data-stu-id="184da-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="184da-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="184da-125">Request body</span></span>
<span data-ttu-id="184da-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto notificationMessageTemplate.</span><span class="sxs-lookup"><span data-stu-id="184da-126">In the request body, supply a JSON representation for the notificationMessageTemplate object.</span></span>

<span data-ttu-id="184da-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto notificationMessageTemplate.</span><span class="sxs-lookup"><span data-stu-id="184da-127">The following table shows the properties that are required when you create the notificationMessageTemplate.</span></span>

|<span data-ttu-id="184da-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="184da-128">Property</span></span>|<span data-ttu-id="184da-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="184da-129">Type</span></span>|<span data-ttu-id="184da-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="184da-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="184da-131">id</span><span class="sxs-lookup"><span data-stu-id="184da-131">id</span></span>|<span data-ttu-id="184da-132">String</span><span class="sxs-lookup"><span data-stu-id="184da-132">String</span></span>|<span data-ttu-id="184da-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="184da-133">Key of the entity.</span></span>|
|<span data-ttu-id="184da-134">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="184da-134">lastModifiedDateTime</span></span>|<span data-ttu-id="184da-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="184da-135">DateTimeOffset</span></span>|<span data-ttu-id="184da-136">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="184da-136">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="184da-137">displayName</span><span class="sxs-lookup"><span data-stu-id="184da-137">displayName</span></span>|<span data-ttu-id="184da-138">String</span><span class="sxs-lookup"><span data-stu-id="184da-138">String</span></span>|<span data-ttu-id="184da-139">Nombre para mostrar de la plantilla de mensajes de notificación.</span><span class="sxs-lookup"><span data-stu-id="184da-139">Display name for the Notification Message Template.</span></span>|
|<span data-ttu-id="184da-140">defaultLocale</span><span class="sxs-lookup"><span data-stu-id="184da-140">defaultLocale</span></span>|<span data-ttu-id="184da-141">String</span><span class="sxs-lookup"><span data-stu-id="184da-141">String</span></span>|<span data-ttu-id="184da-142">La configuración regional predeterminada de reserva para los casos en que la configuración regional solicitada no está disponible.</span><span class="sxs-lookup"><span data-stu-id="184da-142">The default locale to fallback onto when the requested locale is not available.</span></span>|
|<span data-ttu-id="184da-143">brandingOptions</span><span class="sxs-lookup"><span data-stu-id="184da-143">brandingOptions</span></span>|[<span data-ttu-id="184da-144">notificationTemplateBrandingOptions</span><span class="sxs-lookup"><span data-stu-id="184da-144">notificationTemplateBrandingOptions</span></span>](../resources/intune-notification-notificationtemplatebrandingoptions.md)|<span data-ttu-id="184da-145">Las opciones de personalización de marca de la plantilla de mensaje.</span><span class="sxs-lookup"><span data-stu-id="184da-145">The Message Template Branding Options.</span></span> <span data-ttu-id="184da-146">La personalización de marca está definida en la consola de administración de Intune.</span><span class="sxs-lookup"><span data-stu-id="184da-146">Branding is defined in the Intune Admin Console.</span></span> <span data-ttu-id="184da-147">Los valores posibles son: `none`, `includeCompanyLogo`, `includeCompanyName` y `includeContactInformation`.</span><span class="sxs-lookup"><span data-stu-id="184da-147">Possible values are: `none`, `includeCompanyLogo`, `includeCompanyName`, `includeContactInformation`.</span></span>|



## <a name="response"></a><span data-ttu-id="184da-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="184da-148">Response</span></span>
<span data-ttu-id="184da-149">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="184da-149">If successful, this method returns a `201 Created` response code and a [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="184da-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="184da-150">Example</span></span>
### <a name="request"></a><span data-ttu-id="184da-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="184da-151">Request</span></span>
<span data-ttu-id="184da-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="184da-152">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="184da-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="184da-153">Response</span></span>
<span data-ttu-id="184da-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="184da-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



