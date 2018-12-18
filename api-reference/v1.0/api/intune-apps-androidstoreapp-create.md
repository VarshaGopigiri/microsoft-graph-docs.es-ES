---
title: Crear androidStoreApp
description: Cree un objeto androidStoreApp.
author: tfitzmac
ms.openlocfilehash: e1a43114170016b76ce19d6f2f27fbb5ae15a576
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27351446"
---
# <a name="create-androidstoreapp"></a><span data-ttu-id="32223-103">Crear androidStoreApp</span><span class="sxs-lookup"><span data-stu-id="32223-103">Create androidStoreApp</span></span>

> <span data-ttu-id="32223-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="32223-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="32223-105">Cree un objeto [androidStoreApp](../resources/intune-apps-androidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="32223-105">Create a new [androidStoreApp](../resources/intune-apps-androidstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="32223-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="32223-106">Prerequisites</span></span>
<span data-ttu-id="32223-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="32223-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="32223-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="32223-109">Permission type</span></span>|<span data-ttu-id="32223-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="32223-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="32223-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="32223-111">Delegated (work or school account)</span></span>|<span data-ttu-id="32223-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="32223-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="32223-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="32223-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="32223-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="32223-114">Not supported.</span></span>|
|<span data-ttu-id="32223-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="32223-115">Application</span></span>|<span data-ttu-id="32223-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="32223-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="32223-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="32223-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="32223-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="32223-118">Request headers</span></span>
|<span data-ttu-id="32223-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="32223-119">Header</span></span>|<span data-ttu-id="32223-120">Valor</span><span class="sxs-lookup"><span data-stu-id="32223-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="32223-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="32223-121">Authorization</span></span>|<span data-ttu-id="32223-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="32223-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="32223-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="32223-123">Accept</span></span>|<span data-ttu-id="32223-124">application/json</span><span class="sxs-lookup"><span data-stu-id="32223-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="32223-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="32223-125">Request body</span></span>
<span data-ttu-id="32223-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto androidStoreApp.</span><span class="sxs-lookup"><span data-stu-id="32223-126">In the request body, supply a JSON representation for the androidStoreApp object.</span></span>

<span data-ttu-id="32223-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto androidStoreApp.</span><span class="sxs-lookup"><span data-stu-id="32223-127">The following table shows the properties that are required when you create the androidStoreApp.</span></span>

|<span data-ttu-id="32223-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="32223-128">Property</span></span>|<span data-ttu-id="32223-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="32223-129">Type</span></span>|<span data-ttu-id="32223-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="32223-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="32223-131">id</span><span class="sxs-lookup"><span data-stu-id="32223-131">id</span></span>|<span data-ttu-id="32223-132">String</span><span class="sxs-lookup"><span data-stu-id="32223-132">String</span></span>|<span data-ttu-id="32223-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="32223-133">Key of the entity.</span></span> <span data-ttu-id="32223-134">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="32223-134">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="32223-135">displayName</span><span class="sxs-lookup"><span data-stu-id="32223-135">displayName</span></span>|<span data-ttu-id="32223-136">String</span><span class="sxs-lookup"><span data-stu-id="32223-136">String</span></span>|<span data-ttu-id="32223-137">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="32223-137">The admin provided or imported title of the app.</span></span> <span data-ttu-id="32223-138">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="32223-138">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="32223-139">descripción</span><span class="sxs-lookup"><span data-stu-id="32223-139">description</span></span>|<span data-ttu-id="32223-140">String</span><span class="sxs-lookup"><span data-stu-id="32223-140">String</span></span>|<span data-ttu-id="32223-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="32223-141">The description of the app.</span></span> <span data-ttu-id="32223-142">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="32223-142">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="32223-143">publicador</span><span class="sxs-lookup"><span data-stu-id="32223-143">publisher</span></span>|<span data-ttu-id="32223-144">String</span><span class="sxs-lookup"><span data-stu-id="32223-144">String</span></span>|<span data-ttu-id="32223-145">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="32223-145">The publisher of the app.</span></span> <span data-ttu-id="32223-146">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="32223-146">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="32223-147">largeIcon</span><span class="sxs-lookup"><span data-stu-id="32223-147">largeIcon</span></span>|[<span data-ttu-id="32223-148">mimeContent</span><span class="sxs-lookup"><span data-stu-id="32223-148">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="32223-149">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="32223-149">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="32223-150">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="32223-150">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="32223-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="32223-151">createdDateTime</span></span>|<span data-ttu-id="32223-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="32223-152">DateTimeOffset</span></span>|<span data-ttu-id="32223-153">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="32223-153">The date and time the app was created.</span></span> <span data-ttu-id="32223-154">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="32223-154">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="32223-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="32223-155">lastModifiedDateTime</span></span>|<span data-ttu-id="32223-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="32223-156">DateTimeOffset</span></span>|<span data-ttu-id="32223-157">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="32223-157">The date and time the app was last modified.</span></span> <span data-ttu-id="32223-158">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="32223-158">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="32223-159">isFeatured</span><span class="sxs-lookup"><span data-stu-id="32223-159">isFeatured</span></span>|<span data-ttu-id="32223-160">Boolean</span><span class="sxs-lookup"><span data-stu-id="32223-160">Boolean</span></span>|<span data-ttu-id="32223-161">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="32223-161">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="32223-162">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="32223-162">privacyInformationUrl</span></span>|<span data-ttu-id="32223-163">String</span><span class="sxs-lookup"><span data-stu-id="32223-163">String</span></span>|<span data-ttu-id="32223-164">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="32223-164">The privacy statement Url.</span></span> <span data-ttu-id="32223-165">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="32223-165">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="32223-166">informationUrl</span><span class="sxs-lookup"><span data-stu-id="32223-166">informationUrl</span></span>|<span data-ttu-id="32223-167">String</span><span class="sxs-lookup"><span data-stu-id="32223-167">String</span></span>|<span data-ttu-id="32223-168">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="32223-168">The more information Url.</span></span> <span data-ttu-id="32223-169">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="32223-169">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="32223-170">owner</span><span class="sxs-lookup"><span data-stu-id="32223-170">owner</span></span>|<span data-ttu-id="32223-171">String</span><span class="sxs-lookup"><span data-stu-id="32223-171">String</span></span>|<span data-ttu-id="32223-172">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="32223-172">The owner of the app.</span></span> <span data-ttu-id="32223-173">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="32223-173">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="32223-174">developer</span><span class="sxs-lookup"><span data-stu-id="32223-174">developer</span></span>|<span data-ttu-id="32223-175">String</span><span class="sxs-lookup"><span data-stu-id="32223-175">String</span></span>|<span data-ttu-id="32223-176">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="32223-176">The developer of the app.</span></span> <span data-ttu-id="32223-177">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="32223-177">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="32223-178">notas</span><span class="sxs-lookup"><span data-stu-id="32223-178">notes</span></span>|<span data-ttu-id="32223-179">String</span><span class="sxs-lookup"><span data-stu-id="32223-179">String</span></span>|<span data-ttu-id="32223-180">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="32223-180">Notes for the app.</span></span> <span data-ttu-id="32223-181">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="32223-181">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="32223-182">publishingState</span><span class="sxs-lookup"><span data-stu-id="32223-182">publishingState</span></span>|[<span data-ttu-id="32223-183">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="32223-183">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="32223-184">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="32223-184">The publishing state for the app.</span></span> <span data-ttu-id="32223-185">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="32223-185">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="32223-186">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="32223-186">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="32223-187">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="32223-187">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="32223-188">packageId</span><span class="sxs-lookup"><span data-stu-id="32223-188">packageId</span></span>|<span data-ttu-id="32223-189">String</span><span class="sxs-lookup"><span data-stu-id="32223-189">String</span></span>|<span data-ttu-id="32223-190">El identificador del paquete.</span><span class="sxs-lookup"><span data-stu-id="32223-190">The package identifier.</span></span>|
|<span data-ttu-id="32223-191">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="32223-191">appStoreUrl</span></span>|<span data-ttu-id="32223-192">String</span><span class="sxs-lookup"><span data-stu-id="32223-192">String</span></span>|<span data-ttu-id="32223-193">La dirección URL de la tienda de aplicaciones de Android.</span><span class="sxs-lookup"><span data-stu-id="32223-193">The Android app store URL.</span></span>|
|<span data-ttu-id="32223-194">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="32223-194">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="32223-195">androidMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="32223-195">androidMinimumOperatingSystem</span></span>](../resources/intune-apps-androidminimumoperatingsystem.md)|<span data-ttu-id="32223-196">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="32223-196">The value for the minimum applicable operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="32223-197">Respuesta</span><span class="sxs-lookup"><span data-stu-id="32223-197">Response</span></span>
<span data-ttu-id="32223-198">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [androidStoreApp](../resources/intune-apps-androidstoreapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="32223-198">If successful, this method returns a `201 Created` response code and a [androidStoreApp](../resources/intune-apps-androidstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="32223-199">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="32223-199">Example</span></span>
### <a name="request"></a><span data-ttu-id="32223-200">Solicitud</span><span class="sxs-lookup"><span data-stu-id="32223-200">Request</span></span>
<span data-ttu-id="32223-201">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="32223-201">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 938

{
  "@odata.type": "#microsoft.graph.androidStoreApp",
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
  "packageId": "Package Id value",
  "appStoreUrl": "https://example.com/appStoreUrl/",
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.androidMinimumOperatingSystem",
    "v4_0": true,
    "v4_0_3": true,
    "v4_1": true,
    "v4_2": true,
    "v4_3": true,
    "v4_4": true,
    "v5_0": true,
    "v5_1": true
  }
}
```

### <a name="response"></a><span data-ttu-id="32223-202">Respuesta</span><span class="sxs-lookup"><span data-stu-id="32223-202">Response</span></span>
<span data-ttu-id="32223-p115">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="32223-p115">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1110

{
  "@odata.type": "#microsoft.graph.androidStoreApp",
  "id": "1f2b7654-7654-1f2b-5476-2b1f54762b1f",
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
  "packageId": "Package Id value",
  "appStoreUrl": "https://example.com/appStoreUrl/",
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.androidMinimumOperatingSystem",
    "v4_0": true,
    "v4_0_3": true,
    "v4_1": true,
    "v4_2": true,
    "v4_3": true,
    "v4_4": true,
    "v5_0": true,
    "v5_1": true
  }
}
```



