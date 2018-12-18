---
title: Crear macOSOfficeSuiteApp
description: Cree un objeto macOSOfficeSuiteApp.
author: tfitzmac
ms.openlocfilehash: 1e4a2f4bbcbe32407df468fe8c89c57d30a3d815
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27311861"
---
# <a name="create-macosofficesuiteapp"></a><span data-ttu-id="f4339-103">Crear macOSOfficeSuiteApp</span><span class="sxs-lookup"><span data-stu-id="f4339-103">Create macOSOfficeSuiteApp</span></span>

> <span data-ttu-id="f4339-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f4339-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f4339-105">Cree un objeto [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md).</span><span class="sxs-lookup"><span data-stu-id="f4339-105">Create a new [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f4339-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f4339-106">Prerequisites</span></span>
<span data-ttu-id="f4339-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f4339-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f4339-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f4339-109">Permission type</span></span>|<span data-ttu-id="f4339-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f4339-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f4339-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f4339-111">Delegated (work or school account)</span></span>|<span data-ttu-id="f4339-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f4339-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="f4339-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f4339-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f4339-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f4339-114">Not supported.</span></span>|
|<span data-ttu-id="f4339-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f4339-115">Application</span></span>|<span data-ttu-id="f4339-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f4339-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f4339-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f4339-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="f4339-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f4339-118">Request headers</span></span>
|<span data-ttu-id="f4339-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f4339-119">Header</span></span>|<span data-ttu-id="f4339-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f4339-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f4339-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="f4339-121">Authorization</span></span>|<span data-ttu-id="f4339-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f4339-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f4339-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f4339-123">Accept</span></span>|<span data-ttu-id="f4339-124">application/json</span><span class="sxs-lookup"><span data-stu-id="f4339-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f4339-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f4339-125">Request body</span></span>
<span data-ttu-id="f4339-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto macOSOfficeSuiteApp.</span><span class="sxs-lookup"><span data-stu-id="f4339-126">In the request body, supply a JSON representation for the macOSOfficeSuiteApp object.</span></span>

<span data-ttu-id="f4339-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto macOSOfficeSuiteApp.</span><span class="sxs-lookup"><span data-stu-id="f4339-127">The following table shows the properties that are required when you create the macOSOfficeSuiteApp.</span></span>

|<span data-ttu-id="f4339-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f4339-128">Property</span></span>|<span data-ttu-id="f4339-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="f4339-129">Type</span></span>|<span data-ttu-id="f4339-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4339-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f4339-131">id</span><span class="sxs-lookup"><span data-stu-id="f4339-131">id</span></span>|<span data-ttu-id="f4339-132">String</span><span class="sxs-lookup"><span data-stu-id="f4339-132">String</span></span>|<span data-ttu-id="f4339-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f4339-133">Key of the entity.</span></span> <span data-ttu-id="f4339-134">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f4339-134">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f4339-135">displayName</span><span class="sxs-lookup"><span data-stu-id="f4339-135">displayName</span></span>|<span data-ttu-id="f4339-136">String</span><span class="sxs-lookup"><span data-stu-id="f4339-136">String</span></span>|<span data-ttu-id="f4339-137">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="f4339-137">The admin provided or imported title of the app.</span></span> <span data-ttu-id="f4339-138">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f4339-138">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f4339-139">descripción</span><span class="sxs-lookup"><span data-stu-id="f4339-139">description</span></span>|<span data-ttu-id="f4339-140">String</span><span class="sxs-lookup"><span data-stu-id="f4339-140">String</span></span>|<span data-ttu-id="f4339-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f4339-141">The description of the app.</span></span> <span data-ttu-id="f4339-142">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f4339-142">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f4339-143">publicador</span><span class="sxs-lookup"><span data-stu-id="f4339-143">publisher</span></span>|<span data-ttu-id="f4339-144">String</span><span class="sxs-lookup"><span data-stu-id="f4339-144">String</span></span>|<span data-ttu-id="f4339-145">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f4339-145">The publisher of the app.</span></span> <span data-ttu-id="f4339-146">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f4339-146">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f4339-147">largeIcon</span><span class="sxs-lookup"><span data-stu-id="f4339-147">largeIcon</span></span>|[<span data-ttu-id="f4339-148">mimeContent</span><span class="sxs-lookup"><span data-stu-id="f4339-148">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="f4339-149">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="f4339-149">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="f4339-150">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f4339-150">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f4339-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="f4339-151">createdDateTime</span></span>|<span data-ttu-id="f4339-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f4339-152">DateTimeOffset</span></span>|<span data-ttu-id="f4339-153">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f4339-153">The date and time the app was created.</span></span> <span data-ttu-id="f4339-154">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f4339-154">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f4339-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="f4339-155">lastModifiedDateTime</span></span>|<span data-ttu-id="f4339-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f4339-156">DateTimeOffset</span></span>|<span data-ttu-id="f4339-157">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f4339-157">The date and time the app was last modified.</span></span> <span data-ttu-id="f4339-158">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f4339-158">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f4339-159">isFeatured</span><span class="sxs-lookup"><span data-stu-id="f4339-159">isFeatured</span></span>|<span data-ttu-id="f4339-160">Boolean</span><span class="sxs-lookup"><span data-stu-id="f4339-160">Boolean</span></span>|<span data-ttu-id="f4339-161">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f4339-161">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f4339-162">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="f4339-162">privacyInformationUrl</span></span>|<span data-ttu-id="f4339-163">String</span><span class="sxs-lookup"><span data-stu-id="f4339-163">String</span></span>|<span data-ttu-id="f4339-164">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="f4339-164">The privacy statement Url.</span></span> <span data-ttu-id="f4339-165">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f4339-165">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f4339-166">informationUrl</span><span class="sxs-lookup"><span data-stu-id="f4339-166">informationUrl</span></span>|<span data-ttu-id="f4339-167">String</span><span class="sxs-lookup"><span data-stu-id="f4339-167">String</span></span>|<span data-ttu-id="f4339-168">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="f4339-168">The more information Url.</span></span> <span data-ttu-id="f4339-169">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f4339-169">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f4339-170">owner</span><span class="sxs-lookup"><span data-stu-id="f4339-170">owner</span></span>|<span data-ttu-id="f4339-171">String</span><span class="sxs-lookup"><span data-stu-id="f4339-171">String</span></span>|<span data-ttu-id="f4339-172">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f4339-172">The owner of the app.</span></span> <span data-ttu-id="f4339-173">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f4339-173">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f4339-174">developer</span><span class="sxs-lookup"><span data-stu-id="f4339-174">developer</span></span>|<span data-ttu-id="f4339-175">String</span><span class="sxs-lookup"><span data-stu-id="f4339-175">String</span></span>|<span data-ttu-id="f4339-176">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f4339-176">The developer of the app.</span></span> <span data-ttu-id="f4339-177">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f4339-177">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f4339-178">notas</span><span class="sxs-lookup"><span data-stu-id="f4339-178">notes</span></span>|<span data-ttu-id="f4339-179">String</span><span class="sxs-lookup"><span data-stu-id="f4339-179">String</span></span>|<span data-ttu-id="f4339-180">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f4339-180">Notes for the app.</span></span> <span data-ttu-id="f4339-181">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f4339-181">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f4339-182">publishingState</span><span class="sxs-lookup"><span data-stu-id="f4339-182">publishingState</span></span>|[<span data-ttu-id="f4339-183">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="f4339-183">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="f4339-184">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f4339-184">The publishing state for the app.</span></span> <span data-ttu-id="f4339-185">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="f4339-185">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="f4339-186">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f4339-186">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="f4339-187">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="f4339-187">Possible values are: `notPublished`, `processing`, `published`.</span></span>|



## <a name="response"></a><span data-ttu-id="f4339-188">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f4339-188">Response</span></span>
<span data-ttu-id="f4339-189">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f4339-189">If successful, this method returns a `201 Created` response code and a [macOSOfficeSuiteApp](../resources/intune-apps-macosofficesuiteapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f4339-190">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f4339-190">Example</span></span>
### <a name="request"></a><span data-ttu-id="f4339-191">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f4339-191">Request</span></span>
<span data-ttu-id="f4339-192">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f4339-192">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 584

{
  "@odata.type": "#microsoft.graph.macOSOfficeSuiteApp",
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
  "publishingState": "processing"
}
```

### <a name="response"></a><span data-ttu-id="f4339-193">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f4339-193">Response</span></span>
<span data-ttu-id="f4339-p115">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f4339-p115">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 756

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
  "publishingState": "processing"
}
```



