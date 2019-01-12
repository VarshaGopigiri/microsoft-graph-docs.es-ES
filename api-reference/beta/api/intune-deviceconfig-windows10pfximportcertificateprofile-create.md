---
title: Crear windows10PFXImportCertificateProfile
description: Crear un nuevo objeto windows10PFXImportCertificateProfile.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a7d30e521df0b5e9d48471d153d2d5bde1d6fad9
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27973373"
---
# <a name="create-windows10pfximportcertificateprofile"></a><span data-ttu-id="a4a97-103">Crear windows10PFXImportCertificateProfile</span><span class="sxs-lookup"><span data-stu-id="a4a97-103">Create windows10PFXImportCertificateProfile</span></span>

> <span data-ttu-id="a4a97-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a4a97-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a4a97-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a4a97-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a4a97-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a4a97-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a4a97-107">Crear un nuevo objeto [windows10PFXImportCertificateProfile](../resources/intune-deviceconfig-windows10pfximportcertificateprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="a4a97-107">Create a new [windows10PFXImportCertificateProfile](../resources/intune-deviceconfig-windows10pfximportcertificateprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a4a97-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a4a97-108">Prerequisites</span></span>
<span data-ttu-id="a4a97-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a4a97-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a4a97-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a4a97-111">Permission type</span></span>|<span data-ttu-id="a4a97-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a4a97-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a4a97-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a4a97-113">Delegated (work or school account)</span></span>|<span data-ttu-id="a4a97-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a4a97-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="a4a97-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a4a97-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a4a97-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a4a97-116">Not supported.</span></span>|
|<span data-ttu-id="a4a97-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a4a97-117">Application</span></span>|<span data-ttu-id="a4a97-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a4a97-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a4a97-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a4a97-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="a4a97-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a4a97-120">Request headers</span></span>
|<span data-ttu-id="a4a97-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a4a97-121">Header</span></span>|<span data-ttu-id="a4a97-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a4a97-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a4a97-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="a4a97-123">Authorization</span></span>|<span data-ttu-id="a4a97-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a4a97-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a4a97-125">Accept</span><span class="sxs-lookup"><span data-stu-id="a4a97-125">Accept</span></span>|<span data-ttu-id="a4a97-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a4a97-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a4a97-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a4a97-127">Request body</span></span>
<span data-ttu-id="a4a97-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto windows10PFXImportCertificateProfile.</span><span class="sxs-lookup"><span data-stu-id="a4a97-128">In the request body, supply a JSON representation for the windows10PFXImportCertificateProfile object.</span></span>

<span data-ttu-id="a4a97-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el windows10PFXImportCertificateProfile.</span><span class="sxs-lookup"><span data-stu-id="a4a97-129">The following table shows the properties that are required when you create the windows10PFXImportCertificateProfile.</span></span>

|<span data-ttu-id="a4a97-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a4a97-130">Property</span></span>|<span data-ttu-id="a4a97-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="a4a97-131">Type</span></span>|<span data-ttu-id="a4a97-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4a97-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a4a97-133">id</span><span class="sxs-lookup"><span data-stu-id="a4a97-133">id</span></span>|<span data-ttu-id="a4a97-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="a4a97-134">String</span></span>|<span data-ttu-id="a4a97-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a4a97-135">Key of the entity.</span></span> <span data-ttu-id="a4a97-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a4a97-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a4a97-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="a4a97-137">lastModifiedDateTime</span></span>|<span data-ttu-id="a4a97-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a4a97-138">DateTimeOffset</span></span>|<span data-ttu-id="a4a97-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="a4a97-139">DateTime the object was last modified.</span></span> <span data-ttu-id="a4a97-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a4a97-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a4a97-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="a4a97-141">roleScopeTagIds</span></span>|<span data-ttu-id="a4a97-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="a4a97-142">String collection</span></span>|<span data-ttu-id="a4a97-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="a4a97-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="a4a97-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a4a97-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a4a97-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="a4a97-145">supportsScopeTags</span></span>|<span data-ttu-id="a4a97-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="a4a97-146">Boolean</span></span>|<span data-ttu-id="a4a97-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="a4a97-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="a4a97-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="a4a97-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="a4a97-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="a4a97-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="a4a97-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="a4a97-150">This property is read-only.</span></span> <span data-ttu-id="a4a97-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a4a97-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a4a97-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="a4a97-152">createdDateTime</span></span>|<span data-ttu-id="a4a97-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a4a97-153">DateTimeOffset</span></span>|<span data-ttu-id="a4a97-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="a4a97-154">DateTime the object was created.</span></span> <span data-ttu-id="a4a97-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a4a97-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a4a97-156">descripción</span><span class="sxs-lookup"><span data-stu-id="a4a97-156">description</span></span>|<span data-ttu-id="a4a97-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="a4a97-157">String</span></span>|<span data-ttu-id="a4a97-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4a97-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="a4a97-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a4a97-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a4a97-160">displayName</span><span class="sxs-lookup"><span data-stu-id="a4a97-160">displayName</span></span>|<span data-ttu-id="a4a97-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="a4a97-161">String</span></span>|<span data-ttu-id="a4a97-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4a97-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="a4a97-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a4a97-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a4a97-164">version</span><span class="sxs-lookup"><span data-stu-id="a4a97-164">version</span></span>|<span data-ttu-id="a4a97-165">Int32</span><span class="sxs-lookup"><span data-stu-id="a4a97-165">Int32</span></span>|<span data-ttu-id="a4a97-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4a97-166">Version of the device configuration.</span></span> <span data-ttu-id="a4a97-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a4a97-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="a4a97-168">keyStorageProvider</span><span class="sxs-lookup"><span data-stu-id="a4a97-168">keyStorageProvider</span></span>|[<span data-ttu-id="a4a97-169">keyStorageProviderOption</span><span class="sxs-lookup"><span data-stu-id="a4a97-169">keyStorageProviderOption</span></span>](../resources/intune-deviceconfig-keystorageprovideroption.md)|<span data-ttu-id="a4a97-170">Todavía no está documentada.</span><span class="sxs-lookup"><span data-stu-id="a4a97-170">Not yet documented.</span></span> <span data-ttu-id="a4a97-171">Los valores posibles son: `useTpmKspOtherwiseUseSoftwareKsp`, `useTpmKspOtherwiseFail`, `usePassportForWorkKspOtherwiseFail` y `useSoftwareKsp`.</span><span class="sxs-lookup"><span data-stu-id="a4a97-171">Possible values are: `useTpmKspOtherwiseUseSoftwareKsp`, `useTpmKspOtherwiseFail`, `usePassportForWorkKspOtherwiseFail`, `useSoftwareKsp`.</span></span>|



## <a name="response"></a><span data-ttu-id="a4a97-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a4a97-172">Response</span></span>
<span data-ttu-id="a4a97-173">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [windows10PFXImportCertificateProfile](../resources/intune-deviceconfig-windows10pfximportcertificateprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a4a97-173">If successful, this method returns a `201 Created` response code and a [windows10PFXImportCertificateProfile](../resources/intune-deviceconfig-windows10pfximportcertificateprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a4a97-174">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a4a97-174">Example</span></span>
### <a name="request"></a><span data-ttu-id="a4a97-175">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a4a97-175">Request</span></span>
<span data-ttu-id="a4a97-176">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a4a97-176">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 381

{
  "@odata.type": "#microsoft.graph.windows10PFXImportCertificateProfile",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "keyStorageProvider": "useTpmKspOtherwiseFail"
}
```

### <a name="response"></a><span data-ttu-id="a4a97-177">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a4a97-177">Response</span></span>
<span data-ttu-id="a4a97-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a4a97-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 489

{
  "@odata.type": "#microsoft.graph.windows10PFXImportCertificateProfile",
  "id": "4244277a-277a-4244-7a27-44427a274442",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "keyStorageProvider": "useTpmKspOtherwiseFail"
}
```





