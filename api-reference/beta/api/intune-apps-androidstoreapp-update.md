---
title: Actualizar androidStoreApp
description: Actualice las propiedades de un objeto androidStoreApp.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 8cd9efebe6d7a68c2b0e023e17e881850e01843f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27818840"
---
# <a name="update-androidstoreapp"></a><span data-ttu-id="21f30-103">Actualizar androidStoreApp</span><span class="sxs-lookup"><span data-stu-id="21f30-103">Update androidStoreApp</span></span>

> <span data-ttu-id="21f30-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="21f30-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="21f30-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="21f30-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="21f30-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="21f30-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="21f30-107">Actualice las propiedades de un objeto [androidStoreApp](../resources/intune-apps-androidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="21f30-107">Update the properties of a [androidStoreApp](../resources/intune-apps-androidstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="21f30-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="21f30-108">Prerequisites</span></span>
<span data-ttu-id="21f30-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="21f30-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="21f30-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="21f30-111">Permission type</span></span>|<span data-ttu-id="21f30-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="21f30-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="21f30-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="21f30-113">Delegated (work or school account)</span></span>|<span data-ttu-id="21f30-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="21f30-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="21f30-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="21f30-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="21f30-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="21f30-116">Not supported.</span></span>|
|<span data-ttu-id="21f30-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="21f30-117">Application</span></span>|<span data-ttu-id="21f30-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="21f30-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="21f30-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="21f30-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="request-headers"></a><span data-ttu-id="21f30-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="21f30-120">Request headers</span></span>
|<span data-ttu-id="21f30-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="21f30-121">Header</span></span>|<span data-ttu-id="21f30-122">Valor</span><span class="sxs-lookup"><span data-stu-id="21f30-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="21f30-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="21f30-123">Authorization</span></span>|<span data-ttu-id="21f30-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="21f30-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="21f30-125">Accept</span><span class="sxs-lookup"><span data-stu-id="21f30-125">Accept</span></span>|<span data-ttu-id="21f30-126">application/json</span><span class="sxs-lookup"><span data-stu-id="21f30-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="21f30-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="21f30-127">Request body</span></span>
<span data-ttu-id="21f30-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [androidStoreApp](../resources/intune-apps-androidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="21f30-128">In the request body, supply a JSON representation for the [androidStoreApp](../resources/intune-apps-androidstoreapp.md) object.</span></span>

<span data-ttu-id="21f30-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [androidStoreApp](../resources/intune-apps-androidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="21f30-129">The following table shows the properties that are required when you create the [androidStoreApp](../resources/intune-apps-androidstoreapp.md).</span></span>

|<span data-ttu-id="21f30-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="21f30-130">Property</span></span>|<span data-ttu-id="21f30-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="21f30-131">Type</span></span>|<span data-ttu-id="21f30-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="21f30-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="21f30-133">id</span><span class="sxs-lookup"><span data-stu-id="21f30-133">id</span></span>|<span data-ttu-id="21f30-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="21f30-134">String</span></span>|<span data-ttu-id="21f30-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="21f30-135">Key of the entity.</span></span> <span data-ttu-id="21f30-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="21f30-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="21f30-137">displayName</span><span class="sxs-lookup"><span data-stu-id="21f30-137">displayName</span></span>|<span data-ttu-id="21f30-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="21f30-138">String</span></span>|<span data-ttu-id="21f30-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="21f30-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="21f30-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="21f30-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="21f30-141">descripción</span><span class="sxs-lookup"><span data-stu-id="21f30-141">description</span></span>|<span data-ttu-id="21f30-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="21f30-142">String</span></span>|<span data-ttu-id="21f30-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="21f30-143">The description of the app.</span></span> <span data-ttu-id="21f30-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="21f30-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="21f30-145">publicador</span><span class="sxs-lookup"><span data-stu-id="21f30-145">publisher</span></span>|<span data-ttu-id="21f30-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="21f30-146">String</span></span>|<span data-ttu-id="21f30-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="21f30-147">The publisher of the app.</span></span> <span data-ttu-id="21f30-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="21f30-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="21f30-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="21f30-149">largeIcon</span></span>|[<span data-ttu-id="21f30-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="21f30-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="21f30-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="21f30-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="21f30-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="21f30-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="21f30-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="21f30-153">createdDateTime</span></span>|<span data-ttu-id="21f30-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="21f30-154">DateTimeOffset</span></span>|<span data-ttu-id="21f30-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="21f30-155">The date and time the app was created.</span></span> <span data-ttu-id="21f30-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="21f30-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="21f30-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="21f30-157">lastModifiedDateTime</span></span>|<span data-ttu-id="21f30-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="21f30-158">DateTimeOffset</span></span>|<span data-ttu-id="21f30-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="21f30-159">The date and time the app was last modified.</span></span> <span data-ttu-id="21f30-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="21f30-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="21f30-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="21f30-161">isFeatured</span></span>|<span data-ttu-id="21f30-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="21f30-162">Boolean</span></span>|<span data-ttu-id="21f30-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="21f30-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="21f30-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="21f30-164">privacyInformationUrl</span></span>|<span data-ttu-id="21f30-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="21f30-165">String</span></span>|<span data-ttu-id="21f30-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="21f30-166">The privacy statement Url.</span></span> <span data-ttu-id="21f30-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="21f30-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="21f30-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="21f30-168">informationUrl</span></span>|<span data-ttu-id="21f30-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="21f30-169">String</span></span>|<span data-ttu-id="21f30-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="21f30-170">The more information Url.</span></span> <span data-ttu-id="21f30-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="21f30-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="21f30-172">owner</span><span class="sxs-lookup"><span data-stu-id="21f30-172">owner</span></span>|<span data-ttu-id="21f30-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="21f30-173">String</span></span>|<span data-ttu-id="21f30-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="21f30-174">The owner of the app.</span></span> <span data-ttu-id="21f30-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="21f30-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="21f30-176">developer</span><span class="sxs-lookup"><span data-stu-id="21f30-176">developer</span></span>|<span data-ttu-id="21f30-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="21f30-177">String</span></span>|<span data-ttu-id="21f30-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="21f30-178">The developer of the app.</span></span> <span data-ttu-id="21f30-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="21f30-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="21f30-180">notas</span><span class="sxs-lookup"><span data-stu-id="21f30-180">notes</span></span>|<span data-ttu-id="21f30-181">Cadena</span><span class="sxs-lookup"><span data-stu-id="21f30-181">String</span></span>|<span data-ttu-id="21f30-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="21f30-182">Notes for the app.</span></span> <span data-ttu-id="21f30-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="21f30-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="21f30-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="21f30-184">uploadState</span></span>|<span data-ttu-id="21f30-185">Int32</span><span class="sxs-lookup"><span data-stu-id="21f30-185">Int32</span></span>|<span data-ttu-id="21f30-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="21f30-186">The upload state.</span></span> <span data-ttu-id="21f30-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="21f30-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="21f30-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="21f30-188">publishingState</span></span>|[<span data-ttu-id="21f30-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="21f30-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="21f30-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="21f30-190">The publishing state for the app.</span></span> <span data-ttu-id="21f30-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="21f30-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="21f30-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="21f30-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="21f30-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="21f30-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="21f30-194">packageId</span><span class="sxs-lookup"><span data-stu-id="21f30-194">packageId</span></span>|<span data-ttu-id="21f30-195">Cadena</span><span class="sxs-lookup"><span data-stu-id="21f30-195">String</span></span>|<span data-ttu-id="21f30-196">El identificador del paquete.</span><span class="sxs-lookup"><span data-stu-id="21f30-196">The package identifier.</span></span>|
|<span data-ttu-id="21f30-197">appIdentifier</span><span class="sxs-lookup"><span data-stu-id="21f30-197">appIdentifier</span></span>|<span data-ttu-id="21f30-198">Cadena</span><span class="sxs-lookup"><span data-stu-id="21f30-198">String</span></span>|<span data-ttu-id="21f30-199">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="21f30-199">The Identity Name.</span></span>|
|<span data-ttu-id="21f30-200">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="21f30-200">appStoreUrl</span></span>|<span data-ttu-id="21f30-201">Cadena</span><span class="sxs-lookup"><span data-stu-id="21f30-201">String</span></span>|<span data-ttu-id="21f30-202">La dirección URL de la tienda de aplicaciones de Android.</span><span class="sxs-lookup"><span data-stu-id="21f30-202">The Android app store URL.</span></span>|
|<span data-ttu-id="21f30-203">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="21f30-203">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="21f30-204">androidMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="21f30-204">androidMinimumOperatingSystem</span></span>](../resources/intune-apps-androidminimumoperatingsystem.md)|<span data-ttu-id="21f30-205">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="21f30-205">The value for the minimum applicable operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="21f30-206">Respuesta</span><span class="sxs-lookup"><span data-stu-id="21f30-206">Response</span></span>
<span data-ttu-id="21f30-207">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [androidStoreApp](../resources/intune-apps-androidstoreapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="21f30-207">If successful, this method returns a `200 OK` response code and an updated [androidStoreApp](../resources/intune-apps-androidstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="21f30-208">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="21f30-208">Example</span></span>
### <a name="request"></a><span data-ttu-id="21f30-209">Solicitud</span><span class="sxs-lookup"><span data-stu-id="21f30-209">Request</span></span>
<span data-ttu-id="21f30-210">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="21f30-210">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1128

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
  "packageId": "Package Id value",
  "appIdentifier": "App Identifier value",
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
    "v5_1": true,
    "v6_0": true,
    "v7_0": true,
    "v7_1": true,
    "v8_0": true,
    "v8_1": true,
    "v9_0": true
  }
}
```

### <a name="response"></a><span data-ttu-id="21f30-211">Respuesta</span><span class="sxs-lookup"><span data-stu-id="21f30-211">Response</span></span>
<span data-ttu-id="21f30-p117">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="21f30-p117">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1290

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
  "uploadState": 11,
  "publishingState": "processing",
  "packageId": "Package Id value",
  "appIdentifier": "App Identifier value",
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
    "v5_1": true,
    "v6_0": true,
    "v7_0": true,
    "v7_1": true,
    "v8_0": true,
    "v8_1": true,
    "v9_0": true
  }
}
```





