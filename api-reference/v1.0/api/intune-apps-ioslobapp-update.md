---
title: Actualizar iosLobApp
description: Actualice las propiedades de un objeto iosLobApp.
author: tfitzmac
ms.openlocfilehash: cffa5603cf92bd8e45c95ebb805618c1293851eb
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27354267"
---
# <a name="update-ioslobapp"></a><span data-ttu-id="c2009-103">Actualizar iosLobApp</span><span class="sxs-lookup"><span data-stu-id="c2009-103">Update iosLobApp</span></span>

> <span data-ttu-id="c2009-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c2009-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c2009-105">Actualice las propiedades de un objeto [iosLobApp](../resources/intune-apps-ioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="c2009-105">Update the properties of a [iosLobApp](../resources/intune-apps-ioslobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c2009-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c2009-106">Prerequisites</span></span>
<span data-ttu-id="c2009-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c2009-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c2009-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c2009-109">Permission type</span></span>|<span data-ttu-id="c2009-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c2009-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c2009-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c2009-111">Delegated (work or school account)</span></span>|<span data-ttu-id="c2009-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c2009-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="c2009-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c2009-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c2009-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c2009-114">Not supported.</span></span>|
|<span data-ttu-id="c2009-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c2009-115">Application</span></span>|<span data-ttu-id="c2009-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c2009-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c2009-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c2009-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="c2009-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c2009-118">Request headers</span></span>
|<span data-ttu-id="c2009-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c2009-119">Header</span></span>|<span data-ttu-id="c2009-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c2009-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c2009-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="c2009-121">Authorization</span></span>|<span data-ttu-id="c2009-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c2009-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c2009-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c2009-123">Accept</span></span>|<span data-ttu-id="c2009-124">application/json</span><span class="sxs-lookup"><span data-stu-id="c2009-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c2009-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c2009-125">Request body</span></span>
<span data-ttu-id="c2009-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosLobApp](../resources/intune-apps-ioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="c2009-126">In the request body, supply a JSON representation for the [iosLobApp](../resources/intune-apps-ioslobapp.md) object.</span></span>

<span data-ttu-id="c2009-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosLobApp](../resources/intune-apps-ioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="c2009-127">The following table shows the properties that are required when you create the [iosLobApp](../resources/intune-apps-ioslobapp.md).</span></span>

|<span data-ttu-id="c2009-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c2009-128">Property</span></span>|<span data-ttu-id="c2009-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="c2009-129">Type</span></span>|<span data-ttu-id="c2009-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2009-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c2009-131">id</span><span class="sxs-lookup"><span data-stu-id="c2009-131">id</span></span>|<span data-ttu-id="c2009-132">String</span><span class="sxs-lookup"><span data-stu-id="c2009-132">String</span></span>|<span data-ttu-id="c2009-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="c2009-133">Key of the entity.</span></span> <span data-ttu-id="c2009-134">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c2009-134">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="c2009-135">displayName</span><span class="sxs-lookup"><span data-stu-id="c2009-135">displayName</span></span>|<span data-ttu-id="c2009-136">String</span><span class="sxs-lookup"><span data-stu-id="c2009-136">String</span></span>|<span data-ttu-id="c2009-137">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="c2009-137">The admin provided or imported title of the app.</span></span> <span data-ttu-id="c2009-138">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c2009-138">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="c2009-139">descripción</span><span class="sxs-lookup"><span data-stu-id="c2009-139">description</span></span>|<span data-ttu-id="c2009-140">String</span><span class="sxs-lookup"><span data-stu-id="c2009-140">String</span></span>|<span data-ttu-id="c2009-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c2009-141">The description of the app.</span></span> <span data-ttu-id="c2009-142">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c2009-142">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="c2009-143">publicador</span><span class="sxs-lookup"><span data-stu-id="c2009-143">publisher</span></span>|<span data-ttu-id="c2009-144">String</span><span class="sxs-lookup"><span data-stu-id="c2009-144">String</span></span>|<span data-ttu-id="c2009-145">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c2009-145">The publisher of the app.</span></span> <span data-ttu-id="c2009-146">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c2009-146">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="c2009-147">largeIcon</span><span class="sxs-lookup"><span data-stu-id="c2009-147">largeIcon</span></span>|[<span data-ttu-id="c2009-148">mimeContent</span><span class="sxs-lookup"><span data-stu-id="c2009-148">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="c2009-149">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="c2009-149">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="c2009-150">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c2009-150">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="c2009-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="c2009-151">createdDateTime</span></span>|<span data-ttu-id="c2009-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c2009-152">DateTimeOffset</span></span>|<span data-ttu-id="c2009-153">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c2009-153">The date and time the app was created.</span></span> <span data-ttu-id="c2009-154">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c2009-154">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="c2009-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="c2009-155">lastModifiedDateTime</span></span>|<span data-ttu-id="c2009-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c2009-156">DateTimeOffset</span></span>|<span data-ttu-id="c2009-157">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c2009-157">The date and time the app was last modified.</span></span> <span data-ttu-id="c2009-158">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c2009-158">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="c2009-159">isFeatured</span><span class="sxs-lookup"><span data-stu-id="c2009-159">isFeatured</span></span>|<span data-ttu-id="c2009-160">Boolean</span><span class="sxs-lookup"><span data-stu-id="c2009-160">Boolean</span></span>|<span data-ttu-id="c2009-161">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c2009-161">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="c2009-162">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="c2009-162">privacyInformationUrl</span></span>|<span data-ttu-id="c2009-163">String</span><span class="sxs-lookup"><span data-stu-id="c2009-163">String</span></span>|<span data-ttu-id="c2009-164">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="c2009-164">The privacy statement Url.</span></span> <span data-ttu-id="c2009-165">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c2009-165">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="c2009-166">informationUrl</span><span class="sxs-lookup"><span data-stu-id="c2009-166">informationUrl</span></span>|<span data-ttu-id="c2009-167">String</span><span class="sxs-lookup"><span data-stu-id="c2009-167">String</span></span>|<span data-ttu-id="c2009-168">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="c2009-168">The more information Url.</span></span> <span data-ttu-id="c2009-169">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c2009-169">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="c2009-170">owner</span><span class="sxs-lookup"><span data-stu-id="c2009-170">owner</span></span>|<span data-ttu-id="c2009-171">String</span><span class="sxs-lookup"><span data-stu-id="c2009-171">String</span></span>|<span data-ttu-id="c2009-172">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c2009-172">The owner of the app.</span></span> <span data-ttu-id="c2009-173">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c2009-173">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="c2009-174">developer</span><span class="sxs-lookup"><span data-stu-id="c2009-174">developer</span></span>|<span data-ttu-id="c2009-175">String</span><span class="sxs-lookup"><span data-stu-id="c2009-175">String</span></span>|<span data-ttu-id="c2009-176">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c2009-176">The developer of the app.</span></span> <span data-ttu-id="c2009-177">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c2009-177">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="c2009-178">notas</span><span class="sxs-lookup"><span data-stu-id="c2009-178">notes</span></span>|<span data-ttu-id="c2009-179">String</span><span class="sxs-lookup"><span data-stu-id="c2009-179">String</span></span>|<span data-ttu-id="c2009-180">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c2009-180">Notes for the app.</span></span> <span data-ttu-id="c2009-181">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c2009-181">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="c2009-182">publishingState</span><span class="sxs-lookup"><span data-stu-id="c2009-182">publishingState</span></span>|[<span data-ttu-id="c2009-183">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="c2009-183">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="c2009-184">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c2009-184">The publishing state for the app.</span></span> <span data-ttu-id="c2009-185">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="c2009-185">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="c2009-186">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c2009-186">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="c2009-187">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="c2009-187">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="c2009-188">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="c2009-188">committedContentVersion</span></span>|<span data-ttu-id="c2009-189">String</span><span class="sxs-lookup"><span data-stu-id="c2009-189">String</span></span>|<span data-ttu-id="c2009-190">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="c2009-190">The internal committed content version.</span></span> <span data-ttu-id="c2009-191">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="c2009-191">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="c2009-192">fileName</span><span class="sxs-lookup"><span data-stu-id="c2009-192">fileName</span></span>|<span data-ttu-id="c2009-193">String</span><span class="sxs-lookup"><span data-stu-id="c2009-193">String</span></span>|<span data-ttu-id="c2009-194">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="c2009-194">The name of the main Lob application file.</span></span> <span data-ttu-id="c2009-195">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="c2009-195">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="c2009-196">size</span><span class="sxs-lookup"><span data-stu-id="c2009-196">size</span></span>|<span data-ttu-id="c2009-197">Int64</span><span class="sxs-lookup"><span data-stu-id="c2009-197">Int64</span></span>|<span data-ttu-id="c2009-198">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="c2009-198">The total size, including all uploaded files.</span></span> <span data-ttu-id="c2009-199">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="c2009-199">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="c2009-200">bundleId</span><span class="sxs-lookup"><span data-stu-id="c2009-200">bundleId</span></span>|<span data-ttu-id="c2009-201">String</span><span class="sxs-lookup"><span data-stu-id="c2009-201">String</span></span>|<span data-ttu-id="c2009-202">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="c2009-202">The Identity Name.</span></span>|
|<span data-ttu-id="c2009-203">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="c2009-203">applicableDeviceType</span></span>|[<span data-ttu-id="c2009-204">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="c2009-204">iosDeviceType</span></span>](../resources/intune-apps-iosdevicetype.md)|<span data-ttu-id="c2009-205">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="c2009-205">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="c2009-206">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="c2009-206">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="c2009-207">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="c2009-207">iosMinimumOperatingSystem</span></span>](../resources/intune-apps-iosminimumoperatingsystem.md)|<span data-ttu-id="c2009-208">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="c2009-208">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="c2009-209">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="c2009-209">expirationDateTime</span></span>|<span data-ttu-id="c2009-210">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c2009-210">DateTimeOffset</span></span>|<span data-ttu-id="c2009-211">Fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="c2009-211">The expiration time.</span></span>|
|<span data-ttu-id="c2009-212">versionNumber</span><span class="sxs-lookup"><span data-stu-id="c2009-212">versionNumber</span></span>|<span data-ttu-id="c2009-213">String</span><span class="sxs-lookup"><span data-stu-id="c2009-213">String</span></span>|<span data-ttu-id="c2009-214">El número de la versión de la aplicación de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="c2009-214">The version number of iOS Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="c2009-215">buildNumber</span><span class="sxs-lookup"><span data-stu-id="c2009-215">buildNumber</span></span>|<span data-ttu-id="c2009-216">String</span><span class="sxs-lookup"><span data-stu-id="c2009-216">String</span></span>|<span data-ttu-id="c2009-217">El número de compilación de la aplicación de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="c2009-217">The build number of iOS Line of Business (LoB) app.</span></span>|



## <a name="response"></a><span data-ttu-id="c2009-218">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2009-218">Response</span></span>
<span data-ttu-id="c2009-219">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosLobApp](../resources/intune-apps-ioslobapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c2009-219">If successful, this method returns a `200 OK` response code and an updated [iosLobApp](../resources/intune-apps-ioslobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c2009-220">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c2009-220">Example</span></span>
### <a name="request"></a><span data-ttu-id="c2009-221">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c2009-221">Request</span></span>
<span data-ttu-id="c2009-222">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c2009-222">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1209

{
  "@odata.type": "#microsoft.graph.iosLobApp",
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
  "bundleId": "Bundle Id value",
  "applicableDeviceType": {
    "@odata.type": "microsoft.graph.iosDeviceType",
    "iPad": true,
    "iPhoneAndIPod": true
  },
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.iosMinimumOperatingSystem",
    "v8_0": true,
    "v9_0": true,
    "v10_0": true,
    "v11_0": true,
    "v12_0": true
  },
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "versionNumber": "Version Number value",
  "buildNumber": "Build Number value"
}
```

### <a name="response"></a><span data-ttu-id="c2009-223">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2009-223">Response</span></span>
<span data-ttu-id="c2009-p118">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c2009-p118">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1381

{
  "@odata.type": "#microsoft.graph.iosLobApp",
  "id": "b34052ea-52ea-b340-ea52-40b3ea5240b3",
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
  "bundleId": "Bundle Id value",
  "applicableDeviceType": {
    "@odata.type": "microsoft.graph.iosDeviceType",
    "iPad": true,
    "iPhoneAndIPod": true
  },
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.iosMinimumOperatingSystem",
    "v8_0": true,
    "v9_0": true,
    "v10_0": true,
    "v11_0": true,
    "v12_0": true
  },
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "versionNumber": "Version Number value",
  "buildNumber": "Build Number value"
}
```



