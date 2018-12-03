---
title: Crear iosStoreApp
description: Cree un objeto iosStoreApp.
ms.openlocfilehash: 7dbf1dd5ff0318d054d99bc4f7ae9a8fcfce8523
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031055"
---
# <a name="create-iosstoreapp"></a><span data-ttu-id="e7fe6-103">Crear iosStoreApp</span><span class="sxs-lookup"><span data-stu-id="e7fe6-103">Create iosStoreApp</span></span>

> <span data-ttu-id="e7fe6-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e7fe6-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e7fe6-105">Cree un objeto [iosStoreApp](../resources/intune-apps-iosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="e7fe6-105">Create a new [iosStoreApp](../resources/intune-apps-iosstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e7fe6-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e7fe6-106">Prerequisites</span></span>
<span data-ttu-id="e7fe6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e7fe6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e7fe6-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e7fe6-109">Permission type</span></span>|<span data-ttu-id="e7fe6-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e7fe6-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e7fe6-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e7fe6-111">Delegated (work or school account)</span></span>|<span data-ttu-id="e7fe6-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e7fe6-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="e7fe6-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e7fe6-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e7fe6-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e7fe6-114">Not supported.</span></span>|
|<span data-ttu-id="e7fe6-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e7fe6-115">Application</span></span>|<span data-ttu-id="e7fe6-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e7fe6-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e7fe6-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e7fe6-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="e7fe6-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e7fe6-118">Request headers</span></span>
|<span data-ttu-id="e7fe6-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7fe6-119">Header</span></span>|<span data-ttu-id="e7fe6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e7fe6-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e7fe6-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="e7fe6-121">Authorization</span></span>|<span data-ttu-id="e7fe6-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e7fe6-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e7fe6-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e7fe6-123">Accept</span></span>|<span data-ttu-id="e7fe6-124">application/json</span><span class="sxs-lookup"><span data-stu-id="e7fe6-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e7fe6-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e7fe6-125">Request body</span></span>
<span data-ttu-id="e7fe6-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosStoreApp.</span><span class="sxs-lookup"><span data-stu-id="e7fe6-126">In the request body, supply a JSON representation for the iosStoreApp object.</span></span>

<span data-ttu-id="e7fe6-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosStoreApp.</span><span class="sxs-lookup"><span data-stu-id="e7fe6-127">The following table shows the properties that are required when you create the iosStoreApp.</span></span>

|<span data-ttu-id="e7fe6-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e7fe6-128">Property</span></span>|<span data-ttu-id="e7fe6-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="e7fe6-129">Type</span></span>|<span data-ttu-id="e7fe6-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7fe6-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e7fe6-131">id</span><span class="sxs-lookup"><span data-stu-id="e7fe6-131">id</span></span>|<span data-ttu-id="e7fe6-132">String</span><span class="sxs-lookup"><span data-stu-id="e7fe6-132">String</span></span>|<span data-ttu-id="e7fe6-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="e7fe6-133">Key of the entity.</span></span> <span data-ttu-id="e7fe6-134">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e7fe6-134">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e7fe6-135">displayName</span><span class="sxs-lookup"><span data-stu-id="e7fe6-135">displayName</span></span>|<span data-ttu-id="e7fe6-136">String</span><span class="sxs-lookup"><span data-stu-id="e7fe6-136">String</span></span>|<span data-ttu-id="e7fe6-137">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="e7fe6-137">The admin provided or imported title of the app.</span></span> <span data-ttu-id="e7fe6-138">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e7fe6-138">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e7fe6-139">descripción</span><span class="sxs-lookup"><span data-stu-id="e7fe6-139">description</span></span>|<span data-ttu-id="e7fe6-140">String</span><span class="sxs-lookup"><span data-stu-id="e7fe6-140">String</span></span>|<span data-ttu-id="e7fe6-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e7fe6-141">The description of the app.</span></span> <span data-ttu-id="e7fe6-142">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e7fe6-142">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e7fe6-143">publicador</span><span class="sxs-lookup"><span data-stu-id="e7fe6-143">publisher</span></span>|<span data-ttu-id="e7fe6-144">String</span><span class="sxs-lookup"><span data-stu-id="e7fe6-144">String</span></span>|<span data-ttu-id="e7fe6-145">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e7fe6-145">The publisher of the app.</span></span> <span data-ttu-id="e7fe6-146">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e7fe6-146">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e7fe6-147">largeIcon</span><span class="sxs-lookup"><span data-stu-id="e7fe6-147">largeIcon</span></span>|[<span data-ttu-id="e7fe6-148">mimeContent</span><span class="sxs-lookup"><span data-stu-id="e7fe6-148">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="e7fe6-149">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="e7fe6-149">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="e7fe6-150">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e7fe6-150">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e7fe6-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="e7fe6-151">createdDateTime</span></span>|<span data-ttu-id="e7fe6-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e7fe6-152">DateTimeOffset</span></span>|<span data-ttu-id="e7fe6-153">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e7fe6-153">The date and time the app was created.</span></span> <span data-ttu-id="e7fe6-154">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e7fe6-154">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e7fe6-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="e7fe6-155">lastModifiedDateTime</span></span>|<span data-ttu-id="e7fe6-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e7fe6-156">DateTimeOffset</span></span>|<span data-ttu-id="e7fe6-157">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e7fe6-157">The date and time the app was last modified.</span></span> <span data-ttu-id="e7fe6-158">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e7fe6-158">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e7fe6-159">isFeatured</span><span class="sxs-lookup"><span data-stu-id="e7fe6-159">isFeatured</span></span>|<span data-ttu-id="e7fe6-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="e7fe6-160">Boolean</span></span>|<span data-ttu-id="e7fe6-161">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e7fe6-161">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e7fe6-162">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="e7fe6-162">privacyInformationUrl</span></span>|<span data-ttu-id="e7fe6-163">String</span><span class="sxs-lookup"><span data-stu-id="e7fe6-163">String</span></span>|<span data-ttu-id="e7fe6-164">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="e7fe6-164">The privacy statement Url.</span></span> <span data-ttu-id="e7fe6-165">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e7fe6-165">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e7fe6-166">informationUrl</span><span class="sxs-lookup"><span data-stu-id="e7fe6-166">informationUrl</span></span>|<span data-ttu-id="e7fe6-167">String</span><span class="sxs-lookup"><span data-stu-id="e7fe6-167">String</span></span>|<span data-ttu-id="e7fe6-168">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="e7fe6-168">The more information Url.</span></span> <span data-ttu-id="e7fe6-169">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e7fe6-169">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e7fe6-170">owner</span><span class="sxs-lookup"><span data-stu-id="e7fe6-170">owner</span></span>|<span data-ttu-id="e7fe6-171">String</span><span class="sxs-lookup"><span data-stu-id="e7fe6-171">String</span></span>|<span data-ttu-id="e7fe6-172">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e7fe6-172">The owner of the app.</span></span> <span data-ttu-id="e7fe6-173">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e7fe6-173">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e7fe6-174">developer</span><span class="sxs-lookup"><span data-stu-id="e7fe6-174">developer</span></span>|<span data-ttu-id="e7fe6-175">String</span><span class="sxs-lookup"><span data-stu-id="e7fe6-175">String</span></span>|<span data-ttu-id="e7fe6-176">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e7fe6-176">The developer of the app.</span></span> <span data-ttu-id="e7fe6-177">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e7fe6-177">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e7fe6-178">notas</span><span class="sxs-lookup"><span data-stu-id="e7fe6-178">notes</span></span>|<span data-ttu-id="e7fe6-179">String</span><span class="sxs-lookup"><span data-stu-id="e7fe6-179">String</span></span>|<span data-ttu-id="e7fe6-180">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e7fe6-180">Notes for the app.</span></span> <span data-ttu-id="e7fe6-181">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e7fe6-181">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e7fe6-182">publishingState</span><span class="sxs-lookup"><span data-stu-id="e7fe6-182">publishingState</span></span>|[<span data-ttu-id="e7fe6-183">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="e7fe6-183">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="e7fe6-184">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e7fe6-184">The publishing state for the app.</span></span> <span data-ttu-id="e7fe6-185">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="e7fe6-185">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="e7fe6-186">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e7fe6-186">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="e7fe6-187">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="e7fe6-187">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="e7fe6-188">bundleId</span><span class="sxs-lookup"><span data-stu-id="e7fe6-188">bundleId</span></span>|<span data-ttu-id="e7fe6-189">String</span><span class="sxs-lookup"><span data-stu-id="e7fe6-189">String</span></span>|<span data-ttu-id="e7fe6-190">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="e7fe6-190">The Identity Name.</span></span>|
|<span data-ttu-id="e7fe6-191">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="e7fe6-191">appStoreUrl</span></span>|<span data-ttu-id="e7fe6-192">String</span><span class="sxs-lookup"><span data-stu-id="e7fe6-192">String</span></span>|<span data-ttu-id="e7fe6-193">Dirección URL de la App Store de Apple</span><span class="sxs-lookup"><span data-stu-id="e7fe6-193">The Apple App Store URL</span></span>|
|<span data-ttu-id="e7fe6-194">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="e7fe6-194">applicableDeviceType</span></span>|[<span data-ttu-id="e7fe6-195">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="e7fe6-195">iosDeviceType</span></span>](../resources/intune-apps-iosdevicetype.md)|<span data-ttu-id="e7fe6-196">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="e7fe6-196">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="e7fe6-197">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="e7fe6-197">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="e7fe6-198">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="e7fe6-198">iosMinimumOperatingSystem</span></span>](../resources/intune-apps-iosminimumoperatingsystem.md)|<span data-ttu-id="e7fe6-199">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="e7fe6-199">The value for the minimum applicable operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="e7fe6-200">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e7fe6-200">Response</span></span>
<span data-ttu-id="e7fe6-201">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosStoreApp](../resources/intune-apps-iosstoreapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e7fe6-201">If successful, this method returns a `201 Created` response code and a [iosStoreApp](../resources/intune-apps-iosstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e7fe6-202">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e7fe6-202">Example</span></span>
### <a name="request"></a><span data-ttu-id="e7fe6-203">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e7fe6-203">Request</span></span>
<span data-ttu-id="e7fe6-204">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e7fe6-204">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 1006

{
  "@odata.type": "#microsoft.graph.iosStoreApp",
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "isFeatured": true,
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "informationUrl": "https://example.com/informationUrl/",
  "owner": "Owner value",
  "developer": "Developer value",
  "notes": "Notes value",
  "publishingState": "processing",
  "bundleId": "Bundle Id value",
  "appStoreUrl": "https://example.com/appStoreUrl/",
  "applicableDeviceType": {
    "@odata.type": "microsoft.graph.iosDeviceType",
    "iPad": true,
    "iPhoneAndIPod": true
  },
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.iosMinimumOperatingSystem",
    "v8_0": true,
    "v9_0": true,
    "v10_0": true,
    "v11_0": true,
    "v12_0": true
  }
}
```

### <a name="response"></a><span data-ttu-id="e7fe6-205">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e7fe6-205">Response</span></span>
<span data-ttu-id="e7fe6-p115">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e7fe6-p115">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1178

{
  "@odata.type": "#microsoft.graph.iosStoreApp",
  "id": "a04adbe2-dbe2-a04a-e2db-4aa0e2db4aa0",
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
  "publishingState": "processing",
  "bundleId": "Bundle Id value",
  "appStoreUrl": "https://example.com/appStoreUrl/",
  "applicableDeviceType": {
    "@odata.type": "microsoft.graph.iosDeviceType",
    "iPad": true,
    "iPhoneAndIPod": true
  },
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.iosMinimumOperatingSystem",
    "v8_0": true,
    "v9_0": true,
    "v10_0": true,
    "v11_0": true,
    "v12_0": true
  }
}
```



