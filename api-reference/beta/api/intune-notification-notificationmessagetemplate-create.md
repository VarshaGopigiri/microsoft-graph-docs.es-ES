---
title: Crear notificationMessageTemplate
description: Cree un objeto notificationMessageTemplate.
author: tfitzmac
ms.openlocfilehash: 396d8cbcb312e4bbacc94770e3eceb4a4dc88067
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27347631"
---
# <a name="create-notificationmessagetemplate"></a><span data-ttu-id="a7218-103">Crear notificationMessageTemplate</span><span class="sxs-lookup"><span data-stu-id="a7218-103">Create notificationMessageTemplate</span></span>

> <span data-ttu-id="a7218-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a7218-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a7218-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a7218-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a7218-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a7218-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a7218-107">Cree un objeto [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md).</span><span class="sxs-lookup"><span data-stu-id="a7218-107">Create a new [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a7218-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a7218-108">Prerequisites</span></span>
<span data-ttu-id="a7218-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a7218-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a7218-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a7218-111">Permission type</span></span>|<span data-ttu-id="a7218-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a7218-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a7218-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a7218-113">Delegated (work or school account)</span></span>|<span data-ttu-id="a7218-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a7218-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="a7218-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a7218-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a7218-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a7218-116">Not supported.</span></span>|
|<span data-ttu-id="a7218-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a7218-117">Application</span></span>|<span data-ttu-id="a7218-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a7218-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a7218-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a7218-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/notificationMessageTemplates
```

## <a name="request-headers"></a><span data-ttu-id="a7218-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a7218-120">Request headers</span></span>
|<span data-ttu-id="a7218-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a7218-121">Header</span></span>|<span data-ttu-id="a7218-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a7218-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a7218-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="a7218-123">Authorization</span></span>|<span data-ttu-id="a7218-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a7218-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a7218-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a7218-125">Accept</span></span>|<span data-ttu-id="a7218-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a7218-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a7218-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a7218-127">Request body</span></span>
<span data-ttu-id="a7218-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto notificationMessageTemplate.</span><span class="sxs-lookup"><span data-stu-id="a7218-128">In the request body, supply a JSON representation for the notificationMessageTemplate object.</span></span>

<span data-ttu-id="a7218-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto notificationMessageTemplate.</span><span class="sxs-lookup"><span data-stu-id="a7218-129">The following table shows the properties that are required when you create the notificationMessageTemplate.</span></span>

|<span data-ttu-id="a7218-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a7218-130">Property</span></span>|<span data-ttu-id="a7218-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="a7218-131">Type</span></span>|<span data-ttu-id="a7218-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7218-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a7218-133">id</span><span class="sxs-lookup"><span data-stu-id="a7218-133">id</span></span>|<span data-ttu-id="a7218-134">String</span><span class="sxs-lookup"><span data-stu-id="a7218-134">String</span></span>|<span data-ttu-id="a7218-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a7218-135">Key of the entity.</span></span>|
|<span data-ttu-id="a7218-136">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="a7218-136">lastModifiedDateTime</span></span>|<span data-ttu-id="a7218-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a7218-137">DateTimeOffset</span></span>|<span data-ttu-id="a7218-138">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="a7218-138">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="a7218-139">displayName</span><span class="sxs-lookup"><span data-stu-id="a7218-139">displayName</span></span>|<span data-ttu-id="a7218-140">String</span><span class="sxs-lookup"><span data-stu-id="a7218-140">String</span></span>|<span data-ttu-id="a7218-141">Nombre para mostrar de la plantilla de mensajes de notificación.</span><span class="sxs-lookup"><span data-stu-id="a7218-141">Display name for the Notification Message Template.</span></span>|
|<span data-ttu-id="a7218-142">defaultLocale</span><span class="sxs-lookup"><span data-stu-id="a7218-142">defaultLocale</span></span>|<span data-ttu-id="a7218-143">String</span><span class="sxs-lookup"><span data-stu-id="a7218-143">String</span></span>|<span data-ttu-id="a7218-144">La configuración regional predeterminada de reserva para los casos en que la configuración regional solicitada no está disponible.</span><span class="sxs-lookup"><span data-stu-id="a7218-144">The default locale to fallback onto when the requested locale is not available.</span></span>|
|<span data-ttu-id="a7218-145">brandingOptions</span><span class="sxs-lookup"><span data-stu-id="a7218-145">brandingOptions</span></span>|[<span data-ttu-id="a7218-146">notificationTemplateBrandingOptions</span><span class="sxs-lookup"><span data-stu-id="a7218-146">notificationTemplateBrandingOptions</span></span>](../resources/intune-notification-notificationtemplatebrandingoptions.md)|<span data-ttu-id="a7218-147">Las opciones de personalización de marca de la plantilla de mensaje.</span><span class="sxs-lookup"><span data-stu-id="a7218-147">The Message Template Branding Options.</span></span> <span data-ttu-id="a7218-148">La personalización de marca está definida en la consola de administración de Intune.</span><span class="sxs-lookup"><span data-stu-id="a7218-148">Branding is defined in the Intune Admin Console.</span></span> <span data-ttu-id="a7218-149">Los valores posibles son: `none`, `includeCompanyLogo`, `includeCompanyName` y `includeContactInformation`.</span><span class="sxs-lookup"><span data-stu-id="a7218-149">Possible values are: `none`, `includeCompanyLogo`, `includeCompanyName`, `includeContactInformation`.</span></span>|
|<span data-ttu-id="a7218-150">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="a7218-150">roleScopeTagIds</span></span>|<span data-ttu-id="a7218-151">Colección String</span><span class="sxs-lookup"><span data-stu-id="a7218-151">String collection</span></span>|<span data-ttu-id="a7218-152">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="a7218-152">List of Scope Tags for this Entity instance.</span></span>|



## <a name="response"></a><span data-ttu-id="a7218-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a7218-153">Response</span></span>
<span data-ttu-id="a7218-154">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a7218-154">If successful, this method returns a `201 Created` response code and a [notificationMessageTemplate](../resources/intune-notification-notificationmessagetemplate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a7218-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a7218-155">Example</span></span>
### <a name="request"></a><span data-ttu-id="a7218-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a7218-156">Request</span></span>
<span data-ttu-id="a7218-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a7218-157">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/notificationMessageTemplates
Content-type: application/json
Content-length: 323

{
  "@odata.type": "#microsoft.graph.notificationMessageTemplate",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "defaultLocale": "Default Locale value",
  "brandingOptions": "includeCompanyLogo",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ]
}
```

### <a name="response"></a><span data-ttu-id="a7218-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a7218-158">Response</span></span>
<span data-ttu-id="a7218-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a7218-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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





