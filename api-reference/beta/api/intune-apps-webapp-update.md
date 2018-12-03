---
title: Actualizar webApp
description: Actualice las propiedades de un objeto webApp.
ms.openlocfilehash: cdd5269257a52e3aa4c378743771dfd482ac224e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089608"
---
# <a name="update-webapp"></a><span data-ttu-id="80738-103">Actualizar webApp</span><span class="sxs-lookup"><span data-stu-id="80738-103">Update webApp</span></span>

> <span data-ttu-id="80738-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="80738-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="80738-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="80738-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="80738-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="80738-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="80738-107">Actualice las propiedades de un objeto [webApp](../resources/intune-apps-webapp.md).</span><span class="sxs-lookup"><span data-stu-id="80738-107">Update the properties of a [webApp](../resources/intune-apps-webapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="80738-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="80738-108">Prerequisites</span></span>
<span data-ttu-id="80738-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="80738-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="80738-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="80738-111">Permission type</span></span>|<span data-ttu-id="80738-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="80738-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="80738-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="80738-113">Delegated (work or school account)</span></span>|<span data-ttu-id="80738-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="80738-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="80738-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="80738-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="80738-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="80738-116">Not supported.</span></span>|
|<span data-ttu-id="80738-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="80738-117">Application</span></span>|<span data-ttu-id="80738-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="80738-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="80738-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="80738-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="request-headers"></a><span data-ttu-id="80738-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="80738-120">Request headers</span></span>
|<span data-ttu-id="80738-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="80738-121">Header</span></span>|<span data-ttu-id="80738-122">Valor</span><span class="sxs-lookup"><span data-stu-id="80738-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="80738-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="80738-123">Authorization</span></span>|<span data-ttu-id="80738-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="80738-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="80738-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="80738-125">Accept</span></span>|<span data-ttu-id="80738-126">application/json</span><span class="sxs-lookup"><span data-stu-id="80738-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="80738-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="80738-127">Request body</span></span>
<span data-ttu-id="80738-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [webApp](../resources/intune-apps-webapp.md).</span><span class="sxs-lookup"><span data-stu-id="80738-128">In the request body, supply a JSON representation for the [webApp](../resources/intune-apps-webapp.md) object.</span></span>

<span data-ttu-id="80738-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [webApp](../resources/intune-apps-webapp.md).</span><span class="sxs-lookup"><span data-stu-id="80738-129">The following table shows the properties that are required when you create the [webApp](../resources/intune-apps-webapp.md).</span></span>

|<span data-ttu-id="80738-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="80738-130">Property</span></span>|<span data-ttu-id="80738-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="80738-131">Type</span></span>|<span data-ttu-id="80738-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="80738-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="80738-133">id</span><span class="sxs-lookup"><span data-stu-id="80738-133">id</span></span>|<span data-ttu-id="80738-134">String</span><span class="sxs-lookup"><span data-stu-id="80738-134">String</span></span>|<span data-ttu-id="80738-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="80738-135">Key of the entity.</span></span> <span data-ttu-id="80738-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="80738-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="80738-137">displayName</span><span class="sxs-lookup"><span data-stu-id="80738-137">displayName</span></span>|<span data-ttu-id="80738-138">String</span><span class="sxs-lookup"><span data-stu-id="80738-138">String</span></span>|<span data-ttu-id="80738-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="80738-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="80738-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="80738-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="80738-141">descripción</span><span class="sxs-lookup"><span data-stu-id="80738-141">description</span></span>|<span data-ttu-id="80738-142">String</span><span class="sxs-lookup"><span data-stu-id="80738-142">String</span></span>|<span data-ttu-id="80738-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="80738-143">The description of the app.</span></span> <span data-ttu-id="80738-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="80738-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="80738-145">publicador</span><span class="sxs-lookup"><span data-stu-id="80738-145">publisher</span></span>|<span data-ttu-id="80738-146">String</span><span class="sxs-lookup"><span data-stu-id="80738-146">String</span></span>|<span data-ttu-id="80738-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="80738-147">The publisher of the app.</span></span> <span data-ttu-id="80738-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="80738-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="80738-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="80738-149">largeIcon</span></span>|[<span data-ttu-id="80738-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="80738-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="80738-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="80738-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="80738-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="80738-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="80738-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="80738-153">createdDateTime</span></span>|<span data-ttu-id="80738-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="80738-154">DateTimeOffset</span></span>|<span data-ttu-id="80738-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="80738-155">The date and time the app was created.</span></span> <span data-ttu-id="80738-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="80738-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="80738-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="80738-157">lastModifiedDateTime</span></span>|<span data-ttu-id="80738-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="80738-158">DateTimeOffset</span></span>|<span data-ttu-id="80738-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="80738-159">The date and time the app was last modified.</span></span> <span data-ttu-id="80738-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="80738-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="80738-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="80738-161">isFeatured</span></span>|<span data-ttu-id="80738-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="80738-162">Boolean</span></span>|<span data-ttu-id="80738-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="80738-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="80738-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="80738-164">privacyInformationUrl</span></span>|<span data-ttu-id="80738-165">String</span><span class="sxs-lookup"><span data-stu-id="80738-165">String</span></span>|<span data-ttu-id="80738-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="80738-166">The privacy statement Url.</span></span> <span data-ttu-id="80738-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="80738-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="80738-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="80738-168">informationUrl</span></span>|<span data-ttu-id="80738-169">String</span><span class="sxs-lookup"><span data-stu-id="80738-169">String</span></span>|<span data-ttu-id="80738-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="80738-170">The more information Url.</span></span> <span data-ttu-id="80738-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="80738-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="80738-172">owner</span><span class="sxs-lookup"><span data-stu-id="80738-172">owner</span></span>|<span data-ttu-id="80738-173">String</span><span class="sxs-lookup"><span data-stu-id="80738-173">String</span></span>|<span data-ttu-id="80738-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="80738-174">The owner of the app.</span></span> <span data-ttu-id="80738-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="80738-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="80738-176">developer</span><span class="sxs-lookup"><span data-stu-id="80738-176">developer</span></span>|<span data-ttu-id="80738-177">String</span><span class="sxs-lookup"><span data-stu-id="80738-177">String</span></span>|<span data-ttu-id="80738-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="80738-178">The developer of the app.</span></span> <span data-ttu-id="80738-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="80738-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="80738-180">notas</span><span class="sxs-lookup"><span data-stu-id="80738-180">notes</span></span>|<span data-ttu-id="80738-181">String</span><span class="sxs-lookup"><span data-stu-id="80738-181">String</span></span>|<span data-ttu-id="80738-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="80738-182">Notes for the app.</span></span> <span data-ttu-id="80738-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="80738-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="80738-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="80738-184">uploadState</span></span>|<span data-ttu-id="80738-185">Int32</span><span class="sxs-lookup"><span data-stu-id="80738-185">Int32</span></span>|<span data-ttu-id="80738-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="80738-186">The upload state.</span></span> <span data-ttu-id="80738-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="80738-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="80738-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="80738-188">publishingState</span></span>|[<span data-ttu-id="80738-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="80738-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="80738-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="80738-190">The publishing state for the app.</span></span> <span data-ttu-id="80738-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="80738-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="80738-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="80738-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="80738-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="80738-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="80738-194">appUrl</span><span class="sxs-lookup"><span data-stu-id="80738-194">appUrl</span></span>|<span data-ttu-id="80738-195">String</span><span class="sxs-lookup"><span data-stu-id="80738-195">String</span></span>|<span data-ttu-id="80738-196">Dirección URL de la aplicación web.</span><span class="sxs-lookup"><span data-stu-id="80738-196">The web app URL.</span></span>|
|<span data-ttu-id="80738-197">useManagedBrowser</span><span class="sxs-lookup"><span data-stu-id="80738-197">useManagedBrowser</span></span>|<span data-ttu-id="80738-198">Booleano</span><span class="sxs-lookup"><span data-stu-id="80738-198">Boolean</span></span>|<span data-ttu-id="80738-199">Indica si se va a usar el explorador administrado.</span><span class="sxs-lookup"><span data-stu-id="80738-199">Whether or not to use managed browser.</span></span> <span data-ttu-id="80738-200">Esta propiedad solo es aplicable a iOS y Android.</span><span class="sxs-lookup"><span data-stu-id="80738-200">This property is only applicable for Android and IOS.</span></span>|



## <a name="response"></a><span data-ttu-id="80738-201">Respuesta</span><span class="sxs-lookup"><span data-stu-id="80738-201">Response</span></span>
<span data-ttu-id="80738-202">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [webApp](../resources/intune-apps-webapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="80738-202">If successful, this method returns a `200 OK` response code and an updated [webApp](../resources/intune-apps-webapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="80738-203">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="80738-203">Example</span></span>
### <a name="request"></a><span data-ttu-id="80738-204">Solicitud</span><span class="sxs-lookup"><span data-stu-id="80738-204">Request</span></span>
<span data-ttu-id="80738-205">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="80738-205">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 686

{
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "isFeatured": true,
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "informationUrl": "https://example.com/informationUrl/",
  "owner": "Owner value",
  "developer": "Developer value",
  "notes": "Notes value",
  "uploadState": 11,
  "publishingState": "processing",
  "appUrl": "https://example.com/appUrl/",
  "useManagedBrowser": true
}
```

### <a name="response"></a><span data-ttu-id="80738-206">Respuesta</span><span class="sxs-lookup"><span data-stu-id="80738-206">Response</span></span>
<span data-ttu-id="80738-p118">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="80738-p118">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 839

{
  "@odata.type": "#microsoft.graph.webApp",
  "id": "4bdc5d30-5d30-4bdc-305d-dc4b305ddc4b",
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "isFeatured": true,
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "informationUrl": "https://example.com/informationUrl/",
  "owner": "Owner value",
  "developer": "Developer value",
  "notes": "Notes value",
  "uploadState": 11,
  "publishingState": "processing",
  "appUrl": "https://example.com/appUrl/",
  "useManagedBrowser": true
}
```





