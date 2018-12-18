---
title: Actualizar windowsPhone81AppX
description: Actualizar las propiedades de un objeto windowsPhone81AppX.
author: tfitzmac
ms.openlocfilehash: 7ebd110bd76797682ebd9a53b72e661e9e71d583
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27321619"
---
# <a name="update-windowsphone81appx"></a><span data-ttu-id="491d7-103">Actualizar windowsPhone81AppX</span><span class="sxs-lookup"><span data-stu-id="491d7-103">Update windowsPhone81AppX</span></span>

> <span data-ttu-id="491d7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="491d7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="491d7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="491d7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="491d7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="491d7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="491d7-107">Actualizar las propiedades de un objeto [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md) .</span><span class="sxs-lookup"><span data-stu-id="491d7-107">Update the properties of a [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="491d7-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="491d7-108">Prerequisites</span></span>
<span data-ttu-id="491d7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="491d7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="491d7-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="491d7-111">Permission type</span></span>|<span data-ttu-id="491d7-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="491d7-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="491d7-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="491d7-113">Delegated (work or school account)</span></span>|<span data-ttu-id="491d7-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="491d7-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="491d7-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="491d7-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="491d7-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="491d7-116">Not supported.</span></span>|
|<span data-ttu-id="491d7-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="491d7-117">Application</span></span>|<span data-ttu-id="491d7-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="491d7-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="491d7-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="491d7-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="request-headers"></a><span data-ttu-id="491d7-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="491d7-120">Request headers</span></span>
|<span data-ttu-id="491d7-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="491d7-121">Header</span></span>|<span data-ttu-id="491d7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="491d7-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="491d7-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="491d7-123">Authorization</span></span>|<span data-ttu-id="491d7-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="491d7-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="491d7-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="491d7-125">Accept</span></span>|<span data-ttu-id="491d7-126">application/json</span><span class="sxs-lookup"><span data-stu-id="491d7-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="491d7-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="491d7-127">Request body</span></span>
<span data-ttu-id="491d7-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md) .</span><span class="sxs-lookup"><span data-stu-id="491d7-128">In the request body, supply a JSON representation for the [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md) object.</span></span>

<span data-ttu-id="491d7-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md).</span><span class="sxs-lookup"><span data-stu-id="491d7-129">The following table shows the properties that are required when you create the [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md).</span></span>

|<span data-ttu-id="491d7-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="491d7-130">Property</span></span>|<span data-ttu-id="491d7-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="491d7-131">Type</span></span>|<span data-ttu-id="491d7-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="491d7-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="491d7-133">id</span><span class="sxs-lookup"><span data-stu-id="491d7-133">id</span></span>|<span data-ttu-id="491d7-134">String</span><span class="sxs-lookup"><span data-stu-id="491d7-134">String</span></span>|<span data-ttu-id="491d7-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="491d7-135">Key of the entity.</span></span> <span data-ttu-id="491d7-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="491d7-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="491d7-137">displayName</span><span class="sxs-lookup"><span data-stu-id="491d7-137">displayName</span></span>|<span data-ttu-id="491d7-138">String</span><span class="sxs-lookup"><span data-stu-id="491d7-138">String</span></span>|<span data-ttu-id="491d7-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="491d7-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="491d7-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="491d7-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="491d7-141">descripción</span><span class="sxs-lookup"><span data-stu-id="491d7-141">description</span></span>|<span data-ttu-id="491d7-142">String</span><span class="sxs-lookup"><span data-stu-id="491d7-142">String</span></span>|<span data-ttu-id="491d7-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="491d7-143">The description of the app.</span></span> <span data-ttu-id="491d7-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="491d7-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="491d7-145">publicador</span><span class="sxs-lookup"><span data-stu-id="491d7-145">publisher</span></span>|<span data-ttu-id="491d7-146">String</span><span class="sxs-lookup"><span data-stu-id="491d7-146">String</span></span>|<span data-ttu-id="491d7-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="491d7-147">The publisher of the app.</span></span> <span data-ttu-id="491d7-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="491d7-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="491d7-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="491d7-149">largeIcon</span></span>|[<span data-ttu-id="491d7-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="491d7-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="491d7-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="491d7-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="491d7-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="491d7-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="491d7-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="491d7-153">createdDateTime</span></span>|<span data-ttu-id="491d7-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="491d7-154">DateTimeOffset</span></span>|<span data-ttu-id="491d7-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="491d7-155">The date and time the app was created.</span></span> <span data-ttu-id="491d7-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="491d7-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="491d7-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="491d7-157">lastModifiedDateTime</span></span>|<span data-ttu-id="491d7-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="491d7-158">DateTimeOffset</span></span>|<span data-ttu-id="491d7-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="491d7-159">The date and time the app was last modified.</span></span> <span data-ttu-id="491d7-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="491d7-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="491d7-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="491d7-161">isFeatured</span></span>|<span data-ttu-id="491d7-162">Boolean</span><span class="sxs-lookup"><span data-stu-id="491d7-162">Boolean</span></span>|<span data-ttu-id="491d7-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="491d7-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="491d7-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="491d7-164">privacyInformationUrl</span></span>|<span data-ttu-id="491d7-165">String</span><span class="sxs-lookup"><span data-stu-id="491d7-165">String</span></span>|<span data-ttu-id="491d7-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="491d7-166">The privacy statement Url.</span></span> <span data-ttu-id="491d7-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="491d7-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="491d7-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="491d7-168">informationUrl</span></span>|<span data-ttu-id="491d7-169">String</span><span class="sxs-lookup"><span data-stu-id="491d7-169">String</span></span>|<span data-ttu-id="491d7-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="491d7-170">The more information Url.</span></span> <span data-ttu-id="491d7-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="491d7-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="491d7-172">owner</span><span class="sxs-lookup"><span data-stu-id="491d7-172">owner</span></span>|<span data-ttu-id="491d7-173">String</span><span class="sxs-lookup"><span data-stu-id="491d7-173">String</span></span>|<span data-ttu-id="491d7-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="491d7-174">The owner of the app.</span></span> <span data-ttu-id="491d7-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="491d7-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="491d7-176">developer</span><span class="sxs-lookup"><span data-stu-id="491d7-176">developer</span></span>|<span data-ttu-id="491d7-177">String</span><span class="sxs-lookup"><span data-stu-id="491d7-177">String</span></span>|<span data-ttu-id="491d7-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="491d7-178">The developer of the app.</span></span> <span data-ttu-id="491d7-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="491d7-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="491d7-180">notas</span><span class="sxs-lookup"><span data-stu-id="491d7-180">notes</span></span>|<span data-ttu-id="491d7-181">String</span><span class="sxs-lookup"><span data-stu-id="491d7-181">String</span></span>|<span data-ttu-id="491d7-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="491d7-182">Notes for the app.</span></span> <span data-ttu-id="491d7-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="491d7-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="491d7-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="491d7-184">uploadState</span></span>|<span data-ttu-id="491d7-185">Int32</span><span class="sxs-lookup"><span data-stu-id="491d7-185">Int32</span></span>|<span data-ttu-id="491d7-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="491d7-186">The upload state.</span></span> <span data-ttu-id="491d7-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="491d7-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="491d7-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="491d7-188">publishingState</span></span>|[<span data-ttu-id="491d7-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="491d7-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="491d7-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="491d7-190">The publishing state for the app.</span></span> <span data-ttu-id="491d7-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="491d7-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="491d7-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="491d7-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="491d7-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="491d7-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="491d7-194">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="491d7-194">committedContentVersion</span></span>|<span data-ttu-id="491d7-195">String</span><span class="sxs-lookup"><span data-stu-id="491d7-195">String</span></span>|<span data-ttu-id="491d7-196">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="491d7-196">The internal committed content version.</span></span> <span data-ttu-id="491d7-197">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="491d7-197">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="491d7-198">fileName</span><span class="sxs-lookup"><span data-stu-id="491d7-198">fileName</span></span>|<span data-ttu-id="491d7-199">String</span><span class="sxs-lookup"><span data-stu-id="491d7-199">String</span></span>|<span data-ttu-id="491d7-200">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="491d7-200">The name of the main Lob application file.</span></span> <span data-ttu-id="491d7-201">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="491d7-201">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="491d7-202">size</span><span class="sxs-lookup"><span data-stu-id="491d7-202">size</span></span>|<span data-ttu-id="491d7-203">Int64</span><span class="sxs-lookup"><span data-stu-id="491d7-203">Int64</span></span>|<span data-ttu-id="491d7-204">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="491d7-204">The total size, including all uploaded files.</span></span> <span data-ttu-id="491d7-205">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="491d7-205">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="491d7-206">applicableArchitectures</span><span class="sxs-lookup"><span data-stu-id="491d7-206">applicableArchitectures</span></span>|[<span data-ttu-id="491d7-207">windowsArchitecture</span><span class="sxs-lookup"><span data-stu-id="491d7-207">windowsArchitecture</span></span>](../resources/intune-apps-windowsarchitecture.md)|<span data-ttu-id="491d7-208">Arquitecturas de Windows en las que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="491d7-208">The Windows architecture(s) for which this app can run on.</span></span> <span data-ttu-id="491d7-209">Los valores posibles son: `none`, `x86`, `x64`, `arm` y `neutral`.</span><span class="sxs-lookup"><span data-stu-id="491d7-209">Possible values are: `none`, `x86`, `x64`, `arm`, `neutral`.</span></span>|
|<span data-ttu-id="491d7-210">identityName</span><span class="sxs-lookup"><span data-stu-id="491d7-210">identityName</span></span>|<span data-ttu-id="491d7-211">String</span><span class="sxs-lookup"><span data-stu-id="491d7-211">String</span></span>|<span data-ttu-id="491d7-212">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="491d7-212">The Identity Name.</span></span>|
|<span data-ttu-id="491d7-213">identityPublisherHash</span><span class="sxs-lookup"><span data-stu-id="491d7-213">identityPublisherHash</span></span>|<span data-ttu-id="491d7-214">String</span><span class="sxs-lookup"><span data-stu-id="491d7-214">String</span></span>|<span data-ttu-id="491d7-215">Hash del publicador de identidad.</span><span class="sxs-lookup"><span data-stu-id="491d7-215">The Identity Publisher Hash.</span></span>|
|<span data-ttu-id="491d7-216">identityResourceIdentifier</span><span class="sxs-lookup"><span data-stu-id="491d7-216">identityResourceIdentifier</span></span>|<span data-ttu-id="491d7-217">String</span><span class="sxs-lookup"><span data-stu-id="491d7-217">String</span></span>|<span data-ttu-id="491d7-218">Identificador del recurso de identidad.</span><span class="sxs-lookup"><span data-stu-id="491d7-218">The Identity Resource Identifier.</span></span>|
|<span data-ttu-id="491d7-219">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="491d7-219">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="491d7-220">windowsMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="491d7-220">windowsMinimumOperatingSystem</span></span>](../resources/intune-apps-windowsminimumoperatingsystem.md)|<span data-ttu-id="491d7-221">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="491d7-221">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="491d7-222">phoneProductIdentifier</span><span class="sxs-lookup"><span data-stu-id="491d7-222">phoneProductIdentifier</span></span>|<span data-ttu-id="491d7-223">String</span><span class="sxs-lookup"><span data-stu-id="491d7-223">String</span></span>|<span data-ttu-id="491d7-224">El identificador de producto del teléfono.</span><span class="sxs-lookup"><span data-stu-id="491d7-224">The Phone Product Identifier.</span></span>|
|<span data-ttu-id="491d7-225">phonePublisherId</span><span class="sxs-lookup"><span data-stu-id="491d7-225">phonePublisherId</span></span>|<span data-ttu-id="491d7-226">String</span><span class="sxs-lookup"><span data-stu-id="491d7-226">String</span></span>|<span data-ttu-id="491d7-227">El identificador de Publisher de teléfono.</span><span class="sxs-lookup"><span data-stu-id="491d7-227">The Phone Publisher Id.</span></span>|
|<span data-ttu-id="491d7-228">identityVersion</span><span class="sxs-lookup"><span data-stu-id="491d7-228">identityVersion</span></span>|<span data-ttu-id="491d7-229">String</span><span class="sxs-lookup"><span data-stu-id="491d7-229">String</span></span>|<span data-ttu-id="491d7-230">Versión de la identidad.</span><span class="sxs-lookup"><span data-stu-id="491d7-230">The identity version.</span></span>|



## <a name="response"></a><span data-ttu-id="491d7-231">Respuesta</span><span class="sxs-lookup"><span data-stu-id="491d7-231">Response</span></span>
<span data-ttu-id="491d7-232">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="491d7-232">If successful, this method returns a `200 OK` response code and an updated [windowsPhone81AppX](../resources/intune-apps-windowsphone81appx.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="491d7-233">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="491d7-233">Example</span></span>
### <a name="request"></a><span data-ttu-id="491d7-234">Solicitud</span><span class="sxs-lookup"><span data-stu-id="491d7-234">Request</span></span>
<span data-ttu-id="491d7-235">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="491d7-235">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1362

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
  "committedContentVersion": "Committed Content Version value",
  "fileName": "File Name value",
  "size": 4,
  "applicableArchitectures": "x86",
  "identityName": "Identity Name value",
  "identityPublisherHash": "Identity Publisher Hash value",
  "identityResourceIdentifier": "Identity Resource Identifier value",
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem",
    "v8_0": true,
    "v8_1": true,
    "v10_0": true,
    "v10_1607": true,
    "v10_1703": true,
    "v10_1709": true,
    "v10_1803": true
  },
  "phoneProductIdentifier": "Phone Product Identifier value",
  "phonePublisherId": "Phone Publisher Id value",
  "identityVersion": "Identity Version value"
}
```

### <a name="response"></a><span data-ttu-id="491d7-236">Respuesta</span><span class="sxs-lookup"><span data-stu-id="491d7-236">Response</span></span>
<span data-ttu-id="491d7-p121">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="491d7-p121">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1527

{
  "@odata.type": "#microsoft.graph.windowsPhone81AppX",
  "id": "4ff27f80-7f80-4ff2-807f-f24f807ff24f",
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
  "committedContentVersion": "Committed Content Version value",
  "fileName": "File Name value",
  "size": 4,
  "applicableArchitectures": "x86",
  "identityName": "Identity Name value",
  "identityPublisherHash": "Identity Publisher Hash value",
  "identityResourceIdentifier": "Identity Resource Identifier value",
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem",
    "v8_0": true,
    "v8_1": true,
    "v10_0": true,
    "v10_1607": true,
    "v10_1703": true,
    "v10_1709": true,
    "v10_1803": true
  },
  "phoneProductIdentifier": "Phone Product Identifier value",
  "phonePublisherId": "Phone Publisher Id value",
  "identityVersion": "Identity Version value"
}
```





