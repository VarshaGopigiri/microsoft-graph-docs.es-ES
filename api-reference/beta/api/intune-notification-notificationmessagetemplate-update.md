---
title: Actualizar notificationMessageTemplate
description: Actualice las propiedades de un objeto notificationMessageTemplate.
ms.openlocfilehash: d86fd844165df3deb0f3a183e3d0d65b8b210d2d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27091130"
---
# <a name="update-notificationmessagetemplate"></a><span data-ttu-id="01bbf-103">Actualizar notificationMessageTemplate</span><span class="sxs-lookup"><span data-stu-id="01bbf-103">Update notificationMessageTemplate</span></span>

> <span data-ttu-id="01bbf-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="01bbf-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="01bbf-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="01bbf-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="01bbf-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="01bbf-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="01bbf-107">Actualice las propiedades de un objeto [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md).</span><span class="sxs-lookup"><span data-stu-id="01bbf-107">Update the properties of a [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="01bbf-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="01bbf-108">Prerequisites</span></span>
<span data-ttu-id="01bbf-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="01bbf-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="01bbf-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="01bbf-111">Permission type</span></span>|<span data-ttu-id="01bbf-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="01bbf-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="01bbf-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="01bbf-113">Delegated (work or school account)</span></span>|<span data-ttu-id="01bbf-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="01bbf-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="01bbf-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="01bbf-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="01bbf-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="01bbf-116">Not supported.</span></span>|
|<span data-ttu-id="01bbf-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="01bbf-117">Application</span></span>|<span data-ttu-id="01bbf-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="01bbf-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="01bbf-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="01bbf-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/notificationMessageTemplates/{notificationMessageTemplateId}
```

## <a name="request-headers"></a><span data-ttu-id="01bbf-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="01bbf-120">Request headers</span></span>
|<span data-ttu-id="01bbf-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="01bbf-121">Header</span></span>|<span data-ttu-id="01bbf-122">Valor</span><span class="sxs-lookup"><span data-stu-id="01bbf-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="01bbf-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="01bbf-123">Authorization</span></span>|<span data-ttu-id="01bbf-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="01bbf-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="01bbf-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="01bbf-125">Accept</span></span>|<span data-ttu-id="01bbf-126">application/json</span><span class="sxs-lookup"><span data-stu-id="01bbf-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="01bbf-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="01bbf-127">Request body</span></span>
<span data-ttu-id="01bbf-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md).</span><span class="sxs-lookup"><span data-stu-id="01bbf-128">In the request body, supply a JSON representation for the [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md) object.</span></span>

<span data-ttu-id="01bbf-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md).</span><span class="sxs-lookup"><span data-stu-id="01bbf-129">The following table shows the properties that are required when you create the [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md).</span></span>

|<span data-ttu-id="01bbf-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="01bbf-130">Property</span></span>|<span data-ttu-id="01bbf-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="01bbf-131">Type</span></span>|<span data-ttu-id="01bbf-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="01bbf-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="01bbf-133">id</span><span class="sxs-lookup"><span data-stu-id="01bbf-133">id</span></span>|<span data-ttu-id="01bbf-134">String</span><span class="sxs-lookup"><span data-stu-id="01bbf-134">String</span></span>|<span data-ttu-id="01bbf-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="01bbf-135">Key of the entity.</span></span>|
|<span data-ttu-id="01bbf-136">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="01bbf-136">lastModifiedDateTime</span></span>|<span data-ttu-id="01bbf-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="01bbf-137">DateTimeOffset</span></span>|<span data-ttu-id="01bbf-138">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="01bbf-138">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="01bbf-139">displayName</span><span class="sxs-lookup"><span data-stu-id="01bbf-139">displayName</span></span>|<span data-ttu-id="01bbf-140">String</span><span class="sxs-lookup"><span data-stu-id="01bbf-140">String</span></span>|<span data-ttu-id="01bbf-141">Nombre para mostrar de la plantilla de mensajes de notificación.</span><span class="sxs-lookup"><span data-stu-id="01bbf-141">Display name for the Notification Message Template.</span></span>|
|<span data-ttu-id="01bbf-142">defaultLocale</span><span class="sxs-lookup"><span data-stu-id="01bbf-142">defaultLocale</span></span>|<span data-ttu-id="01bbf-143">String</span><span class="sxs-lookup"><span data-stu-id="01bbf-143">String</span></span>|<span data-ttu-id="01bbf-144">La configuración regional predeterminada de reserva para los casos en que la configuración regional solicitada no está disponible.</span><span class="sxs-lookup"><span data-stu-id="01bbf-144">The default locale to fallback onto when the requested locale is not available.</span></span>|
|<span data-ttu-id="01bbf-145">brandingOptions</span><span class="sxs-lookup"><span data-stu-id="01bbf-145">brandingOptions</span></span>|[<span data-ttu-id="01bbf-146">notificationTemplateBrandingOptions</span><span class="sxs-lookup"><span data-stu-id="01bbf-146">notificationTemplateBrandingOptions</span></span>](../resources/intune-notification-notificationtemplatebrandingoptions.md)|<span data-ttu-id="01bbf-147">Las opciones de personalización de marca de la plantilla de mensaje.</span><span class="sxs-lookup"><span data-stu-id="01bbf-147">The Message Template Branding Options.</span></span> <span data-ttu-id="01bbf-148">La personalización de marca está definida en la consola de administración de Intune.</span><span class="sxs-lookup"><span data-stu-id="01bbf-148">Branding is defined in the Intune Admin Console.</span></span> <span data-ttu-id="01bbf-149">Los valores posibles son: `none`, `includeCompanyLogo`, `includeCompanyName` y `includeContactInformation`.</span><span class="sxs-lookup"><span data-stu-id="01bbf-149">Possible values are: `none`, `includeCompanyLogo`, `includeCompanyName`, `includeContactInformation`.</span></span>|
|<span data-ttu-id="01bbf-150">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="01bbf-150">roleScopeTagIds</span></span>|<span data-ttu-id="01bbf-151">Colección String</span><span class="sxs-lookup"><span data-stu-id="01bbf-151">String collection</span></span>|<span data-ttu-id="01bbf-152">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="01bbf-152">List of Scope Tags for this Entity instance.</span></span>|



## <a name="response"></a><span data-ttu-id="01bbf-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01bbf-153">Response</span></span>
<span data-ttu-id="01bbf-154">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="01bbf-154">If successful, this method returns a `200 OK` response code and an updated [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="01bbf-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="01bbf-155">Example</span></span>
### <a name="request"></a><span data-ttu-id="01bbf-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="01bbf-156">Request</span></span>
<span data-ttu-id="01bbf-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="01bbf-157">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/notificationMessageTemplates/{notificationMessageTemplateId}
Content-type: application/json
Content-length: 257

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "defaultLocale": "Default Locale value",
  "brandingOptions": "includeCompanyLogo",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ]
}
```

### <a name="response"></a><span data-ttu-id="01bbf-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01bbf-158">Response</span></span>
<span data-ttu-id="01bbf-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="01bbf-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 372

{
  "@odata.type": "#microsoft.graph.notificationMessageTemplate",
  "id": "e1db399b-399b-e1db-9b39-dbe19b39dbe1",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "defaultLocale": "Default Locale value",
  "brandingOptions": "includeCompanyLogo",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ]
}
```





