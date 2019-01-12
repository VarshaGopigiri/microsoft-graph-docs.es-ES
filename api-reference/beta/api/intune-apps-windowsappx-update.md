---
title: Actualizar windowsAppX
description: Actualizar las propiedades de un objeto windowsAppX.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 7123364c618dbbdf0eb37dd9e080f54a67b6809b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27946171"
---
# <a name="update-windowsappx"></a><span data-ttu-id="45a0b-103">Actualizar windowsAppX</span><span class="sxs-lookup"><span data-stu-id="45a0b-103">Update windowsAppX</span></span>

> <span data-ttu-id="45a0b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="45a0b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="45a0b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="45a0b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="45a0b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="45a0b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="45a0b-107">Actualizar las propiedades de un objeto [windowsAppX](../resources/intune-apps-windowsappx.md) .</span><span class="sxs-lookup"><span data-stu-id="45a0b-107">Update the properties of a [windowsAppX](../resources/intune-apps-windowsappx.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="45a0b-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="45a0b-108">Prerequisites</span></span>
<span data-ttu-id="45a0b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="45a0b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="45a0b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="45a0b-111">Permission type</span></span>|<span data-ttu-id="45a0b-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="45a0b-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="45a0b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="45a0b-113">Delegated (work or school account)</span></span>|<span data-ttu-id="45a0b-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="45a0b-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="45a0b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="45a0b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="45a0b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="45a0b-116">Not supported.</span></span>|
|<span data-ttu-id="45a0b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="45a0b-117">Application</span></span>|<span data-ttu-id="45a0b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="45a0b-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="45a0b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="45a0b-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app
```

## <a name="request-headers"></a><span data-ttu-id="45a0b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="45a0b-120">Request headers</span></span>
|<span data-ttu-id="45a0b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="45a0b-121">Header</span></span>|<span data-ttu-id="45a0b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="45a0b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="45a0b-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="45a0b-123">Authorization</span></span>|<span data-ttu-id="45a0b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="45a0b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="45a0b-125">Accept</span><span class="sxs-lookup"><span data-stu-id="45a0b-125">Accept</span></span>|<span data-ttu-id="45a0b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="45a0b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="45a0b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="45a0b-127">Request body</span></span>
<span data-ttu-id="45a0b-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [windowsAppX](../resources/intune-apps-windowsappx.md) .</span><span class="sxs-lookup"><span data-stu-id="45a0b-128">In the request body, supply a JSON representation for the [windowsAppX](../resources/intune-apps-windowsappx.md) object.</span></span>

<span data-ttu-id="45a0b-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [windowsAppX](../resources/intune-apps-windowsappx.md).</span><span class="sxs-lookup"><span data-stu-id="45a0b-129">The following table shows the properties that are required when you create the [windowsAppX](../resources/intune-apps-windowsappx.md).</span></span>

|<span data-ttu-id="45a0b-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="45a0b-130">Property</span></span>|<span data-ttu-id="45a0b-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="45a0b-131">Type</span></span>|<span data-ttu-id="45a0b-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="45a0b-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="45a0b-133">id</span><span class="sxs-lookup"><span data-stu-id="45a0b-133">id</span></span>|<span data-ttu-id="45a0b-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="45a0b-134">String</span></span>|<span data-ttu-id="45a0b-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="45a0b-135">Key of the entity.</span></span> <span data-ttu-id="45a0b-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="45a0b-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="45a0b-137">displayName</span><span class="sxs-lookup"><span data-stu-id="45a0b-137">displayName</span></span>|<span data-ttu-id="45a0b-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="45a0b-138">String</span></span>|<span data-ttu-id="45a0b-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="45a0b-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="45a0b-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="45a0b-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="45a0b-141">descripción</span><span class="sxs-lookup"><span data-stu-id="45a0b-141">description</span></span>|<span data-ttu-id="45a0b-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="45a0b-142">String</span></span>|<span data-ttu-id="45a0b-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="45a0b-143">The description of the app.</span></span> <span data-ttu-id="45a0b-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="45a0b-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="45a0b-145">publicador</span><span class="sxs-lookup"><span data-stu-id="45a0b-145">publisher</span></span>|<span data-ttu-id="45a0b-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="45a0b-146">String</span></span>|<span data-ttu-id="45a0b-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="45a0b-147">The publisher of the app.</span></span> <span data-ttu-id="45a0b-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="45a0b-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="45a0b-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="45a0b-149">largeIcon</span></span>|[<span data-ttu-id="45a0b-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="45a0b-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="45a0b-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="45a0b-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="45a0b-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="45a0b-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="45a0b-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="45a0b-153">createdDateTime</span></span>|<span data-ttu-id="45a0b-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="45a0b-154">DateTimeOffset</span></span>|<span data-ttu-id="45a0b-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="45a0b-155">The date and time the app was created.</span></span> <span data-ttu-id="45a0b-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="45a0b-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="45a0b-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="45a0b-157">lastModifiedDateTime</span></span>|<span data-ttu-id="45a0b-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="45a0b-158">DateTimeOffset</span></span>|<span data-ttu-id="45a0b-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="45a0b-159">The date and time the app was last modified.</span></span> <span data-ttu-id="45a0b-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="45a0b-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="45a0b-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="45a0b-161">isFeatured</span></span>|<span data-ttu-id="45a0b-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="45a0b-162">Boolean</span></span>|<span data-ttu-id="45a0b-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="45a0b-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="45a0b-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="45a0b-164">privacyInformationUrl</span></span>|<span data-ttu-id="45a0b-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="45a0b-165">String</span></span>|<span data-ttu-id="45a0b-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="45a0b-166">The privacy statement Url.</span></span> <span data-ttu-id="45a0b-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="45a0b-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="45a0b-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="45a0b-168">informationUrl</span></span>|<span data-ttu-id="45a0b-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="45a0b-169">String</span></span>|<span data-ttu-id="45a0b-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="45a0b-170">The more information Url.</span></span> <span data-ttu-id="45a0b-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="45a0b-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="45a0b-172">owner</span><span class="sxs-lookup"><span data-stu-id="45a0b-172">owner</span></span>|<span data-ttu-id="45a0b-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="45a0b-173">String</span></span>|<span data-ttu-id="45a0b-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="45a0b-174">The owner of the app.</span></span> <span data-ttu-id="45a0b-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="45a0b-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="45a0b-176">developer</span><span class="sxs-lookup"><span data-stu-id="45a0b-176">developer</span></span>|<span data-ttu-id="45a0b-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="45a0b-177">String</span></span>|<span data-ttu-id="45a0b-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="45a0b-178">The developer of the app.</span></span> <span data-ttu-id="45a0b-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="45a0b-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="45a0b-180">notas</span><span class="sxs-lookup"><span data-stu-id="45a0b-180">notes</span></span>|<span data-ttu-id="45a0b-181">Cadena</span><span class="sxs-lookup"><span data-stu-id="45a0b-181">String</span></span>|<span data-ttu-id="45a0b-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="45a0b-182">Notes for the app.</span></span> <span data-ttu-id="45a0b-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="45a0b-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="45a0b-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="45a0b-184">uploadState</span></span>|<span data-ttu-id="45a0b-185">Int32</span><span class="sxs-lookup"><span data-stu-id="45a0b-185">Int32</span></span>|<span data-ttu-id="45a0b-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="45a0b-186">The upload state.</span></span> <span data-ttu-id="45a0b-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="45a0b-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="45a0b-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="45a0b-188">publishingState</span></span>|[<span data-ttu-id="45a0b-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="45a0b-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="45a0b-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="45a0b-190">The publishing state for the app.</span></span> <span data-ttu-id="45a0b-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="45a0b-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="45a0b-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="45a0b-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="45a0b-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="45a0b-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="45a0b-194">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="45a0b-194">committedContentVersion</span></span>|<span data-ttu-id="45a0b-195">Cadena</span><span class="sxs-lookup"><span data-stu-id="45a0b-195">String</span></span>|<span data-ttu-id="45a0b-196">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="45a0b-196">The internal committed content version.</span></span> <span data-ttu-id="45a0b-197">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="45a0b-197">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="45a0b-198">fileName</span><span class="sxs-lookup"><span data-stu-id="45a0b-198">fileName</span></span>|<span data-ttu-id="45a0b-199">Cadena</span><span class="sxs-lookup"><span data-stu-id="45a0b-199">String</span></span>|<span data-ttu-id="45a0b-200">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="45a0b-200">The name of the main Lob application file.</span></span> <span data-ttu-id="45a0b-201">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="45a0b-201">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="45a0b-202">size</span><span class="sxs-lookup"><span data-stu-id="45a0b-202">size</span></span>|<span data-ttu-id="45a0b-203">Int64</span><span class="sxs-lookup"><span data-stu-id="45a0b-203">Int64</span></span>|<span data-ttu-id="45a0b-204">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="45a0b-204">The total size, including all uploaded files.</span></span> <span data-ttu-id="45a0b-205">Heredado de [mobileLobApp](../resources/intune-apps-mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="45a0b-205">Inherited from [mobileLobApp](../resources/intune-apps-mobilelobapp.md)</span></span>|
|<span data-ttu-id="45a0b-206">applicableArchitectures</span><span class="sxs-lookup"><span data-stu-id="45a0b-206">applicableArchitectures</span></span>|[<span data-ttu-id="45a0b-207">windowsArchitecture</span><span class="sxs-lookup"><span data-stu-id="45a0b-207">windowsArchitecture</span></span>](../resources/intune-apps-windowsarchitecture.md)|<span data-ttu-id="45a0b-208">Arquitecturas de Windows en las que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="45a0b-208">The Windows architecture(s) for which this app can run on.</span></span> <span data-ttu-id="45a0b-209">Los valores posibles son: `none`, `x86`, `x64`, `arm` y `neutral`.</span><span class="sxs-lookup"><span data-stu-id="45a0b-209">Possible values are: `none`, `x86`, `x64`, `arm`, `neutral`.</span></span>|
|<span data-ttu-id="45a0b-210">identityName</span><span class="sxs-lookup"><span data-stu-id="45a0b-210">identityName</span></span>|<span data-ttu-id="45a0b-211">Cadena</span><span class="sxs-lookup"><span data-stu-id="45a0b-211">String</span></span>|<span data-ttu-id="45a0b-212">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="45a0b-212">The Identity Name.</span></span>|
|<span data-ttu-id="45a0b-213">identityPublisherHash</span><span class="sxs-lookup"><span data-stu-id="45a0b-213">identityPublisherHash</span></span>|<span data-ttu-id="45a0b-214">Cadena</span><span class="sxs-lookup"><span data-stu-id="45a0b-214">String</span></span>|<span data-ttu-id="45a0b-215">Hash del publicador de identidad.</span><span class="sxs-lookup"><span data-stu-id="45a0b-215">The Identity Publisher Hash.</span></span>|
|<span data-ttu-id="45a0b-216">identityResourceIdentifier</span><span class="sxs-lookup"><span data-stu-id="45a0b-216">identityResourceIdentifier</span></span>|<span data-ttu-id="45a0b-217">Cadena</span><span class="sxs-lookup"><span data-stu-id="45a0b-217">String</span></span>|<span data-ttu-id="45a0b-218">Identificador del recurso de identidad.</span><span class="sxs-lookup"><span data-stu-id="45a0b-218">The Identity Resource Identifier.</span></span>|
|<span data-ttu-id="45a0b-219">isBundle</span><span class="sxs-lookup"><span data-stu-id="45a0b-219">isBundle</span></span>|<span data-ttu-id="45a0b-220">Booleano</span><span class="sxs-lookup"><span data-stu-id="45a0b-220">Boolean</span></span>|<span data-ttu-id="45a0b-221">Indica si la aplicación es una agrupación.</span><span class="sxs-lookup"><span data-stu-id="45a0b-221">Whether or not the app is a bundle.</span></span>|
|<span data-ttu-id="45a0b-222">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="45a0b-222">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="45a0b-223">windowsMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="45a0b-223">windowsMinimumOperatingSystem</span></span>](../resources/intune-apps-windowsminimumoperatingsystem.md)|<span data-ttu-id="45a0b-224">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="45a0b-224">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="45a0b-225">identityVersion</span><span class="sxs-lookup"><span data-stu-id="45a0b-225">identityVersion</span></span>|<span data-ttu-id="45a0b-226">Cadena</span><span class="sxs-lookup"><span data-stu-id="45a0b-226">String</span></span>|<span data-ttu-id="45a0b-227">Versión de la identidad.</span><span class="sxs-lookup"><span data-stu-id="45a0b-227">The identity version.</span></span>|



## <a name="response"></a><span data-ttu-id="45a0b-228">Respuesta</span><span class="sxs-lookup"><span data-stu-id="45a0b-228">Response</span></span>
<span data-ttu-id="45a0b-229">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [windowsAppX](../resources/intune-apps-windowsappx.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="45a0b-229">If successful, this method returns a `200 OK` response code and an updated [windowsAppX](../resources/intune-apps-windowsappx.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="45a0b-230">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="45a0b-230">Example</span></span>
### <a name="request"></a><span data-ttu-id="45a0b-231">Solicitud</span><span class="sxs-lookup"><span data-stu-id="45a0b-231">Request</span></span>
<span data-ttu-id="45a0b-232">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="45a0b-232">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1269

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
  "committedContentVersion": "Committed Content Version value",
  "fileName": "File Name value",
  "size": 4,
  "applicableArchitectures": "x86",
  "identityName": "Identity Name value",
  "identityPublisherHash": "Identity Publisher Hash value",
  "identityResourceIdentifier": "Identity Resource Identifier value",
  "isBundle": true,
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem",
    "v8_0": true,
    "v8_1": true,
    "v10_0": true,
    "v10_1607": true,
    "v10_1703": true,
    "v10_1709": true,
    "v10_1803": true
  },
  "identityVersion": "Identity Version value"
}
```

### <a name="response"></a><span data-ttu-id="45a0b-233">Respuesta</span><span class="sxs-lookup"><span data-stu-id="45a0b-233">Response</span></span>
<span data-ttu-id="45a0b-p121">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="45a0b-p121">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1427

{
  "@odata.type": "#microsoft.graph.windowsAppX",
  "id": "b5179a93-9a93-b517-939a-17b5939a17b5",
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
  "applicableArchitectures": "x86",
  "identityName": "Identity Name value",
  "identityPublisherHash": "Identity Publisher Hash value",
  "identityResourceIdentifier": "Identity Resource Identifier value",
  "isBundle": true,
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem",
    "v8_0": true,
    "v8_1": true,
    "v10_0": true,
    "v10_1607": true,
    "v10_1703": true,
    "v10_1709": true,
    "v10_1803": true
  },
  "identityVersion": "Identity Version value"
}
```





