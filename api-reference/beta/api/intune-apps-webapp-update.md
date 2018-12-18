---
title: Actualizar webApp
description: Actualice las propiedades de un objeto webApp.
author: tfitzmac
ms.openlocfilehash: c64c12aa6e9d29576990ad5f4572250d8cca4023
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27346154"
---
# <a name="update-webapp"></a><span data-ttu-id="6611d-103">Actualizar webApp</span><span class="sxs-lookup"><span data-stu-id="6611d-103">Update webApp</span></span>

> <span data-ttu-id="6611d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6611d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6611d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6611d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6611d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6611d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6611d-107">Actualice las propiedades de un objeto [webApp](../resources/intune-apps-webapp.md).</span><span class="sxs-lookup"><span data-stu-id="6611d-107">Update the properties of a [webApp](../resources/intune-apps-webapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6611d-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6611d-108">Prerequisites</span></span>
<span data-ttu-id="6611d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6611d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6611d-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6611d-111">Permission type</span></span>|<span data-ttu-id="6611d-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6611d-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6611d-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6611d-113">Delegated (work or school account)</span></span>|<span data-ttu-id="6611d-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6611d-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="6611d-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6611d-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6611d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6611d-116">Not supported.</span></span>|
|<span data-ttu-id="6611d-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6611d-117">Application</span></span>|<span data-ttu-id="6611d-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6611d-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6611d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6611d-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="request-headers"></a><span data-ttu-id="6611d-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6611d-120">Request headers</span></span>
|<span data-ttu-id="6611d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6611d-121">Header</span></span>|<span data-ttu-id="6611d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6611d-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6611d-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="6611d-123">Authorization</span></span>|<span data-ttu-id="6611d-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6611d-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6611d-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6611d-125">Accept</span></span>|<span data-ttu-id="6611d-126">application/json</span><span class="sxs-lookup"><span data-stu-id="6611d-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6611d-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6611d-127">Request body</span></span>
<span data-ttu-id="6611d-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [webApp](../resources/intune-apps-webapp.md).</span><span class="sxs-lookup"><span data-stu-id="6611d-128">In the request body, supply a JSON representation for the [webApp](../resources/intune-apps-webapp.md) object.</span></span>

<span data-ttu-id="6611d-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [webApp](../resources/intune-apps-webapp.md).</span><span class="sxs-lookup"><span data-stu-id="6611d-129">The following table shows the properties that are required when you create the [webApp](../resources/intune-apps-webapp.md).</span></span>

|<span data-ttu-id="6611d-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6611d-130">Property</span></span>|<span data-ttu-id="6611d-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="6611d-131">Type</span></span>|<span data-ttu-id="6611d-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="6611d-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6611d-133">id</span><span class="sxs-lookup"><span data-stu-id="6611d-133">id</span></span>|<span data-ttu-id="6611d-134">String</span><span class="sxs-lookup"><span data-stu-id="6611d-134">String</span></span>|<span data-ttu-id="6611d-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="6611d-135">Key of the entity.</span></span> <span data-ttu-id="6611d-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6611d-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="6611d-137">displayName</span><span class="sxs-lookup"><span data-stu-id="6611d-137">displayName</span></span>|<span data-ttu-id="6611d-138">String</span><span class="sxs-lookup"><span data-stu-id="6611d-138">String</span></span>|<span data-ttu-id="6611d-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="6611d-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="6611d-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6611d-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="6611d-141">descripción</span><span class="sxs-lookup"><span data-stu-id="6611d-141">description</span></span>|<span data-ttu-id="6611d-142">String</span><span class="sxs-lookup"><span data-stu-id="6611d-142">String</span></span>|<span data-ttu-id="6611d-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6611d-143">The description of the app.</span></span> <span data-ttu-id="6611d-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6611d-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="6611d-145">publicador</span><span class="sxs-lookup"><span data-stu-id="6611d-145">publisher</span></span>|<span data-ttu-id="6611d-146">String</span><span class="sxs-lookup"><span data-stu-id="6611d-146">String</span></span>|<span data-ttu-id="6611d-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6611d-147">The publisher of the app.</span></span> <span data-ttu-id="6611d-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6611d-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="6611d-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="6611d-149">largeIcon</span></span>|[<span data-ttu-id="6611d-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="6611d-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="6611d-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="6611d-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="6611d-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6611d-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="6611d-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="6611d-153">createdDateTime</span></span>|<span data-ttu-id="6611d-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6611d-154">DateTimeOffset</span></span>|<span data-ttu-id="6611d-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6611d-155">The date and time the app was created.</span></span> <span data-ttu-id="6611d-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6611d-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="6611d-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="6611d-157">lastModifiedDateTime</span></span>|<span data-ttu-id="6611d-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6611d-158">DateTimeOffset</span></span>|<span data-ttu-id="6611d-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6611d-159">The date and time the app was last modified.</span></span> <span data-ttu-id="6611d-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6611d-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="6611d-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="6611d-161">isFeatured</span></span>|<span data-ttu-id="6611d-162">Boolean</span><span class="sxs-lookup"><span data-stu-id="6611d-162">Boolean</span></span>|<span data-ttu-id="6611d-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6611d-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="6611d-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="6611d-164">privacyInformationUrl</span></span>|<span data-ttu-id="6611d-165">String</span><span class="sxs-lookup"><span data-stu-id="6611d-165">String</span></span>|<span data-ttu-id="6611d-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="6611d-166">The privacy statement Url.</span></span> <span data-ttu-id="6611d-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6611d-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="6611d-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="6611d-168">informationUrl</span></span>|<span data-ttu-id="6611d-169">String</span><span class="sxs-lookup"><span data-stu-id="6611d-169">String</span></span>|<span data-ttu-id="6611d-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="6611d-170">The more information Url.</span></span> <span data-ttu-id="6611d-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6611d-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="6611d-172">owner</span><span class="sxs-lookup"><span data-stu-id="6611d-172">owner</span></span>|<span data-ttu-id="6611d-173">String</span><span class="sxs-lookup"><span data-stu-id="6611d-173">String</span></span>|<span data-ttu-id="6611d-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6611d-174">The owner of the app.</span></span> <span data-ttu-id="6611d-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6611d-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="6611d-176">developer</span><span class="sxs-lookup"><span data-stu-id="6611d-176">developer</span></span>|<span data-ttu-id="6611d-177">String</span><span class="sxs-lookup"><span data-stu-id="6611d-177">String</span></span>|<span data-ttu-id="6611d-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6611d-178">The developer of the app.</span></span> <span data-ttu-id="6611d-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6611d-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="6611d-180">notas</span><span class="sxs-lookup"><span data-stu-id="6611d-180">notes</span></span>|<span data-ttu-id="6611d-181">String</span><span class="sxs-lookup"><span data-stu-id="6611d-181">String</span></span>|<span data-ttu-id="6611d-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6611d-182">Notes for the app.</span></span> <span data-ttu-id="6611d-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6611d-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="6611d-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="6611d-184">uploadState</span></span>|<span data-ttu-id="6611d-185">Int32</span><span class="sxs-lookup"><span data-stu-id="6611d-185">Int32</span></span>|<span data-ttu-id="6611d-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="6611d-186">The upload state.</span></span> <span data-ttu-id="6611d-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6611d-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="6611d-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="6611d-188">publishingState</span></span>|[<span data-ttu-id="6611d-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="6611d-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="6611d-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6611d-190">The publishing state for the app.</span></span> <span data-ttu-id="6611d-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="6611d-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="6611d-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6611d-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="6611d-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="6611d-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="6611d-194">appUrl</span><span class="sxs-lookup"><span data-stu-id="6611d-194">appUrl</span></span>|<span data-ttu-id="6611d-195">String</span><span class="sxs-lookup"><span data-stu-id="6611d-195">String</span></span>|<span data-ttu-id="6611d-196">Dirección URL de la aplicación web.</span><span class="sxs-lookup"><span data-stu-id="6611d-196">The web app URL.</span></span>|
|<span data-ttu-id="6611d-197">useManagedBrowser</span><span class="sxs-lookup"><span data-stu-id="6611d-197">useManagedBrowser</span></span>|<span data-ttu-id="6611d-198">Booleano</span><span class="sxs-lookup"><span data-stu-id="6611d-198">Boolean</span></span>|<span data-ttu-id="6611d-199">Indica si se va a usar el explorador administrado.</span><span class="sxs-lookup"><span data-stu-id="6611d-199">Whether or not to use managed browser.</span></span> <span data-ttu-id="6611d-200">Esta propiedad solo es aplicable a iOS y Android.</span><span class="sxs-lookup"><span data-stu-id="6611d-200">This property is only applicable for Android and IOS.</span></span>|



## <a name="response"></a><span data-ttu-id="6611d-201">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6611d-201">Response</span></span>
<span data-ttu-id="6611d-202">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [webApp](../resources/intune-apps-webapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6611d-202">If successful, this method returns a `200 OK` response code and an updated [webApp](../resources/intune-apps-webapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6611d-203">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6611d-203">Example</span></span>
### <a name="request"></a><span data-ttu-id="6611d-204">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6611d-204">Request</span></span>
<span data-ttu-id="6611d-205">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6611d-205">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="6611d-206">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6611d-206">Response</span></span>
<span data-ttu-id="6611d-p118">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6611d-p118">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





