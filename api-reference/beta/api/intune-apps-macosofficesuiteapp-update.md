---
title: Actualizar macOSOfficeSuiteApp
description: Actualice las propiedades de un objeto macOSOfficeSuiteApp.
author: tfitzmac
ms.openlocfilehash: 2b09e415d19a41128eeb6caf21f06d3617c8322c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27341906"
---
# <a name="update-macosofficesuiteapp"></a><span data-ttu-id="53c5a-103">Actualizar macOSOfficeSuiteApp</span><span class="sxs-lookup"><span data-stu-id="53c5a-103">Update macOSOfficeSuiteApp</span></span>

> <span data-ttu-id="53c5a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="53c5a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="53c5a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="53c5a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="53c5a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="53c5a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="53c5a-107">Actualice las propiedades de un objeto [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md).</span><span class="sxs-lookup"><span data-stu-id="53c5a-107">Update the properties of a [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="53c5a-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="53c5a-108">Prerequisites</span></span>
<span data-ttu-id="53c5a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="53c5a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="53c5a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="53c5a-111">Permission type</span></span>|<span data-ttu-id="53c5a-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="53c5a-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="53c5a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="53c5a-113">Delegated (work or school account)</span></span>|<span data-ttu-id="53c5a-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="53c5a-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="53c5a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="53c5a-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="53c5a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="53c5a-116">Not supported.</span></span>|
|<span data-ttu-id="53c5a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="53c5a-117">Application</span></span>|<span data-ttu-id="53c5a-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="53c5a-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="53c5a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="53c5a-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="request-headers"></a><span data-ttu-id="53c5a-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="53c5a-120">Request headers</span></span>
|<span data-ttu-id="53c5a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53c5a-121">Header</span></span>|<span data-ttu-id="53c5a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="53c5a-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="53c5a-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="53c5a-123">Authorization</span></span>|<span data-ttu-id="53c5a-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="53c5a-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="53c5a-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="53c5a-125">Accept</span></span>|<span data-ttu-id="53c5a-126">application/json</span><span class="sxs-lookup"><span data-stu-id="53c5a-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="53c5a-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="53c5a-127">Request body</span></span>
<span data-ttu-id="53c5a-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md).</span><span class="sxs-lookup"><span data-stu-id="53c5a-128">In the request body, supply a JSON representation for the [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md) object.</span></span>

<span data-ttu-id="53c5a-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md).</span><span class="sxs-lookup"><span data-stu-id="53c5a-129">The following table shows the properties that are required when you create the [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md).</span></span>

|<span data-ttu-id="53c5a-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="53c5a-130">Property</span></span>|<span data-ttu-id="53c5a-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="53c5a-131">Type</span></span>|<span data-ttu-id="53c5a-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="53c5a-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="53c5a-133">id</span><span class="sxs-lookup"><span data-stu-id="53c5a-133">id</span></span>|<span data-ttu-id="53c5a-134">String</span><span class="sxs-lookup"><span data-stu-id="53c5a-134">String</span></span>|<span data-ttu-id="53c5a-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="53c5a-135">Key of the entity.</span></span> <span data-ttu-id="53c5a-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="53c5a-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="53c5a-137">displayName</span><span class="sxs-lookup"><span data-stu-id="53c5a-137">displayName</span></span>|<span data-ttu-id="53c5a-138">String</span><span class="sxs-lookup"><span data-stu-id="53c5a-138">String</span></span>|<span data-ttu-id="53c5a-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="53c5a-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="53c5a-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="53c5a-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="53c5a-141">descripción</span><span class="sxs-lookup"><span data-stu-id="53c5a-141">description</span></span>|<span data-ttu-id="53c5a-142">String</span><span class="sxs-lookup"><span data-stu-id="53c5a-142">String</span></span>|<span data-ttu-id="53c5a-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="53c5a-143">The description of the app.</span></span> <span data-ttu-id="53c5a-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="53c5a-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="53c5a-145">publicador</span><span class="sxs-lookup"><span data-stu-id="53c5a-145">publisher</span></span>|<span data-ttu-id="53c5a-146">String</span><span class="sxs-lookup"><span data-stu-id="53c5a-146">String</span></span>|<span data-ttu-id="53c5a-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="53c5a-147">The publisher of the app.</span></span> <span data-ttu-id="53c5a-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="53c5a-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="53c5a-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="53c5a-149">largeIcon</span></span>|[<span data-ttu-id="53c5a-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="53c5a-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="53c5a-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="53c5a-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="53c5a-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="53c5a-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="53c5a-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="53c5a-153">createdDateTime</span></span>|<span data-ttu-id="53c5a-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="53c5a-154">DateTimeOffset</span></span>|<span data-ttu-id="53c5a-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="53c5a-155">The date and time the app was created.</span></span> <span data-ttu-id="53c5a-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="53c5a-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="53c5a-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="53c5a-157">lastModifiedDateTime</span></span>|<span data-ttu-id="53c5a-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="53c5a-158">DateTimeOffset</span></span>|<span data-ttu-id="53c5a-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="53c5a-159">The date and time the app was last modified.</span></span> <span data-ttu-id="53c5a-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="53c5a-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="53c5a-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="53c5a-161">isFeatured</span></span>|<span data-ttu-id="53c5a-162">Boolean</span><span class="sxs-lookup"><span data-stu-id="53c5a-162">Boolean</span></span>|<span data-ttu-id="53c5a-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="53c5a-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="53c5a-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="53c5a-164">privacyInformationUrl</span></span>|<span data-ttu-id="53c5a-165">String</span><span class="sxs-lookup"><span data-stu-id="53c5a-165">String</span></span>|<span data-ttu-id="53c5a-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="53c5a-166">The privacy statement Url.</span></span> <span data-ttu-id="53c5a-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="53c5a-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="53c5a-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="53c5a-168">informationUrl</span></span>|<span data-ttu-id="53c5a-169">String</span><span class="sxs-lookup"><span data-stu-id="53c5a-169">String</span></span>|<span data-ttu-id="53c5a-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="53c5a-170">The more information Url.</span></span> <span data-ttu-id="53c5a-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="53c5a-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="53c5a-172">owner</span><span class="sxs-lookup"><span data-stu-id="53c5a-172">owner</span></span>|<span data-ttu-id="53c5a-173">String</span><span class="sxs-lookup"><span data-stu-id="53c5a-173">String</span></span>|<span data-ttu-id="53c5a-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="53c5a-174">The owner of the app.</span></span> <span data-ttu-id="53c5a-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="53c5a-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="53c5a-176">developer</span><span class="sxs-lookup"><span data-stu-id="53c5a-176">developer</span></span>|<span data-ttu-id="53c5a-177">String</span><span class="sxs-lookup"><span data-stu-id="53c5a-177">String</span></span>|<span data-ttu-id="53c5a-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="53c5a-178">The developer of the app.</span></span> <span data-ttu-id="53c5a-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="53c5a-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="53c5a-180">notas</span><span class="sxs-lookup"><span data-stu-id="53c5a-180">notes</span></span>|<span data-ttu-id="53c5a-181">String</span><span class="sxs-lookup"><span data-stu-id="53c5a-181">String</span></span>|<span data-ttu-id="53c5a-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="53c5a-182">Notes for the app.</span></span> <span data-ttu-id="53c5a-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="53c5a-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="53c5a-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="53c5a-184">uploadState</span></span>|<span data-ttu-id="53c5a-185">Int32</span><span class="sxs-lookup"><span data-stu-id="53c5a-185">Int32</span></span>|<span data-ttu-id="53c5a-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="53c5a-186">The upload state.</span></span> <span data-ttu-id="53c5a-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="53c5a-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="53c5a-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="53c5a-188">publishingState</span></span>|[<span data-ttu-id="53c5a-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="53c5a-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="53c5a-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="53c5a-190">The publishing state for the app.</span></span> <span data-ttu-id="53c5a-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="53c5a-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="53c5a-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="53c5a-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="53c5a-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="53c5a-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|



## <a name="response"></a><span data-ttu-id="53c5a-194">Respuesta</span><span class="sxs-lookup"><span data-stu-id="53c5a-194">Response</span></span>
<span data-ttu-id="53c5a-195">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="53c5a-195">If successful, this method returns a `200 OK` response code and an updated [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="53c5a-196">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="53c5a-196">Example</span></span>
### <a name="request"></a><span data-ttu-id="53c5a-197">Solicitud</span><span class="sxs-lookup"><span data-stu-id="53c5a-197">Request</span></span>
<span data-ttu-id="53c5a-198">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="53c5a-198">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 612

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
  "publishingState": "processing"
}
```

### <a name="response"></a><span data-ttu-id="53c5a-199">Respuesta</span><span class="sxs-lookup"><span data-stu-id="53c5a-199">Response</span></span>
<span data-ttu-id="53c5a-p117">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="53c5a-p117">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 778

{
  "@odata.type": "#microsoft.graph.macOSOfficeSuiteApp",
  "id": "bf39e35d-e35d-bf39-5de3-39bf5de339bf",
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
  "publishingState": "processing"
}
```





