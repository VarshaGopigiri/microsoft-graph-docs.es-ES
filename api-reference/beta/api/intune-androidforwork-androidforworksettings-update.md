---
title: Actualizar androidForWorkSettings
description: Actualice las propiedades de un objeto androidForWorkSettings.
author: tfitzmac
ms.openlocfilehash: 5514de226d138291743c5b017a50682e91e1e9ce
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27352545"
---
# <a name="update-androidforworksettings"></a><span data-ttu-id="16315-103">Actualizar androidForWorkSettings</span><span class="sxs-lookup"><span data-stu-id="16315-103">Update androidForWorkSettings</span></span>

> <span data-ttu-id="16315-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="16315-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="16315-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="16315-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="16315-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="16315-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="16315-107">Actualice las propiedades de un objeto [androidForWorkSettings](../resources/intune-androidforwork-androidforworksettings.md).</span><span class="sxs-lookup"><span data-stu-id="16315-107">Update the properties of a [androidForWorkSettings](../resources/intune-androidforwork-androidforworksettings.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="16315-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="16315-108">Prerequisites</span></span>
<span data-ttu-id="16315-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="16315-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="16315-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="16315-111">Permission type</span></span>|<span data-ttu-id="16315-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="16315-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="16315-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="16315-113">Delegated (work or school account)</span></span>|<span data-ttu-id="16315-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="16315-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="16315-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="16315-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="16315-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="16315-116">Not supported.</span></span>|
|<span data-ttu-id="16315-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="16315-117">Application</span></span>|<span data-ttu-id="16315-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="16315-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="16315-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="16315-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/androidForWorkSettings
```

## <a name="request-headers"></a><span data-ttu-id="16315-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="16315-120">Request headers</span></span>
|<span data-ttu-id="16315-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="16315-121">Header</span></span>|<span data-ttu-id="16315-122">Valor</span><span class="sxs-lookup"><span data-stu-id="16315-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="16315-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="16315-123">Authorization</span></span>|<span data-ttu-id="16315-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="16315-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="16315-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="16315-125">Accept</span></span>|<span data-ttu-id="16315-126">application/json</span><span class="sxs-lookup"><span data-stu-id="16315-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="16315-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="16315-127">Request body</span></span>
<span data-ttu-id="16315-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [androidForWorkSettings](../resources/intune-androidforwork-androidforworksettings.md).</span><span class="sxs-lookup"><span data-stu-id="16315-128">In the request body, supply a JSON representation for the [androidForWorkSettings](../resources/intune-androidforwork-androidforworksettings.md) object.</span></span>

<span data-ttu-id="16315-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [androidForWorkSettings](../resources/intune-androidforwork-androidforworksettings.md).</span><span class="sxs-lookup"><span data-stu-id="16315-129">The following table shows the properties that are required when you create the [androidForWorkSettings](../resources/intune-androidforwork-androidforworksettings.md).</span></span>

|<span data-ttu-id="16315-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="16315-130">Property</span></span>|<span data-ttu-id="16315-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="16315-131">Type</span></span>|<span data-ttu-id="16315-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="16315-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="16315-133">id</span><span class="sxs-lookup"><span data-stu-id="16315-133">id</span></span>|<span data-ttu-id="16315-134">String</span><span class="sxs-lookup"><span data-stu-id="16315-134">String</span></span>|<span data-ttu-id="16315-135">Identificador de la configuración de Android for Work</span><span class="sxs-lookup"><span data-stu-id="16315-135">The Android for Work settings identifier</span></span>|
|<span data-ttu-id="16315-136">bindStatus</span><span class="sxs-lookup"><span data-stu-id="16315-136">bindStatus</span></span>|[<span data-ttu-id="16315-137">androidForWorkBindStatus</span><span class="sxs-lookup"><span data-stu-id="16315-137">androidForWorkBindStatus</span></span>](../resources/intune-androidforwork-androidforworkbindstatus.md)|<span data-ttu-id="16315-138">Enlazar el estado del inquilino con la API de Google EMM.</span><span class="sxs-lookup"><span data-stu-id="16315-138">Bind status of the tenant with the Google EMM API.</span></span> <span data-ttu-id="16315-139">Los valores posibles son: `notBound`, `bound`, `boundAndValidated` y `unbinding`.</span><span class="sxs-lookup"><span data-stu-id="16315-139">Possible values are: `notBound`, `bound`, `boundAndValidated`, `unbinding`.</span></span>|
|<span data-ttu-id="16315-140">lastAppSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="16315-140">lastAppSyncDateTime</span></span>|<span data-ttu-id="16315-141">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="16315-141">DateTimeOffset</span></span>|<span data-ttu-id="16315-142">Última hora de finalización para la sincronización de la aplicación</span><span class="sxs-lookup"><span data-stu-id="16315-142">Last completion time for app sync</span></span>|
|<span data-ttu-id="16315-143">lastAppSyncStatus</span><span class="sxs-lookup"><span data-stu-id="16315-143">lastAppSyncStatus</span></span>|[<span data-ttu-id="16315-144">androidForWorkSyncStatus</span><span class="sxs-lookup"><span data-stu-id="16315-144">androidForWorkSyncStatus</span></span>](../resources/intune-androidforwork-androidforworksyncstatus.md)|<span data-ttu-id="16315-145">Resultado de la última sincronización de aplicación.</span><span class="sxs-lookup"><span data-stu-id="16315-145">Last application sync result.</span></span> <span data-ttu-id="16315-146">Los valores posibles son: `success`, `credentialsNotValid`, `androidForWorkApiError`, `managementServiceError`, `unknownError`, `none`.</span><span class="sxs-lookup"><span data-stu-id="16315-146">Possible values are: `success`, `credentialsNotValid`, `androidForWorkApiError`, `managementServiceError`, `unknownError`, `none`.</span></span>|
|<span data-ttu-id="16315-147">ownerUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="16315-147">ownerUserPrincipalName</span></span>|<span data-ttu-id="16315-148">String</span><span class="sxs-lookup"><span data-stu-id="16315-148">String</span></span>|<span data-ttu-id="16315-149">UPN del propietario que creó la empresa</span><span class="sxs-lookup"><span data-stu-id="16315-149">Owner UPN that created the enterprise</span></span>|
|<span data-ttu-id="16315-150">ownerOrganizationName</span><span class="sxs-lookup"><span data-stu-id="16315-150">ownerOrganizationName</span></span>|<span data-ttu-id="16315-151">String</span><span class="sxs-lookup"><span data-stu-id="16315-151">String</span></span>|<span data-ttu-id="16315-152">Nombre de organización usado al incorporar Android for Work</span><span class="sxs-lookup"><span data-stu-id="16315-152">Organization name used when onboarding Android for Work</span></span>|
|<span data-ttu-id="16315-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="16315-153">lastModifiedDateTime</span></span>|<span data-ttu-id="16315-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="16315-154">DateTimeOffset</span></span>|<span data-ttu-id="16315-155">Última hora de modificación para la configuración de Android for Work</span><span class="sxs-lookup"><span data-stu-id="16315-155">Last modification time for Android for Work settings</span></span>|
|<span data-ttu-id="16315-156">enrollmentTarget</span><span class="sxs-lookup"><span data-stu-id="16315-156">enrollmentTarget</span></span>|[<span data-ttu-id="16315-157">androidForWorkEnrollmentTarget</span><span class="sxs-lookup"><span data-stu-id="16315-157">androidForWorkEnrollmentTarget</span></span>](../resources/intune-androidforwork-androidforworkenrollmenttarget.md)|<span data-ttu-id="16315-158">Indica qué usuarios pueden inscribirse dispositivos para Android para administración de dispositivos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="16315-158">Indicates which users can enroll devices in Android for Work device management.</span></span> <span data-ttu-id="16315-159">Los valores posibles son: `none`, `all`, `targeted` y `targetedAsEnrollmentRestrictions`.</span><span class="sxs-lookup"><span data-stu-id="16315-159">Possible values are: `none`, `all`, `targeted`, `targetedAsEnrollmentRestrictions`.</span></span>|
|<span data-ttu-id="16315-160">targetGroupIds</span><span class="sxs-lookup"><span data-stu-id="16315-160">targetGroupIds</span></span>|<span data-ttu-id="16315-161">Colección String</span><span class="sxs-lookup"><span data-stu-id="16315-161">String collection</span></span>|<span data-ttu-id="16315-162">Especifica los grupos de AAD que pueden inscribir dispositivos en la administración de dispositivos de Android for Work si se establece enrollmentTarget en "Dirigido"</span><span class="sxs-lookup"><span data-stu-id="16315-162">Specifies which AAD groups can enroll devices in Android for Work device management if enrollmentTarget is set to 'Targeted'</span></span>|
|<span data-ttu-id="16315-163">deviceOwnerManagementEnabled</span><span class="sxs-lookup"><span data-stu-id="16315-163">deviceOwnerManagementEnabled</span></span>|<span data-ttu-id="16315-164">Boolean</span><span class="sxs-lookup"><span data-stu-id="16315-164">Boolean</span></span>|<span data-ttu-id="16315-165">Indica si esta cuenta es flighting para la administración de propietario dispositivos Android con CloudDPC.</span><span class="sxs-lookup"><span data-stu-id="16315-165">Indicates if this account is flighting for Android Device Owner Management with CloudDPC.</span></span>|



## <a name="response"></a><span data-ttu-id="16315-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="16315-166">Response</span></span>
<span data-ttu-id="16315-167">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [androidForWorkSettings](../resources/intune-androidforwork-androidforworksettings.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="16315-167">If successful, this method returns a `200 OK` response code and an updated [androidForWorkSettings](../resources/intune-androidforwork-androidforworksettings.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="16315-168">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="16315-168">Example</span></span>
### <a name="request"></a><span data-ttu-id="16315-169">Solicitud</span><span class="sxs-lookup"><span data-stu-id="16315-169">Request</span></span>
<span data-ttu-id="16315-170">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="16315-170">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/androidForWorkSettings
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

### <a name="response"></a><span data-ttu-id="16315-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="16315-171">Response</span></span>
<span data-ttu-id="16315-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="16315-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 568

{
  "@odata.type": "#microsoft.graph.androidForWorkSettings",
  "id": "97adc169-c169-97ad-69c1-ad9769c1ad97",
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





