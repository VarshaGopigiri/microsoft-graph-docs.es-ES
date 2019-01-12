---
title: Crear intuneBrandingProfile
description: Crear un nuevo objeto intuneBrandingProfile.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 755de596da82aa2ef7a8d5bc142f43e6bf2ca4c8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27964546"
---
# <a name="create-intunebrandingprofile"></a><span data-ttu-id="540f1-103">Crear intuneBrandingProfile</span><span class="sxs-lookup"><span data-stu-id="540f1-103">Create intuneBrandingProfile</span></span>

> <span data-ttu-id="540f1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="540f1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="540f1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="540f1-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="540f1-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="540f1-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="540f1-107">Crear un nuevo objeto [intuneBrandingProfile](../resources/intune-wip-intunebrandingprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="540f1-107">Create a new [intuneBrandingProfile](../resources/intune-wip-intunebrandingprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="540f1-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="540f1-108">Prerequisites</span></span>
<span data-ttu-id="540f1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="540f1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="540f1-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="540f1-111">Permission type</span></span>|<span data-ttu-id="540f1-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="540f1-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="540f1-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="540f1-113">Delegated (work or school account)</span></span>|<span data-ttu-id="540f1-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="540f1-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="540f1-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="540f1-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="540f1-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="540f1-116">Not supported.</span></span>|
|<span data-ttu-id="540f1-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="540f1-117">Application</span></span>|<span data-ttu-id="540f1-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="540f1-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="540f1-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="540f1-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/intuneBrandingProfiles
```

## <a name="request-headers"></a><span data-ttu-id="540f1-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="540f1-120">Request headers</span></span>
|<span data-ttu-id="540f1-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="540f1-121">Header</span></span>|<span data-ttu-id="540f1-122">Valor</span><span class="sxs-lookup"><span data-stu-id="540f1-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="540f1-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="540f1-123">Authorization</span></span>|<span data-ttu-id="540f1-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="540f1-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="540f1-125">Accept</span><span class="sxs-lookup"><span data-stu-id="540f1-125">Accept</span></span>|<span data-ttu-id="540f1-126">application/json</span><span class="sxs-lookup"><span data-stu-id="540f1-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="540f1-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="540f1-127">Request body</span></span>
<span data-ttu-id="540f1-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto intuneBrandingProfile.</span><span class="sxs-lookup"><span data-stu-id="540f1-128">In the request body, supply a JSON representation for the intuneBrandingProfile object.</span></span>

<span data-ttu-id="540f1-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el intuneBrandingProfile.</span><span class="sxs-lookup"><span data-stu-id="540f1-129">The following table shows the properties that are required when you create the intuneBrandingProfile.</span></span>

|<span data-ttu-id="540f1-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="540f1-130">Property</span></span>|<span data-ttu-id="540f1-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="540f1-131">Type</span></span>|<span data-ttu-id="540f1-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="540f1-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="540f1-133">id</span><span class="sxs-lookup"><span data-stu-id="540f1-133">id</span></span>|<span data-ttu-id="540f1-134">String</span><span class="sxs-lookup"><span data-stu-id="540f1-134">String</span></span>|<span data-ttu-id="540f1-135">Clave de perfil</span><span class="sxs-lookup"><span data-stu-id="540f1-135">Profile Key</span></span>|
|<span data-ttu-id="540f1-136">nombre del perfil</span><span class="sxs-lookup"><span data-stu-id="540f1-136">profileName</span></span>|<span data-ttu-id="540f1-137">String</span><span class="sxs-lookup"><span data-stu-id="540f1-137">String</span></span>|<span data-ttu-id="540f1-138">Nombre del perfil</span><span class="sxs-lookup"><span data-stu-id="540f1-138">Name of the profile</span></span>|
|<span data-ttu-id="540f1-139">profileDescription</span><span class="sxs-lookup"><span data-stu-id="540f1-139">profileDescription</span></span>|<span data-ttu-id="540f1-140">String</span><span class="sxs-lookup"><span data-stu-id="540f1-140">String</span></span>|<span data-ttu-id="540f1-141">Descripción del perfil</span><span class="sxs-lookup"><span data-stu-id="540f1-141">Description of the profile</span></span>|
|<span data-ttu-id="540f1-142">isDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="540f1-142">isDefaultProfile</span></span>|<span data-ttu-id="540f1-143">Booleano</span><span class="sxs-lookup"><span data-stu-id="540f1-143">Boolean</span></span>|<span data-ttu-id="540f1-144">Presenta si se utiliza el perfil de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="540f1-144">Presents if the profile is used for default.</span></span>|
|<span data-ttu-id="540f1-145">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="540f1-145">createdDateTime</span></span>|<span data-ttu-id="540f1-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="540f1-146">DateTimeOffset</span></span>|<span data-ttu-id="540f1-147">Cuando se creó el BrandingProfile.</span><span class="sxs-lookup"><span data-stu-id="540f1-147">When the BrandingProfile was created.</span></span>|
|<span data-ttu-id="540f1-148">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="540f1-148">lastModifiedDateTime</span></span>|<span data-ttu-id="540f1-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="540f1-149">DateTimeOffset</span></span>|<span data-ttu-id="540f1-150">Cuando el BrandingProfile se modificó por última vez.</span><span class="sxs-lookup"><span data-stu-id="540f1-150">When the BrandingProfile was last modified.</span></span>|
|<span data-ttu-id="540f1-151">displayName</span><span class="sxs-lookup"><span data-stu-id="540f1-151">displayName</span></span>|<span data-ttu-id="540f1-152">Cadena</span><span class="sxs-lookup"><span data-stu-id="540f1-152">String</span></span>|<span data-ttu-id="540f1-153">Nombre de la compañía u organización que se muestra a los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="540f1-153">Company/organization name that is displayed to end users.</span></span>|
|<span data-ttu-id="540f1-154">contactITName</span><span class="sxs-lookup"><span data-stu-id="540f1-154">contactITName</span></span>|<span data-ttu-id="540f1-155">Cadena</span><span class="sxs-lookup"><span data-stu-id="540f1-155">String</span></span>|<span data-ttu-id="540f1-156">Nombre de la persona u organización responsable del soporte técnico de TI.</span><span class="sxs-lookup"><span data-stu-id="540f1-156">Name of the person/organization responsible for IT support.</span></span>|
|<span data-ttu-id="540f1-157">contactITPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="540f1-157">contactITPhoneNumber</span></span>|<span data-ttu-id="540f1-158">Cadena</span><span class="sxs-lookup"><span data-stu-id="540f1-158">String</span></span>|<span data-ttu-id="540f1-159">Número de teléfono de la persona u organización responsable del soporte técnico de TI.</span><span class="sxs-lookup"><span data-stu-id="540f1-159">Phone number of the person/organization responsible for IT support.</span></span>|
|<span data-ttu-id="540f1-160">contactITEmailAddress</span><span class="sxs-lookup"><span data-stu-id="540f1-160">contactITEmailAddress</span></span>|<span data-ttu-id="540f1-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="540f1-161">String</span></span>|<span data-ttu-id="540f1-162">Dirección de correo electrónico de la persona u organización responsable del soporte técnico de TI.</span><span class="sxs-lookup"><span data-stu-id="540f1-162">Email address of the person/organization responsible for IT support.</span></span>|
|<span data-ttu-id="540f1-163">contactITNotes</span><span class="sxs-lookup"><span data-stu-id="540f1-163">contactITNotes</span></span>|<span data-ttu-id="540f1-164">Cadena</span><span class="sxs-lookup"><span data-stu-id="540f1-164">String</span></span>|<span data-ttu-id="540f1-165">Comentarios de texto con respecto a la persona u organización responsable del soporte técnico de TI.</span><span class="sxs-lookup"><span data-stu-id="540f1-165">Text comments regarding the person/organization responsible for IT support.</span></span>|
|<span data-ttu-id="540f1-166">privacyUrl</span><span class="sxs-lookup"><span data-stu-id="540f1-166">privacyUrl</span></span>|<span data-ttu-id="540f1-167">Cadena</span><span class="sxs-lookup"><span data-stu-id="540f1-167">String</span></span>|<span data-ttu-id="540f1-168">Dirección URL de la directiva de privacidad de la empresa u organización.</span><span class="sxs-lookup"><span data-stu-id="540f1-168">URL to the company/organization’s privacy policy.</span></span>|
|<span data-ttu-id="540f1-169">onlineSupportSiteUrl</span><span class="sxs-lookup"><span data-stu-id="540f1-169">onlineSupportSiteUrl</span></span>|<span data-ttu-id="540f1-170">Cadena</span><span class="sxs-lookup"><span data-stu-id="540f1-170">String</span></span>|<span data-ttu-id="540f1-171">Dirección URL del sitio del departamento de soporte técnico de la empresa u organización.</span><span class="sxs-lookup"><span data-stu-id="540f1-171">URL to the company/organization’s IT helpdesk site.</span></span>|
|<span data-ttu-id="540f1-172">onlineSupportSiteName</span><span class="sxs-lookup"><span data-stu-id="540f1-172">onlineSupportSiteName</span></span>|<span data-ttu-id="540f1-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="540f1-173">String</span></span>|<span data-ttu-id="540f1-174">Nombre para mostrar del sitio del departamento de soporte técnico de la empresa u organización.</span><span class="sxs-lookup"><span data-stu-id="540f1-174">Display name of the company/organization’s IT helpdesk site.</span></span>|
|<span data-ttu-id="540f1-175">themeColor</span><span class="sxs-lookup"><span data-stu-id="540f1-175">themeColor</span></span>|[<span data-ttu-id="540f1-176">rgbColor</span><span class="sxs-lookup"><span data-stu-id="540f1-176">rgbColor</span></span>](../resources/intune-shared-rgbcolor.md)|<span data-ttu-id="540f1-177">Color de tema principal utilizado en el portal web y las aplicaciones del Portal de empresa.</span><span class="sxs-lookup"><span data-stu-id="540f1-177">Primary theme color used in the Company Portal applications and web portal.</span></span>|
|<span data-ttu-id="540f1-178">showLogo</span><span class="sxs-lookup"><span data-stu-id="540f1-178">showLogo</span></span>|<span data-ttu-id="540f1-179">Booleano</span><span class="sxs-lookup"><span data-stu-id="540f1-179">Boolean</span></span>|<span data-ttu-id="540f1-180">Booleano que indica si se muestran o no las imágenes de logotipo proporcionadas por el administrador.</span><span class="sxs-lookup"><span data-stu-id="540f1-180">Boolean that represents whether the administrator-supplied logo images are shown or not shown.</span></span>|
|<span data-ttu-id="540f1-181">showDisplayNameNextToLogo</span><span class="sxs-lookup"><span data-stu-id="540f1-181">showDisplayNameNextToLogo</span></span>|<span data-ttu-id="540f1-182">Booleano</span><span class="sxs-lookup"><span data-stu-id="540f1-182">Boolean</span></span>|<span data-ttu-id="540f1-183">Booleano que indica si se muestra o no el nombre para mostrar proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="540f1-183">Boolean that represents whether the administrator-supplied display name will be shown next to the logo image.</span></span>|
|<span data-ttu-id="540f1-184">themeColorLogo</span><span class="sxs-lookup"><span data-stu-id="540f1-184">themeColorLogo</span></span>|[<span data-ttu-id="540f1-185">mimeContent</span><span class="sxs-lookup"><span data-stu-id="540f1-185">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="540f1-186">Imagen de logotipo que se muestra en las aplicaciones de Portal de empresa de fondos de color del tema.</span><span class="sxs-lookup"><span data-stu-id="540f1-186">Logo image displayed in Company Portal apps on theme color backgrounds.</span></span>|
|<span data-ttu-id="540f1-187">lightBackgroundLogo</span><span class="sxs-lookup"><span data-stu-id="540f1-187">lightBackgroundLogo</span></span>|[<span data-ttu-id="540f1-188">mimeContent</span><span class="sxs-lookup"><span data-stu-id="540f1-188">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="540f1-189">Imagen de logotipo que se muestra en las aplicaciones de Portal de empresa de fondos claras.</span><span class="sxs-lookup"><span data-stu-id="540f1-189">Logo image displayed in Company Portal apps on light backgrounds.</span></span>|
|<span data-ttu-id="540f1-190">landingPageCustomizedImage</span><span class="sxs-lookup"><span data-stu-id="540f1-190">landingPageCustomizedImage</span></span>|[<span data-ttu-id="540f1-191">mimeContent</span><span class="sxs-lookup"><span data-stu-id="540f1-191">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="540f1-192">Imagen personalizada que se muestra en la página de inicio de aplicaciones de Portal de empresa</span><span class="sxs-lookup"><span data-stu-id="540f1-192">Customized image displayed in Company Portal apps landing page</span></span>|



## <a name="response"></a><span data-ttu-id="540f1-193">Respuesta</span><span class="sxs-lookup"><span data-stu-id="540f1-193">Response</span></span>
<span data-ttu-id="540f1-194">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [intuneBrandingProfile](../resources/intune-wip-intunebrandingprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="540f1-194">If successful, this method returns a `201 Created` response code and a [intuneBrandingProfile](../resources/intune-wip-intunebrandingprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="540f1-195">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="540f1-195">Example</span></span>
### <a name="request"></a><span data-ttu-id="540f1-196">Solicitud</span><span class="sxs-lookup"><span data-stu-id="540f1-196">Request</span></span>
<span data-ttu-id="540f1-197">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="540f1-197">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/intuneBrandingProfiles
Content-type: application/json
Content-length: 1269

{
  "@odata.type": "#microsoft.graph.intuneBrandingProfile",
  "profileName": "Profile Name value",
  "profileDescription": "Profile Description value",
  "isDefaultProfile": true,
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "contactITName": "Contact ITName value",
  "contactITPhoneNumber": "Contact ITPhone Number value",
  "contactITEmailAddress": "Contact ITEmail Address value",
  "contactITNotes": "Contact ITNotes value",
  "privacyUrl": "https://example.com/privacyUrl/",
  "onlineSupportSiteUrl": "https://example.com/onlineSupportSiteUrl/",
  "onlineSupportSiteName": "Online Support Site Name value",
  "themeColor": {
    "@odata.type": "microsoft.graph.rgbColor",
    "r": 1,
    "g": 1,
    "b": 1
  },
  "showLogo": true,
  "showDisplayNameNextToLogo": true,
  "themeColorLogo": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "lightBackgroundLogo": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "landingPageCustomizedImage": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  }
}
```

### <a name="response"></a><span data-ttu-id="540f1-198">Respuesta</span><span class="sxs-lookup"><span data-stu-id="540f1-198">Response</span></span>
<span data-ttu-id="540f1-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="540f1-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1377

{
  "@odata.type": "#microsoft.graph.intuneBrandingProfile",
  "id": "fcd6136c-136c-fcd6-6c13-d6fc6c13d6fc",
  "profileName": "Profile Name value",
  "profileDescription": "Profile Description value",
  "isDefaultProfile": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "contactITName": "Contact ITName value",
  "contactITPhoneNumber": "Contact ITPhone Number value",
  "contactITEmailAddress": "Contact ITEmail Address value",
  "contactITNotes": "Contact ITNotes value",
  "privacyUrl": "https://example.com/privacyUrl/",
  "onlineSupportSiteUrl": "https://example.com/onlineSupportSiteUrl/",
  "onlineSupportSiteName": "Online Support Site Name value",
  "themeColor": {
    "@odata.type": "microsoft.graph.rgbColor",
    "r": 1,
    "g": 1,
    "b": 1
  },
  "showLogo": true,
  "showDisplayNameNextToLogo": true,
  "themeColorLogo": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "lightBackgroundLogo": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "landingPageCustomizedImage": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  }
}
```





