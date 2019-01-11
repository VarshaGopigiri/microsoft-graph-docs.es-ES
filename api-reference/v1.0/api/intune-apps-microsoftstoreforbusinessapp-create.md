---
title: Crear microsoftStoreForBusinessApp
description: Crear un objeto microsoftStoreForBusinessApp.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: eff4f4e03c69d866c879aec746c9b4e47d3dbe93
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27840484"
---
# <a name="create-microsoftstoreforbusinessapp"></a><span data-ttu-id="690de-103">Crear microsoftStoreForBusinessApp</span><span class="sxs-lookup"><span data-stu-id="690de-103">Create microsoftStoreForBusinessApp</span></span>

> <span data-ttu-id="690de-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="690de-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="690de-105">Crear un objeto [microsoftStoreForBusinessApp](../resources/intune-apps-microsoftstoreforbusinessapp.md).</span><span class="sxs-lookup"><span data-stu-id="690de-105">Create a new [microsoftStoreForBusinessApp](../resources/intune-apps-microsoftstoreforbusinessapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="690de-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="690de-106">Prerequisites</span></span>
<span data-ttu-id="690de-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="690de-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="690de-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="690de-109">Permission type</span></span>|<span data-ttu-id="690de-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="690de-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="690de-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="690de-111">Delegated (work or school account)</span></span>|<span data-ttu-id="690de-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="690de-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="690de-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="690de-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="690de-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="690de-114">Not supported.</span></span>|
|<span data-ttu-id="690de-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="690de-115">Application</span></span>|<span data-ttu-id="690de-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="690de-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="690de-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="690de-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="690de-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="690de-118">Request headers</span></span>
|<span data-ttu-id="690de-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="690de-119">Header</span></span>|<span data-ttu-id="690de-120">Valor</span><span class="sxs-lookup"><span data-stu-id="690de-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="690de-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="690de-121">Authorization</span></span>|<span data-ttu-id="690de-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="690de-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="690de-123">Accept</span><span class="sxs-lookup"><span data-stu-id="690de-123">Accept</span></span>|<span data-ttu-id="690de-124">application/json</span><span class="sxs-lookup"><span data-stu-id="690de-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="690de-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="690de-125">Request body</span></span>
<span data-ttu-id="690de-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto microsoftStoreForBusinessApp.</span><span class="sxs-lookup"><span data-stu-id="690de-126">In the request body, supply a JSON representation for the microsoftStoreForBusinessApp object.</span></span>

<span data-ttu-id="690de-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto microsoftStoreForBusinessApp.</span><span class="sxs-lookup"><span data-stu-id="690de-127">The following table shows the properties that are required when you create the microsoftStoreForBusinessApp.</span></span>

|<span data-ttu-id="690de-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="690de-128">Property</span></span>|<span data-ttu-id="690de-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="690de-129">Type</span></span>|<span data-ttu-id="690de-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="690de-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="690de-131">id</span><span class="sxs-lookup"><span data-stu-id="690de-131">id</span></span>|<span data-ttu-id="690de-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="690de-132">String</span></span>|<span data-ttu-id="690de-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="690de-133">Key of the entity.</span></span> <span data-ttu-id="690de-134">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="690de-134">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="690de-135">displayName</span><span class="sxs-lookup"><span data-stu-id="690de-135">displayName</span></span>|<span data-ttu-id="690de-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="690de-136">String</span></span>|<span data-ttu-id="690de-137">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="690de-137">The admin provided or imported title of the app.</span></span> <span data-ttu-id="690de-138">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="690de-138">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="690de-139">descripción</span><span class="sxs-lookup"><span data-stu-id="690de-139">description</span></span>|<span data-ttu-id="690de-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="690de-140">String</span></span>|<span data-ttu-id="690de-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="690de-141">The description of the app.</span></span> <span data-ttu-id="690de-142">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="690de-142">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="690de-143">publicador</span><span class="sxs-lookup"><span data-stu-id="690de-143">publisher</span></span>|<span data-ttu-id="690de-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="690de-144">String</span></span>|<span data-ttu-id="690de-145">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="690de-145">The publisher of the app.</span></span> <span data-ttu-id="690de-146">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="690de-146">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="690de-147">largeIcon</span><span class="sxs-lookup"><span data-stu-id="690de-147">largeIcon</span></span>|[<span data-ttu-id="690de-148">mimeContent</span><span class="sxs-lookup"><span data-stu-id="690de-148">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="690de-149">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="690de-149">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="690de-150">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="690de-150">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="690de-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="690de-151">createdDateTime</span></span>|<span data-ttu-id="690de-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="690de-152">DateTimeOffset</span></span>|<span data-ttu-id="690de-153">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="690de-153">The date and time the app was created.</span></span> <span data-ttu-id="690de-154">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="690de-154">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="690de-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="690de-155">lastModifiedDateTime</span></span>|<span data-ttu-id="690de-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="690de-156">DateTimeOffset</span></span>|<span data-ttu-id="690de-157">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="690de-157">The date and time the app was last modified.</span></span> <span data-ttu-id="690de-158">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="690de-158">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="690de-159">isFeatured</span><span class="sxs-lookup"><span data-stu-id="690de-159">isFeatured</span></span>|<span data-ttu-id="690de-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="690de-160">Boolean</span></span>|<span data-ttu-id="690de-161">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="690de-161">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="690de-162">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="690de-162">privacyInformationUrl</span></span>|<span data-ttu-id="690de-163">Cadena</span><span class="sxs-lookup"><span data-stu-id="690de-163">String</span></span>|<span data-ttu-id="690de-164">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="690de-164">The privacy statement Url.</span></span> <span data-ttu-id="690de-165">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="690de-165">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="690de-166">informationUrl</span><span class="sxs-lookup"><span data-stu-id="690de-166">informationUrl</span></span>|<span data-ttu-id="690de-167">Cadena</span><span class="sxs-lookup"><span data-stu-id="690de-167">String</span></span>|<span data-ttu-id="690de-168">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="690de-168">The more information Url.</span></span> <span data-ttu-id="690de-169">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="690de-169">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="690de-170">owner</span><span class="sxs-lookup"><span data-stu-id="690de-170">owner</span></span>|<span data-ttu-id="690de-171">Cadena</span><span class="sxs-lookup"><span data-stu-id="690de-171">String</span></span>|<span data-ttu-id="690de-172">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="690de-172">The owner of the app.</span></span> <span data-ttu-id="690de-173">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="690de-173">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="690de-174">developer</span><span class="sxs-lookup"><span data-stu-id="690de-174">developer</span></span>|<span data-ttu-id="690de-175">Cadena</span><span class="sxs-lookup"><span data-stu-id="690de-175">String</span></span>|<span data-ttu-id="690de-176">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="690de-176">The developer of the app.</span></span> <span data-ttu-id="690de-177">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="690de-177">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="690de-178">notas</span><span class="sxs-lookup"><span data-stu-id="690de-178">notes</span></span>|<span data-ttu-id="690de-179">Cadena</span><span class="sxs-lookup"><span data-stu-id="690de-179">String</span></span>|<span data-ttu-id="690de-180">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="690de-180">Notes for the app.</span></span> <span data-ttu-id="690de-181">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="690de-181">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="690de-182">publishingState</span><span class="sxs-lookup"><span data-stu-id="690de-182">publishingState</span></span>|[<span data-ttu-id="690de-183">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="690de-183">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="690de-184">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="690de-184">The publishing state for the app.</span></span> <span data-ttu-id="690de-185">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="690de-185">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="690de-186">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="690de-186">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="690de-187">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="690de-187">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="690de-188">usedLicenseCount</span><span class="sxs-lookup"><span data-stu-id="690de-188">usedLicenseCount</span></span>|<span data-ttu-id="690de-189">Int32</span><span class="sxs-lookup"><span data-stu-id="690de-189">Int32</span></span>|<span data-ttu-id="690de-190">Número de licencias de Microsoft Store para Empresas en uso.</span><span class="sxs-lookup"><span data-stu-id="690de-190">The number of Microsoft Store for Business licenses in use.</span></span>|
|<span data-ttu-id="690de-191">totalLicenseCount</span><span class="sxs-lookup"><span data-stu-id="690de-191">totalLicenseCount</span></span>|<span data-ttu-id="690de-192">Int32</span><span class="sxs-lookup"><span data-stu-id="690de-192">Int32</span></span>|<span data-ttu-id="690de-193">Número total de licencias de Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="690de-193">The total number of Microsoft Store for Business licenses.</span></span>|
|<span data-ttu-id="690de-194">productKey</span><span class="sxs-lookup"><span data-stu-id="690de-194">productKey</span></span>|<span data-ttu-id="690de-195">Cadena</span><span class="sxs-lookup"><span data-stu-id="690de-195">String</span></span>|<span data-ttu-id="690de-196">Clave de producto de la aplicación</span><span class="sxs-lookup"><span data-stu-id="690de-196">The app product key</span></span>|
|<span data-ttu-id="690de-197">licenseType</span><span class="sxs-lookup"><span data-stu-id="690de-197">licenseType</span></span>|[<span data-ttu-id="690de-198">microsoftStoreForBusinessLicenseType</span><span class="sxs-lookup"><span data-stu-id="690de-198">microsoftStoreForBusinessLicenseType</span></span>](../resources/intune-apps-microsoftstoreforbusinesslicensetype.md)|<span data-ttu-id="690de-199">El tipo de licencia de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="690de-199">The app license type.</span></span> <span data-ttu-id="690de-200">Los valores posibles son: `offline` y `online`.</span><span class="sxs-lookup"><span data-stu-id="690de-200">Possible values are: `offline`, `online`.</span></span>|
|<span data-ttu-id="690de-201">packageIdentityName</span><span class="sxs-lookup"><span data-stu-id="690de-201">packageIdentityName</span></span>|<span data-ttu-id="690de-202">Cadena</span><span class="sxs-lookup"><span data-stu-id="690de-202">String</span></span>|<span data-ttu-id="690de-203">Identificador del paquete de aplicación.</span><span class="sxs-lookup"><span data-stu-id="690de-203">The app package identifier</span></span>|



## <a name="response"></a><span data-ttu-id="690de-204">Respuesta</span><span class="sxs-lookup"><span data-stu-id="690de-204">Response</span></span>
<span data-ttu-id="690de-205">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [microsoftStoreForBusinessApp](../resources/intune-apps-microsoftstoreforbusinessapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="690de-205">If successful, this method returns a `201 Created` response code and a [microsoftStoreForBusinessApp](../resources/intune-apps-microsoftstoreforbusinessapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="690de-206">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="690de-206">Example</span></span>
### <a name="request"></a><span data-ttu-id="690de-207">Solicitud</span><span class="sxs-lookup"><span data-stu-id="690de-207">Request</span></span>
<span data-ttu-id="690de-208">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="690de-208">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="690de-209">Respuesta</span><span class="sxs-lookup"><span data-stu-id="690de-209">Response</span></span>
<span data-ttu-id="690de-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="690de-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



