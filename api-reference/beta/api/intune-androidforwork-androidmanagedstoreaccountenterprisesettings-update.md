---
title: Actualizar androidManagedStoreAccountEnterpriseSettings
description: Actualizar las propiedades de un objeto androidManagedStoreAccountEnterpriseSettings.
author: tfitzmac
ms.openlocfilehash: ee5fda9e9c6ce92cdf44ec878c2c5835ceed2c49
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27356031"
---
# <a name="update-androidmanagedstoreaccountenterprisesettings"></a><span data-ttu-id="bff36-103">Actualizar androidManagedStoreAccountEnterpriseSettings</span><span class="sxs-lookup"><span data-stu-id="bff36-103">Update androidManagedStoreAccountEnterpriseSettings</span></span>

> <span data-ttu-id="bff36-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bff36-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bff36-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bff36-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="bff36-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bff36-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bff36-107">Actualizar las propiedades de un objeto [androidManagedStoreAccountEnterpriseSettings](../resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings.md) .</span><span class="sxs-lookup"><span data-stu-id="bff36-107">Update the properties of a [androidManagedStoreAccountEnterpriseSettings](../resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bff36-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bff36-108">Prerequisites</span></span>
<span data-ttu-id="bff36-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bff36-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bff36-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bff36-111">Permission type</span></span>|<span data-ttu-id="bff36-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bff36-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bff36-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bff36-113">Delegated (work or school account)</span></span>|<span data-ttu-id="bff36-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bff36-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="bff36-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bff36-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bff36-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bff36-116">Not supported.</span></span>|
|<span data-ttu-id="bff36-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bff36-117">Application</span></span>|<span data-ttu-id="bff36-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bff36-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bff36-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bff36-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/androidManagedStoreAccountEnterpriseSettings
```

## <a name="request-headers"></a><span data-ttu-id="bff36-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bff36-120">Request headers</span></span>
|<span data-ttu-id="bff36-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bff36-121">Header</span></span>|<span data-ttu-id="bff36-122">Valor</span><span class="sxs-lookup"><span data-stu-id="bff36-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bff36-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="bff36-123">Authorization</span></span>|<span data-ttu-id="bff36-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bff36-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bff36-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="bff36-125">Accept</span></span>|<span data-ttu-id="bff36-126">application/json</span><span class="sxs-lookup"><span data-stu-id="bff36-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bff36-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bff36-127">Request body</span></span>
<span data-ttu-id="bff36-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [androidManagedStoreAccountEnterpriseSettings](../resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings.md) .</span><span class="sxs-lookup"><span data-stu-id="bff36-128">In the request body, supply a JSON representation for the [androidManagedStoreAccountEnterpriseSettings](../resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings.md) object.</span></span>

<span data-ttu-id="bff36-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [androidManagedStoreAccountEnterpriseSettings](../resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings.md).</span><span class="sxs-lookup"><span data-stu-id="bff36-129">The following table shows the properties that are required when you create the [androidManagedStoreAccountEnterpriseSettings](../resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings.md).</span></span>

|<span data-ttu-id="bff36-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bff36-130">Property</span></span>|<span data-ttu-id="bff36-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="bff36-131">Type</span></span>|<span data-ttu-id="bff36-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="bff36-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bff36-133">id</span><span class="sxs-lookup"><span data-stu-id="bff36-133">id</span></span>|<span data-ttu-id="bff36-134">String</span><span class="sxs-lookup"><span data-stu-id="bff36-134">String</span></span>|<span data-ttu-id="bff36-135">El Android almacenar el identificador de configuración de cuenta de empresa</span><span class="sxs-lookup"><span data-stu-id="bff36-135">The Android store account enterprise settings identifier</span></span>|
|<span data-ttu-id="bff36-136">bindStatus</span><span class="sxs-lookup"><span data-stu-id="bff36-136">bindStatus</span></span>|[<span data-ttu-id="bff36-137">androidManagedStoreAccountBindStatus</span><span class="sxs-lookup"><span data-stu-id="bff36-137">androidManagedStoreAccountBindStatus</span></span>](../resources/intune-androidforwork-androidmanagedstoreaccountbindstatus.md)|<span data-ttu-id="bff36-138">Enlazar el estado del inquilino con la API de Google EMM.</span><span class="sxs-lookup"><span data-stu-id="bff36-138">Bind status of the tenant with the Google EMM API.</span></span> <span data-ttu-id="bff36-139">Los valores posibles son: `notBound`, `bound`, `boundAndValidated` y `unbinding`.</span><span class="sxs-lookup"><span data-stu-id="bff36-139">Possible values are: `notBound`, `bound`, `boundAndValidated`, `unbinding`.</span></span>|
|<span data-ttu-id="bff36-140">lastAppSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="bff36-140">lastAppSyncDateTime</span></span>|<span data-ttu-id="bff36-141">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bff36-141">DateTimeOffset</span></span>|<span data-ttu-id="bff36-142">Última hora de finalización para la sincronización de la aplicación</span><span class="sxs-lookup"><span data-stu-id="bff36-142">Last completion time for app sync</span></span>|
|<span data-ttu-id="bff36-143">lastAppSyncStatus</span><span class="sxs-lookup"><span data-stu-id="bff36-143">lastAppSyncStatus</span></span>|[<span data-ttu-id="bff36-144">androidManagedStoreAccountAppSyncStatus</span><span class="sxs-lookup"><span data-stu-id="bff36-144">androidManagedStoreAccountAppSyncStatus</span></span>](../resources/intune-androidforwork-androidmanagedstoreaccountappsyncstatus.md)|<span data-ttu-id="bff36-145">Resultado de la última sincronización de aplicación.</span><span class="sxs-lookup"><span data-stu-id="bff36-145">Last application sync result.</span></span> <span data-ttu-id="bff36-146">Los valores posibles son: `success`, `credentialsNotValid`, `androidForWorkApiError`, `managementServiceError`, `unknownError`, `none`.</span><span class="sxs-lookup"><span data-stu-id="bff36-146">Possible values are: `success`, `credentialsNotValid`, `androidForWorkApiError`, `managementServiceError`, `unknownError`, `none`.</span></span>|
|<span data-ttu-id="bff36-147">ownerUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="bff36-147">ownerUserPrincipalName</span></span>|<span data-ttu-id="bff36-148">String</span><span class="sxs-lookup"><span data-stu-id="bff36-148">String</span></span>|<span data-ttu-id="bff36-149">UPN del propietario que creó la empresa</span><span class="sxs-lookup"><span data-stu-id="bff36-149">Owner UPN that created the enterprise</span></span>|
|<span data-ttu-id="bff36-150">ownerOrganizationName</span><span class="sxs-lookup"><span data-stu-id="bff36-150">ownerOrganizationName</span></span>|<span data-ttu-id="bff36-151">String</span><span class="sxs-lookup"><span data-stu-id="bff36-151">String</span></span>|<span data-ttu-id="bff36-152">Nombre de la organización utiliza cuando incorporación Enterprise Android</span><span class="sxs-lookup"><span data-stu-id="bff36-152">Organization name used when onboarding Android Enterprise</span></span>|
|<span data-ttu-id="bff36-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="bff36-153">lastModifiedDateTime</span></span>|<span data-ttu-id="bff36-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bff36-154">DateTimeOffset</span></span>|<span data-ttu-id="bff36-155">Hora de última modificación de la configuración de la empresa para Android</span><span class="sxs-lookup"><span data-stu-id="bff36-155">Last modification time for Android enterprise settings</span></span>|
|<span data-ttu-id="bff36-156">enrollmentTarget</span><span class="sxs-lookup"><span data-stu-id="bff36-156">enrollmentTarget</span></span>|[<span data-ttu-id="bff36-157">androidManagedStoreAccountEnrollmentTarget</span><span class="sxs-lookup"><span data-stu-id="bff36-157">androidManagedStoreAccountEnrollmentTarget</span></span>](../resources/intune-androidforwork-androidmanagedstoreaccountenrollmenttarget.md)|<span data-ttu-id="bff36-158">Indica qué usuarios pueden inscribirse dispositivos en administración de dispositivos Android empresariales.</span><span class="sxs-lookup"><span data-stu-id="bff36-158">Indicates which users can enroll devices in Android Enterprise device management.</span></span> <span data-ttu-id="bff36-159">Los valores posibles son: `none`, `all`, `targeted` y `targetedAsEnrollmentRestrictions`.</span><span class="sxs-lookup"><span data-stu-id="bff36-159">Possible values are: `none`, `all`, `targeted`, `targetedAsEnrollmentRestrictions`.</span></span>|
|<span data-ttu-id="bff36-160">targetGroupIds</span><span class="sxs-lookup"><span data-stu-id="bff36-160">targetGroupIds</span></span>|<span data-ttu-id="bff36-161">Colección String</span><span class="sxs-lookup"><span data-stu-id="bff36-161">String collection</span></span>|<span data-ttu-id="bff36-162">Especifica los grupos de AAD que pueden inscribir dispositivos en la administración de dispositivos de Android for Work si se establece enrollmentTarget en "Dirigido"</span><span class="sxs-lookup"><span data-stu-id="bff36-162">Specifies which AAD groups can enroll devices in Android for Work device management if enrollmentTarget is set to 'Targeted'</span></span>|
|<span data-ttu-id="bff36-163">deviceOwnerManagementEnabled</span><span class="sxs-lookup"><span data-stu-id="bff36-163">deviceOwnerManagementEnabled</span></span>|<span data-ttu-id="bff36-164">Boolean</span><span class="sxs-lookup"><span data-stu-id="bff36-164">Boolean</span></span>|<span data-ttu-id="bff36-165">Indica si esta cuenta es flighting para la administración de propietario dispositivos Android con CloudDPC.</span><span class="sxs-lookup"><span data-stu-id="bff36-165">Indicates if this account is flighting for Android Device Owner Management with CloudDPC.</span></span>|



## <a name="response"></a><span data-ttu-id="bff36-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bff36-166">Response</span></span>
<span data-ttu-id="bff36-167">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [androidManagedStoreAccountEnterpriseSettings](../resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bff36-167">If successful, this method returns a `200 OK` response code and an updated [androidManagedStoreAccountEnterpriseSettings](../resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bff36-168">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bff36-168">Example</span></span>
### <a name="request"></a><span data-ttu-id="bff36-169">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bff36-169">Request</span></span>
<span data-ttu-id="bff36-170">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bff36-170">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/androidManagedStoreAccountEnterpriseSettings
Content-type: application/json
Content-length: 458

{
  "bindStatus": "bound",
  "lastAppSyncDateTime": "2016-12-31T23:57:22.8606813-08:00",
  "lastAppSyncStatus": "credentialsNotValid",
  "ownerUserPrincipalName": "Owner User Principal Name value",
  "ownerOrganizationName": "Owner Organization Name value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "enrollmentTarget": "all",
  "targetGroupIds": [
    "Target Group Ids value"
  ],
  "deviceOwnerManagementEnabled": true
}
```

### <a name="response"></a><span data-ttu-id="bff36-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bff36-171">Response</span></span>
<span data-ttu-id="bff36-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bff36-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 590

{
  "@odata.type": "#microsoft.graph.androidManagedStoreAccountEnterpriseSettings",
  "id": "b71357c9-57c9-b713-c957-13b7c95713b7",
  "bindStatus": "bound",
  "lastAppSyncDateTime": "2016-12-31T23:57:22.8606813-08:00",
  "lastAppSyncStatus": "credentialsNotValid",
  "ownerUserPrincipalName": "Owner User Principal Name value",
  "ownerOrganizationName": "Owner Organization Name value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "enrollmentTarget": "all",
  "targetGroupIds": [
    "Target Group Ids value"
  ],
  "deviceOwnerManagementEnabled": true
}
```





