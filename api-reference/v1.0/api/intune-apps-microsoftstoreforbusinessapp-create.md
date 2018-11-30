---
title: Crear microsoftStoreForBusinessApp
description: Crear un objeto microsoftStoreForBusinessApp.
ms.openlocfilehash: 478bf95892628b4b3bc0195804a48c9d9cf415e2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029547"
---
# <a name="create-microsoftstoreforbusinessapp"></a><span data-ttu-id="1071c-103">Crear microsoftStoreForBusinessApp</span><span class="sxs-lookup"><span data-stu-id="1071c-103">Create microsoftStoreForBusinessApp</span></span>

> <span data-ttu-id="1071c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1071c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1071c-105">Crear un objeto [microsoftStoreForBusinessApp](../resources/intune-apps-microsoftstoreforbusinessapp.md).</span><span class="sxs-lookup"><span data-stu-id="1071c-105">Create a new [microsoftStoreForBusinessApp](../resources/intune-apps-microsoftstoreforbusinessapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1071c-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1071c-106">Prerequisites</span></span>
<span data-ttu-id="1071c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1071c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1071c-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1071c-109">Permission type</span></span>|<span data-ttu-id="1071c-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1071c-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1071c-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1071c-111">Delegated (work or school account)</span></span>|<span data-ttu-id="1071c-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1071c-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="1071c-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1071c-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1071c-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1071c-114">Not supported.</span></span>|
|<span data-ttu-id="1071c-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1071c-115">Application</span></span>|<span data-ttu-id="1071c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1071c-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1071c-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1071c-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="1071c-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1071c-118">Request headers</span></span>
|<span data-ttu-id="1071c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1071c-119">Header</span></span>|<span data-ttu-id="1071c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1071c-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1071c-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="1071c-121">Authorization</span></span>|<span data-ttu-id="1071c-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1071c-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1071c-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1071c-123">Accept</span></span>|<span data-ttu-id="1071c-124">application/json</span><span class="sxs-lookup"><span data-stu-id="1071c-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1071c-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1071c-125">Request body</span></span>
<span data-ttu-id="1071c-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto microsoftStoreForBusinessApp.</span><span class="sxs-lookup"><span data-stu-id="1071c-126">In the request body, supply a JSON representation for the microsoftStoreForBusinessApp object.</span></span>

<span data-ttu-id="1071c-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto microsoftStoreForBusinessApp.</span><span class="sxs-lookup"><span data-stu-id="1071c-127">The following table shows the properties that are required when you create the microsoftStoreForBusinessApp.</span></span>

|<span data-ttu-id="1071c-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1071c-128">Property</span></span>|<span data-ttu-id="1071c-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="1071c-129">Type</span></span>|<span data-ttu-id="1071c-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="1071c-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1071c-131">id</span><span class="sxs-lookup"><span data-stu-id="1071c-131">id</span></span>|<span data-ttu-id="1071c-132">String</span><span class="sxs-lookup"><span data-stu-id="1071c-132">String</span></span>|<span data-ttu-id="1071c-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="1071c-133">Key of the entity.</span></span> <span data-ttu-id="1071c-134">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1071c-134">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="1071c-135">displayName</span><span class="sxs-lookup"><span data-stu-id="1071c-135">displayName</span></span>|<span data-ttu-id="1071c-136">String</span><span class="sxs-lookup"><span data-stu-id="1071c-136">String</span></span>|<span data-ttu-id="1071c-137">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="1071c-137">The admin provided or imported title of the app.</span></span> <span data-ttu-id="1071c-138">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1071c-138">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="1071c-139">descripción</span><span class="sxs-lookup"><span data-stu-id="1071c-139">description</span></span>|<span data-ttu-id="1071c-140">String</span><span class="sxs-lookup"><span data-stu-id="1071c-140">String</span></span>|<span data-ttu-id="1071c-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1071c-141">The description of the app.</span></span> <span data-ttu-id="1071c-142">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1071c-142">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="1071c-143">publicador</span><span class="sxs-lookup"><span data-stu-id="1071c-143">publisher</span></span>|<span data-ttu-id="1071c-144">String</span><span class="sxs-lookup"><span data-stu-id="1071c-144">String</span></span>|<span data-ttu-id="1071c-145">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1071c-145">The publisher of the app.</span></span> <span data-ttu-id="1071c-146">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1071c-146">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="1071c-147">largeIcon</span><span class="sxs-lookup"><span data-stu-id="1071c-147">largeIcon</span></span>|[<span data-ttu-id="1071c-148">mimeContent</span><span class="sxs-lookup"><span data-stu-id="1071c-148">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="1071c-149">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="1071c-149">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="1071c-150">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1071c-150">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="1071c-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="1071c-151">createdDateTime</span></span>|<span data-ttu-id="1071c-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1071c-152">DateTimeOffset</span></span>|<span data-ttu-id="1071c-153">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1071c-153">The date and time the app was created.</span></span> <span data-ttu-id="1071c-154">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1071c-154">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="1071c-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="1071c-155">lastModifiedDateTime</span></span>|<span data-ttu-id="1071c-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1071c-156">DateTimeOffset</span></span>|<span data-ttu-id="1071c-157">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1071c-157">The date and time the app was last modified.</span></span> <span data-ttu-id="1071c-158">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1071c-158">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="1071c-159">isFeatured</span><span class="sxs-lookup"><span data-stu-id="1071c-159">isFeatured</span></span>|<span data-ttu-id="1071c-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="1071c-160">Boolean</span></span>|<span data-ttu-id="1071c-161">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1071c-161">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="1071c-162">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="1071c-162">privacyInformationUrl</span></span>|<span data-ttu-id="1071c-163">String</span><span class="sxs-lookup"><span data-stu-id="1071c-163">String</span></span>|<span data-ttu-id="1071c-164">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="1071c-164">The privacy statement Url.</span></span> <span data-ttu-id="1071c-165">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1071c-165">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="1071c-166">informationUrl</span><span class="sxs-lookup"><span data-stu-id="1071c-166">informationUrl</span></span>|<span data-ttu-id="1071c-167">String</span><span class="sxs-lookup"><span data-stu-id="1071c-167">String</span></span>|<span data-ttu-id="1071c-168">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="1071c-168">The more information Url.</span></span> <span data-ttu-id="1071c-169">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1071c-169">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="1071c-170">owner</span><span class="sxs-lookup"><span data-stu-id="1071c-170">owner</span></span>|<span data-ttu-id="1071c-171">String</span><span class="sxs-lookup"><span data-stu-id="1071c-171">String</span></span>|<span data-ttu-id="1071c-172">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1071c-172">The owner of the app.</span></span> <span data-ttu-id="1071c-173">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1071c-173">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="1071c-174">developer</span><span class="sxs-lookup"><span data-stu-id="1071c-174">developer</span></span>|<span data-ttu-id="1071c-175">String</span><span class="sxs-lookup"><span data-stu-id="1071c-175">String</span></span>|<span data-ttu-id="1071c-176">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1071c-176">The developer of the app.</span></span> <span data-ttu-id="1071c-177">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1071c-177">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="1071c-178">notas</span><span class="sxs-lookup"><span data-stu-id="1071c-178">notes</span></span>|<span data-ttu-id="1071c-179">String</span><span class="sxs-lookup"><span data-stu-id="1071c-179">String</span></span>|<span data-ttu-id="1071c-180">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1071c-180">Notes for the app.</span></span> <span data-ttu-id="1071c-181">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1071c-181">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="1071c-182">publishingState</span><span class="sxs-lookup"><span data-stu-id="1071c-182">publishingState</span></span>|[<span data-ttu-id="1071c-183">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="1071c-183">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="1071c-184">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1071c-184">The publishing state for the app.</span></span> <span data-ttu-id="1071c-185">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="1071c-185">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="1071c-186">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="1071c-186">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="1071c-187">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="1071c-187">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="1071c-188">usedLicenseCount</span><span class="sxs-lookup"><span data-stu-id="1071c-188">usedLicenseCount</span></span>|<span data-ttu-id="1071c-189">Int32</span><span class="sxs-lookup"><span data-stu-id="1071c-189">Int32</span></span>|<span data-ttu-id="1071c-190">Número de licencias de Microsoft Store para Empresas en uso.</span><span class="sxs-lookup"><span data-stu-id="1071c-190">The number of Microsoft Store for Business licenses in use.</span></span>|
|<span data-ttu-id="1071c-191">totalLicenseCount</span><span class="sxs-lookup"><span data-stu-id="1071c-191">totalLicenseCount</span></span>|<span data-ttu-id="1071c-192">Int32</span><span class="sxs-lookup"><span data-stu-id="1071c-192">Int32</span></span>|<span data-ttu-id="1071c-193">Número total de licencias de Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="1071c-193">The total number of Microsoft Store for Business licenses.</span></span>|
|<span data-ttu-id="1071c-194">productKey</span><span class="sxs-lookup"><span data-stu-id="1071c-194">productKey</span></span>|<span data-ttu-id="1071c-195">String</span><span class="sxs-lookup"><span data-stu-id="1071c-195">String</span></span>|<span data-ttu-id="1071c-196">Clave de producto de la aplicación</span><span class="sxs-lookup"><span data-stu-id="1071c-196">The app product key</span></span>|
|<span data-ttu-id="1071c-197">licenseType</span><span class="sxs-lookup"><span data-stu-id="1071c-197">licenseType</span></span>|[<span data-ttu-id="1071c-198">microsoftStoreForBusinessLicenseType</span><span class="sxs-lookup"><span data-stu-id="1071c-198">microsoftStoreForBusinessLicenseType</span></span>](../resources/intune-apps-microsoftstoreforbusinesslicensetype.md)|<span data-ttu-id="1071c-199">El tipo de licencia de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1071c-199">The app license type.</span></span> <span data-ttu-id="1071c-200">Los valores posibles son: `offline` y `online`.</span><span class="sxs-lookup"><span data-stu-id="1071c-200">Possible values are: `offline`, `online`.</span></span>|
|<span data-ttu-id="1071c-201">packageIdentityName</span><span class="sxs-lookup"><span data-stu-id="1071c-201">packageIdentityName</span></span>|<span data-ttu-id="1071c-202">String</span><span class="sxs-lookup"><span data-stu-id="1071c-202">String</span></span>|<span data-ttu-id="1071c-203">Identificador del paquete de aplicación.</span><span class="sxs-lookup"><span data-stu-id="1071c-203">The app package identifier</span></span>|



## <a name="response"></a><span data-ttu-id="1071c-204">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1071c-204">Response</span></span>
<span data-ttu-id="1071c-205">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [microsoftStoreForBusinessApp](../resources/intune-apps-microsoftstoreforbusinessapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1071c-205">If successful, this method returns a `201 Created` response code and a [microsoftStoreForBusinessApp](../resources/intune-apps-microsoftstoreforbusinessapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1071c-206">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1071c-206">Example</span></span>
### <a name="request"></a><span data-ttu-id="1071c-207">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1071c-207">Request</span></span>
<span data-ttu-id="1071c-208">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1071c-208">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 769

{
  "@odata.type": "#microsoft.graph.microsoftStoreForBusinessApp",
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
  "usedLicenseCount": 0,
  "totalLicenseCount": 1,
  "productKey": "Product Key value",
  "licenseType": "online",
  "packageIdentityName": "Package Identity Name value"
}
```

### <a name="response"></a><span data-ttu-id="1071c-209">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1071c-209">Response</span></span>
<span data-ttu-id="1071c-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1071c-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 941

{
  "@odata.type": "#microsoft.graph.microsoftStoreForBusinessApp",
  "id": "f33358bc-58bc-f333-bc58-33f3bc5833f3",
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
  "usedLicenseCount": 0,
  "totalLicenseCount": 1,
  "productKey": "Product Key value",
  "licenseType": "online",
  "packageIdentityName": "Package Identity Name value"
}
```



