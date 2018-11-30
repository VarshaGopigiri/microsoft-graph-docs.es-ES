---
title: Crear iosLobApp
description: Cree un objeto iosLobApp.
ms.openlocfilehash: 2720192b45dcc55f74881163c93205ad5fecb24c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084395"
---
# <a name="create-ioslobapp"></a><span data-ttu-id="e9c4c-103">Crear iosLobApp</span><span class="sxs-lookup"><span data-stu-id="e9c4c-103">Create iosLobApp</span></span>

> <span data-ttu-id="e9c4c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e9c4c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e9c4c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e9c4c-107">Cree un objeto [iosLobApp](../resources/intune-apps-ioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-107">Create a new [iosLobApp](../resources/intune-apps-ioslobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e9c4c-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e9c4c-108">Prerequisites</span></span>
<span data-ttu-id="e9c4c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e9c4c-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e9c4c-111">Permission type</span></span>|<span data-ttu-id="e9c4c-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e9c4c-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e9c4c-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e9c4c-113">Delegated (work or school account)</span></span>|<span data-ttu-id="e9c4c-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e9c4c-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="e9c4c-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e9c4c-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e9c4c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-116">Not supported.</span></span>|
|<span data-ttu-id="e9c4c-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e9c4c-117">Application</span></span>|<span data-ttu-id="e9c4c-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e9c4c-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e9c4c-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="e9c4c-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e9c4c-120">Request headers</span></span>
|<span data-ttu-id="e9c4c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9c4c-121">Header</span></span>|<span data-ttu-id="e9c4c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e9c4c-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e9c4c-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="e9c4c-123">Authorization</span></span>|<span data-ttu-id="e9c4c-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e9c4c-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e9c4c-125">Accept</span></span>|<span data-ttu-id="e9c4c-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e9c4c-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e9c4c-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e9c4c-127">Request body</span></span>
<span data-ttu-id="e9c4c-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosLobApp.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-128">In the request body, supply a JSON representation for the iosLobApp object.</span></span>

<span data-ttu-id="e9c4c-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosLobApp.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-129">The following table shows the properties that are required when you create the iosLobApp.</span></span>

|<span data-ttu-id="e9c4c-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e9c4c-130">Property</span></span>|<span data-ttu-id="e9c4c-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9c4c-131">Type</span></span>|<span data-ttu-id="e9c4c-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9c4c-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e9c4c-133">id</span><span class="sxs-lookup"><span data-stu-id="e9c4c-133">id</span></span>|<span data-ttu-id="e9c4c-134">String</span><span class="sxs-lookup"><span data-stu-id="e9c4c-134">String</span></span>|<span data-ttu-id="e9c4c-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-135">Key of the entity.</span></span> <span data-ttu-id="e9c4c-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e9c4c-137">displayName</span><span class="sxs-lookup"><span data-stu-id="e9c4c-137">displayName</span></span>|<span data-ttu-id="e9c4c-138">String</span><span class="sxs-lookup"><span data-stu-id="e9c4c-138">String</span></span>|<span data-ttu-id="e9c4c-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="e9c4c-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e9c4c-141">descripción</span><span class="sxs-lookup"><span data-stu-id="e9c4c-141">description</span></span>|<span data-ttu-id="e9c4c-142">String</span><span class="sxs-lookup"><span data-stu-id="e9c4c-142">String</span></span>|<span data-ttu-id="e9c4c-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-143">The description of the app.</span></span> <span data-ttu-id="e9c4c-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e9c4c-145">publicador</span><span class="sxs-lookup"><span data-stu-id="e9c4c-145">publisher</span></span>|<span data-ttu-id="e9c4c-146">String</span><span class="sxs-lookup"><span data-stu-id="e9c4c-146">String</span></span>|<span data-ttu-id="e9c4c-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-147">The publisher of the app.</span></span> <span data-ttu-id="e9c4c-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e9c4c-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="e9c4c-149">largeIcon</span></span>|[<span data-ttu-id="e9c4c-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="e9c4c-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="e9c4c-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="e9c4c-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e9c4c-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="e9c4c-153">createdDateTime</span></span>|<span data-ttu-id="e9c4c-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e9c4c-154">DateTimeOffset</span></span>|<span data-ttu-id="e9c4c-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-155">The date and time the app was created.</span></span> <span data-ttu-id="e9c4c-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e9c4c-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="e9c4c-157">lastModifiedDateTime</span></span>|<span data-ttu-id="e9c4c-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e9c4c-158">DateTimeOffset</span></span>|<span data-ttu-id="e9c4c-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-159">The date and time the app was last modified.</span></span> <span data-ttu-id="e9c4c-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e9c4c-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="e9c4c-161">isFeatured</span></span>|<span data-ttu-id="e9c4c-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="e9c4c-162">Boolean</span></span>|<span data-ttu-id="e9c4c-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e9c4c-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="e9c4c-164">privacyInformationUrl</span></span>|<span data-ttu-id="e9c4c-165">String</span><span class="sxs-lookup"><span data-stu-id="e9c4c-165">String</span></span>|<span data-ttu-id="e9c4c-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-166">The privacy statement Url.</span></span> <span data-ttu-id="e9c4c-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e9c4c-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="e9c4c-168">informationUrl</span></span>|<span data-ttu-id="e9c4c-169">String</span><span class="sxs-lookup"><span data-stu-id="e9c4c-169">String</span></span>|<span data-ttu-id="e9c4c-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-170">The more information Url.</span></span> <span data-ttu-id="e9c4c-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e9c4c-172">owner</span><span class="sxs-lookup"><span data-stu-id="e9c4c-172">owner</span></span>|<span data-ttu-id="e9c4c-173">String</span><span class="sxs-lookup"><span data-stu-id="e9c4c-173">String</span></span>|<span data-ttu-id="e9c4c-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-174">The owner of the app.</span></span> <span data-ttu-id="e9c4c-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e9c4c-176">developer</span><span class="sxs-lookup"><span data-stu-id="e9c4c-176">developer</span></span>|<span data-ttu-id="e9c4c-177">String</span><span class="sxs-lookup"><span data-stu-id="e9c4c-177">String</span></span>|<span data-ttu-id="e9c4c-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-178">The developer of the app.</span></span> <span data-ttu-id="e9c4c-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e9c4c-180">notas</span><span class="sxs-lookup"><span data-stu-id="e9c4c-180">notes</span></span>|<span data-ttu-id="e9c4c-181">String</span><span class="sxs-lookup"><span data-stu-id="e9c4c-181">String</span></span>|<span data-ttu-id="e9c4c-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-182">Notes for the app.</span></span> <span data-ttu-id="e9c4c-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e9c4c-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="e9c4c-184">uploadState</span></span>|<span data-ttu-id="e9c4c-185">Int32</span><span class="sxs-lookup"><span data-stu-id="e9c4c-185">Int32</span></span>|<span data-ttu-id="e9c4c-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-186">The upload state.</span></span> <span data-ttu-id="e9c4c-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="e9c4c-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="e9c4c-188">publishingState</span></span>|[<span data-ttu-id="e9c4c-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="e9c4c-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="e9c4c-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-190">The publishing state for the app.</span></span> <span data-ttu-id="e9c4c-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="e9c4c-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="e9c4c-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="e9c4c-194">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="e9c4c-194">committedContentVersion</span></span>|<span data-ttu-id="e9c4c-195">String</span><span class="sxs-lookup"><span data-stu-id="e9c4c-195">String</span></span>|<span data-ttu-id="e9c4c-196">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-196">The internal committed content version.</span></span> <span data-ttu-id="e9c4c-197">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-197">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="e9c4c-198">fileName</span><span class="sxs-lookup"><span data-stu-id="e9c4c-198">fileName</span></span>|<span data-ttu-id="e9c4c-199">String</span><span class="sxs-lookup"><span data-stu-id="e9c4c-199">String</span></span>|<span data-ttu-id="e9c4c-200">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-200">The name of the main Lob application file.</span></span> <span data-ttu-id="e9c4c-201">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-201">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="e9c4c-202">size</span><span class="sxs-lookup"><span data-stu-id="e9c4c-202">size</span></span>|<span data-ttu-id="e9c4c-203">Int64</span><span class="sxs-lookup"><span data-stu-id="e9c4c-203">Int64</span></span>|<span data-ttu-id="e9c4c-204">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-204">The total size, including all uploaded files.</span></span> <span data-ttu-id="e9c4c-205">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9c4c-205">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="e9c4c-206">bundleId</span><span class="sxs-lookup"><span data-stu-id="e9c4c-206">bundleId</span></span>|<span data-ttu-id="e9c4c-207">String</span><span class="sxs-lookup"><span data-stu-id="e9c4c-207">String</span></span>|<span data-ttu-id="e9c4c-208">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-208">The Identity Name.</span></span>|
|<span data-ttu-id="e9c4c-209">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="e9c4c-209">applicableDeviceType</span></span>|[<span data-ttu-id="e9c4c-210">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="e9c4c-210">iosDeviceType</span></span>](../resources/intune-apps-iosdevicetype.md)|<span data-ttu-id="e9c4c-211">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-211">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="e9c4c-212">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="e9c4c-212">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="e9c4c-213">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="e9c4c-213">iosMinimumOperatingSystem</span></span>](../resources/intune-apps-iosminimumoperatingsystem.md)|<span data-ttu-id="e9c4c-214">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-214">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="e9c4c-215">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="e9c4c-215">expirationDateTime</span></span>|<span data-ttu-id="e9c4c-216">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e9c4c-216">DateTimeOffset</span></span>|<span data-ttu-id="e9c4c-217">Fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-217">The expiration time.</span></span>|
|<span data-ttu-id="e9c4c-218">versionNumber</span><span class="sxs-lookup"><span data-stu-id="e9c4c-218">versionNumber</span></span>|<span data-ttu-id="e9c4c-219">String</span><span class="sxs-lookup"><span data-stu-id="e9c4c-219">String</span></span>|<span data-ttu-id="e9c4c-220">El número de la versión de la aplicación de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-220">The version number of iOS Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="e9c4c-221">buildNumber</span><span class="sxs-lookup"><span data-stu-id="e9c4c-221">buildNumber</span></span>|<span data-ttu-id="e9c4c-222">String</span><span class="sxs-lookup"><span data-stu-id="e9c4c-222">String</span></span>|<span data-ttu-id="e9c4c-223">El número de compilación de la aplicación de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-223">The build number of iOS Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="e9c4c-224">identityVersion</span><span class="sxs-lookup"><span data-stu-id="e9c4c-224">identityVersion</span></span>|<span data-ttu-id="e9c4c-225">String</span><span class="sxs-lookup"><span data-stu-id="e9c4c-225">String</span></span>|<span data-ttu-id="e9c4c-226">Versión de la identidad.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-226">The identity version.</span></span>|



## <a name="response"></a><span data-ttu-id="e9c4c-227">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9c4c-227">Response</span></span>
<span data-ttu-id="e9c4c-228">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosLobApp](../resources/intune-apps-ioslobapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-228">If successful, this method returns a `201 Created` response code and a [iosLobApp](../resources/intune-apps-ioslobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e9c4c-229">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e9c4c-229">Example</span></span>
### <a name="request"></a><span data-ttu-id="e9c4c-230">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e9c4c-230">Request</span></span>
<span data-ttu-id="e9c4c-231">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-231">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 1343

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
  "buildNumber": "Build Number value",
  "identityVersion": "Identity Version value"
}
```

### <a name="response"></a><span data-ttu-id="e9c4c-232">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9c4c-232">Response</span></span>
<span data-ttu-id="e9c4c-p120">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e9c4c-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1451

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
  "uploadState": 11,
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
  "buildNumber": "Build Number value",
  "identityVersion": "Identity Version value"
}
```





