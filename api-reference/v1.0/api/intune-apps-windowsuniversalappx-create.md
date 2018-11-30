---
title: Crear windowsUniversalAppX
description: Crear un objeto windowsUniversalAppX.
ms.openlocfilehash: eee8edddb8376b33f4e357803d55bded0f604ae4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030773"
---
# <a name="create-windowsuniversalappx"></a><span data-ttu-id="cdfaf-103">Crear windowsUniversalAppX</span><span class="sxs-lookup"><span data-stu-id="cdfaf-103">Create windowsUniversalAppX</span></span>

> <span data-ttu-id="cdfaf-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cdfaf-105">Crear un objeto [windowsUniversalAppX](../resources/intune-apps-windowsuniversalappx.md).</span><span class="sxs-lookup"><span data-stu-id="cdfaf-105">Create a new [windowsUniversalAppX](../resources/intune-apps-windowsuniversalappx.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cdfaf-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cdfaf-106">Prerequisites</span></span>
<span data-ttu-id="cdfaf-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cdfaf-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cdfaf-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cdfaf-109">Permission type</span></span>|<span data-ttu-id="cdfaf-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cdfaf-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="cdfaf-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cdfaf-111">Delegated (work or school account)</span></span>|<span data-ttu-id="cdfaf-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cdfaf-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="cdfaf-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cdfaf-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="cdfaf-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-114">Not supported.</span></span>|
|<span data-ttu-id="cdfaf-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cdfaf-115">Application</span></span>|<span data-ttu-id="cdfaf-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="cdfaf-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cdfaf-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="cdfaf-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cdfaf-118">Request headers</span></span>
|<span data-ttu-id="cdfaf-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cdfaf-119">Header</span></span>|<span data-ttu-id="cdfaf-120">Valor</span><span class="sxs-lookup"><span data-stu-id="cdfaf-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="cdfaf-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="cdfaf-121">Authorization</span></span>|<span data-ttu-id="cdfaf-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="cdfaf-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="cdfaf-123">Accept</span></span>|<span data-ttu-id="cdfaf-124">application/json</span><span class="sxs-lookup"><span data-stu-id="cdfaf-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="cdfaf-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cdfaf-125">Request body</span></span>
<span data-ttu-id="cdfaf-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsUniversalAppX.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-126">In the request body, supply a JSON representation for the windowsUniversalAppX object.</span></span>

<span data-ttu-id="cdfaf-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsUniversalAppX.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-127">The following table shows the properties that are required when you create the windowsUniversalAppX.</span></span>

|<span data-ttu-id="cdfaf-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cdfaf-128">Property</span></span>|<span data-ttu-id="cdfaf-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="cdfaf-129">Type</span></span>|<span data-ttu-id="cdfaf-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="cdfaf-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cdfaf-131">id</span><span class="sxs-lookup"><span data-stu-id="cdfaf-131">id</span></span>|<span data-ttu-id="cdfaf-132">String</span><span class="sxs-lookup"><span data-stu-id="cdfaf-132">String</span></span>|<span data-ttu-id="cdfaf-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-133">Key of the entity.</span></span> <span data-ttu-id="cdfaf-134">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cdfaf-134">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cdfaf-135">displayName</span><span class="sxs-lookup"><span data-stu-id="cdfaf-135">displayName</span></span>|<span data-ttu-id="cdfaf-136">String</span><span class="sxs-lookup"><span data-stu-id="cdfaf-136">String</span></span>|<span data-ttu-id="cdfaf-137">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-137">The admin provided or imported title of the app.</span></span> <span data-ttu-id="cdfaf-138">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cdfaf-138">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cdfaf-139">descripción</span><span class="sxs-lookup"><span data-stu-id="cdfaf-139">description</span></span>|<span data-ttu-id="cdfaf-140">String</span><span class="sxs-lookup"><span data-stu-id="cdfaf-140">String</span></span>|<span data-ttu-id="cdfaf-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-141">The description of the app.</span></span> <span data-ttu-id="cdfaf-142">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cdfaf-142">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cdfaf-143">publicador</span><span class="sxs-lookup"><span data-stu-id="cdfaf-143">publisher</span></span>|<span data-ttu-id="cdfaf-144">String</span><span class="sxs-lookup"><span data-stu-id="cdfaf-144">String</span></span>|<span data-ttu-id="cdfaf-145">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-145">The publisher of the app.</span></span> <span data-ttu-id="cdfaf-146">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cdfaf-146">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cdfaf-147">largeIcon</span><span class="sxs-lookup"><span data-stu-id="cdfaf-147">largeIcon</span></span>|[<span data-ttu-id="cdfaf-148">mimeContent</span><span class="sxs-lookup"><span data-stu-id="cdfaf-148">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="cdfaf-149">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-149">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="cdfaf-150">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cdfaf-150">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cdfaf-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="cdfaf-151">createdDateTime</span></span>|<span data-ttu-id="cdfaf-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cdfaf-152">DateTimeOffset</span></span>|<span data-ttu-id="cdfaf-153">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-153">The date and time the app was created.</span></span> <span data-ttu-id="cdfaf-154">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cdfaf-154">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cdfaf-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="cdfaf-155">lastModifiedDateTime</span></span>|<span data-ttu-id="cdfaf-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cdfaf-156">DateTimeOffset</span></span>|<span data-ttu-id="cdfaf-157">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-157">The date and time the app was last modified.</span></span> <span data-ttu-id="cdfaf-158">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cdfaf-158">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cdfaf-159">isFeatured</span><span class="sxs-lookup"><span data-stu-id="cdfaf-159">isFeatured</span></span>|<span data-ttu-id="cdfaf-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="cdfaf-160">Boolean</span></span>|<span data-ttu-id="cdfaf-161">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cdfaf-161">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cdfaf-162">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="cdfaf-162">privacyInformationUrl</span></span>|<span data-ttu-id="cdfaf-163">String</span><span class="sxs-lookup"><span data-stu-id="cdfaf-163">String</span></span>|<span data-ttu-id="cdfaf-164">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-164">The privacy statement Url.</span></span> <span data-ttu-id="cdfaf-165">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cdfaf-165">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cdfaf-166">informationUrl</span><span class="sxs-lookup"><span data-stu-id="cdfaf-166">informationUrl</span></span>|<span data-ttu-id="cdfaf-167">String</span><span class="sxs-lookup"><span data-stu-id="cdfaf-167">String</span></span>|<span data-ttu-id="cdfaf-168">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-168">The more information Url.</span></span> <span data-ttu-id="cdfaf-169">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cdfaf-169">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cdfaf-170">owner</span><span class="sxs-lookup"><span data-stu-id="cdfaf-170">owner</span></span>|<span data-ttu-id="cdfaf-171">String</span><span class="sxs-lookup"><span data-stu-id="cdfaf-171">String</span></span>|<span data-ttu-id="cdfaf-172">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-172">The owner of the app.</span></span> <span data-ttu-id="cdfaf-173">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cdfaf-173">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cdfaf-174">developer</span><span class="sxs-lookup"><span data-stu-id="cdfaf-174">developer</span></span>|<span data-ttu-id="cdfaf-175">String</span><span class="sxs-lookup"><span data-stu-id="cdfaf-175">String</span></span>|<span data-ttu-id="cdfaf-176">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-176">The developer of the app.</span></span> <span data-ttu-id="cdfaf-177">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cdfaf-177">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cdfaf-178">notas</span><span class="sxs-lookup"><span data-stu-id="cdfaf-178">notes</span></span>|<span data-ttu-id="cdfaf-179">String</span><span class="sxs-lookup"><span data-stu-id="cdfaf-179">String</span></span>|<span data-ttu-id="cdfaf-180">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-180">Notes for the app.</span></span> <span data-ttu-id="cdfaf-181">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cdfaf-181">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cdfaf-182">publishingState</span><span class="sxs-lookup"><span data-stu-id="cdfaf-182">publishingState</span></span>|[<span data-ttu-id="cdfaf-183">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="cdfaf-183">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="cdfaf-184">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-184">The publishing state for the app.</span></span> <span data-ttu-id="cdfaf-185">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-185">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="cdfaf-186">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cdfaf-186">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="cdfaf-187">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-187">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="cdfaf-188">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="cdfaf-188">committedContentVersion</span></span>|<span data-ttu-id="cdfaf-189">String</span><span class="sxs-lookup"><span data-stu-id="cdfaf-189">String</span></span>|<span data-ttu-id="cdfaf-190">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-190">The internal committed content version.</span></span> <span data-ttu-id="cdfaf-191">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="cdfaf-191">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="cdfaf-192">fileName</span><span class="sxs-lookup"><span data-stu-id="cdfaf-192">fileName</span></span>|<span data-ttu-id="cdfaf-193">String</span><span class="sxs-lookup"><span data-stu-id="cdfaf-193">String</span></span>|<span data-ttu-id="cdfaf-194">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-194">The name of the main Lob application file.</span></span> <span data-ttu-id="cdfaf-195">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="cdfaf-195">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="cdfaf-196">size</span><span class="sxs-lookup"><span data-stu-id="cdfaf-196">size</span></span>|<span data-ttu-id="cdfaf-197">Int64</span><span class="sxs-lookup"><span data-stu-id="cdfaf-197">Int64</span></span>|<span data-ttu-id="cdfaf-198">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-198">The total size, including all uploaded files.</span></span> <span data-ttu-id="cdfaf-199">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="cdfaf-199">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="cdfaf-200">applicableArchitectures</span><span class="sxs-lookup"><span data-stu-id="cdfaf-200">applicableArchitectures</span></span>|[<span data-ttu-id="cdfaf-201">windowsArchitecture</span><span class="sxs-lookup"><span data-stu-id="cdfaf-201">windowsArchitecture</span></span>](../resources/intune-apps-windowsarchitecture.md)|<span data-ttu-id="cdfaf-202">Arquitecturas de Windows en las que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-202">The Windows architecture(s) for which this app can run on.</span></span> <span data-ttu-id="cdfaf-203">Los valores posibles son: `none`, `x86`, `x64`, `arm` y `neutral`.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-203">Possible values are: `none`, `x86`, `x64`, `arm`, `neutral`.</span></span>|
|<span data-ttu-id="cdfaf-204">applicableDeviceTypes</span><span class="sxs-lookup"><span data-stu-id="cdfaf-204">applicableDeviceTypes</span></span>|[<span data-ttu-id="cdfaf-205">windowsDeviceType</span><span class="sxs-lookup"><span data-stu-id="cdfaf-205">windowsDeviceType</span></span>](../resources/intune-apps-windowsdevicetype.md)|<span data-ttu-id="cdfaf-206">Tipos de dispositivos Windows en los que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-206">The Windows device type(s) for which this app can run on.</span></span> <span data-ttu-id="cdfaf-207">Los valores posibles son: `none`, `desktop`, `mobile`, `holographic` y `team`.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-207">Possible values are: `none`, `desktop`, `mobile`, `holographic`, `team`.</span></span>|
|<span data-ttu-id="cdfaf-208">identityName</span><span class="sxs-lookup"><span data-stu-id="cdfaf-208">identityName</span></span>|<span data-ttu-id="cdfaf-209">String</span><span class="sxs-lookup"><span data-stu-id="cdfaf-209">String</span></span>|<span data-ttu-id="cdfaf-210">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-210">The Identity Name.</span></span>|
|<span data-ttu-id="cdfaf-211">identityPublisherHash</span><span class="sxs-lookup"><span data-stu-id="cdfaf-211">identityPublisherHash</span></span>|<span data-ttu-id="cdfaf-212">String</span><span class="sxs-lookup"><span data-stu-id="cdfaf-212">String</span></span>|<span data-ttu-id="cdfaf-213">Hash del publicador de identidad.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-213">The Identity Publisher Hash.</span></span>|
|<span data-ttu-id="cdfaf-214">identityResourceIdentifier</span><span class="sxs-lookup"><span data-stu-id="cdfaf-214">identityResourceIdentifier</span></span>|<span data-ttu-id="cdfaf-215">String</span><span class="sxs-lookup"><span data-stu-id="cdfaf-215">String</span></span>|<span data-ttu-id="cdfaf-216">Identificador del recurso de identidad.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-216">The Identity Resource Identifier.</span></span>|
|<span data-ttu-id="cdfaf-217">isBundle</span><span class="sxs-lookup"><span data-stu-id="cdfaf-217">isBundle</span></span>|<span data-ttu-id="cdfaf-218">Booleano</span><span class="sxs-lookup"><span data-stu-id="cdfaf-218">Boolean</span></span>|<span data-ttu-id="cdfaf-219">Indica si la aplicación es una agrupación.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-219">Whether or not the app is a bundle.</span></span>|
|<span data-ttu-id="cdfaf-220">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="cdfaf-220">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="cdfaf-221">windowsMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="cdfaf-221">windowsMinimumOperatingSystem</span></span>](../resources/intune-apps-windowsminimumoperatingsystem.md)|<span data-ttu-id="cdfaf-222">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-222">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="cdfaf-223">identityVersion</span><span class="sxs-lookup"><span data-stu-id="cdfaf-223">identityVersion</span></span>|<span data-ttu-id="cdfaf-224">String</span><span class="sxs-lookup"><span data-stu-id="cdfaf-224">String</span></span>|<span data-ttu-id="cdfaf-225">Versión de la identidad.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-225">The identity version.</span></span>|



## <a name="response"></a><span data-ttu-id="cdfaf-226">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cdfaf-226">Response</span></span>
<span data-ttu-id="cdfaf-227">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsUniversalAppX](../resources/intune-apps-windowsuniversalappx.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-227">If successful, this method returns a `201 Created` response code and a [windowsUniversalAppX](../resources/intune-apps-windowsuniversalappx.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cdfaf-228">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cdfaf-228">Example</span></span>
### <a name="request"></a><span data-ttu-id="cdfaf-229">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cdfaf-229">Request</span></span>
<span data-ttu-id="cdfaf-230">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-230">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 1189

{
  "@odata.type": "#microsoft.graph.windowsUniversalAppX",
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
  "committedContentVersion": "Committed Content Version value",
  "fileName": "File Name value",
  "size": 4,
  "applicableArchitectures": "x86",
  "applicableDeviceTypes": "desktop",
  "identityName": "Identity Name value",
  "identityPublisherHash": "Identity Publisher Hash value",
  "identityResourceIdentifier": "Identity Resource Identifier value",
  "isBundle": true,
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem",
    "v8_0": true,
    "v8_1": true,
    "v10_0": true
  },
  "identityVersion": "Identity Version value"
}
```

### <a name="response"></a><span data-ttu-id="cdfaf-231">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cdfaf-231">Response</span></span>
<span data-ttu-id="cdfaf-p120">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cdfaf-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1361

{
  "@odata.type": "#microsoft.graph.windowsUniversalAppX",
  "id": "4bc47eba-7eba-4bc4-ba7e-c44bba7ec44b",
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
  "committedContentVersion": "Committed Content Version value",
  "fileName": "File Name value",
  "size": 4,
  "applicableArchitectures": "x86",
  "applicableDeviceTypes": "desktop",
  "identityName": "Identity Name value",
  "identityPublisherHash": "Identity Publisher Hash value",
  "identityResourceIdentifier": "Identity Resource Identifier value",
  "isBundle": true,
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem",
    "v8_0": true,
    "v8_1": true,
    "v10_0": true
  },
  "identityVersion": "Identity Version value"
}
```



