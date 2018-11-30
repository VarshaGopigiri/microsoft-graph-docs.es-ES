---
title: Actualizar iosLobApp
description: Actualice las propiedades de un objeto iosLobApp.
ms.openlocfilehash: 159bdb4091d5ab0005ad0e9c1ba1720ee85a775e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030772"
---
# <a name="update-ioslobapp"></a><span data-ttu-id="4862f-103">Actualizar iosLobApp</span><span class="sxs-lookup"><span data-stu-id="4862f-103">Update iosLobApp</span></span>

> <span data-ttu-id="4862f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4862f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4862f-105">Actualice las propiedades de un objeto [iosLobApp](../resources/intune-apps-ioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="4862f-105">Update the properties of a [iosLobApp](../resources/intune-apps-ioslobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4862f-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4862f-106">Prerequisites</span></span>
<span data-ttu-id="4862f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4862f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4862f-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4862f-109">Permission type</span></span>|<span data-ttu-id="4862f-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4862f-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4862f-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4862f-111">Delegated (work or school account)</span></span>|<span data-ttu-id="4862f-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4862f-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="4862f-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4862f-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4862f-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4862f-114">Not supported.</span></span>|
|<span data-ttu-id="4862f-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4862f-115">Application</span></span>|<span data-ttu-id="4862f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4862f-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4862f-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4862f-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="4862f-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4862f-118">Request headers</span></span>
|<span data-ttu-id="4862f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4862f-119">Header</span></span>|<span data-ttu-id="4862f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4862f-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4862f-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="4862f-121">Authorization</span></span>|<span data-ttu-id="4862f-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4862f-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4862f-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="4862f-123">Accept</span></span>|<span data-ttu-id="4862f-124">application/json</span><span class="sxs-lookup"><span data-stu-id="4862f-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4862f-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4862f-125">Request body</span></span>
<span data-ttu-id="4862f-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosLobApp](../resources/intune-apps-ioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="4862f-126">In the request body, supply a JSON representation for the [iosLobApp](../resources/intune-apps-ioslobapp.md) object.</span></span>

<span data-ttu-id="4862f-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosLobApp](../resources/intune-apps-ioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="4862f-127">The following table shows the properties that are required when you create the [iosLobApp](../resources/intune-apps-ioslobapp.md).</span></span>

|<span data-ttu-id="4862f-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4862f-128">Property</span></span>|<span data-ttu-id="4862f-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="4862f-129">Type</span></span>|<span data-ttu-id="4862f-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="4862f-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4862f-131">id</span><span class="sxs-lookup"><span data-stu-id="4862f-131">id</span></span>|<span data-ttu-id="4862f-132">String</span><span class="sxs-lookup"><span data-stu-id="4862f-132">String</span></span>|<span data-ttu-id="4862f-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="4862f-133">Key of the entity.</span></span> <span data-ttu-id="4862f-134">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4862f-134">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4862f-135">displayName</span><span class="sxs-lookup"><span data-stu-id="4862f-135">displayName</span></span>|<span data-ttu-id="4862f-136">String</span><span class="sxs-lookup"><span data-stu-id="4862f-136">String</span></span>|<span data-ttu-id="4862f-137">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="4862f-137">The admin provided or imported title of the app.</span></span> <span data-ttu-id="4862f-138">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4862f-138">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4862f-139">descripción</span><span class="sxs-lookup"><span data-stu-id="4862f-139">description</span></span>|<span data-ttu-id="4862f-140">String</span><span class="sxs-lookup"><span data-stu-id="4862f-140">String</span></span>|<span data-ttu-id="4862f-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4862f-141">The description of the app.</span></span> <span data-ttu-id="4862f-142">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4862f-142">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4862f-143">publicador</span><span class="sxs-lookup"><span data-stu-id="4862f-143">publisher</span></span>|<span data-ttu-id="4862f-144">String</span><span class="sxs-lookup"><span data-stu-id="4862f-144">String</span></span>|<span data-ttu-id="4862f-145">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4862f-145">The publisher of the app.</span></span> <span data-ttu-id="4862f-146">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4862f-146">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4862f-147">largeIcon</span><span class="sxs-lookup"><span data-stu-id="4862f-147">largeIcon</span></span>|[<span data-ttu-id="4862f-148">mimeContent</span><span class="sxs-lookup"><span data-stu-id="4862f-148">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="4862f-149">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="4862f-149">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="4862f-150">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4862f-150">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4862f-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="4862f-151">createdDateTime</span></span>|<span data-ttu-id="4862f-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4862f-152">DateTimeOffset</span></span>|<span data-ttu-id="4862f-153">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4862f-153">The date and time the app was created.</span></span> <span data-ttu-id="4862f-154">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4862f-154">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4862f-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="4862f-155">lastModifiedDateTime</span></span>|<span data-ttu-id="4862f-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4862f-156">DateTimeOffset</span></span>|<span data-ttu-id="4862f-157">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4862f-157">The date and time the app was last modified.</span></span> <span data-ttu-id="4862f-158">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4862f-158">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4862f-159">isFeatured</span><span class="sxs-lookup"><span data-stu-id="4862f-159">isFeatured</span></span>|<span data-ttu-id="4862f-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="4862f-160">Boolean</span></span>|<span data-ttu-id="4862f-161">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4862f-161">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4862f-162">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="4862f-162">privacyInformationUrl</span></span>|<span data-ttu-id="4862f-163">String</span><span class="sxs-lookup"><span data-stu-id="4862f-163">String</span></span>|<span data-ttu-id="4862f-164">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="4862f-164">The privacy statement Url.</span></span> <span data-ttu-id="4862f-165">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4862f-165">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4862f-166">informationUrl</span><span class="sxs-lookup"><span data-stu-id="4862f-166">informationUrl</span></span>|<span data-ttu-id="4862f-167">String</span><span class="sxs-lookup"><span data-stu-id="4862f-167">String</span></span>|<span data-ttu-id="4862f-168">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="4862f-168">The more information Url.</span></span> <span data-ttu-id="4862f-169">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4862f-169">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4862f-170">owner</span><span class="sxs-lookup"><span data-stu-id="4862f-170">owner</span></span>|<span data-ttu-id="4862f-171">String</span><span class="sxs-lookup"><span data-stu-id="4862f-171">String</span></span>|<span data-ttu-id="4862f-172">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4862f-172">The owner of the app.</span></span> <span data-ttu-id="4862f-173">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4862f-173">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4862f-174">developer</span><span class="sxs-lookup"><span data-stu-id="4862f-174">developer</span></span>|<span data-ttu-id="4862f-175">String</span><span class="sxs-lookup"><span data-stu-id="4862f-175">String</span></span>|<span data-ttu-id="4862f-176">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4862f-176">The developer of the app.</span></span> <span data-ttu-id="4862f-177">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4862f-177">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4862f-178">notas</span><span class="sxs-lookup"><span data-stu-id="4862f-178">notes</span></span>|<span data-ttu-id="4862f-179">String</span><span class="sxs-lookup"><span data-stu-id="4862f-179">String</span></span>|<span data-ttu-id="4862f-180">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4862f-180">Notes for the app.</span></span> <span data-ttu-id="4862f-181">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4862f-181">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="4862f-182">publishingState</span><span class="sxs-lookup"><span data-stu-id="4862f-182">publishingState</span></span>|[<span data-ttu-id="4862f-183">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="4862f-183">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="4862f-184">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4862f-184">The publishing state for the app.</span></span> <span data-ttu-id="4862f-185">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="4862f-185">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="4862f-186">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4862f-186">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="4862f-187">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="4862f-187">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="4862f-188">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="4862f-188">committedContentVersion</span></span>|<span data-ttu-id="4862f-189">String</span><span class="sxs-lookup"><span data-stu-id="4862f-189">String</span></span>|<span data-ttu-id="4862f-190">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="4862f-190">The internal committed content version.</span></span> <span data-ttu-id="4862f-191">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="4862f-191">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="4862f-192">fileName</span><span class="sxs-lookup"><span data-stu-id="4862f-192">fileName</span></span>|<span data-ttu-id="4862f-193">String</span><span class="sxs-lookup"><span data-stu-id="4862f-193">String</span></span>|<span data-ttu-id="4862f-194">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="4862f-194">The name of the main Lob application file.</span></span> <span data-ttu-id="4862f-195">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="4862f-195">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="4862f-196">size</span><span class="sxs-lookup"><span data-stu-id="4862f-196">size</span></span>|<span data-ttu-id="4862f-197">Int64</span><span class="sxs-lookup"><span data-stu-id="4862f-197">Int64</span></span>|<span data-ttu-id="4862f-198">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="4862f-198">The total size, including all uploaded files.</span></span> <span data-ttu-id="4862f-199">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="4862f-199">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="4862f-200">bundleId</span><span class="sxs-lookup"><span data-stu-id="4862f-200">bundleId</span></span>|<span data-ttu-id="4862f-201">String</span><span class="sxs-lookup"><span data-stu-id="4862f-201">String</span></span>|<span data-ttu-id="4862f-202">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="4862f-202">The Identity Name.</span></span>|
|<span data-ttu-id="4862f-203">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="4862f-203">applicableDeviceType</span></span>|[<span data-ttu-id="4862f-204">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="4862f-204">iosDeviceType</span></span>](../resources/intune-apps-iosdevicetype.md)|<span data-ttu-id="4862f-205">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="4862f-205">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="4862f-206">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="4862f-206">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="4862f-207">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="4862f-207">iosMinimumOperatingSystem</span></span>](../resources/intune-apps-iosminimumoperatingsystem.md)|<span data-ttu-id="4862f-208">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="4862f-208">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="4862f-209">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="4862f-209">expirationDateTime</span></span>|<span data-ttu-id="4862f-210">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4862f-210">DateTimeOffset</span></span>|<span data-ttu-id="4862f-211">Fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="4862f-211">The expiration time.</span></span>|
|<span data-ttu-id="4862f-212">versionNumber</span><span class="sxs-lookup"><span data-stu-id="4862f-212">versionNumber</span></span>|<span data-ttu-id="4862f-213">String</span><span class="sxs-lookup"><span data-stu-id="4862f-213">String</span></span>|<span data-ttu-id="4862f-214">El número de la versión de la aplicación de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="4862f-214">The version number of iOS Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="4862f-215">buildNumber</span><span class="sxs-lookup"><span data-stu-id="4862f-215">buildNumber</span></span>|<span data-ttu-id="4862f-216">String</span><span class="sxs-lookup"><span data-stu-id="4862f-216">String</span></span>|<span data-ttu-id="4862f-217">El número de compilación de la aplicación de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="4862f-217">The build number of iOS Line of Business (LoB) app.</span></span>|



## <a name="response"></a><span data-ttu-id="4862f-218">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4862f-218">Response</span></span>
<span data-ttu-id="4862f-219">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosLobApp](../resources/intune-apps-ioslobapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4862f-219">If successful, this method returns a `200 OK` response code and an updated [iosLobApp](../resources/intune-apps-ioslobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4862f-220">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4862f-220">Example</span></span>
### <a name="request"></a><span data-ttu-id="4862f-221">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4862f-221">Request</span></span>
<span data-ttu-id="4862f-222">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4862f-222">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="4862f-223">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4862f-223">Response</span></span>
<span data-ttu-id="4862f-p118">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4862f-p118">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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


