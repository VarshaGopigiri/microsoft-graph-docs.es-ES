---
title: Actualizar iosVppApp
description: Actualice las propiedades de un objeto iosVppApp.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: b93a85cf49eb700259c18c036ca7448fc3e9ad24
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27873531"
---
# <a name="update-iosvppapp"></a><span data-ttu-id="4fd7d-103">Actualizar iosVppApp</span><span class="sxs-lookup"><span data-stu-id="4fd7d-103">Update iosVppApp</span></span>

> <span data-ttu-id="4fd7d-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4fd7d-105">Actualice las propiedades de un objeto [iosVppApp](../resources/intune-apps-iosvppapp.md).</span><span class="sxs-lookup"><span data-stu-id="4fd7d-105">Update the properties of a [iosVppApp](../resources/intune-apps-iosvppapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4fd7d-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4fd7d-106">Prerequisites</span></span>
<span data-ttu-id="4fd7d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4fd7d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4fd7d-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4fd7d-109">Permission type</span></span>|<span data-ttu-id="4fd7d-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4fd7d-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4fd7d-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4fd7d-111">Delegated (work or school account)</span></span>|<span data-ttu-id="4fd7d-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4fd7d-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="4fd7d-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4fd7d-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4fd7d-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-114">Not supported.</span></span>|
|<span data-ttu-id="4fd7d-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4fd7d-115">Application</span></span>|<span data-ttu-id="4fd7d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4fd7d-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4fd7d-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="4fd7d-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4fd7d-118">Request headers</span></span>
|<span data-ttu-id="4fd7d-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4fd7d-119">Header</span></span>|<span data-ttu-id="4fd7d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4fd7d-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4fd7d-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="4fd7d-121">Authorization</span></span>|<span data-ttu-id="4fd7d-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4fd7d-123">Accept</span><span class="sxs-lookup"><span data-stu-id="4fd7d-123">Accept</span></span>|<span data-ttu-id="4fd7d-124">application/json</span><span class="sxs-lookup"><span data-stu-id="4fd7d-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4fd7d-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4fd7d-125">Request body</span></span>
<span data-ttu-id="4fd7d-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosVppApp](../resources/intune-apps-iosvppapp.md).</span><span class="sxs-lookup"><span data-stu-id="4fd7d-126">In the request body, supply a JSON representation for the [iosVppApp](../resources/intune-apps-iosvppapp.md) object.</span></span>

<span data-ttu-id="4fd7d-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosVppApp](../resources/intune-apps-iosvppapp.md).</span><span class="sxs-lookup"><span data-stu-id="4fd7d-127">The following table shows the properties that are required when you create the [iosVppApp](../resources/intune-apps-iosvppapp.md).</span></span>

|<span data-ttu-id="4fd7d-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4fd7d-128">Property</span></span>|<span data-ttu-id="4fd7d-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="4fd7d-129">Type</span></span>|<span data-ttu-id="4fd7d-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="4fd7d-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4fd7d-131">id</span><span class="sxs-lookup"><span data-stu-id="4fd7d-131">id</span></span>|<span data-ttu-id="4fd7d-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="4fd7d-132">String</span></span>|<span data-ttu-id="4fd7d-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-133">Key of the entity.</span></span> <span data-ttu-id="4fd7d-134">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4fd7d-134">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4fd7d-135">displayName</span><span class="sxs-lookup"><span data-stu-id="4fd7d-135">displayName</span></span>|<span data-ttu-id="4fd7d-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="4fd7d-136">String</span></span>|<span data-ttu-id="4fd7d-137">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-137">The admin provided or imported title of the app.</span></span> <span data-ttu-id="4fd7d-138">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4fd7d-138">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4fd7d-139">descripción</span><span class="sxs-lookup"><span data-stu-id="4fd7d-139">description</span></span>|<span data-ttu-id="4fd7d-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="4fd7d-140">String</span></span>|<span data-ttu-id="4fd7d-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-141">The description of the app.</span></span> <span data-ttu-id="4fd7d-142">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4fd7d-142">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4fd7d-143">publicador</span><span class="sxs-lookup"><span data-stu-id="4fd7d-143">publisher</span></span>|<span data-ttu-id="4fd7d-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="4fd7d-144">String</span></span>|<span data-ttu-id="4fd7d-145">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-145">The publisher of the app.</span></span> <span data-ttu-id="4fd7d-146">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4fd7d-146">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4fd7d-147">largeIcon</span><span class="sxs-lookup"><span data-stu-id="4fd7d-147">largeIcon</span></span>|[<span data-ttu-id="4fd7d-148">mimeContent</span><span class="sxs-lookup"><span data-stu-id="4fd7d-148">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="4fd7d-149">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-149">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="4fd7d-150">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4fd7d-150">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4fd7d-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="4fd7d-151">createdDateTime</span></span>|<span data-ttu-id="4fd7d-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4fd7d-152">DateTimeOffset</span></span>|<span data-ttu-id="4fd7d-153">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-153">The date and time the app was created.</span></span> <span data-ttu-id="4fd7d-154">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4fd7d-154">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4fd7d-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="4fd7d-155">lastModifiedDateTime</span></span>|<span data-ttu-id="4fd7d-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4fd7d-156">DateTimeOffset</span></span>|<span data-ttu-id="4fd7d-157">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-157">The date and time the app was last modified.</span></span> <span data-ttu-id="4fd7d-158">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4fd7d-158">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4fd7d-159">isFeatured</span><span class="sxs-lookup"><span data-stu-id="4fd7d-159">isFeatured</span></span>|<span data-ttu-id="4fd7d-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="4fd7d-160">Boolean</span></span>|<span data-ttu-id="4fd7d-161">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4fd7d-161">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4fd7d-162">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="4fd7d-162">privacyInformationUrl</span></span>|<span data-ttu-id="4fd7d-163">Cadena</span><span class="sxs-lookup"><span data-stu-id="4fd7d-163">String</span></span>|<span data-ttu-id="4fd7d-164">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-164">The privacy statement Url.</span></span> <span data-ttu-id="4fd7d-165">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4fd7d-165">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4fd7d-166">informationUrl</span><span class="sxs-lookup"><span data-stu-id="4fd7d-166">informationUrl</span></span>|<span data-ttu-id="4fd7d-167">Cadena</span><span class="sxs-lookup"><span data-stu-id="4fd7d-167">String</span></span>|<span data-ttu-id="4fd7d-168">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-168">The more information Url.</span></span> <span data-ttu-id="4fd7d-169">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4fd7d-169">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4fd7d-170">owner</span><span class="sxs-lookup"><span data-stu-id="4fd7d-170">owner</span></span>|<span data-ttu-id="4fd7d-171">Cadena</span><span class="sxs-lookup"><span data-stu-id="4fd7d-171">String</span></span>|<span data-ttu-id="4fd7d-172">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-172">The owner of the app.</span></span> <span data-ttu-id="4fd7d-173">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4fd7d-173">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4fd7d-174">developer</span><span class="sxs-lookup"><span data-stu-id="4fd7d-174">developer</span></span>|<span data-ttu-id="4fd7d-175">Cadena</span><span class="sxs-lookup"><span data-stu-id="4fd7d-175">String</span></span>|<span data-ttu-id="4fd7d-176">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-176">The developer of the app.</span></span> <span data-ttu-id="4fd7d-177">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4fd7d-177">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4fd7d-178">notas</span><span class="sxs-lookup"><span data-stu-id="4fd7d-178">notes</span></span>|<span data-ttu-id="4fd7d-179">Cadena</span><span class="sxs-lookup"><span data-stu-id="4fd7d-179">String</span></span>|<span data-ttu-id="4fd7d-180">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-180">Notes for the app.</span></span> <span data-ttu-id="4fd7d-181">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4fd7d-181">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4fd7d-182">publishingState</span><span class="sxs-lookup"><span data-stu-id="4fd7d-182">publishingState</span></span>|[<span data-ttu-id="4fd7d-183">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="4fd7d-183">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="4fd7d-184">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-184">The publishing state for the app.</span></span> <span data-ttu-id="4fd7d-185">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-185">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="4fd7d-186">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4fd7d-186">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="4fd7d-187">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-187">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="4fd7d-188">usedLicenseCount</span><span class="sxs-lookup"><span data-stu-id="4fd7d-188">usedLicenseCount</span></span>|<span data-ttu-id="4fd7d-189">Int32</span><span class="sxs-lookup"><span data-stu-id="4fd7d-189">Int32</span></span>|<span data-ttu-id="4fd7d-190">Número de licencias VPP en uso.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-190">The number of VPP licenses in use.</span></span>|
|<span data-ttu-id="4fd7d-191">totalLicenseCount</span><span class="sxs-lookup"><span data-stu-id="4fd7d-191">totalLicenseCount</span></span>|<span data-ttu-id="4fd7d-192">Int32</span><span class="sxs-lookup"><span data-stu-id="4fd7d-192">Int32</span></span>|<span data-ttu-id="4fd7d-193">Número total de licencias VPP.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-193">The total number of VPP licenses.</span></span>|
|<span data-ttu-id="4fd7d-194">releaseDateTime</span><span class="sxs-lookup"><span data-stu-id="4fd7d-194">releaseDateTime</span></span>|<span data-ttu-id="4fd7d-195">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4fd7d-195">DateTimeOffset</span></span>|<span data-ttu-id="4fd7d-196">Fecha y hora de publicación de la aplicación de VPP.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-196">The VPP application release date and time.</span></span>|
|<span data-ttu-id="4fd7d-197">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="4fd7d-197">appStoreUrl</span></span>|<span data-ttu-id="4fd7d-198">Cadena</span><span class="sxs-lookup"><span data-stu-id="4fd7d-198">String</span></span>|<span data-ttu-id="4fd7d-199">Dirección URL de la tienda.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-199">The store URL.</span></span>|
|<span data-ttu-id="4fd7d-200">licensingType</span><span class="sxs-lookup"><span data-stu-id="4fd7d-200">licensingType</span></span>|[<span data-ttu-id="4fd7d-201">vppLicensingType</span><span class="sxs-lookup"><span data-stu-id="4fd7d-201">vppLicensingType</span></span>](../resources/intune-apps-vpplicensingtype.md)|<span data-ttu-id="4fd7d-202">Tipo de licencia compatible.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-202">The supported License Type.</span></span>|
|<span data-ttu-id="4fd7d-203">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="4fd7d-203">applicableDeviceType</span></span>|[<span data-ttu-id="4fd7d-204">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="4fd7d-204">iosDeviceType</span></span>](../resources/intune-apps-iosdevicetype.md)|<span data-ttu-id="4fd7d-205">Tipo de dispositivo iOS aplicable.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-205">The applicable iOS Device Type.</span></span>|
|<span data-ttu-id="4fd7d-206">vppTokenOrganizationName</span><span class="sxs-lookup"><span data-stu-id="4fd7d-206">vppTokenOrganizationName</span></span>|<span data-ttu-id="4fd7d-207">Cadena</span><span class="sxs-lookup"><span data-stu-id="4fd7d-207">String</span></span>|<span data-ttu-id="4fd7d-208">Organización asociada al token del Programa de Compras por Volumen de Apple</span><span class="sxs-lookup"><span data-stu-id="4fd7d-208">The organization associated with the Apple Volume Purchase Program Token</span></span>|
|<span data-ttu-id="4fd7d-209">vppTokenAccountType</span><span class="sxs-lookup"><span data-stu-id="4fd7d-209">vppTokenAccountType</span></span>|[<span data-ttu-id="4fd7d-210">vppTokenAccountType</span><span class="sxs-lookup"><span data-stu-id="4fd7d-210">vppTokenAccountType</span></span>](../resources/intune-shared-vpptokenaccounttype.md)|<span data-ttu-id="4fd7d-211">Tipo de programa de compras por volumen al que está asociado el token del Programa de Compras por Volumen de Apple especificado.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-211">The type of volume purchase program which the given Apple Volume Purchase Program Token is associated with.</span></span> <span data-ttu-id="4fd7d-212">Los valores posibles son: `business` y `education`.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-212">Possible values are: `business`, `education`.</span></span> <span data-ttu-id="4fd7d-213">Los valores posibles son: `business` y `education`.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-213">Possible values are: `business`, `education`.</span></span>|
|<span data-ttu-id="4fd7d-214">vppTokenAppleId</span><span class="sxs-lookup"><span data-stu-id="4fd7d-214">vppTokenAppleId</span></span>|<span data-ttu-id="4fd7d-215">Cadena</span><span class="sxs-lookup"><span data-stu-id="4fd7d-215">String</span></span>|<span data-ttu-id="4fd7d-216">Identificador de Apple asociado al token del Programa de Compras por Volumen de Apple especificado.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-216">The Apple Id associated with the given Apple Volume Purchase Program Token.</span></span>|
|<span data-ttu-id="4fd7d-217">bundleId</span><span class="sxs-lookup"><span data-stu-id="4fd7d-217">bundleId</span></span>|<span data-ttu-id="4fd7d-218">Cadena</span><span class="sxs-lookup"><span data-stu-id="4fd7d-218">String</span></span>|<span data-ttu-id="4fd7d-219">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-219">The Identity Name.</span></span>|



## <a name="response"></a><span data-ttu-id="4fd7d-220">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4fd7d-220">Response</span></span>
<span data-ttu-id="4fd7d-221">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosVppApp](../resources/intune-apps-iosvppapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-221">If successful, this method returns a `200 OK` response code and an updated [iosVppApp](../resources/intune-apps-iosvppapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4fd7d-222">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4fd7d-222">Example</span></span>
### <a name="request"></a><span data-ttu-id="4fd7d-223">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4fd7d-223">Request</span></span>
<span data-ttu-id="4fd7d-224">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-224">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
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

### <a name="response"></a><span data-ttu-id="4fd7d-225">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4fd7d-225">Response</span></span>
<span data-ttu-id="4fd7d-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4fd7d-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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



