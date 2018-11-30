---
title: Crear iosVppApp
description: Cree un objeto iosVppApp.
ms.openlocfilehash: cb7b0926145d2448195662cef817292fb41ac1e9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029727"
---
# <a name="create-iosvppapp"></a><span data-ttu-id="9ff06-103">Crear iosVppApp</span><span class="sxs-lookup"><span data-stu-id="9ff06-103">Create iosVppApp</span></span>

> <span data-ttu-id="9ff06-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9ff06-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9ff06-105">Cree un objeto [iosVppApp](../resources/intune-apps-iosvppapp.md).</span><span class="sxs-lookup"><span data-stu-id="9ff06-105">Create a new [iosVppApp](../resources/intune-apps-iosvppapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9ff06-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9ff06-106">Prerequisites</span></span>
<span data-ttu-id="9ff06-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9ff06-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9ff06-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9ff06-109">Permission type</span></span>|<span data-ttu-id="9ff06-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9ff06-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9ff06-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9ff06-111">Delegated (work or school account)</span></span>|<span data-ttu-id="9ff06-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9ff06-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="9ff06-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9ff06-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9ff06-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9ff06-114">Not supported.</span></span>|
|<span data-ttu-id="9ff06-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9ff06-115">Application</span></span>|<span data-ttu-id="9ff06-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9ff06-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9ff06-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9ff06-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="9ff06-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9ff06-118">Request headers</span></span>
|<span data-ttu-id="9ff06-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9ff06-119">Header</span></span>|<span data-ttu-id="9ff06-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9ff06-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9ff06-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="9ff06-121">Authorization</span></span>|<span data-ttu-id="9ff06-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9ff06-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9ff06-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="9ff06-123">Accept</span></span>|<span data-ttu-id="9ff06-124">application/json</span><span class="sxs-lookup"><span data-stu-id="9ff06-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9ff06-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9ff06-125">Request body</span></span>
<span data-ttu-id="9ff06-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosVppApp.</span><span class="sxs-lookup"><span data-stu-id="9ff06-126">In the request body, supply a JSON representation for the iosVppApp object.</span></span>

<span data-ttu-id="9ff06-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosVppApp.</span><span class="sxs-lookup"><span data-stu-id="9ff06-127">The following table shows the properties that are required when you create the iosVppApp.</span></span>

|<span data-ttu-id="9ff06-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9ff06-128">Property</span></span>|<span data-ttu-id="9ff06-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="9ff06-129">Type</span></span>|<span data-ttu-id="9ff06-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="9ff06-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9ff06-131">id</span><span class="sxs-lookup"><span data-stu-id="9ff06-131">id</span></span>|<span data-ttu-id="9ff06-132">String</span><span class="sxs-lookup"><span data-stu-id="9ff06-132">String</span></span>|<span data-ttu-id="9ff06-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="9ff06-133">Key of the entity.</span></span> <span data-ttu-id="9ff06-134">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9ff06-134">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="9ff06-135">displayName</span><span class="sxs-lookup"><span data-stu-id="9ff06-135">displayName</span></span>|<span data-ttu-id="9ff06-136">String</span><span class="sxs-lookup"><span data-stu-id="9ff06-136">String</span></span>|<span data-ttu-id="9ff06-137">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="9ff06-137">The admin provided or imported title of the app.</span></span> <span data-ttu-id="9ff06-138">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9ff06-138">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="9ff06-139">descripción</span><span class="sxs-lookup"><span data-stu-id="9ff06-139">description</span></span>|<span data-ttu-id="9ff06-140">String</span><span class="sxs-lookup"><span data-stu-id="9ff06-140">String</span></span>|<span data-ttu-id="9ff06-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9ff06-141">The description of the app.</span></span> <span data-ttu-id="9ff06-142">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9ff06-142">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="9ff06-143">publicador</span><span class="sxs-lookup"><span data-stu-id="9ff06-143">publisher</span></span>|<span data-ttu-id="9ff06-144">String</span><span class="sxs-lookup"><span data-stu-id="9ff06-144">String</span></span>|<span data-ttu-id="9ff06-145">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9ff06-145">The publisher of the app.</span></span> <span data-ttu-id="9ff06-146">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9ff06-146">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="9ff06-147">largeIcon</span><span class="sxs-lookup"><span data-stu-id="9ff06-147">largeIcon</span></span>|[<span data-ttu-id="9ff06-148">mimeContent</span><span class="sxs-lookup"><span data-stu-id="9ff06-148">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="9ff06-149">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="9ff06-149">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="9ff06-150">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9ff06-150">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="9ff06-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="9ff06-151">createdDateTime</span></span>|<span data-ttu-id="9ff06-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9ff06-152">DateTimeOffset</span></span>|<span data-ttu-id="9ff06-153">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9ff06-153">The date and time the app was created.</span></span> <span data-ttu-id="9ff06-154">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9ff06-154">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="9ff06-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="9ff06-155">lastModifiedDateTime</span></span>|<span data-ttu-id="9ff06-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9ff06-156">DateTimeOffset</span></span>|<span data-ttu-id="9ff06-157">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9ff06-157">The date and time the app was last modified.</span></span> <span data-ttu-id="9ff06-158">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9ff06-158">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="9ff06-159">isFeatured</span><span class="sxs-lookup"><span data-stu-id="9ff06-159">isFeatured</span></span>|<span data-ttu-id="9ff06-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="9ff06-160">Boolean</span></span>|<span data-ttu-id="9ff06-161">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9ff06-161">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="9ff06-162">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="9ff06-162">privacyInformationUrl</span></span>|<span data-ttu-id="9ff06-163">String</span><span class="sxs-lookup"><span data-stu-id="9ff06-163">String</span></span>|<span data-ttu-id="9ff06-164">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="9ff06-164">The privacy statement Url.</span></span> <span data-ttu-id="9ff06-165">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9ff06-165">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="9ff06-166">informationUrl</span><span class="sxs-lookup"><span data-stu-id="9ff06-166">informationUrl</span></span>|<span data-ttu-id="9ff06-167">String</span><span class="sxs-lookup"><span data-stu-id="9ff06-167">String</span></span>|<span data-ttu-id="9ff06-168">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="9ff06-168">The more information Url.</span></span> <span data-ttu-id="9ff06-169">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9ff06-169">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="9ff06-170">owner</span><span class="sxs-lookup"><span data-stu-id="9ff06-170">owner</span></span>|<span data-ttu-id="9ff06-171">String</span><span class="sxs-lookup"><span data-stu-id="9ff06-171">String</span></span>|<span data-ttu-id="9ff06-172">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9ff06-172">The owner of the app.</span></span> <span data-ttu-id="9ff06-173">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9ff06-173">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="9ff06-174">developer</span><span class="sxs-lookup"><span data-stu-id="9ff06-174">developer</span></span>|<span data-ttu-id="9ff06-175">String</span><span class="sxs-lookup"><span data-stu-id="9ff06-175">String</span></span>|<span data-ttu-id="9ff06-176">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9ff06-176">The developer of the app.</span></span> <span data-ttu-id="9ff06-177">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9ff06-177">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="9ff06-178">notas</span><span class="sxs-lookup"><span data-stu-id="9ff06-178">notes</span></span>|<span data-ttu-id="9ff06-179">String</span><span class="sxs-lookup"><span data-stu-id="9ff06-179">String</span></span>|<span data-ttu-id="9ff06-180">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9ff06-180">Notes for the app.</span></span> <span data-ttu-id="9ff06-181">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9ff06-181">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="9ff06-182">publishingState</span><span class="sxs-lookup"><span data-stu-id="9ff06-182">publishingState</span></span>|[<span data-ttu-id="9ff06-183">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="9ff06-183">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="9ff06-184">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9ff06-184">The publishing state for the app.</span></span> <span data-ttu-id="9ff06-185">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="9ff06-185">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="9ff06-186">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9ff06-186">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="9ff06-187">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="9ff06-187">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="9ff06-188">usedLicenseCount</span><span class="sxs-lookup"><span data-stu-id="9ff06-188">usedLicenseCount</span></span>|<span data-ttu-id="9ff06-189">Int32</span><span class="sxs-lookup"><span data-stu-id="9ff06-189">Int32</span></span>|<span data-ttu-id="9ff06-190">Número de licencias VPP en uso.</span><span class="sxs-lookup"><span data-stu-id="9ff06-190">The number of VPP licenses in use.</span></span>|
|<span data-ttu-id="9ff06-191">totalLicenseCount</span><span class="sxs-lookup"><span data-stu-id="9ff06-191">totalLicenseCount</span></span>|<span data-ttu-id="9ff06-192">Int32</span><span class="sxs-lookup"><span data-stu-id="9ff06-192">Int32</span></span>|<span data-ttu-id="9ff06-193">Número total de licencias VPP.</span><span class="sxs-lookup"><span data-stu-id="9ff06-193">The total number of VPP licenses.</span></span>|
|<span data-ttu-id="9ff06-194">releaseDateTime</span><span class="sxs-lookup"><span data-stu-id="9ff06-194">releaseDateTime</span></span>|<span data-ttu-id="9ff06-195">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9ff06-195">DateTimeOffset</span></span>|<span data-ttu-id="9ff06-196">Fecha y hora de publicación de la aplicación de VPP.</span><span class="sxs-lookup"><span data-stu-id="9ff06-196">The VPP application release date and time.</span></span>|
|<span data-ttu-id="9ff06-197">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="9ff06-197">appStoreUrl</span></span>|<span data-ttu-id="9ff06-198">String</span><span class="sxs-lookup"><span data-stu-id="9ff06-198">String</span></span>|<span data-ttu-id="9ff06-199">Dirección URL de la tienda.</span><span class="sxs-lookup"><span data-stu-id="9ff06-199">The store URL.</span></span>|
|<span data-ttu-id="9ff06-200">licensingType</span><span class="sxs-lookup"><span data-stu-id="9ff06-200">licensingType</span></span>|[<span data-ttu-id="9ff06-201">vppLicensingType</span><span class="sxs-lookup"><span data-stu-id="9ff06-201">vppLicensingType</span></span>](../resources/intune-apps-vpplicensingtype.md)|<span data-ttu-id="9ff06-202">Tipo de licencia compatible.</span><span class="sxs-lookup"><span data-stu-id="9ff06-202">The supported License Type.</span></span>|
|<span data-ttu-id="9ff06-203">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="9ff06-203">applicableDeviceType</span></span>|[<span data-ttu-id="9ff06-204">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="9ff06-204">iosDeviceType</span></span>](../resources/intune-apps-iosdevicetype.md)|<span data-ttu-id="9ff06-205">Tipo de dispositivo iOS aplicable.</span><span class="sxs-lookup"><span data-stu-id="9ff06-205">The applicable iOS Device Type.</span></span>|
|<span data-ttu-id="9ff06-206">vppTokenOrganizationName</span><span class="sxs-lookup"><span data-stu-id="9ff06-206">vppTokenOrganizationName</span></span>|<span data-ttu-id="9ff06-207">String</span><span class="sxs-lookup"><span data-stu-id="9ff06-207">String</span></span>|<span data-ttu-id="9ff06-208">Organización asociada al token del Programa de Compras por Volumen de Apple</span><span class="sxs-lookup"><span data-stu-id="9ff06-208">The organization associated with the Apple Volume Purchase Program Token</span></span>|
|<span data-ttu-id="9ff06-209">vppTokenAccountType</span><span class="sxs-lookup"><span data-stu-id="9ff06-209">vppTokenAccountType</span></span>|[<span data-ttu-id="9ff06-210">vppTokenAccountType</span><span class="sxs-lookup"><span data-stu-id="9ff06-210">vppTokenAccountType</span></span>](../resources/intune-shared-vpptokenaccounttype.md)|<span data-ttu-id="9ff06-211">Tipo de programa de compras por volumen al que está asociado el token del Programa de Compras por Volumen de Apple especificado.</span><span class="sxs-lookup"><span data-stu-id="9ff06-211">The type of volume purchase program which the given Apple Volume Purchase Program Token is associated with.</span></span> <span data-ttu-id="9ff06-212">Los valores posibles son: `business` y `education`.</span><span class="sxs-lookup"><span data-stu-id="9ff06-212">Possible values are: `business`, `education`.</span></span> <span data-ttu-id="9ff06-213">Los valores posibles son: `business` y `education`.</span><span class="sxs-lookup"><span data-stu-id="9ff06-213">Possible values are: `business`, `education`.</span></span>|
|<span data-ttu-id="9ff06-214">vppTokenAppleId</span><span class="sxs-lookup"><span data-stu-id="9ff06-214">vppTokenAppleId</span></span>|<span data-ttu-id="9ff06-215">String</span><span class="sxs-lookup"><span data-stu-id="9ff06-215">String</span></span>|<span data-ttu-id="9ff06-216">Identificador de Apple asociado al token del Programa de Compras por Volumen de Apple especificado.</span><span class="sxs-lookup"><span data-stu-id="9ff06-216">The Apple Id associated with the given Apple Volume Purchase Program Token.</span></span>|
|<span data-ttu-id="9ff06-217">bundleId</span><span class="sxs-lookup"><span data-stu-id="9ff06-217">bundleId</span></span>|<span data-ttu-id="9ff06-218">String</span><span class="sxs-lookup"><span data-stu-id="9ff06-218">String</span></span>|<span data-ttu-id="9ff06-219">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="9ff06-219">The Identity Name.</span></span>|



## <a name="response"></a><span data-ttu-id="9ff06-220">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9ff06-220">Response</span></span>
<span data-ttu-id="9ff06-221">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosVppApp](../resources/intune-apps-iosvppapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9ff06-221">If successful, this method returns a `201 Created` response code and a [iosVppApp](../resources/intune-apps-iosvppapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9ff06-222">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9ff06-222">Example</span></span>
### <a name="request"></a><span data-ttu-id="9ff06-223">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9ff06-223">Request</span></span>
<span data-ttu-id="9ff06-224">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9ff06-224">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 1222

{
  "@odata.type": "#microsoft.graph.iosVppApp",
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
  "usedLicenseCount": 0,
  "totalLicenseCount": 1,
  "releaseDateTime": "2017-01-01T00:01:34.7470482-08:00",
  "appStoreUrl": "https://example.com/appStoreUrl/",
  "licensingType": {
    "@odata.type": "microsoft.graph.vppLicensingType",
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
  "bundleId": "Bundle Id value"
}
```

### <a name="response"></a><span data-ttu-id="9ff06-225">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9ff06-225">Response</span></span>
<span data-ttu-id="9ff06-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9ff06-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1394

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
  "publishingState": "processing",
  "usedLicenseCount": 0,
  "totalLicenseCount": 1,
  "releaseDateTime": "2017-01-01T00:01:34.7470482-08:00",
  "appStoreUrl": "https://example.com/appStoreUrl/",
  "licensingType": {
    "@odata.type": "microsoft.graph.vppLicensingType",
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
  "bundleId": "Bundle Id value"
}
```


