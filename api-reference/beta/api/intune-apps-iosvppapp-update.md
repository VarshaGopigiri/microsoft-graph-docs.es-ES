---
title: Actualizar iosVppApp
description: Actualice las propiedades de un objeto iosVppApp.
ms.openlocfilehash: 07bc0e929b884a8933da34abf704818a992ac93f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089767"
---
# <a name="update-iosvppapp"></a><span data-ttu-id="69868-103">Actualizar iosVppApp</span><span class="sxs-lookup"><span data-stu-id="69868-103">Update iosVppApp</span></span>

> <span data-ttu-id="69868-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="69868-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="69868-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="69868-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="69868-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="69868-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="69868-107">Actualice las propiedades de un objeto [iosVppApp](../resources/intune-apps-iosvppapp.md).</span><span class="sxs-lookup"><span data-stu-id="69868-107">Update the properties of a [iosVppApp](../resources/intune-apps-iosvppapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="69868-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="69868-108">Prerequisites</span></span>
<span data-ttu-id="69868-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="69868-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="69868-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="69868-111">Permission type</span></span>|<span data-ttu-id="69868-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="69868-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="69868-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="69868-113">Delegated (work or school account)</span></span>|<span data-ttu-id="69868-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="69868-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="69868-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="69868-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="69868-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="69868-116">Not supported.</span></span>|
|<span data-ttu-id="69868-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="69868-117">Application</span></span>|<span data-ttu-id="69868-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="69868-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="69868-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="69868-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="request-headers"></a><span data-ttu-id="69868-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="69868-120">Request headers</span></span>
|<span data-ttu-id="69868-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69868-121">Header</span></span>|<span data-ttu-id="69868-122">Valor</span><span class="sxs-lookup"><span data-stu-id="69868-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="69868-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="69868-123">Authorization</span></span>|<span data-ttu-id="69868-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="69868-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="69868-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="69868-125">Accept</span></span>|<span data-ttu-id="69868-126">application/json</span><span class="sxs-lookup"><span data-stu-id="69868-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="69868-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="69868-127">Request body</span></span>
<span data-ttu-id="69868-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosVppApp](../resources/intune-apps-iosvppapp.md).</span><span class="sxs-lookup"><span data-stu-id="69868-128">In the request body, supply a JSON representation for the [iosVppApp](../resources/intune-apps-iosvppapp.md) object.</span></span>

<span data-ttu-id="69868-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosVppApp](../resources/intune-apps-iosvppapp.md).</span><span class="sxs-lookup"><span data-stu-id="69868-129">The following table shows the properties that are required when you create the [iosVppApp](../resources/intune-apps-iosvppapp.md).</span></span>

|<span data-ttu-id="69868-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="69868-130">Property</span></span>|<span data-ttu-id="69868-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="69868-131">Type</span></span>|<span data-ttu-id="69868-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="69868-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="69868-133">id</span><span class="sxs-lookup"><span data-stu-id="69868-133">id</span></span>|<span data-ttu-id="69868-134">String</span><span class="sxs-lookup"><span data-stu-id="69868-134">String</span></span>|<span data-ttu-id="69868-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="69868-135">Key of the entity.</span></span> <span data-ttu-id="69868-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69868-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="69868-137">displayName</span><span class="sxs-lookup"><span data-stu-id="69868-137">displayName</span></span>|<span data-ttu-id="69868-138">String</span><span class="sxs-lookup"><span data-stu-id="69868-138">String</span></span>|<span data-ttu-id="69868-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="69868-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="69868-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69868-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="69868-141">descripción</span><span class="sxs-lookup"><span data-stu-id="69868-141">description</span></span>|<span data-ttu-id="69868-142">String</span><span class="sxs-lookup"><span data-stu-id="69868-142">String</span></span>|<span data-ttu-id="69868-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="69868-143">The description of the app.</span></span> <span data-ttu-id="69868-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69868-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="69868-145">publicador</span><span class="sxs-lookup"><span data-stu-id="69868-145">publisher</span></span>|<span data-ttu-id="69868-146">String</span><span class="sxs-lookup"><span data-stu-id="69868-146">String</span></span>|<span data-ttu-id="69868-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="69868-147">The publisher of the app.</span></span> <span data-ttu-id="69868-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69868-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="69868-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="69868-149">largeIcon</span></span>|[<span data-ttu-id="69868-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="69868-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="69868-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="69868-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="69868-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69868-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="69868-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="69868-153">createdDateTime</span></span>|<span data-ttu-id="69868-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="69868-154">DateTimeOffset</span></span>|<span data-ttu-id="69868-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="69868-155">The date and time the app was created.</span></span> <span data-ttu-id="69868-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69868-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="69868-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="69868-157">lastModifiedDateTime</span></span>|<span data-ttu-id="69868-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="69868-158">DateTimeOffset</span></span>|<span data-ttu-id="69868-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="69868-159">The date and time the app was last modified.</span></span> <span data-ttu-id="69868-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69868-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="69868-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="69868-161">isFeatured</span></span>|<span data-ttu-id="69868-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="69868-162">Boolean</span></span>|<span data-ttu-id="69868-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69868-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="69868-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="69868-164">privacyInformationUrl</span></span>|<span data-ttu-id="69868-165">String</span><span class="sxs-lookup"><span data-stu-id="69868-165">String</span></span>|<span data-ttu-id="69868-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="69868-166">The privacy statement Url.</span></span> <span data-ttu-id="69868-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69868-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="69868-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="69868-168">informationUrl</span></span>|<span data-ttu-id="69868-169">String</span><span class="sxs-lookup"><span data-stu-id="69868-169">String</span></span>|<span data-ttu-id="69868-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="69868-170">The more information Url.</span></span> <span data-ttu-id="69868-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69868-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="69868-172">owner</span><span class="sxs-lookup"><span data-stu-id="69868-172">owner</span></span>|<span data-ttu-id="69868-173">String</span><span class="sxs-lookup"><span data-stu-id="69868-173">String</span></span>|<span data-ttu-id="69868-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="69868-174">The owner of the app.</span></span> <span data-ttu-id="69868-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69868-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="69868-176">developer</span><span class="sxs-lookup"><span data-stu-id="69868-176">developer</span></span>|<span data-ttu-id="69868-177">String</span><span class="sxs-lookup"><span data-stu-id="69868-177">String</span></span>|<span data-ttu-id="69868-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="69868-178">The developer of the app.</span></span> <span data-ttu-id="69868-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69868-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="69868-180">notas</span><span class="sxs-lookup"><span data-stu-id="69868-180">notes</span></span>|<span data-ttu-id="69868-181">String</span><span class="sxs-lookup"><span data-stu-id="69868-181">String</span></span>|<span data-ttu-id="69868-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="69868-182">Notes for the app.</span></span> <span data-ttu-id="69868-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69868-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="69868-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="69868-184">uploadState</span></span>|<span data-ttu-id="69868-185">Int32</span><span class="sxs-lookup"><span data-stu-id="69868-185">Int32</span></span>|<span data-ttu-id="69868-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="69868-186">The upload state.</span></span> <span data-ttu-id="69868-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69868-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="69868-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="69868-188">publishingState</span></span>|[<span data-ttu-id="69868-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="69868-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="69868-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="69868-190">The publishing state for the app.</span></span> <span data-ttu-id="69868-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="69868-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="69868-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="69868-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="69868-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="69868-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="69868-194">usedLicenseCount</span><span class="sxs-lookup"><span data-stu-id="69868-194">usedLicenseCount</span></span>|<span data-ttu-id="69868-195">Int32</span><span class="sxs-lookup"><span data-stu-id="69868-195">Int32</span></span>|<span data-ttu-id="69868-196">Número de licencias VPP en uso.</span><span class="sxs-lookup"><span data-stu-id="69868-196">The number of VPP licenses in use.</span></span>|
|<span data-ttu-id="69868-197">totalLicenseCount</span><span class="sxs-lookup"><span data-stu-id="69868-197">totalLicenseCount</span></span>|<span data-ttu-id="69868-198">Int32</span><span class="sxs-lookup"><span data-stu-id="69868-198">Int32</span></span>|<span data-ttu-id="69868-199">Número total de licencias VPP.</span><span class="sxs-lookup"><span data-stu-id="69868-199">The total number of VPP licenses.</span></span>|
|<span data-ttu-id="69868-200">releaseDateTime</span><span class="sxs-lookup"><span data-stu-id="69868-200">releaseDateTime</span></span>|<span data-ttu-id="69868-201">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="69868-201">DateTimeOffset</span></span>|<span data-ttu-id="69868-202">Fecha y hora de publicación de la aplicación de VPP.</span><span class="sxs-lookup"><span data-stu-id="69868-202">The VPP application release date and time.</span></span>|
|<span data-ttu-id="69868-203">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="69868-203">appStoreUrl</span></span>|<span data-ttu-id="69868-204">String</span><span class="sxs-lookup"><span data-stu-id="69868-204">String</span></span>|<span data-ttu-id="69868-205">Dirección URL de la tienda.</span><span class="sxs-lookup"><span data-stu-id="69868-205">The store URL.</span></span>|
|<span data-ttu-id="69868-206">licensingType</span><span class="sxs-lookup"><span data-stu-id="69868-206">licensingType</span></span>|[<span data-ttu-id="69868-207">vppLicensingType</span><span class="sxs-lookup"><span data-stu-id="69868-207">vppLicensingType</span></span>](../resources/intune-apps-vpplicensingtype.md)|<span data-ttu-id="69868-208">Tipo de licencia compatible.</span><span class="sxs-lookup"><span data-stu-id="69868-208">The supported License Type.</span></span>|
|<span data-ttu-id="69868-209">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="69868-209">applicableDeviceType</span></span>|[<span data-ttu-id="69868-210">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="69868-210">iosDeviceType</span></span>](../resources/intune-apps-iosdevicetype.md)|<span data-ttu-id="69868-211">Tipo de dispositivo iOS aplicable.</span><span class="sxs-lookup"><span data-stu-id="69868-211">The applicable iOS Device Type.</span></span>|
|<span data-ttu-id="69868-212">vppTokenOrganizationName</span><span class="sxs-lookup"><span data-stu-id="69868-212">vppTokenOrganizationName</span></span>|<span data-ttu-id="69868-213">String</span><span class="sxs-lookup"><span data-stu-id="69868-213">String</span></span>|<span data-ttu-id="69868-214">Organización asociada al token del Programa de Compras por Volumen de Apple</span><span class="sxs-lookup"><span data-stu-id="69868-214">The organization associated with the Apple Volume Purchase Program Token</span></span>|
|<span data-ttu-id="69868-215">vppTokenAccountType</span><span class="sxs-lookup"><span data-stu-id="69868-215">vppTokenAccountType</span></span>|[<span data-ttu-id="69868-216">vppTokenAccountType</span><span class="sxs-lookup"><span data-stu-id="69868-216">vppTokenAccountType</span></span>](../resources/intune-shared-vpptokenaccounttype.md)|<span data-ttu-id="69868-217">Tipo de programa de compras por volumen al que está asociado el token del Programa de Compras por Volumen de Apple especificado.</span><span class="sxs-lookup"><span data-stu-id="69868-217">The type of volume purchase program which the given Apple Volume Purchase Program Token is associated with.</span></span> <span data-ttu-id="69868-218">Los valores posibles son: `business` y `education`.</span><span class="sxs-lookup"><span data-stu-id="69868-218">Possible values are: `business`, `education`.</span></span> <span data-ttu-id="69868-219">Los valores posibles son: `business` y `education`.</span><span class="sxs-lookup"><span data-stu-id="69868-219">Possible values are: `business`, `education`.</span></span>|
|<span data-ttu-id="69868-220">vppTokenAppleId</span><span class="sxs-lookup"><span data-stu-id="69868-220">vppTokenAppleId</span></span>|<span data-ttu-id="69868-221">String</span><span class="sxs-lookup"><span data-stu-id="69868-221">String</span></span>|<span data-ttu-id="69868-222">Identificador de Apple asociado al token del Programa de Compras por Volumen de Apple especificado.</span><span class="sxs-lookup"><span data-stu-id="69868-222">The Apple Id associated with the given Apple Volume Purchase Program Token.</span></span>|
|<span data-ttu-id="69868-223">bundleId</span><span class="sxs-lookup"><span data-stu-id="69868-223">bundleId</span></span>|<span data-ttu-id="69868-224">String</span><span class="sxs-lookup"><span data-stu-id="69868-224">String</span></span>|<span data-ttu-id="69868-225">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="69868-225">The Identity Name.</span></span>|
|<span data-ttu-id="69868-226">vppTokenId</span><span class="sxs-lookup"><span data-stu-id="69868-226">vppTokenId</span></span>|<span data-ttu-id="69868-227">String</span><span class="sxs-lookup"><span data-stu-id="69868-227">String</span></span>|<span data-ttu-id="69868-228">Identificador del símbolo (token) VPP asociado con esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="69868-228">Identifier of the VPP token associated with this app.</span></span>|
|<span data-ttu-id="69868-229">revokeLicenseActionResults</span><span class="sxs-lookup"><span data-stu-id="69868-229">revokeLicenseActionResults</span></span>|<span data-ttu-id="69868-230">colección de [iosVppAppRevokeLicensesActionResult](../resources/intune-apps-iosvppapprevokelicensesactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="69868-230">[iosVppAppRevokeLicensesActionResult](../resources/intune-apps-iosvppapprevokelicensesactionresult.md) collection</span></span>|<span data-ttu-id="69868-231">Resultados de revocación acciones de licencia en esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="69868-231">Results of revoke license actions on this app.</span></span>|



## <a name="response"></a><span data-ttu-id="69868-232">Respuesta</span><span class="sxs-lookup"><span data-stu-id="69868-232">Response</span></span>
<span data-ttu-id="69868-233">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosVppApp](../resources/intune-apps-iosvppapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="69868-233">If successful, this method returns a `200 OK` response code and an updated [iosVppApp](../resources/intune-apps-iosvppapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="69868-234">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="69868-234">Example</span></span>
### <a name="request"></a><span data-ttu-id="69868-235">Solicitud</span><span class="sxs-lookup"><span data-stu-id="69868-235">Request</span></span>
<span data-ttu-id="69868-236">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="69868-236">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1903

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
  "usedLicenseCount": 0,
  "totalLicenseCount": 1,
  "releaseDateTime": "2017-01-01T00:01:34.7470482-08:00",
  "appStoreUrl": "https://example.com/appStoreUrl/",
  "licensingType": {
    "@odata.type": "microsoft.graph.vppLicensingType",
    "supportUserLicensing": true,
    "supportDeviceLicensing": true,
    "supportsUserLicensing": true,
    "supportsDeviceLicensing": true
  },
  "applicableDeviceType": {
    "@odata.type": "microsoft.graph.iosDeviceType",
    "iPad": true,
    "iPhoneAndIPod": true
  },
  "vppTokenOrganizationName": "Vpp Token Organization Name value",
  "vppTokenAccountType": "education",
  "vppTokenAppleId": "Vpp Token Apple Id value",
  "bundleId": "Bundle Id value",
  "vppTokenId": "Vpp Token Id value",
  "revokeLicenseActionResults": [
    {
      "@odata.type": "microsoft.graph.iosVppAppRevokeLicensesActionResult",
      "userId": "User Id value",
      "managedDeviceId": "Managed Device Id value",
      "totalLicensesCount": 2,
      "failedLicensesCount": 3,
      "actionFailureReason": "appleFailure",
      "actionName": "Action Name value",
      "actionState": "pending",
      "startDateTime": "2016-12-31T23:58:46.7156189-08:00",
      "lastUpdatedDateTime": "2017-01-01T00:00:56.8321556-08:00"
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="69868-237">Respuesta</span><span class="sxs-lookup"><span data-stu-id="69868-237">Response</span></span>
<span data-ttu-id="69868-p118">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="69868-p118">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2059

{
  "@odata.type": "#microsoft.graph.iosVppApp",
  "id": "a0ac9b6f-9b6f-a0ac-6f9b-aca06f9baca0",
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
  "usedLicenseCount": 0,
  "totalLicenseCount": 1,
  "releaseDateTime": "2017-01-01T00:01:34.7470482-08:00",
  "appStoreUrl": "https://example.com/appStoreUrl/",
  "licensingType": {
    "@odata.type": "microsoft.graph.vppLicensingType",
    "supportUserLicensing": true,
    "supportDeviceLicensing": true,
    "supportsUserLicensing": true,
    "supportsDeviceLicensing": true
  },
  "applicableDeviceType": {
    "@odata.type": "microsoft.graph.iosDeviceType",
    "iPad": true,
    "iPhoneAndIPod": true
  },
  "vppTokenOrganizationName": "Vpp Token Organization Name value",
  "vppTokenAccountType": "education",
  "vppTokenAppleId": "Vpp Token Apple Id value",
  "bundleId": "Bundle Id value",
  "vppTokenId": "Vpp Token Id value",
  "revokeLicenseActionResults": [
    {
      "@odata.type": "microsoft.graph.iosVppAppRevokeLicensesActionResult",
      "userId": "User Id value",
      "managedDeviceId": "Managed Device Id value",
      "totalLicensesCount": 2,
      "failedLicensesCount": 3,
      "actionFailureReason": "appleFailure",
      "actionName": "Action Name value",
      "actionState": "pending",
      "startDateTime": "2016-12-31T23:58:46.7156189-08:00",
      "lastUpdatedDateTime": "2017-01-01T00:00:56.8321556-08:00"
    }
  ]
}
```




