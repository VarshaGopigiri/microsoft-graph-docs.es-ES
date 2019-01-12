---
title: Crear windowsMobileMSI
description: Crear un objeto windowsMobileMSI.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 9fa4fd686c870a2f649c8a8af5b3f7fb909ece90
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27952919"
---
# <a name="create-windowsmobilemsi"></a><span data-ttu-id="0865b-103">Crear windowsMobileMSI</span><span class="sxs-lookup"><span data-stu-id="0865b-103">Create windowsMobileMSI</span></span>

> <span data-ttu-id="0865b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0865b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0865b-105">Crear un objeto [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md).</span><span class="sxs-lookup"><span data-stu-id="0865b-105">Create a new [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0865b-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0865b-106">Prerequisites</span></span>
<span data-ttu-id="0865b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0865b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0865b-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0865b-109">Permission type</span></span>|<span data-ttu-id="0865b-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0865b-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0865b-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0865b-111">Delegated (work or school account)</span></span>|<span data-ttu-id="0865b-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0865b-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="0865b-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0865b-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0865b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0865b-114">Not supported.</span></span>|
|<span data-ttu-id="0865b-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0865b-115">Application</span></span>|<span data-ttu-id="0865b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0865b-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0865b-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0865b-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="0865b-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0865b-118">Request headers</span></span>
|<span data-ttu-id="0865b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0865b-119">Header</span></span>|<span data-ttu-id="0865b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0865b-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0865b-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="0865b-121">Authorization</span></span>|<span data-ttu-id="0865b-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0865b-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0865b-123">Accept</span><span class="sxs-lookup"><span data-stu-id="0865b-123">Accept</span></span>|<span data-ttu-id="0865b-124">application/json</span><span class="sxs-lookup"><span data-stu-id="0865b-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0865b-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0865b-125">Request body</span></span>
<span data-ttu-id="0865b-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsMobileMSI.</span><span class="sxs-lookup"><span data-stu-id="0865b-126">In the request body, supply a JSON representation for the windowsMobileMSI object.</span></span>

<span data-ttu-id="0865b-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsMobileMSI.</span><span class="sxs-lookup"><span data-stu-id="0865b-127">The following table shows the properties that are required when you create the windowsMobileMSI.</span></span>

|<span data-ttu-id="0865b-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0865b-128">Property</span></span>|<span data-ttu-id="0865b-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="0865b-129">Type</span></span>|<span data-ttu-id="0865b-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="0865b-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0865b-131">id</span><span class="sxs-lookup"><span data-stu-id="0865b-131">id</span></span>|<span data-ttu-id="0865b-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="0865b-132">String</span></span>|<span data-ttu-id="0865b-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="0865b-133">Key of the entity.</span></span> <span data-ttu-id="0865b-134">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0865b-134">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="0865b-135">displayName</span><span class="sxs-lookup"><span data-stu-id="0865b-135">displayName</span></span>|<span data-ttu-id="0865b-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="0865b-136">String</span></span>|<span data-ttu-id="0865b-137">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="0865b-137">The admin provided or imported title of the app.</span></span> <span data-ttu-id="0865b-138">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0865b-138">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="0865b-139">descripción</span><span class="sxs-lookup"><span data-stu-id="0865b-139">description</span></span>|<span data-ttu-id="0865b-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="0865b-140">String</span></span>|<span data-ttu-id="0865b-141">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0865b-141">The description of the app.</span></span> <span data-ttu-id="0865b-142">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0865b-142">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="0865b-143">publicador</span><span class="sxs-lookup"><span data-stu-id="0865b-143">publisher</span></span>|<span data-ttu-id="0865b-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="0865b-144">String</span></span>|<span data-ttu-id="0865b-145">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0865b-145">The publisher of the app.</span></span> <span data-ttu-id="0865b-146">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0865b-146">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="0865b-147">largeIcon</span><span class="sxs-lookup"><span data-stu-id="0865b-147">largeIcon</span></span>|[<span data-ttu-id="0865b-148">mimeContent</span><span class="sxs-lookup"><span data-stu-id="0865b-148">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="0865b-149">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="0865b-149">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="0865b-150">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0865b-150">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="0865b-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="0865b-151">createdDateTime</span></span>|<span data-ttu-id="0865b-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0865b-152">DateTimeOffset</span></span>|<span data-ttu-id="0865b-153">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0865b-153">The date and time the app was created.</span></span> <span data-ttu-id="0865b-154">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0865b-154">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="0865b-155">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="0865b-155">lastModifiedDateTime</span></span>|<span data-ttu-id="0865b-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0865b-156">DateTimeOffset</span></span>|<span data-ttu-id="0865b-157">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0865b-157">The date and time the app was last modified.</span></span> <span data-ttu-id="0865b-158">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0865b-158">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="0865b-159">isFeatured</span><span class="sxs-lookup"><span data-stu-id="0865b-159">isFeatured</span></span>|<span data-ttu-id="0865b-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="0865b-160">Boolean</span></span>|<span data-ttu-id="0865b-161">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0865b-161">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="0865b-162">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="0865b-162">privacyInformationUrl</span></span>|<span data-ttu-id="0865b-163">Cadena</span><span class="sxs-lookup"><span data-stu-id="0865b-163">String</span></span>|<span data-ttu-id="0865b-164">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="0865b-164">The privacy statement Url.</span></span> <span data-ttu-id="0865b-165">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0865b-165">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="0865b-166">informationUrl</span><span class="sxs-lookup"><span data-stu-id="0865b-166">informationUrl</span></span>|<span data-ttu-id="0865b-167">Cadena</span><span class="sxs-lookup"><span data-stu-id="0865b-167">String</span></span>|<span data-ttu-id="0865b-168">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="0865b-168">The more information Url.</span></span> <span data-ttu-id="0865b-169">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0865b-169">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="0865b-170">owner</span><span class="sxs-lookup"><span data-stu-id="0865b-170">owner</span></span>|<span data-ttu-id="0865b-171">Cadena</span><span class="sxs-lookup"><span data-stu-id="0865b-171">String</span></span>|<span data-ttu-id="0865b-172">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0865b-172">The owner of the app.</span></span> <span data-ttu-id="0865b-173">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0865b-173">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="0865b-174">developer</span><span class="sxs-lookup"><span data-stu-id="0865b-174">developer</span></span>|<span data-ttu-id="0865b-175">Cadena</span><span class="sxs-lookup"><span data-stu-id="0865b-175">String</span></span>|<span data-ttu-id="0865b-176">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0865b-176">The developer of the app.</span></span> <span data-ttu-id="0865b-177">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0865b-177">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="0865b-178">notas</span><span class="sxs-lookup"><span data-stu-id="0865b-178">notes</span></span>|<span data-ttu-id="0865b-179">Cadena</span><span class="sxs-lookup"><span data-stu-id="0865b-179">String</span></span>|<span data-ttu-id="0865b-180">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0865b-180">Notes for the app.</span></span> <span data-ttu-id="0865b-181">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0865b-181">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="0865b-182">publishingState</span><span class="sxs-lookup"><span data-stu-id="0865b-182">publishingState</span></span>|[<span data-ttu-id="0865b-183">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="0865b-183">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="0865b-184">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0865b-184">The publishing state for the app.</span></span> <span data-ttu-id="0865b-185">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="0865b-185">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="0865b-186">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0865b-186">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="0865b-187">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="0865b-187">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="0865b-188">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="0865b-188">committedContentVersion</span></span>|<span data-ttu-id="0865b-189">Cadena</span><span class="sxs-lookup"><span data-stu-id="0865b-189">String</span></span>|<span data-ttu-id="0865b-190">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="0865b-190">The internal committed content version.</span></span> <span data-ttu-id="0865b-191">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="0865b-191">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="0865b-192">fileName</span><span class="sxs-lookup"><span data-stu-id="0865b-192">fileName</span></span>|<span data-ttu-id="0865b-193">Cadena</span><span class="sxs-lookup"><span data-stu-id="0865b-193">String</span></span>|<span data-ttu-id="0865b-194">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="0865b-194">The name of the main Lob application file.</span></span> <span data-ttu-id="0865b-195">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="0865b-195">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="0865b-196">size</span><span class="sxs-lookup"><span data-stu-id="0865b-196">size</span></span>|<span data-ttu-id="0865b-197">Int64</span><span class="sxs-lookup"><span data-stu-id="0865b-197">Int64</span></span>|<span data-ttu-id="0865b-198">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="0865b-198">The total size, including all uploaded files.</span></span> <span data-ttu-id="0865b-199">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="0865b-199">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="0865b-200">commandLine</span><span class="sxs-lookup"><span data-stu-id="0865b-200">commandLine</span></span>|<span data-ttu-id="0865b-201">Cadena</span><span class="sxs-lookup"><span data-stu-id="0865b-201">String</span></span>|<span data-ttu-id="0865b-202">Línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="0865b-202">The command line.</span></span>|
|<span data-ttu-id="0865b-203">productCode</span><span class="sxs-lookup"><span data-stu-id="0865b-203">productCode</span></span>|<span data-ttu-id="0865b-204">Cadena</span><span class="sxs-lookup"><span data-stu-id="0865b-204">String</span></span>|<span data-ttu-id="0865b-205">Código del producto.</span><span class="sxs-lookup"><span data-stu-id="0865b-205">The product code.</span></span>|
|<span data-ttu-id="0865b-206">productVersion</span><span class="sxs-lookup"><span data-stu-id="0865b-206">productVersion</span></span>|<span data-ttu-id="0865b-207">Cadena</span><span class="sxs-lookup"><span data-stu-id="0865b-207">String</span></span>|<span data-ttu-id="0865b-208">Versión del producto de la aplicación de línea de negocio (LoB) de MSI para Windows Mobile.</span><span class="sxs-lookup"><span data-stu-id="0865b-208">The product version of Windows Mobile MSI Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="0865b-209">ignoreVersionDetection</span><span class="sxs-lookup"><span data-stu-id="0865b-209">ignoreVersionDetection</span></span>|<span data-ttu-id="0865b-210">Booleano</span><span class="sxs-lookup"><span data-stu-id="0865b-210">Boolean</span></span>|<span data-ttu-id="0865b-211">Valor booleano que controla si la versión de la aplicación se usará para detectar la aplicación después de instalarla en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0865b-211">A boolean to control whether the app's version will be used to detect the app after it is installed on a device.</span></span> <span data-ttu-id="0865b-212">Establézcalo en True para aplicaciones de línea de negocio (LoB) de MSI para Windows Mobile que usen la característica de actualización automática.</span><span class="sxs-lookup"><span data-stu-id="0865b-212">Set this to true for Windows Mobile MSI Line of Business (LoB) apps that use a self update feature.</span></span>|



## <a name="response"></a><span data-ttu-id="0865b-213">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0865b-213">Response</span></span>
<span data-ttu-id="0865b-214">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0865b-214">If successful, this method returns a `201 Created` response code and a [windowsMobileMSI](../resources/intune-apps-windowsmobilemsi.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0865b-215">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0865b-215">Example</span></span>
### <a name="request"></a><span data-ttu-id="0865b-216">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0865b-216">Request</span></span>
<span data-ttu-id="0865b-217">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0865b-217">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
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

### <a name="response"></a><span data-ttu-id="0865b-218">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0865b-218">Response</span></span>
<span data-ttu-id="0865b-p119">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0865b-p119">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



