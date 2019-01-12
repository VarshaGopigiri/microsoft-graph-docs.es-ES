---
title: Crear androidLobApp
description: Cree un objeto androidLobApp.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 8a16fd332dda41e7b538f60118ec34eda538c0c6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27991576"
---
# <a name="create-androidlobapp"></a><span data-ttu-id="8a110-103">Crear androidLobApp</span><span class="sxs-lookup"><span data-stu-id="8a110-103">Create androidLobApp</span></span>

> <span data-ttu-id="8a110-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8a110-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8a110-105">Cree un objeto [androidLobApp](../resources/intune-apps-androidlobapp.md).</span><span class="sxs-lookup"><span data-stu-id="8a110-105">Create a new [androidLobApp](../resources/intune-apps-androidlobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8a110-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8a110-106">Prerequisites</span></span>
<span data-ttu-id="8a110-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8a110-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8a110-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8a110-109">Permission type</span></span>|<span data-ttu-id="8a110-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8a110-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8a110-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8a110-111">Delegated (work or school account)</span></span>|<span data-ttu-id="8a110-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8a110-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="8a110-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8a110-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8a110-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8a110-114">Not supported.</span></span>|
|<span data-ttu-id="8a110-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8a110-115">Application</span></span>|<span data-ttu-id="8a110-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8a110-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8a110-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8a110-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="8a110-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8a110-118">Request headers</span></span>
|<span data-ttu-id="8a110-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a110-119">Header</span></span>|<span data-ttu-id="8a110-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8a110-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8a110-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="8a110-121">Authorization</span></span>|<span data-ttu-id="8a110-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8a110-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8a110-123">Accept</span><span class="sxs-lookup"><span data-stu-id="8a110-123">Accept</span></span>|<span data-ttu-id="8a110-124">application/json</span><span class="sxs-lookup"><span data-stu-id="8a110-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8a110-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8a110-125">Request body</span></span>
<span data-ttu-id="8a110-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto androidLobApp.</span><span class="sxs-lookup"><span data-stu-id="8a110-126">In the request body, supply a JSON representation for the androidLobApp object.</span></span>

<span data-ttu-id="8a110-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto androidLobApp.</span><span class="sxs-lookup"><span data-stu-id="8a110-127">The following table shows the properties that are required when you create the androidLobApp.</span></span>

|<span data-ttu-id="8a110-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8a110-128">Property</span></span>|<span data-ttu-id="8a110-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="8a110-129">Type</span></span>|<span data-ttu-id="8a110-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a110-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8a110-131">id</span><span class="sxs-lookup"><span data-stu-id="8a110-131">id</span></span>|<span data-ttu-id="8a110-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="8a110-132">String</span></span>|<span data-ttu-id="8a110-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="8a110-133">Key of the entity.</span></span> <span data-ttu-id="8a110-134">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8a110-134">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="8a110-135">displayName</span><span class="sxs-lookup"><span data-stu-id="8a110-135">displayName</span></span>|<span data-ttu-id="8a110-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="8a110-136">String</span></span>|<span data-ttu-id="8a110-137">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="8a110-137">The admin provided or imported title of the app.</span></span> <span data-ttu-id="8a110-138">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8a110-138">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="8a110-139">descripción</span><span class="sxs-lookup"><span data-stu-id="8a110-139">description</span></span>|<span data-ttu-id="8a110-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="8a110-140">String</span></span>|<span data-ttu-id="8a110-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8a110-141">The description of the app.</span></span> <span data-ttu-id="8a110-142">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8a110-142">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="8a110-143">publicador</span><span class="sxs-lookup"><span data-stu-id="8a110-143">publisher</span></span>|<span data-ttu-id="8a110-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="8a110-144">String</span></span>|<span data-ttu-id="8a110-145">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8a110-145">The publisher of the app.</span></span> <span data-ttu-id="8a110-146">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8a110-146">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="8a110-147">largeIcon</span><span class="sxs-lookup"><span data-stu-id="8a110-147">largeIcon</span></span>|[<span data-ttu-id="8a110-148">mimeContent</span><span class="sxs-lookup"><span data-stu-id="8a110-148">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="8a110-149">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="8a110-149">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="8a110-150">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8a110-150">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="8a110-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="8a110-151">createdDateTime</span></span>|<span data-ttu-id="8a110-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8a110-152">DateTimeOffset</span></span>|<span data-ttu-id="8a110-153">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8a110-153">The date and time the app was created.</span></span> <span data-ttu-id="8a110-154">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8a110-154">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="8a110-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="8a110-155">lastModifiedDateTime</span></span>|<span data-ttu-id="8a110-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8a110-156">DateTimeOffset</span></span>|<span data-ttu-id="8a110-157">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8a110-157">The date and time the app was last modified.</span></span> <span data-ttu-id="8a110-158">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8a110-158">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="8a110-159">isFeatured</span><span class="sxs-lookup"><span data-stu-id="8a110-159">isFeatured</span></span>|<span data-ttu-id="8a110-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="8a110-160">Boolean</span></span>|<span data-ttu-id="8a110-161">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8a110-161">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="8a110-162">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="8a110-162">privacyInformationUrl</span></span>|<span data-ttu-id="8a110-163">Cadena</span><span class="sxs-lookup"><span data-stu-id="8a110-163">String</span></span>|<span data-ttu-id="8a110-164">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="8a110-164">The privacy statement Url.</span></span> <span data-ttu-id="8a110-165">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8a110-165">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="8a110-166">informationUrl</span><span class="sxs-lookup"><span data-stu-id="8a110-166">informationUrl</span></span>|<span data-ttu-id="8a110-167">Cadena</span><span class="sxs-lookup"><span data-stu-id="8a110-167">String</span></span>|<span data-ttu-id="8a110-168">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="8a110-168">The more information Url.</span></span> <span data-ttu-id="8a110-169">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8a110-169">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="8a110-170">owner</span><span class="sxs-lookup"><span data-stu-id="8a110-170">owner</span></span>|<span data-ttu-id="8a110-171">Cadena</span><span class="sxs-lookup"><span data-stu-id="8a110-171">String</span></span>|<span data-ttu-id="8a110-172">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8a110-172">The owner of the app.</span></span> <span data-ttu-id="8a110-173">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8a110-173">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="8a110-174">developer</span><span class="sxs-lookup"><span data-stu-id="8a110-174">developer</span></span>|<span data-ttu-id="8a110-175">Cadena</span><span class="sxs-lookup"><span data-stu-id="8a110-175">String</span></span>|<span data-ttu-id="8a110-176">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8a110-176">The developer of the app.</span></span> <span data-ttu-id="8a110-177">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8a110-177">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="8a110-178">notas</span><span class="sxs-lookup"><span data-stu-id="8a110-178">notes</span></span>|<span data-ttu-id="8a110-179">Cadena</span><span class="sxs-lookup"><span data-stu-id="8a110-179">String</span></span>|<span data-ttu-id="8a110-180">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8a110-180">Notes for the app.</span></span> <span data-ttu-id="8a110-181">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8a110-181">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="8a110-182">publishingState</span><span class="sxs-lookup"><span data-stu-id="8a110-182">publishingState</span></span>|[<span data-ttu-id="8a110-183">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="8a110-183">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="8a110-184">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8a110-184">The publishing state for the app.</span></span> <span data-ttu-id="8a110-185">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="8a110-185">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="8a110-186">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8a110-186">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="8a110-187">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="8a110-187">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="8a110-188">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="8a110-188">committedContentVersion</span></span>|<span data-ttu-id="8a110-189">Cadena</span><span class="sxs-lookup"><span data-stu-id="8a110-189">String</span></span>|<span data-ttu-id="8a110-190">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="8a110-190">The internal committed content version.</span></span> <span data-ttu-id="8a110-191">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="8a110-191">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="8a110-192">fileName</span><span class="sxs-lookup"><span data-stu-id="8a110-192">fileName</span></span>|<span data-ttu-id="8a110-193">Cadena</span><span class="sxs-lookup"><span data-stu-id="8a110-193">String</span></span>|<span data-ttu-id="8a110-194">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="8a110-194">The name of the main Lob application file.</span></span> <span data-ttu-id="8a110-195">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="8a110-195">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="8a110-196">size</span><span class="sxs-lookup"><span data-stu-id="8a110-196">size</span></span>|<span data-ttu-id="8a110-197">Int64</span><span class="sxs-lookup"><span data-stu-id="8a110-197">Int64</span></span>|<span data-ttu-id="8a110-198">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="8a110-198">The total size, including all uploaded files.</span></span> <span data-ttu-id="8a110-199">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="8a110-199">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="8a110-200">packageId</span><span class="sxs-lookup"><span data-stu-id="8a110-200">packageId</span></span>|<span data-ttu-id="8a110-201">Cadena</span><span class="sxs-lookup"><span data-stu-id="8a110-201">String</span></span>|<span data-ttu-id="8a110-202">El identificador del paquete.</span><span class="sxs-lookup"><span data-stu-id="8a110-202">The package identifier.</span></span>|
|<span data-ttu-id="8a110-203">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="8a110-203">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="8a110-204">androidMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="8a110-204">androidMinimumOperatingSystem</span></span>](../resources/intune-apps-androidminimumoperatingsystem.md)|<span data-ttu-id="8a110-205">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="8a110-205">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="8a110-206">versionName</span><span class="sxs-lookup"><span data-stu-id="8a110-206">versionName</span></span>|<span data-ttu-id="8a110-207">Cadena</span><span class="sxs-lookup"><span data-stu-id="8a110-207">String</span></span>|<span data-ttu-id="8a110-208">El nombre de la versión de la aplicación de línea de negocio (LoB) de Android.</span><span class="sxs-lookup"><span data-stu-id="8a110-208">The version name of Android Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="8a110-209">versionCode</span><span class="sxs-lookup"><span data-stu-id="8a110-209">versionCode</span></span>|<span data-ttu-id="8a110-210">Cadena</span><span class="sxs-lookup"><span data-stu-id="8a110-210">String</span></span>|<span data-ttu-id="8a110-211">El código de versión de la aplicación de línea de negocio (LoB) de Android.</span><span class="sxs-lookup"><span data-stu-id="8a110-211">The version code of Android Line of Business (LoB) app.</span></span>|



## <a name="response"></a><span data-ttu-id="8a110-212">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8a110-212">Response</span></span>
<span data-ttu-id="8a110-213">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [androidLobApp](../resources/intune-apps-androidlobapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8a110-213">If successful, this method returns a `201 Created` response code and a [androidLobApp](../resources/intune-apps-androidlobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8a110-214">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8a110-214">Example</span></span>
### <a name="request"></a><span data-ttu-id="8a110-215">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8a110-215">Request</span></span>
<span data-ttu-id="8a110-216">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8a110-216">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
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

### <a name="response"></a><span data-ttu-id="8a110-217">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8a110-217">Response</span></span>
<span data-ttu-id="8a110-p118">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8a110-p118">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



