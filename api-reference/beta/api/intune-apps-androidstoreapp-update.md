---
title: Actualizar androidStoreApp
description: Actualice las propiedades de un objeto androidStoreApp.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 4ff090e0ebee3da71b44060d7d20c6b27d213668
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27984426"
---
# <a name="update-androidstoreapp"></a><span data-ttu-id="302b8-103">Actualizar androidStoreApp</span><span class="sxs-lookup"><span data-stu-id="302b8-103">Update androidStoreApp</span></span>

> <span data-ttu-id="302b8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="302b8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="302b8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="302b8-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="302b8-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="302b8-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="302b8-107">Actualice las propiedades de un objeto [androidStoreApp](../resources/intune-apps-androidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="302b8-107">Update the properties of a [androidStoreApp](../resources/intune-apps-androidstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="302b8-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="302b8-108">Prerequisites</span></span>
<span data-ttu-id="302b8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="302b8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="302b8-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="302b8-111">Permission type</span></span>|<span data-ttu-id="302b8-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="302b8-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="302b8-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="302b8-113">Delegated (work or school account)</span></span>|<span data-ttu-id="302b8-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="302b8-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="302b8-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="302b8-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="302b8-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="302b8-116">Not supported.</span></span>|
|<span data-ttu-id="302b8-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="302b8-117">Application</span></span>|<span data-ttu-id="302b8-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="302b8-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="302b8-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="302b8-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="request-headers"></a><span data-ttu-id="302b8-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="302b8-120">Request headers</span></span>
|<span data-ttu-id="302b8-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="302b8-121">Header</span></span>|<span data-ttu-id="302b8-122">Valor</span><span class="sxs-lookup"><span data-stu-id="302b8-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="302b8-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="302b8-123">Authorization</span></span>|<span data-ttu-id="302b8-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="302b8-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="302b8-125">Accept</span><span class="sxs-lookup"><span data-stu-id="302b8-125">Accept</span></span>|<span data-ttu-id="302b8-126">application/json</span><span class="sxs-lookup"><span data-stu-id="302b8-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="302b8-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="302b8-127">Request body</span></span>
<span data-ttu-id="302b8-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [androidStoreApp](../resources/intune-apps-androidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="302b8-128">In the request body, supply a JSON representation for the [androidStoreApp](../resources/intune-apps-androidstoreapp.md) object.</span></span>

<span data-ttu-id="302b8-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [androidStoreApp](../resources/intune-apps-androidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="302b8-129">The following table shows the properties that are required when you create the [androidStoreApp](../resources/intune-apps-androidstoreapp.md).</span></span>

|<span data-ttu-id="302b8-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="302b8-130">Property</span></span>|<span data-ttu-id="302b8-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="302b8-131">Type</span></span>|<span data-ttu-id="302b8-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="302b8-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="302b8-133">id</span><span class="sxs-lookup"><span data-stu-id="302b8-133">id</span></span>|<span data-ttu-id="302b8-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="302b8-134">String</span></span>|<span data-ttu-id="302b8-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="302b8-135">Key of the entity.</span></span> <span data-ttu-id="302b8-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="302b8-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="302b8-137">displayName</span><span class="sxs-lookup"><span data-stu-id="302b8-137">displayName</span></span>|<span data-ttu-id="302b8-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="302b8-138">String</span></span>|<span data-ttu-id="302b8-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="302b8-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="302b8-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="302b8-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="302b8-141">descripción</span><span class="sxs-lookup"><span data-stu-id="302b8-141">description</span></span>|<span data-ttu-id="302b8-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="302b8-142">String</span></span>|<span data-ttu-id="302b8-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="302b8-143">The description of the app.</span></span> <span data-ttu-id="302b8-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="302b8-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="302b8-145">publicador</span><span class="sxs-lookup"><span data-stu-id="302b8-145">publisher</span></span>|<span data-ttu-id="302b8-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="302b8-146">String</span></span>|<span data-ttu-id="302b8-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="302b8-147">The publisher of the app.</span></span> <span data-ttu-id="302b8-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="302b8-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="302b8-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="302b8-149">largeIcon</span></span>|[<span data-ttu-id="302b8-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="302b8-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="302b8-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="302b8-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="302b8-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="302b8-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="302b8-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="302b8-153">createdDateTime</span></span>|<span data-ttu-id="302b8-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="302b8-154">DateTimeOffset</span></span>|<span data-ttu-id="302b8-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="302b8-155">The date and time the app was created.</span></span> <span data-ttu-id="302b8-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="302b8-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="302b8-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="302b8-157">lastModifiedDateTime</span></span>|<span data-ttu-id="302b8-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="302b8-158">DateTimeOffset</span></span>|<span data-ttu-id="302b8-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="302b8-159">The date and time the app was last modified.</span></span> <span data-ttu-id="302b8-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="302b8-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="302b8-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="302b8-161">isFeatured</span></span>|<span data-ttu-id="302b8-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="302b8-162">Boolean</span></span>|<span data-ttu-id="302b8-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="302b8-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="302b8-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="302b8-164">privacyInformationUrl</span></span>|<span data-ttu-id="302b8-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="302b8-165">String</span></span>|<span data-ttu-id="302b8-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="302b8-166">The privacy statement Url.</span></span> <span data-ttu-id="302b8-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="302b8-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="302b8-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="302b8-168">informationUrl</span></span>|<span data-ttu-id="302b8-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="302b8-169">String</span></span>|<span data-ttu-id="302b8-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="302b8-170">The more information Url.</span></span> <span data-ttu-id="302b8-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="302b8-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="302b8-172">owner</span><span class="sxs-lookup"><span data-stu-id="302b8-172">owner</span></span>|<span data-ttu-id="302b8-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="302b8-173">String</span></span>|<span data-ttu-id="302b8-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="302b8-174">The owner of the app.</span></span> <span data-ttu-id="302b8-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="302b8-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="302b8-176">developer</span><span class="sxs-lookup"><span data-stu-id="302b8-176">developer</span></span>|<span data-ttu-id="302b8-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="302b8-177">String</span></span>|<span data-ttu-id="302b8-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="302b8-178">The developer of the app.</span></span> <span data-ttu-id="302b8-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="302b8-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="302b8-180">notas</span><span class="sxs-lookup"><span data-stu-id="302b8-180">notes</span></span>|<span data-ttu-id="302b8-181">Cadena</span><span class="sxs-lookup"><span data-stu-id="302b8-181">String</span></span>|<span data-ttu-id="302b8-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="302b8-182">Notes for the app.</span></span> <span data-ttu-id="302b8-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="302b8-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="302b8-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="302b8-184">uploadState</span></span>|<span data-ttu-id="302b8-185">Int32</span><span class="sxs-lookup"><span data-stu-id="302b8-185">Int32</span></span>|<span data-ttu-id="302b8-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="302b8-186">The upload state.</span></span> <span data-ttu-id="302b8-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="302b8-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="302b8-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="302b8-188">publishingState</span></span>|[<span data-ttu-id="302b8-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="302b8-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="302b8-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="302b8-190">The publishing state for the app.</span></span> <span data-ttu-id="302b8-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="302b8-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="302b8-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="302b8-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="302b8-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="302b8-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="302b8-194">packageId</span><span class="sxs-lookup"><span data-stu-id="302b8-194">packageId</span></span>|<span data-ttu-id="302b8-195">Cadena</span><span class="sxs-lookup"><span data-stu-id="302b8-195">String</span></span>|<span data-ttu-id="302b8-196">El identificador del paquete.</span><span class="sxs-lookup"><span data-stu-id="302b8-196">The package identifier.</span></span>|
|<span data-ttu-id="302b8-197">appIdentifier</span><span class="sxs-lookup"><span data-stu-id="302b8-197">appIdentifier</span></span>|<span data-ttu-id="302b8-198">Cadena</span><span class="sxs-lookup"><span data-stu-id="302b8-198">String</span></span>|<span data-ttu-id="302b8-199">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="302b8-199">The Identity Name.</span></span>|
|<span data-ttu-id="302b8-200">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="302b8-200">appStoreUrl</span></span>|<span data-ttu-id="302b8-201">Cadena</span><span class="sxs-lookup"><span data-stu-id="302b8-201">String</span></span>|<span data-ttu-id="302b8-202">La dirección URL de la tienda de aplicaciones de Android.</span><span class="sxs-lookup"><span data-stu-id="302b8-202">The Android app store URL.</span></span>|
|<span data-ttu-id="302b8-203">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="302b8-203">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="302b8-204">androidMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="302b8-204">androidMinimumOperatingSystem</span></span>](../resources/intune-apps-androidminimumoperatingsystem.md)|<span data-ttu-id="302b8-205">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="302b8-205">The value for the minimum applicable operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="302b8-206">Respuesta</span><span class="sxs-lookup"><span data-stu-id="302b8-206">Response</span></span>
<span data-ttu-id="302b8-207">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [androidStoreApp](../resources/intune-apps-androidstoreapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="302b8-207">If successful, this method returns a `200 OK` response code and an updated [androidStoreApp](../resources/intune-apps-androidstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="302b8-208">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="302b8-208">Example</span></span>
### <a name="request"></a><span data-ttu-id="302b8-209">Solicitud</span><span class="sxs-lookup"><span data-stu-id="302b8-209">Request</span></span>
<span data-ttu-id="302b8-210">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="302b8-210">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="302b8-211">Respuesta</span><span class="sxs-lookup"><span data-stu-id="302b8-211">Response</span></span>
<span data-ttu-id="302b8-p117">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="302b8-p117">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





