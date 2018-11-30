---
title: Actualizar androidLobApp
description: Actualice las propiedades de un objeto androidLobApp.
ms.openlocfilehash: 5cfbff200540534b8dfd430878929beb8d8ba45b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029182"
---
# <a name="update-androidlobapp"></a><span data-ttu-id="cf3e3-103">Actualizar androidLobApp</span><span class="sxs-lookup"><span data-stu-id="cf3e3-103">Update androidLobApp</span></span>

> <span data-ttu-id="cf3e3-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cf3e3-105">Actualice las propiedades de un objeto [androidLobApp](../resources/intune-apps-androidlobapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf3e3-105">Update the properties of a [androidLobApp](../resources/intune-apps-androidlobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cf3e3-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cf3e3-106">Prerequisites</span></span>
<span data-ttu-id="cf3e3-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cf3e3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cf3e3-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cf3e3-109">Permission type</span></span>|<span data-ttu-id="cf3e3-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cf3e3-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="cf3e3-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cf3e3-111">Delegated (work or school account)</span></span>|<span data-ttu-id="cf3e3-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cf3e3-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="cf3e3-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cf3e3-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="cf3e3-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-114">Not supported.</span></span>|
|<span data-ttu-id="cf3e3-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cf3e3-115">Application</span></span>|<span data-ttu-id="cf3e3-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="cf3e3-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cf3e3-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="cf3e3-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cf3e3-118">Request headers</span></span>
|<span data-ttu-id="cf3e3-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf3e3-119">Header</span></span>|<span data-ttu-id="cf3e3-120">Valor</span><span class="sxs-lookup"><span data-stu-id="cf3e3-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="cf3e3-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="cf3e3-121">Authorization</span></span>|<span data-ttu-id="cf3e3-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="cf3e3-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="cf3e3-123">Accept</span></span>|<span data-ttu-id="cf3e3-124">application/json</span><span class="sxs-lookup"><span data-stu-id="cf3e3-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="cf3e3-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cf3e3-125">Request body</span></span>
<span data-ttu-id="cf3e3-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [androidLobApp](../resources/intune-apps-androidlobapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf3e3-126">In the request body, supply a JSON representation for the [androidLobApp](../resources/intune-apps-androidlobapp.md) object.</span></span>

<span data-ttu-id="cf3e3-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [androidLobApp](../resources/intune-apps-androidlobapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf3e3-127">The following table shows the properties that are required when you create the [androidLobApp](../resources/intune-apps-androidlobapp.md).</span></span>

|<span data-ttu-id="cf3e3-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cf3e3-128">Property</span></span>|<span data-ttu-id="cf3e3-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf3e3-129">Type</span></span>|<span data-ttu-id="cf3e3-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf3e3-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cf3e3-131">id</span><span class="sxs-lookup"><span data-stu-id="cf3e3-131">id</span></span>|<span data-ttu-id="cf3e3-132">String</span><span class="sxs-lookup"><span data-stu-id="cf3e3-132">String</span></span>|<span data-ttu-id="cf3e3-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-133">Key of the entity.</span></span> <span data-ttu-id="cf3e3-134">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf3e3-134">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cf3e3-135">displayName</span><span class="sxs-lookup"><span data-stu-id="cf3e3-135">displayName</span></span>|<span data-ttu-id="cf3e3-136">String</span><span class="sxs-lookup"><span data-stu-id="cf3e3-136">String</span></span>|<span data-ttu-id="cf3e3-137">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-137">The admin provided or imported title of the app.</span></span> <span data-ttu-id="cf3e3-138">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf3e3-138">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cf3e3-139">descripción</span><span class="sxs-lookup"><span data-stu-id="cf3e3-139">description</span></span>|<span data-ttu-id="cf3e3-140">String</span><span class="sxs-lookup"><span data-stu-id="cf3e3-140">String</span></span>|<span data-ttu-id="cf3e3-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-141">The description of the app.</span></span> <span data-ttu-id="cf3e3-142">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf3e3-142">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cf3e3-143">publicador</span><span class="sxs-lookup"><span data-stu-id="cf3e3-143">publisher</span></span>|<span data-ttu-id="cf3e3-144">String</span><span class="sxs-lookup"><span data-stu-id="cf3e3-144">String</span></span>|<span data-ttu-id="cf3e3-145">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-145">The publisher of the app.</span></span> <span data-ttu-id="cf3e3-146">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf3e3-146">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cf3e3-147">largeIcon</span><span class="sxs-lookup"><span data-stu-id="cf3e3-147">largeIcon</span></span>|[<span data-ttu-id="cf3e3-148">mimeContent</span><span class="sxs-lookup"><span data-stu-id="cf3e3-148">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="cf3e3-149">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-149">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="cf3e3-150">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf3e3-150">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cf3e3-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="cf3e3-151">createdDateTime</span></span>|<span data-ttu-id="cf3e3-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cf3e3-152">DateTimeOffset</span></span>|<span data-ttu-id="cf3e3-153">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-153">The date and time the app was created.</span></span> <span data-ttu-id="cf3e3-154">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf3e3-154">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cf3e3-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="cf3e3-155">lastModifiedDateTime</span></span>|<span data-ttu-id="cf3e3-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cf3e3-156">DateTimeOffset</span></span>|<span data-ttu-id="cf3e3-157">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-157">The date and time the app was last modified.</span></span> <span data-ttu-id="cf3e3-158">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf3e3-158">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cf3e3-159">isFeatured</span><span class="sxs-lookup"><span data-stu-id="cf3e3-159">isFeatured</span></span>|<span data-ttu-id="cf3e3-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="cf3e3-160">Boolean</span></span>|<span data-ttu-id="cf3e3-161">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf3e3-161">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cf3e3-162">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="cf3e3-162">privacyInformationUrl</span></span>|<span data-ttu-id="cf3e3-163">String</span><span class="sxs-lookup"><span data-stu-id="cf3e3-163">String</span></span>|<span data-ttu-id="cf3e3-164">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-164">The privacy statement Url.</span></span> <span data-ttu-id="cf3e3-165">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf3e3-165">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cf3e3-166">informationUrl</span><span class="sxs-lookup"><span data-stu-id="cf3e3-166">informationUrl</span></span>|<span data-ttu-id="cf3e3-167">String</span><span class="sxs-lookup"><span data-stu-id="cf3e3-167">String</span></span>|<span data-ttu-id="cf3e3-168">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-168">The more information Url.</span></span> <span data-ttu-id="cf3e3-169">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf3e3-169">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cf3e3-170">owner</span><span class="sxs-lookup"><span data-stu-id="cf3e3-170">owner</span></span>|<span data-ttu-id="cf3e3-171">String</span><span class="sxs-lookup"><span data-stu-id="cf3e3-171">String</span></span>|<span data-ttu-id="cf3e3-172">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-172">The owner of the app.</span></span> <span data-ttu-id="cf3e3-173">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf3e3-173">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cf3e3-174">developer</span><span class="sxs-lookup"><span data-stu-id="cf3e3-174">developer</span></span>|<span data-ttu-id="cf3e3-175">String</span><span class="sxs-lookup"><span data-stu-id="cf3e3-175">String</span></span>|<span data-ttu-id="cf3e3-176">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-176">The developer of the app.</span></span> <span data-ttu-id="cf3e3-177">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf3e3-177">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cf3e3-178">notas</span><span class="sxs-lookup"><span data-stu-id="cf3e3-178">notes</span></span>|<span data-ttu-id="cf3e3-179">String</span><span class="sxs-lookup"><span data-stu-id="cf3e3-179">String</span></span>|<span data-ttu-id="cf3e3-180">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-180">Notes for the app.</span></span> <span data-ttu-id="cf3e3-181">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf3e3-181">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="cf3e3-182">publishingState</span><span class="sxs-lookup"><span data-stu-id="cf3e3-182">publishingState</span></span>|[<span data-ttu-id="cf3e3-183">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="cf3e3-183">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="cf3e3-184">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-184">The publishing state for the app.</span></span> <span data-ttu-id="cf3e3-185">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-185">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="cf3e3-186">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf3e3-186">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="cf3e3-187">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-187">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="cf3e3-188">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="cf3e3-188">committedContentVersion</span></span>|<span data-ttu-id="cf3e3-189">String</span><span class="sxs-lookup"><span data-stu-id="cf3e3-189">String</span></span>|<span data-ttu-id="cf3e3-190">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-190">The internal committed content version.</span></span> <span data-ttu-id="cf3e3-191">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf3e3-191">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="cf3e3-192">fileName</span><span class="sxs-lookup"><span data-stu-id="cf3e3-192">fileName</span></span>|<span data-ttu-id="cf3e3-193">String</span><span class="sxs-lookup"><span data-stu-id="cf3e3-193">String</span></span>|<span data-ttu-id="cf3e3-194">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-194">The name of the main Lob application file.</span></span> <span data-ttu-id="cf3e3-195">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf3e3-195">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="cf3e3-196">size</span><span class="sxs-lookup"><span data-stu-id="cf3e3-196">size</span></span>|<span data-ttu-id="cf3e3-197">Int64</span><span class="sxs-lookup"><span data-stu-id="cf3e3-197">Int64</span></span>|<span data-ttu-id="cf3e3-198">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-198">The total size, including all uploaded files.</span></span> <span data-ttu-id="cf3e3-199">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="cf3e3-199">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="cf3e3-200">packageId</span><span class="sxs-lookup"><span data-stu-id="cf3e3-200">packageId</span></span>|<span data-ttu-id="cf3e3-201">String</span><span class="sxs-lookup"><span data-stu-id="cf3e3-201">String</span></span>|<span data-ttu-id="cf3e3-202">El identificador del paquete.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-202">The package identifier.</span></span>|
|<span data-ttu-id="cf3e3-203">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="cf3e3-203">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="cf3e3-204">androidMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="cf3e3-204">androidMinimumOperatingSystem</span></span>](../resources/intune-apps-androidminimumoperatingsystem.md)|<span data-ttu-id="cf3e3-205">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-205">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="cf3e3-206">versionName</span><span class="sxs-lookup"><span data-stu-id="cf3e3-206">versionName</span></span>|<span data-ttu-id="cf3e3-207">String</span><span class="sxs-lookup"><span data-stu-id="cf3e3-207">String</span></span>|<span data-ttu-id="cf3e3-208">El nombre de la versión de la aplicación de línea de negocio (LoB) de Android.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-208">The version name of Android Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="cf3e3-209">versionCode</span><span class="sxs-lookup"><span data-stu-id="cf3e3-209">versionCode</span></span>|<span data-ttu-id="cf3e3-210">String</span><span class="sxs-lookup"><span data-stu-id="cf3e3-210">String</span></span>|<span data-ttu-id="cf3e3-211">El código de versión de la aplicación de línea de negocio (LoB) de Android.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-211">The version code of Android Line of Business (LoB) app.</span></span>|



## <a name="response"></a><span data-ttu-id="cf3e3-212">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cf3e3-212">Response</span></span>
<span data-ttu-id="cf3e3-213">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [androidLobApp](../resources/intune-apps-androidlobapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-213">If successful, this method returns a `200 OK` response code and an updated [androidLobApp](../resources/intune-apps-androidlobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cf3e3-214">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cf3e3-214">Example</span></span>
### <a name="request"></a><span data-ttu-id="cf3e3-215">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cf3e3-215">Request</span></span>
<span data-ttu-id="cf3e3-216">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-216">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1075

{
  "@odata.type": "#microsoft.graph.androidLobApp",
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
  "packageId": "Package Id value",
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.androidMinimumOperatingSystem",
    "v4_0": true,
    "v4_0_3": true,
    "v4_1": true,
    "v4_2": true,
    "v4_3": true,
    "v4_4": true,
    "v5_0": true,
    "v5_1": true
  },
  "versionName": "Version Name value",
  "versionCode": "Version Code value"
}
```

### <a name="response"></a><span data-ttu-id="cf3e3-217">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cf3e3-217">Response</span></span>
<span data-ttu-id="cf3e3-p118">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cf3e3-p118">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1247

{
  "@odata.type": "#microsoft.graph.androidLobApp",
  "id": "4b9a27d0-27d0-4b9a-d027-9a4bd0279a4b",
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
  "packageId": "Package Id value",
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.androidMinimumOperatingSystem",
    "v4_0": true,
    "v4_0_3": true,
    "v4_1": true,
    "v4_2": true,
    "v4_3": true,
    "v4_4": true,
    "v5_0": true,
    "v5_1": true
  },
  "versionName": "Version Name value",
  "versionCode": "Version Code value"
}
```



