---
title: Actualizar androidStoreApp
description: Actualice las propiedades de un objeto androidStoreApp.
ms.openlocfilehash: 1332373eadb0623c7bdd9e606d52a2a1c8875403
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029176"
---
# <a name="update-androidstoreapp"></a><span data-ttu-id="dbe7a-103">Actualizar androidStoreApp</span><span class="sxs-lookup"><span data-stu-id="dbe7a-103">Update androidStoreApp</span></span>

> <span data-ttu-id="dbe7a-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="dbe7a-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="dbe7a-105">Actualice las propiedades de un objeto [androidStoreApp](../resources/intune-apps-androidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="dbe7a-105">Update the properties of a [androidStoreApp](../resources/intune-apps-androidstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="dbe7a-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="dbe7a-106">Prerequisites</span></span>
<span data-ttu-id="dbe7a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dbe7a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dbe7a-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dbe7a-109">Permission type</span></span>|<span data-ttu-id="dbe7a-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dbe7a-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="dbe7a-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dbe7a-111">Delegated (work or school account)</span></span>|<span data-ttu-id="dbe7a-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="dbe7a-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="dbe7a-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dbe7a-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="dbe7a-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dbe7a-114">Not supported.</span></span>|
|<span data-ttu-id="dbe7a-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dbe7a-115">Application</span></span>|<span data-ttu-id="dbe7a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dbe7a-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="dbe7a-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dbe7a-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="dbe7a-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dbe7a-118">Request headers</span></span>
|<span data-ttu-id="dbe7a-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dbe7a-119">Header</span></span>|<span data-ttu-id="dbe7a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="dbe7a-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="dbe7a-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="dbe7a-121">Authorization</span></span>|<span data-ttu-id="dbe7a-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="dbe7a-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="dbe7a-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="dbe7a-123">Accept</span></span>|<span data-ttu-id="dbe7a-124">application/json</span><span class="sxs-lookup"><span data-stu-id="dbe7a-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="dbe7a-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dbe7a-125">Request body</span></span>
<span data-ttu-id="dbe7a-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [androidStoreApp](../resources/intune-apps-androidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="dbe7a-126">In the request body, supply a JSON representation for the [androidStoreApp](../resources/intune-apps-androidstoreapp.md) object.</span></span>

<span data-ttu-id="dbe7a-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [androidStoreApp](../resources/intune-apps-androidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="dbe7a-127">The following table shows the properties that are required when you create the [androidStoreApp](../resources/intune-apps-androidstoreapp.md).</span></span>

|<span data-ttu-id="dbe7a-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dbe7a-128">Property</span></span>|<span data-ttu-id="dbe7a-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="dbe7a-129">Type</span></span>|<span data-ttu-id="dbe7a-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="dbe7a-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="dbe7a-131">id</span><span class="sxs-lookup"><span data-stu-id="dbe7a-131">id</span></span>|<span data-ttu-id="dbe7a-132">String</span><span class="sxs-lookup"><span data-stu-id="dbe7a-132">String</span></span>|<span data-ttu-id="dbe7a-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="dbe7a-133">Key of the entity.</span></span> <span data-ttu-id="dbe7a-134">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="dbe7a-134">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="dbe7a-135">displayName</span><span class="sxs-lookup"><span data-stu-id="dbe7a-135">displayName</span></span>|<span data-ttu-id="dbe7a-136">String</span><span class="sxs-lookup"><span data-stu-id="dbe7a-136">String</span></span>|<span data-ttu-id="dbe7a-137">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="dbe7a-137">The admin provided or imported title of the app.</span></span> <span data-ttu-id="dbe7a-138">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="dbe7a-138">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="dbe7a-139">descripción</span><span class="sxs-lookup"><span data-stu-id="dbe7a-139">description</span></span>|<span data-ttu-id="dbe7a-140">String</span><span class="sxs-lookup"><span data-stu-id="dbe7a-140">String</span></span>|<span data-ttu-id="dbe7a-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dbe7a-141">The description of the app.</span></span> <span data-ttu-id="dbe7a-142">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="dbe7a-142">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="dbe7a-143">publicador</span><span class="sxs-lookup"><span data-stu-id="dbe7a-143">publisher</span></span>|<span data-ttu-id="dbe7a-144">String</span><span class="sxs-lookup"><span data-stu-id="dbe7a-144">String</span></span>|<span data-ttu-id="dbe7a-145">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dbe7a-145">The publisher of the app.</span></span> <span data-ttu-id="dbe7a-146">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="dbe7a-146">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="dbe7a-147">largeIcon</span><span class="sxs-lookup"><span data-stu-id="dbe7a-147">largeIcon</span></span>|[<span data-ttu-id="dbe7a-148">mimeContent</span><span class="sxs-lookup"><span data-stu-id="dbe7a-148">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="dbe7a-149">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="dbe7a-149">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="dbe7a-150">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="dbe7a-150">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="dbe7a-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="dbe7a-151">createdDateTime</span></span>|<span data-ttu-id="dbe7a-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="dbe7a-152">DateTimeOffset</span></span>|<span data-ttu-id="dbe7a-153">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dbe7a-153">The date and time the app was created.</span></span> <span data-ttu-id="dbe7a-154">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="dbe7a-154">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="dbe7a-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="dbe7a-155">lastModifiedDateTime</span></span>|<span data-ttu-id="dbe7a-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="dbe7a-156">DateTimeOffset</span></span>|<span data-ttu-id="dbe7a-157">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dbe7a-157">The date and time the app was last modified.</span></span> <span data-ttu-id="dbe7a-158">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="dbe7a-158">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="dbe7a-159">isFeatured</span><span class="sxs-lookup"><span data-stu-id="dbe7a-159">isFeatured</span></span>|<span data-ttu-id="dbe7a-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="dbe7a-160">Boolean</span></span>|<span data-ttu-id="dbe7a-161">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="dbe7a-161">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="dbe7a-162">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="dbe7a-162">privacyInformationUrl</span></span>|<span data-ttu-id="dbe7a-163">String</span><span class="sxs-lookup"><span data-stu-id="dbe7a-163">String</span></span>|<span data-ttu-id="dbe7a-164">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="dbe7a-164">The privacy statement Url.</span></span> <span data-ttu-id="dbe7a-165">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="dbe7a-165">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="dbe7a-166">informationUrl</span><span class="sxs-lookup"><span data-stu-id="dbe7a-166">informationUrl</span></span>|<span data-ttu-id="dbe7a-167">String</span><span class="sxs-lookup"><span data-stu-id="dbe7a-167">String</span></span>|<span data-ttu-id="dbe7a-168">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="dbe7a-168">The more information Url.</span></span> <span data-ttu-id="dbe7a-169">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="dbe7a-169">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="dbe7a-170">owner</span><span class="sxs-lookup"><span data-stu-id="dbe7a-170">owner</span></span>|<span data-ttu-id="dbe7a-171">String</span><span class="sxs-lookup"><span data-stu-id="dbe7a-171">String</span></span>|<span data-ttu-id="dbe7a-172">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dbe7a-172">The owner of the app.</span></span> <span data-ttu-id="dbe7a-173">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="dbe7a-173">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="dbe7a-174">developer</span><span class="sxs-lookup"><span data-stu-id="dbe7a-174">developer</span></span>|<span data-ttu-id="dbe7a-175">String</span><span class="sxs-lookup"><span data-stu-id="dbe7a-175">String</span></span>|<span data-ttu-id="dbe7a-176">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dbe7a-176">The developer of the app.</span></span> <span data-ttu-id="dbe7a-177">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="dbe7a-177">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="dbe7a-178">notas</span><span class="sxs-lookup"><span data-stu-id="dbe7a-178">notes</span></span>|<span data-ttu-id="dbe7a-179">String</span><span class="sxs-lookup"><span data-stu-id="dbe7a-179">String</span></span>|<span data-ttu-id="dbe7a-180">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dbe7a-180">Notes for the app.</span></span> <span data-ttu-id="dbe7a-181">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="dbe7a-181">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="dbe7a-182">publishingState</span><span class="sxs-lookup"><span data-stu-id="dbe7a-182">publishingState</span></span>|[<span data-ttu-id="dbe7a-183">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="dbe7a-183">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="dbe7a-184">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dbe7a-184">The publishing state for the app.</span></span> <span data-ttu-id="dbe7a-185">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="dbe7a-185">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="dbe7a-186">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="dbe7a-186">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="dbe7a-187">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="dbe7a-187">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="dbe7a-188">packageId</span><span class="sxs-lookup"><span data-stu-id="dbe7a-188">packageId</span></span>|<span data-ttu-id="dbe7a-189">String</span><span class="sxs-lookup"><span data-stu-id="dbe7a-189">String</span></span>|<span data-ttu-id="dbe7a-190">El identificador del paquete.</span><span class="sxs-lookup"><span data-stu-id="dbe7a-190">The package identifier.</span></span>|
|<span data-ttu-id="dbe7a-191">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="dbe7a-191">appStoreUrl</span></span>|<span data-ttu-id="dbe7a-192">String</span><span class="sxs-lookup"><span data-stu-id="dbe7a-192">String</span></span>|<span data-ttu-id="dbe7a-193">La dirección URL de la tienda de aplicaciones de Android.</span><span class="sxs-lookup"><span data-stu-id="dbe7a-193">The Android app store URL.</span></span>|
|<span data-ttu-id="dbe7a-194">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="dbe7a-194">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="dbe7a-195">androidMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="dbe7a-195">androidMinimumOperatingSystem</span></span>](../resources/intune-apps-androidminimumoperatingsystem.md)|<span data-ttu-id="dbe7a-196">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="dbe7a-196">The value for the minimum applicable operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="dbe7a-197">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dbe7a-197">Response</span></span>
<span data-ttu-id="dbe7a-198">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [androidStoreApp](../resources/intune-apps-androidstoreapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dbe7a-198">If successful, this method returns a `200 OK` response code and an updated [androidStoreApp](../resources/intune-apps-androidstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="dbe7a-199">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dbe7a-199">Example</span></span>
### <a name="request"></a><span data-ttu-id="dbe7a-200">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dbe7a-200">Request</span></span>
<span data-ttu-id="dbe7a-201">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dbe7a-201">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
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

### <a name="response"></a><span data-ttu-id="dbe7a-202">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dbe7a-202">Response</span></span>
<span data-ttu-id="dbe7a-p115">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dbe7a-p115">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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



