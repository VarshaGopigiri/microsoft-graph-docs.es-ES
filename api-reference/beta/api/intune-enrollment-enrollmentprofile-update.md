---
title: Actualizar enrollmentProfile
description: Actualizar las propiedades de un objeto enrollmentProfile.
author: tfitzmac
ms.openlocfilehash: 1f268d07e3636682d77edb238c59e2acaa7ec7d2
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27308319"
---
# <a name="update-enrollmentprofile"></a><span data-ttu-id="f8513-103">Actualizar enrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="f8513-103">Update enrollmentProfile</span></span>

> <span data-ttu-id="f8513-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f8513-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f8513-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f8513-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f8513-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f8513-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f8513-107">Actualizar las propiedades de un objeto [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="f8513-107">Update the properties of a [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f8513-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f8513-108">Prerequisites</span></span>
<span data-ttu-id="f8513-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f8513-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f8513-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f8513-111">Permission type</span></span>|<span data-ttu-id="f8513-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f8513-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f8513-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f8513-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f8513-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f8513-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="f8513-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f8513-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f8513-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f8513-116">Not supported.</span></span>|
|<span data-ttu-id="f8513-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f8513-117">Application</span></span>|<span data-ttu-id="f8513-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f8513-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f8513-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f8513-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/enrollmentProfiles/{enrollmentProfileId}
```

## <a name="request-headers"></a><span data-ttu-id="f8513-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f8513-120">Request headers</span></span>
|<span data-ttu-id="f8513-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8513-121">Header</span></span>|<span data-ttu-id="f8513-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f8513-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f8513-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="f8513-123">Authorization</span></span>|<span data-ttu-id="f8513-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f8513-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f8513-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f8513-125">Accept</span></span>|<span data-ttu-id="f8513-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f8513-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f8513-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f8513-127">Request body</span></span>
<span data-ttu-id="f8513-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="f8513-128">In the request body, supply a JSON representation for the [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) object.</span></span>

<span data-ttu-id="f8513-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md).</span><span class="sxs-lookup"><span data-stu-id="f8513-129">The following table shows the properties that are required when you create the [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md).</span></span>

|<span data-ttu-id="f8513-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f8513-130">Property</span></span>|<span data-ttu-id="f8513-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="f8513-131">Type</span></span>|<span data-ttu-id="f8513-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8513-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f8513-133">id</span><span class="sxs-lookup"><span data-stu-id="f8513-133">id</span></span>|<span data-ttu-id="f8513-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="f8513-134">String</span></span>|<span data-ttu-id="f8513-135">El GUID para el objeto</span><span class="sxs-lookup"><span data-stu-id="f8513-135">The GUID for the object</span></span>|
|<span data-ttu-id="f8513-136">displayName</span><span class="sxs-lookup"><span data-stu-id="f8513-136">displayName</span></span>|<span data-ttu-id="f8513-137">String</span><span class="sxs-lookup"><span data-stu-id="f8513-137">String</span></span>|<span data-ttu-id="f8513-138">Nombre del perfil</span><span class="sxs-lookup"><span data-stu-id="f8513-138">Name of the profile</span></span>|
|<span data-ttu-id="f8513-139">descripción</span><span class="sxs-lookup"><span data-stu-id="f8513-139">description</span></span>|<span data-ttu-id="f8513-140">String</span><span class="sxs-lookup"><span data-stu-id="f8513-140">String</span></span>|<span data-ttu-id="f8513-141">Descripción del perfil</span><span class="sxs-lookup"><span data-stu-id="f8513-141">Description of the profile</span></span>|
|<span data-ttu-id="f8513-142">requiresUserAuthentication</span><span class="sxs-lookup"><span data-stu-id="f8513-142">requiresUserAuthentication</span></span>|<span data-ttu-id="f8513-143">Boolean</span><span class="sxs-lookup"><span data-stu-id="f8513-143">Boolean</span></span>|<span data-ttu-id="f8513-144">Indica si el perfil requiere autenticación de usuario</span><span class="sxs-lookup"><span data-stu-id="f8513-144">Indicates if the profile requires user authentication</span></span>|
|<span data-ttu-id="f8513-145">configurationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="f8513-145">configurationEndpointUrl</span></span>|<span data-ttu-id="f8513-146">String</span><span class="sxs-lookup"><span data-stu-id="f8513-146">String</span></span>|<span data-ttu-id="f8513-147">Dirección url de extremo de configuración que se usará para inscripción</span><span class="sxs-lookup"><span data-stu-id="f8513-147">Configuration endpoint url to use for Enrollment</span></span>|
|<span data-ttu-id="f8513-148">enableAuthenticationViaCompanyPortal</span><span class="sxs-lookup"><span data-stu-id="f8513-148">enableAuthenticationViaCompanyPortal</span></span>|<span data-ttu-id="f8513-149">Boolean</span><span class="sxs-lookup"><span data-stu-id="f8513-149">Boolean</span></span>|<span data-ttu-id="f8513-150">Indica para autenticarse con Apple Asistente para la instalación en lugar de Portal de empresa.</span><span class="sxs-lookup"><span data-stu-id="f8513-150">Indicates to authenticate with Apple Setup Assistant instead of Company Portal.</span></span>|



## <a name="response"></a><span data-ttu-id="f8513-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f8513-151">Response</span></span>
<span data-ttu-id="f8513-152">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f8513-152">If successful, this method returns a `200 OK` response code and an updated [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f8513-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f8513-153">Example</span></span>
### <a name="request"></a><span data-ttu-id="f8513-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f8513-154">Request</span></span>
<span data-ttu-id="f8513-155">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f8513-155">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/enrollmentProfiles/{enrollmentProfileId}
Content-type: application/json
Content-length: 250

{
  "displayName": "Display Name value",
  "description": "Description value",
  "requiresUserAuthentication": true,
  "configurationEndpointUrl": "https://example.com/configurationEndpointUrl/",
  "enableAuthenticationViaCompanyPortal": true
}
```

### <a name="response"></a><span data-ttu-id="f8513-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f8513-156">Response</span></span>
<span data-ttu-id="f8513-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f8513-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 355

{
  "@odata.type": "#microsoft.graph.enrollmentProfile",
  "id": "012d8d5e-8d5e-012d-5e8d-2d015e8d2d01",
  "displayName": "Display Name value",
  "description": "Description value",
  "requiresUserAuthentication": true,
  "configurationEndpointUrl": "https://example.com/configurationEndpointUrl/",
  "enableAuthenticationViaCompanyPortal": true
}
```





