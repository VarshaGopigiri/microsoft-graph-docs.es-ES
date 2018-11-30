---
title: Actualizar windowsMobileMSI
description: Actualice las propiedades de un objeto windowsMobileMSI.
ms.openlocfilehash: a87c76413080b6c5daae828e5ed22e99be1d6bcf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031589"
---
# <a name="update-windowsmobilemsi"></a><span data-ttu-id="82dea-103">Actualizar windowsMobileMSI</span><span class="sxs-lookup"><span data-stu-id="82dea-103">Update windowsMobileMSI</span></span>

> <span data-ttu-id="82dea-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="82dea-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="82dea-105">Actualice las propiedades de un objeto [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md).</span><span class="sxs-lookup"><span data-stu-id="82dea-105">Update the properties of a [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="82dea-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="82dea-106">Prerequisites</span></span>
<span data-ttu-id="82dea-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="82dea-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="82dea-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="82dea-109">Permission type</span></span>|<span data-ttu-id="82dea-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="82dea-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="82dea-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="82dea-111">Delegated (work or school account)</span></span>|<span data-ttu-id="82dea-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="82dea-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="82dea-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="82dea-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="82dea-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="82dea-114">Not supported.</span></span>|
|<span data-ttu-id="82dea-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="82dea-115">Application</span></span>|<span data-ttu-id="82dea-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="82dea-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="82dea-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="82dea-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="82dea-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="82dea-118">Request headers</span></span>
|<span data-ttu-id="82dea-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82dea-119">Header</span></span>|<span data-ttu-id="82dea-120">Valor</span><span class="sxs-lookup"><span data-stu-id="82dea-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="82dea-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="82dea-121">Authorization</span></span>|<span data-ttu-id="82dea-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="82dea-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="82dea-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="82dea-123">Accept</span></span>|<span data-ttu-id="82dea-124">application/json</span><span class="sxs-lookup"><span data-stu-id="82dea-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="82dea-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="82dea-125">Request body</span></span>
<span data-ttu-id="82dea-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md).</span><span class="sxs-lookup"><span data-stu-id="82dea-126">In the request body, supply a JSON representation for the [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md) object.</span></span>

<span data-ttu-id="82dea-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md).</span><span class="sxs-lookup"><span data-stu-id="82dea-127">The following table shows the properties that are required when you create the [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md).</span></span>

|<span data-ttu-id="82dea-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="82dea-128">Property</span></span>|<span data-ttu-id="82dea-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="82dea-129">Type</span></span>|<span data-ttu-id="82dea-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="82dea-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="82dea-131">id</span><span class="sxs-lookup"><span data-stu-id="82dea-131">id</span></span>|<span data-ttu-id="82dea-132">String</span><span class="sxs-lookup"><span data-stu-id="82dea-132">String</span></span>|<span data-ttu-id="82dea-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="82dea-133">Key of the entity.</span></span> <span data-ttu-id="82dea-134">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="82dea-134">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="82dea-135">displayName</span><span class="sxs-lookup"><span data-stu-id="82dea-135">displayName</span></span>|<span data-ttu-id="82dea-136">String</span><span class="sxs-lookup"><span data-stu-id="82dea-136">String</span></span>|<span data-ttu-id="82dea-137">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="82dea-137">The admin provided or imported title of the app.</span></span> <span data-ttu-id="82dea-138">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="82dea-138">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="82dea-139">descripción</span><span class="sxs-lookup"><span data-stu-id="82dea-139">description</span></span>|<span data-ttu-id="82dea-140">String</span><span class="sxs-lookup"><span data-stu-id="82dea-140">String</span></span>|<span data-ttu-id="82dea-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="82dea-141">The description of the app.</span></span> <span data-ttu-id="82dea-142">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="82dea-142">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="82dea-143">publicador</span><span class="sxs-lookup"><span data-stu-id="82dea-143">publisher</span></span>|<span data-ttu-id="82dea-144">String</span><span class="sxs-lookup"><span data-stu-id="82dea-144">String</span></span>|<span data-ttu-id="82dea-145">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="82dea-145">The publisher of the app.</span></span> <span data-ttu-id="82dea-146">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="82dea-146">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="82dea-147">largeIcon</span><span class="sxs-lookup"><span data-stu-id="82dea-147">largeIcon</span></span>|[<span data-ttu-id="82dea-148">mimeContent</span><span class="sxs-lookup"><span data-stu-id="82dea-148">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="82dea-149">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="82dea-149">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="82dea-150">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="82dea-150">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="82dea-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="82dea-151">createdDateTime</span></span>|<span data-ttu-id="82dea-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="82dea-152">DateTimeOffset</span></span>|<span data-ttu-id="82dea-153">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="82dea-153">The date and time the app was created.</span></span> <span data-ttu-id="82dea-154">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="82dea-154">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="82dea-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="82dea-155">lastModifiedDateTime</span></span>|<span data-ttu-id="82dea-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="82dea-156">DateTimeOffset</span></span>|<span data-ttu-id="82dea-157">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="82dea-157">The date and time the app was last modified.</span></span> <span data-ttu-id="82dea-158">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="82dea-158">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="82dea-159">isFeatured</span><span class="sxs-lookup"><span data-stu-id="82dea-159">isFeatured</span></span>|<span data-ttu-id="82dea-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="82dea-160">Boolean</span></span>|<span data-ttu-id="82dea-161">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="82dea-161">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="82dea-162">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="82dea-162">privacyInformationUrl</span></span>|<span data-ttu-id="82dea-163">String</span><span class="sxs-lookup"><span data-stu-id="82dea-163">String</span></span>|<span data-ttu-id="82dea-164">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="82dea-164">The privacy statement Url.</span></span> <span data-ttu-id="82dea-165">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="82dea-165">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="82dea-166">informationUrl</span><span class="sxs-lookup"><span data-stu-id="82dea-166">informationUrl</span></span>|<span data-ttu-id="82dea-167">String</span><span class="sxs-lookup"><span data-stu-id="82dea-167">String</span></span>|<span data-ttu-id="82dea-168">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="82dea-168">The more information Url.</span></span> <span data-ttu-id="82dea-169">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="82dea-169">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="82dea-170">owner</span><span class="sxs-lookup"><span data-stu-id="82dea-170">owner</span></span>|<span data-ttu-id="82dea-171">String</span><span class="sxs-lookup"><span data-stu-id="82dea-171">String</span></span>|<span data-ttu-id="82dea-172">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="82dea-172">The owner of the app.</span></span> <span data-ttu-id="82dea-173">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="82dea-173">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="82dea-174">developer</span><span class="sxs-lookup"><span data-stu-id="82dea-174">developer</span></span>|<span data-ttu-id="82dea-175">String</span><span class="sxs-lookup"><span data-stu-id="82dea-175">String</span></span>|<span data-ttu-id="82dea-176">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="82dea-176">The developer of the app.</span></span> <span data-ttu-id="82dea-177">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="82dea-177">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="82dea-178">notas</span><span class="sxs-lookup"><span data-stu-id="82dea-178">notes</span></span>|<span data-ttu-id="82dea-179">String</span><span class="sxs-lookup"><span data-stu-id="82dea-179">String</span></span>|<span data-ttu-id="82dea-180">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="82dea-180">Notes for the app.</span></span> <span data-ttu-id="82dea-181">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="82dea-181">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="82dea-182">publishingState</span><span class="sxs-lookup"><span data-stu-id="82dea-182">publishingState</span></span>|[<span data-ttu-id="82dea-183">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="82dea-183">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="82dea-184">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="82dea-184">The publishing state for the app.</span></span> <span data-ttu-id="82dea-185">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="82dea-185">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="82dea-186">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="82dea-186">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="82dea-187">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="82dea-187">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="82dea-188">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="82dea-188">committedContentVersion</span></span>|<span data-ttu-id="82dea-189">String</span><span class="sxs-lookup"><span data-stu-id="82dea-189">String</span></span>|<span data-ttu-id="82dea-190">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="82dea-190">The internal committed content version.</span></span> <span data-ttu-id="82dea-191">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="82dea-191">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="82dea-192">fileName</span><span class="sxs-lookup"><span data-stu-id="82dea-192">fileName</span></span>|<span data-ttu-id="82dea-193">String</span><span class="sxs-lookup"><span data-stu-id="82dea-193">String</span></span>|<span data-ttu-id="82dea-194">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="82dea-194">The name of the main Lob application file.</span></span> <span data-ttu-id="82dea-195">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="82dea-195">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="82dea-196">size</span><span class="sxs-lookup"><span data-stu-id="82dea-196">size</span></span>|<span data-ttu-id="82dea-197">Int64</span><span class="sxs-lookup"><span data-stu-id="82dea-197">Int64</span></span>|<span data-ttu-id="82dea-198">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="82dea-198">The total size, including all uploaded files.</span></span> <span data-ttu-id="82dea-199">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="82dea-199">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="82dea-200">commandLine</span><span class="sxs-lookup"><span data-stu-id="82dea-200">commandLine</span></span>|<span data-ttu-id="82dea-201">String</span><span class="sxs-lookup"><span data-stu-id="82dea-201">String</span></span>|<span data-ttu-id="82dea-202">Línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="82dea-202">The command line.</span></span>|
|<span data-ttu-id="82dea-203">productCode</span><span class="sxs-lookup"><span data-stu-id="82dea-203">productCode</span></span>|<span data-ttu-id="82dea-204">String</span><span class="sxs-lookup"><span data-stu-id="82dea-204">String</span></span>|<span data-ttu-id="82dea-205">Código del producto.</span><span class="sxs-lookup"><span data-stu-id="82dea-205">The product code.</span></span>|
|<span data-ttu-id="82dea-206">productVersion</span><span class="sxs-lookup"><span data-stu-id="82dea-206">productVersion</span></span>|<span data-ttu-id="82dea-207">String</span><span class="sxs-lookup"><span data-stu-id="82dea-207">String</span></span>|<span data-ttu-id="82dea-208">Versión del producto de la aplicación de línea de negocio (LoB) de MSI para Windows Mobile.</span><span class="sxs-lookup"><span data-stu-id="82dea-208">The product version of Windows Mobile MSI Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="82dea-209">ignoreVersionDetection</span><span class="sxs-lookup"><span data-stu-id="82dea-209">ignoreVersionDetection</span></span>|<span data-ttu-id="82dea-210">Booleano</span><span class="sxs-lookup"><span data-stu-id="82dea-210">Boolean</span></span>|<span data-ttu-id="82dea-211">Valor booleano que controla si la versión de la aplicación se usará para detectar la aplicación después de instalarla en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="82dea-211">A boolean to control whether the app's version will be used to detect the app after it is installed on a device.</span></span> <span data-ttu-id="82dea-212">Establézcalo en True para aplicaciones de línea de negocio (LoB) de MSI para Windows Mobile que usen la característica de actualización automática.</span><span class="sxs-lookup"><span data-stu-id="82dea-212">Set this to true for Windows Mobile MSI Line of Business (LoB) apps that use a self update feature.</span></span>|



## <a name="response"></a><span data-ttu-id="82dea-213">Respuesta</span><span class="sxs-lookup"><span data-stu-id="82dea-213">Response</span></span>
<span data-ttu-id="82dea-214">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="82dea-214">If successful, this method returns a `200 OK` response code and an updated [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="82dea-215">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="82dea-215">Example</span></span>
### <a name="request"></a><span data-ttu-id="82dea-216">Solicitud</span><span class="sxs-lookup"><span data-stu-id="82dea-216">Request</span></span>
<span data-ttu-id="82dea-217">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="82dea-217">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 855

{
  "@odata.type": "#microsoft.graph.windowsMobileMSI",
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
  "commandLine": "Command Line value",
  "productCode": "Product Code value",
  "productVersion": "Product Version value",
  "ignoreVersionDetection": true
}
```

### <a name="response"></a><span data-ttu-id="82dea-218">Respuesta</span><span class="sxs-lookup"><span data-stu-id="82dea-218">Response</span></span>
<span data-ttu-id="82dea-p119">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="82dea-p119">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1027

{
  "@odata.type": "#microsoft.graph.windowsMobileMSI",
  "id": "aa453e5d-3e5d-aa45-5d3e-45aa5d3e45aa",
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
  "commandLine": "Command Line value",
  "productCode": "Product Code value",
  "productVersion": "Product Version value",
  "ignoreVersionDetection": true
}
```


