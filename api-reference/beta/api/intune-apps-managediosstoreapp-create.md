---
title: Crear managedIOSStoreApp
description: Cree un objeto managedIOSStoreApp.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 2733d9da3a870489e6a9c92e6ba25bf3ab023b61
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27915938"
---
# <a name="create-managediosstoreapp"></a><span data-ttu-id="f30f9-103">Crear managedIOSStoreApp</span><span class="sxs-lookup"><span data-stu-id="f30f9-103">Create managedIOSStoreApp</span></span>

> <span data-ttu-id="f30f9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f30f9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f30f9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f30f9-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f30f9-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f30f9-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f30f9-107">Cree un objeto [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="f30f9-107">Create a new [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f30f9-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f30f9-108">Prerequisites</span></span>
<span data-ttu-id="f30f9-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f30f9-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f30f9-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f30f9-111">Permission type</span></span>|<span data-ttu-id="f30f9-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f30f9-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f30f9-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f30f9-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f30f9-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f30f9-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="f30f9-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f30f9-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f30f9-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f30f9-116">Not supported.</span></span>|
|<span data-ttu-id="f30f9-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f30f9-117">Application</span></span>|<span data-ttu-id="f30f9-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f30f9-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f30f9-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f30f9-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="f30f9-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f30f9-120">Request headers</span></span>
|<span data-ttu-id="f30f9-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f30f9-121">Header</span></span>|<span data-ttu-id="f30f9-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f30f9-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f30f9-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="f30f9-123">Authorization</span></span>|<span data-ttu-id="f30f9-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f30f9-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f30f9-125">Accept</span><span class="sxs-lookup"><span data-stu-id="f30f9-125">Accept</span></span>|<span data-ttu-id="f30f9-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f30f9-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f30f9-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f30f9-127">Request body</span></span>
<span data-ttu-id="f30f9-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto managedIOSStoreApp.</span><span class="sxs-lookup"><span data-stu-id="f30f9-128">In the request body, supply a JSON representation for the managedIOSStoreApp object.</span></span>

<span data-ttu-id="f30f9-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto managedIOSStoreApp.</span><span class="sxs-lookup"><span data-stu-id="f30f9-129">The following table shows the properties that are required when you create the managedIOSStoreApp.</span></span>

|<span data-ttu-id="f30f9-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f30f9-130">Property</span></span>|<span data-ttu-id="f30f9-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="f30f9-131">Type</span></span>|<span data-ttu-id="f30f9-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="f30f9-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f30f9-133">id</span><span class="sxs-lookup"><span data-stu-id="f30f9-133">id</span></span>|<span data-ttu-id="f30f9-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="f30f9-134">String</span></span>|<span data-ttu-id="f30f9-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f30f9-135">Key of the entity.</span></span> <span data-ttu-id="f30f9-136">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f30f9-136">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f30f9-137">displayName</span><span class="sxs-lookup"><span data-stu-id="f30f9-137">displayName</span></span>|<span data-ttu-id="f30f9-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="f30f9-138">String</span></span>|<span data-ttu-id="f30f9-139">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="f30f9-139">The admin provided or imported title of the app.</span></span> <span data-ttu-id="f30f9-140">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f30f9-140">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f30f9-141">descripción</span><span class="sxs-lookup"><span data-stu-id="f30f9-141">description</span></span>|<span data-ttu-id="f30f9-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="f30f9-142">String</span></span>|<span data-ttu-id="f30f9-143">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f30f9-143">The description of the app.</span></span> <span data-ttu-id="f30f9-144">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f30f9-144">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f30f9-145">publicador</span><span class="sxs-lookup"><span data-stu-id="f30f9-145">publisher</span></span>|<span data-ttu-id="f30f9-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="f30f9-146">String</span></span>|<span data-ttu-id="f30f9-147">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f30f9-147">The publisher of the app.</span></span> <span data-ttu-id="f30f9-148">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f30f9-148">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f30f9-149">largeIcon</span><span class="sxs-lookup"><span data-stu-id="f30f9-149">largeIcon</span></span>|[<span data-ttu-id="f30f9-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="f30f9-150">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="f30f9-151">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="f30f9-151">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="f30f9-152">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f30f9-152">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f30f9-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="f30f9-153">createdDateTime</span></span>|<span data-ttu-id="f30f9-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f30f9-154">DateTimeOffset</span></span>|<span data-ttu-id="f30f9-155">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f30f9-155">The date and time the app was created.</span></span> <span data-ttu-id="f30f9-156">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f30f9-156">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f30f9-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="f30f9-157">lastModifiedDateTime</span></span>|<span data-ttu-id="f30f9-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f30f9-158">DateTimeOffset</span></span>|<span data-ttu-id="f30f9-159">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f30f9-159">The date and time the app was last modified.</span></span> <span data-ttu-id="f30f9-160">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f30f9-160">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f30f9-161">isFeatured</span><span class="sxs-lookup"><span data-stu-id="f30f9-161">isFeatured</span></span>|<span data-ttu-id="f30f9-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="f30f9-162">Boolean</span></span>|<span data-ttu-id="f30f9-163">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f30f9-163">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f30f9-164">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="f30f9-164">privacyInformationUrl</span></span>|<span data-ttu-id="f30f9-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="f30f9-165">String</span></span>|<span data-ttu-id="f30f9-166">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="f30f9-166">The privacy statement Url.</span></span> <span data-ttu-id="f30f9-167">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f30f9-167">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f30f9-168">informationUrl</span><span class="sxs-lookup"><span data-stu-id="f30f9-168">informationUrl</span></span>|<span data-ttu-id="f30f9-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="f30f9-169">String</span></span>|<span data-ttu-id="f30f9-170">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="f30f9-170">The more information Url.</span></span> <span data-ttu-id="f30f9-171">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f30f9-171">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f30f9-172">owner</span><span class="sxs-lookup"><span data-stu-id="f30f9-172">owner</span></span>|<span data-ttu-id="f30f9-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="f30f9-173">String</span></span>|<span data-ttu-id="f30f9-174">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f30f9-174">The owner of the app.</span></span> <span data-ttu-id="f30f9-175">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f30f9-175">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f30f9-176">developer</span><span class="sxs-lookup"><span data-stu-id="f30f9-176">developer</span></span>|<span data-ttu-id="f30f9-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="f30f9-177">String</span></span>|<span data-ttu-id="f30f9-178">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f30f9-178">The developer of the app.</span></span> <span data-ttu-id="f30f9-179">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f30f9-179">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f30f9-180">notas</span><span class="sxs-lookup"><span data-stu-id="f30f9-180">notes</span></span>|<span data-ttu-id="f30f9-181">Cadena</span><span class="sxs-lookup"><span data-stu-id="f30f9-181">String</span></span>|<span data-ttu-id="f30f9-182">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f30f9-182">Notes for the app.</span></span> <span data-ttu-id="f30f9-183">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f30f9-183">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f30f9-184">uploadState</span><span class="sxs-lookup"><span data-stu-id="f30f9-184">uploadState</span></span>|<span data-ttu-id="f30f9-185">Int32</span><span class="sxs-lookup"><span data-stu-id="f30f9-185">Int32</span></span>|<span data-ttu-id="f30f9-186">El estado de carga.</span><span class="sxs-lookup"><span data-stu-id="f30f9-186">The upload state.</span></span> <span data-ttu-id="f30f9-187">Heredado de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f30f9-187">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md)</span></span>|
|<span data-ttu-id="f30f9-188">publishingState</span><span class="sxs-lookup"><span data-stu-id="f30f9-188">publishingState</span></span>|[<span data-ttu-id="f30f9-189">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="f30f9-189">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="f30f9-190">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f30f9-190">The publishing state for the app.</span></span> <span data-ttu-id="f30f9-191">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="f30f9-191">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="f30f9-192">Se hereda de [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f30f9-192">Inherited from [mobileApp](../resources/intune-apps-mobileapp.md).</span></span> <span data-ttu-id="f30f9-193">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="f30f9-193">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="f30f9-194">appAvailability</span><span class="sxs-lookup"><span data-stu-id="f30f9-194">appAvailability</span></span>|[<span data-ttu-id="f30f9-195">managedAppAvailability</span><span class="sxs-lookup"><span data-stu-id="f30f9-195">managedAppAvailability</span></span>](../resources/intune-apps-managedappavailability.md)|<span data-ttu-id="f30f9-196">Disponibilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f30f9-196">The Application's availability.</span></span> <span data-ttu-id="f30f9-197">Se hereda de [managedApp](../resources/intune-apps-managedapp.md).</span><span class="sxs-lookup"><span data-stu-id="f30f9-197">Inherited from [managedApp](../resources/intune-apps-managedapp.md).</span></span> <span data-ttu-id="f30f9-198">Los valores posibles son: `global` y `lineOfBusiness`.</span><span class="sxs-lookup"><span data-stu-id="f30f9-198">Possible values are: `global`, `lineOfBusiness`.</span></span>|
|<span data-ttu-id="f30f9-199">versión</span><span class="sxs-lookup"><span data-stu-id="f30f9-199">version</span></span>|<span data-ttu-id="f30f9-200">Cadena</span><span class="sxs-lookup"><span data-stu-id="f30f9-200">String</span></span>|<span data-ttu-id="f30f9-201">Versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f30f9-201">The Application's version.</span></span> <span data-ttu-id="f30f9-202">Heredado de [managedApp](../resources/intune-apps-managedapp.md)</span><span class="sxs-lookup"><span data-stu-id="f30f9-202">Inherited from [managedApp](../resources/intune-apps-managedapp.md)</span></span>|
|<span data-ttu-id="f30f9-203">bundleId</span><span class="sxs-lookup"><span data-stu-id="f30f9-203">bundleId</span></span>|<span data-ttu-id="f30f9-204">Cadena</span><span class="sxs-lookup"><span data-stu-id="f30f9-204">String</span></span>|<span data-ttu-id="f30f9-205">El identificador de lote de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f30f9-205">The app's Bundle ID.</span></span>|
|<span data-ttu-id="f30f9-206">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="f30f9-206">appStoreUrl</span></span>|<span data-ttu-id="f30f9-207">Cadena</span><span class="sxs-lookup"><span data-stu-id="f30f9-207">String</span></span>|<span data-ttu-id="f30f9-208">La AppStoreUrl de Apple.</span><span class="sxs-lookup"><span data-stu-id="f30f9-208">The Apple AppStoreUrl.</span></span>|
|<span data-ttu-id="f30f9-209">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="f30f9-209">applicableDeviceType</span></span>|[<span data-ttu-id="f30f9-210">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="f30f9-210">iosDeviceType</span></span>](../resources/intune-apps-iosdevicetype.md)|<span data-ttu-id="f30f9-211">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="f30f9-211">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="f30f9-212">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="f30f9-212">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="f30f9-213">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="f30f9-213">iosMinimumOperatingSystem</span></span>](../resources/intune-apps-iosminimumoperatingsystem.md)|<span data-ttu-id="f30f9-214">El valor para el sistema operativo mínimo compatible.</span><span class="sxs-lookup"><span data-stu-id="f30f9-214">The value for the minimum supported operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="f30f9-215">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f30f9-215">Response</span></span>
<span data-ttu-id="f30f9-216">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f30f9-216">If successful, this method returns a `201 Created` response code and a [managedIOSStoreApp](../resources/intune-apps-managediosstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f30f9-217">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f30f9-217">Example</span></span>
### <a name="request"></a><span data-ttu-id="f30f9-218">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f30f9-218">Request</span></span>
<span data-ttu-id="f30f9-219">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f30f9-219">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 1170

{
  "@odata.type": "#microsoft.graph.managedIOSStoreApp",
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
  "appAvailability": "lineOfBusiness",
  "version": "Version value",
  "bundleId": "Bundle Id value",
  "appStoreUrl": "https://example.com/appStoreUrl/",
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
  }
}
```

### <a name="response"></a><span data-ttu-id="f30f9-220">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f30f9-220">Response</span></span>
<span data-ttu-id="f30f9-p119">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f30f9-p119">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1278

{
  "@odata.type": "#microsoft.graph.managedIOSStoreApp",
  "id": "51b9830f-830f-51b9-0f83-b9510f83b951",
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
  "appAvailability": "lineOfBusiness",
  "version": "Version value",
  "bundleId": "Bundle Id value",
  "appStoreUrl": "https://example.com/appStoreUrl/",
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
  }
}
```





