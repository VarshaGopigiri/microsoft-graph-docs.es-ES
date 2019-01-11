---
title: Crear officeSuiteApp
description: Crear un nuevo objeto officeSuiteApp.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 6cc3aaff3a206d12d589372a3edc769cb9dc369d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27837957"
---
# <a name="create-officesuiteapp"></a><span data-ttu-id="11328-103">Crear officeSuiteApp</span><span class="sxs-lookup"><span data-stu-id="11328-103">Create officeSuiteApp</span></span>

> <span data-ttu-id="11328-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="11328-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="11328-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="11328-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="11328-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="11328-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="11328-107">Crear un nuevo objeto [officeSuiteApp](../resources/intune-apps-officesuiteapp.md) .</span><span class="sxs-lookup"><span data-stu-id="11328-107">Create a new [officeSuiteApp](../resources/intune-apps-officesuiteapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="11328-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="11328-108">Prerequisites</span></span>
<span data-ttu-id="11328-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="11328-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="11328-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="11328-111">Permission type</span></span>|<span data-ttu-id="11328-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="11328-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="11328-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="11328-113">Delegated (work or school account)</span></span>|<span data-ttu-id="11328-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="11328-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="11328-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="11328-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="11328-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="11328-116">Not supported.</span></span>|
|<span data-ttu-id="11328-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="11328-117">Application</span></span>|<span data-ttu-id="11328-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="11328-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="11328-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="11328-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="11328-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="11328-120">Request headers</span></span>
|<span data-ttu-id="11328-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11328-121">Header</span></span>|<span data-ttu-id="11328-122">Valor</span><span class="sxs-lookup"><span data-stu-id="11328-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="11328-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="11328-123">Authorization</span></span>|<span data-ttu-id="11328-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="11328-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="11328-125">Accept</span><span class="sxs-lookup"><span data-stu-id="11328-125">Accept</span></span>|<span data-ttu-id="11328-126">application/json</span><span class="sxs-lookup"><span data-stu-id="11328-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="11328-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="11328-127">Request body</span></span>
<span data-ttu-id="11328-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto officeSuiteApp.</span><span class="sxs-lookup"><span data-stu-id="11328-128">In the request body, supply a JSON representation for the officeSuiteApp object.</span></span>

<span data-ttu-id="11328-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el officeSuiteApp.</span><span class="sxs-lookup"><span data-stu-id="11328-129">The following table shows the properties that are required when you create the officeSuiteApp.</span></span>

|<span data-ttu-id="11328-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="11328-130">Property</span></span>|<span data-ttu-id="11328-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="11328-131">Type</span></span>|<span data-ttu-id="11328-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="11328-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="11328-133">id</span><span class="sxs-lookup"><span data-stu-id="11328-133">id</span></span>|<span data-ttu-id="11328-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="11328-134">String</span></span>|<span data-ttu-id="11328-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="11328-135">Key of the entity.</span></span> <span data-ttu-id="11328-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="11328-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="11328-137">displayName</span><span class="sxs-lookup"><span data-stu-id="11328-137">displayName</span></span>|<span data-ttu-id="11328-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="11328-138">String</span></span>|<span data-ttu-id="11328-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="11328-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="11328-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="11328-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="11328-141">descripción</span><span class="sxs-lookup"><span data-stu-id="11328-141">description</span></span>|<span data-ttu-id="11328-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="11328-142">String</span></span>|<span data-ttu-id="11328-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="11328-143">The description of the app.</span></span> <span data-ttu-id="11328-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="11328-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="11328-145">publicador</span><span class="sxs-lookup"><span data-stu-id="11328-145">publisher</span></span>|<span data-ttu-id="11328-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="11328-146">String</span></span>|<span data-ttu-id="11328-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="11328-147">The publisher of the app.</span></span> <span data-ttu-id="11328-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="11328-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="11328-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="11328-149">largeIcon</span></span>|[<span data-ttu-id="11328-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="11328-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="11328-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="11328-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="11328-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="11328-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="11328-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="11328-153">createdDateTime</span></span>|<span data-ttu-id="11328-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="11328-154">DateTimeOffset</span></span>|<span data-ttu-id="11328-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="11328-155">The date and time the app was created.</span></span> <span data-ttu-id="11328-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="11328-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="11328-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="11328-157">lastModifiedDateTime</span></span>|<span data-ttu-id="11328-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="11328-158">DateTimeOffset</span></span>|<span data-ttu-id="11328-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="11328-159">The date and time the app was last modified.</span></span> <span data-ttu-id="11328-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="11328-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="11328-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="11328-161">isFeatured</span></span>|<span data-ttu-id="11328-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="11328-162">Boolean</span></span>|<span data-ttu-id="11328-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="11328-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="11328-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="11328-164">privacyInformationUrl</span></span>|<span data-ttu-id="11328-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="11328-165">String</span></span>|<span data-ttu-id="11328-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="11328-166">The privacy statement Url.</span></span> <span data-ttu-id="11328-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="11328-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="11328-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="11328-168">informationUrl</span></span>|<span data-ttu-id="11328-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="11328-169">String</span></span>|<span data-ttu-id="11328-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="11328-170">The more information Url.</span></span> <span data-ttu-id="11328-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="11328-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="11328-172">owner</span><span class="sxs-lookup"><span data-stu-id="11328-172">owner</span></span>|<span data-ttu-id="11328-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="11328-173">String</span></span>|<span data-ttu-id="11328-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="11328-174">The owner of the app.</span></span> <span data-ttu-id="11328-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="11328-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="11328-176">developer</span><span class="sxs-lookup"><span data-stu-id="11328-176">developer</span></span>|<span data-ttu-id="11328-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="11328-177">String</span></span>|<span data-ttu-id="11328-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="11328-178">The developer of the app.</span></span> <span data-ttu-id="11328-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="11328-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="11328-180">notas</span><span class="sxs-lookup"><span data-stu-id="11328-180">notes</span></span>|<span data-ttu-id="11328-181">Cadena</span><span class="sxs-lookup"><span data-stu-id="11328-181">String</span></span>|<span data-ttu-id="11328-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="11328-182">Notes for the app.</span></span> <span data-ttu-id="11328-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="11328-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="11328-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="11328-184">uploadState</span></span>|<span data-ttu-id="11328-185">Int32</span><span class="sxs-lookup"><span data-stu-id="11328-185">Int32</span></span>|<span data-ttu-id="11328-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="11328-186">The upload state.</span></span> <span data-ttu-id="11328-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="11328-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="11328-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="11328-188">publishingState</span></span>|[<span data-ttu-id="11328-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="11328-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="11328-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="11328-190">The publishing state for the app.</span></span> <span data-ttu-id="11328-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="11328-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="11328-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="11328-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="11328-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="11328-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="11328-194">autoAcceptEula</span><span class="sxs-lookup"><span data-stu-id="11328-194">autoAcceptEula</span></span>|<span data-ttu-id="11328-195">Booleano</span><span class="sxs-lookup"><span data-stu-id="11328-195">Boolean</span></span>|<span data-ttu-id="11328-196">El valor que acepte al CLUF automáticamente en el dispositivo de la para el usuario final.</span><span class="sxs-lookup"><span data-stu-id="11328-196">The value to accept the EULA automatically on the enduser's device.</span></span>|
|<span data-ttu-id="11328-197">Datos</span><span class="sxs-lookup"><span data-stu-id="11328-197">productIds</span></span>|<span data-ttu-id="11328-198">colección de [officeProductId](../resources/intune-apps-officeproductid.md)</span><span class="sxs-lookup"><span data-stu-id="11328-198">[officeProductId](../resources/intune-apps-officeproductid.md) collection</span></span>|<span data-ttu-id="11328-199">Los identificadores de producto que representan la SKU del conjunto de aplicaciones de Office365.</span><span class="sxs-lookup"><span data-stu-id="11328-199">The Product Ids that represent the Office365 Suite SKU.</span></span> <span data-ttu-id="11328-200">Los valores posibles son: `o365ProPlusRetail`, `o365BusinessRetail`, `visioProRetail` y `projectProRetail`.</span><span class="sxs-lookup"><span data-stu-id="11328-200">Possible values are: `o365ProPlusRetail`, `o365BusinessRetail`, `visioProRetail`, `projectProRetail`.</span></span>|
|<span data-ttu-id="11328-201">excludedApps</span><span class="sxs-lookup"><span data-stu-id="11328-201">excludedApps</span></span>|[<span data-ttu-id="11328-202">excludedApps</span><span class="sxs-lookup"><span data-stu-id="11328-202">excludedApps</span></span>](../resources/intune-apps-excludedapps.md)|<span data-ttu-id="11328-203">La propiedad para representar las aplicaciones que se excluirán del producto seleccionado de Office365 Id.</span><span class="sxs-lookup"><span data-stu-id="11328-203">The property to represent the apps which are excluded from the selected Office365 Product Id.</span></span>|
|<span data-ttu-id="11328-204">useSharedComputerActivation</span><span class="sxs-lookup"><span data-stu-id="11328-204">useSharedComputerActivation</span></span>|<span data-ttu-id="11328-205">Booleano</span><span class="sxs-lookup"><span data-stu-id="11328-205">Boolean</span></span>|<span data-ttu-id="11328-206">La propiedad para representar si se usa la activación del equipo compartido no para el conjunto de aplicaciones de Office365 app.</span><span class="sxs-lookup"><span data-stu-id="11328-206">The property to represent that whether the shared computer activation is used not for Office365 app suite.</span></span>|
|<span data-ttu-id="11328-207">updateChannel</span><span class="sxs-lookup"><span data-stu-id="11328-207">updateChannel</span></span>|[<span data-ttu-id="11328-208">officeUpdateChannel</span><span class="sxs-lookup"><span data-stu-id="11328-208">officeUpdateChannel</span></span>](../resources/intune-apps-officeupdatechannel.md)|<span data-ttu-id="11328-209">La propiedad para representar el canal de actualización de Office365.</span><span class="sxs-lookup"><span data-stu-id="11328-209">The property to represent the Office365 Update Channel.</span></span> <span data-ttu-id="11328-210">Los valores posibles son: `none`, `current`, `deferred`, `firstReleaseCurrent` y `firstReleaseDeferred`.</span><span class="sxs-lookup"><span data-stu-id="11328-210">Possible values are: `none`, `current`, `deferred`, `firstReleaseCurrent`, `firstReleaseDeferred`.</span></span>|
|<span data-ttu-id="11328-211">officePlatformArchitecture</span><span class="sxs-lookup"><span data-stu-id="11328-211">officePlatformArchitecture</span></span>|[<span data-ttu-id="11328-212">windowsArchitecture</span><span class="sxs-lookup"><span data-stu-id="11328-212">windowsArchitecture</span></span>](../resources/intune-apps-windowsarchitecture.md)|<span data-ttu-id="11328-213">La propiedad para representar la versión de conjunto de programas de aplicación de Office365.</span><span class="sxs-lookup"><span data-stu-id="11328-213">The property to represent the Office365 app suite version.</span></span> <span data-ttu-id="11328-214">Los valores posibles son: `none`, `x86`, `x64`, `arm` y `neutral`.</span><span class="sxs-lookup"><span data-stu-id="11328-214">Possible values are: `none`, `x86`, `x64`, `arm`, `neutral`.</span></span>|
|<span data-ttu-id="11328-215">localesToInstall</span><span class="sxs-lookup"><span data-stu-id="11328-215">localesToInstall</span></span>|<span data-ttu-id="11328-216">Colección String</span><span class="sxs-lookup"><span data-stu-id="11328-216">String collection</span></span>|<span data-ttu-id="11328-217">La propiedad para representar las configuraciones regionales que se instalan cuando se instala las aplicaciones de Office365.</span><span class="sxs-lookup"><span data-stu-id="11328-217">The property to represent the locales which are installed when the apps from Office365 is installed.</span></span> <span data-ttu-id="11328-218">Se utiliza 6033 de RFC estándar.</span><span class="sxs-lookup"><span data-stu-id="11328-218">It uses standard RFC 6033.</span></span> <span data-ttu-id="11328-219">Ref:https://technet.microsoft.com/en-us/library/cc179219(v=office.16).aspx</span><span class="sxs-lookup"><span data-stu-id="11328-219">Ref: https://technet.microsoft.com/en-us/library/cc179219(v=office.16).aspx</span></span>|
|<span data-ttu-id="11328-220">installProgressDisplayLevel</span><span class="sxs-lookup"><span data-stu-id="11328-220">installProgressDisplayLevel</span></span>|[<span data-ttu-id="11328-221">officeSuiteInstallProgressDisplayLevel</span><span class="sxs-lookup"><span data-stu-id="11328-221">officeSuiteInstallProgressDisplayLevel</span></span>](../resources/intune-apps-officesuiteinstallprogressdisplaylevel.md)|<span data-ttu-id="11328-222">Para especificar el nivel de presentación para la interfaz de usuario de instalación progreso del programa de instalación en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="11328-222">To specify the level of display for the Installation Progress Setup UI on the Device.</span></span> <span data-ttu-id="11328-223">Los valores posibles son: `none` y `full`.</span><span class="sxs-lookup"><span data-stu-id="11328-223">Possible values are: `none`, `full`.</span></span>|
|<span data-ttu-id="11328-224">shouldUninstallOlderVersionsOfOffice</span><span class="sxs-lookup"><span data-stu-id="11328-224">shouldUninstallOlderVersionsOfOffice</span></span>|<span data-ttu-id="11328-225">Booleano</span><span class="sxs-lookup"><span data-stu-id="11328-225">Boolean</span></span>|<span data-ttu-id="11328-226">La propiedad para determinar si debe desinstalar MSI de Office existente si se implementa un conjunto de aplicaciones de la aplicación Office365 en el dispositivo o no.</span><span class="sxs-lookup"><span data-stu-id="11328-226">The property to determine whether to uninstall existing Office MSI if an Office365 app suite is deployed to the device or not.</span></span>|
|<span data-ttu-id="11328-227">targetVersion</span><span class="sxs-lookup"><span data-stu-id="11328-227">targetVersion</span></span>|<span data-ttu-id="11328-228">Cadena</span><span class="sxs-lookup"><span data-stu-id="11328-228">String</span></span>|<span data-ttu-id="11328-229">La propiedad para representar la versión de destino específico para el conjunto de aplicaciones de la aplicación de Office365 que debe se mantuvo implementado en los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="11328-229">The property to represent the specific target version for the Office365 app suite that should be remained deployed on the devices.</span></span>|
|<span data-ttu-id="11328-230">updateVersion</span><span class="sxs-lookup"><span data-stu-id="11328-230">updateVersion</span></span>|<span data-ttu-id="11328-231">Cadena</span><span class="sxs-lookup"><span data-stu-id="11328-231">String</span></span>|<span data-ttu-id="11328-232">La propiedad para representar la versión de actualización en la que está disponible para el conjunto de aplicaciones de la aplicación Office365 la versión de destino específica.</span><span class="sxs-lookup"><span data-stu-id="11328-232">The property to represent the update version in which the specific target version is available for the Office365 app suite.</span></span>|



## <a name="response"></a><span data-ttu-id="11328-233">Respuesta</span><span class="sxs-lookup"><span data-stu-id="11328-233">Response</span></span>
<span data-ttu-id="11328-234">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [officeSuiteApp](../resources/intune-apps-officesuiteapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="11328-234">If successful, this method returns a `201 Created` response code and a [officeSuiteApp](../resources/intune-apps-officesuiteapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="11328-235">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="11328-235">Example</span></span>
### <a name="request"></a><span data-ttu-id="11328-236">Solicitud</span><span class="sxs-lookup"><span data-stu-id="11328-236">Request</span></span>
<span data-ttu-id="11328-237">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="11328-237">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 1466

{
  "@odata.type": "#microsoft.graph.officeSuiteApp",
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
  "autoAcceptEula": true,
  "productIds": [
    "o365BusinessRetail"
  ],
  "excludedApps": {
    "@odata.type": "microsoft.graph.excludedApps",
    "access": true,
    "excel": true,
    "groove": true,
    "infoPath": true,
    "lync": true,
    "oneDrive": true,
    "oneNote": true,
    "outlook": true,
    "powerPoint": true,
    "publisher": true,
    "sharePointDesigner": true,
    "visio": true,
    "word": true
  },
  "useSharedComputerActivation": true,
  "updateChannel": "current",
  "officePlatformArchitecture": "x86",
  "localesToInstall": [
    "Locales To Install value"
  ],
  "installProgressDisplayLevel": "full",
  "shouldUninstallOlderVersionsOfOffice": true,
  "targetVersion": "Target Version value",
  "updateVersion": "Update Version value"
}
```

### <a name="response"></a><span data-ttu-id="11328-238">Respuesta</span><span class="sxs-lookup"><span data-stu-id="11328-238">Response</span></span>
<span data-ttu-id="11328-p122">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="11328-p122">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1574

{
  "@odata.type": "#microsoft.graph.officeSuiteApp",
  "id": "9b263b46-3b46-9b26-463b-269b463b269b",
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
  "autoAcceptEula": true,
  "productIds": [
    "o365BusinessRetail"
  ],
  "excludedApps": {
    "@odata.type": "microsoft.graph.excludedApps",
    "access": true,
    "excel": true,
    "groove": true,
    "infoPath": true,
    "lync": true,
    "oneDrive": true,
    "oneNote": true,
    "outlook": true,
    "powerPoint": true,
    "publisher": true,
    "sharePointDesigner": true,
    "visio": true,
    "word": true
  },
  "useSharedComputerActivation": true,
  "updateChannel": "current",
  "officePlatformArchitecture": "x86",
  "localesToInstall": [
    "Locales To Install value"
  ],
  "installProgressDisplayLevel": "full",
  "shouldUninstallOlderVersionsOfOffice": true,
  "targetVersion": "Target Version value",
  "updateVersion": "Update Version value"
}
```





