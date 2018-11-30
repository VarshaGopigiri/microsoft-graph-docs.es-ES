---
title: Crear iosLobAppProvisioningConfiguration
description: Crear un nuevo objeto iosLobAppProvisioningConfiguration.
ms.openlocfilehash: 0c51201e147ff588c210df2a988568807f7d9dcb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085558"
---
# <a name="create-ioslobappprovisioningconfiguration"></a><span data-ttu-id="fd7e4-103">Crear iosLobAppProvisioningConfiguration</span><span class="sxs-lookup"><span data-stu-id="fd7e4-103">Create iosLobAppProvisioningConfiguration</span></span>

> <span data-ttu-id="fd7e4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fd7e4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fd7e4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fd7e4-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="fd7e4-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fd7e4-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fd7e4-107">Crear un nuevo objeto [iosLobAppProvisioningConfiguration](../resources/intune-apps-ioslobappprovisioningconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="fd7e4-107">Create a new [iosLobAppProvisioningConfiguration](../resources/intune-apps-ioslobappprovisioningconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="fd7e4-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fd7e4-108">Prerequisites</span></span>
<span data-ttu-id="fd7e4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fd7e4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fd7e4-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fd7e4-111">Permission type</span></span>|<span data-ttu-id="fd7e4-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fd7e4-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="fd7e4-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fd7e4-113">Delegated (work or school account)</span></span>|<span data-ttu-id="fd7e4-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fd7e4-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="fd7e4-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fd7e4-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="fd7e4-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fd7e4-116">Not supported.</span></span>|
|<span data-ttu-id="fd7e4-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fd7e4-117">Application</span></span>|<span data-ttu-id="fd7e4-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fd7e4-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="fd7e4-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fd7e4-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/iosLobAppProvisioningConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="fd7e4-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fd7e4-120">Request headers</span></span>
|<span data-ttu-id="fd7e4-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd7e4-121">Header</span></span>|<span data-ttu-id="fd7e4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="fd7e4-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="fd7e4-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="fd7e4-123">Authorization</span></span>|<span data-ttu-id="fd7e4-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="fd7e4-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="fd7e4-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="fd7e4-125">Accept</span></span>|<span data-ttu-id="fd7e4-126">application/json</span><span class="sxs-lookup"><span data-stu-id="fd7e4-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="fd7e4-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fd7e4-127">Request body</span></span>
<span data-ttu-id="fd7e4-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto iosLobAppProvisioningConfiguration.</span><span class="sxs-lookup"><span data-stu-id="fd7e4-128">In the request body, supply a JSON representation for the iosLobAppProvisioningConfiguration object.</span></span>

<span data-ttu-id="fd7e4-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el iosLobAppProvisioningConfiguration.</span><span class="sxs-lookup"><span data-stu-id="fd7e4-129">The following table shows the properties that are required when you create the iosLobAppProvisioningConfiguration.</span></span>

|<span data-ttu-id="fd7e4-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fd7e4-130">Property</span></span>|<span data-ttu-id="fd7e4-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="fd7e4-131">Type</span></span>|<span data-ttu-id="fd7e4-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd7e4-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fd7e4-133">id</span><span class="sxs-lookup"><span data-stu-id="fd7e4-133">id</span></span>|<span data-ttu-id="fd7e4-134">String</span><span class="sxs-lookup"><span data-stu-id="fd7e4-134">String</span></span>|<span data-ttu-id="fd7e4-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="fd7e4-135">Key of the entity.</span></span>|
|<span data-ttu-id="fd7e4-136">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="fd7e4-136">expirationDateTime</span></span>|<span data-ttu-id="fd7e4-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="fd7e4-137">DateTimeOffset</span></span>|<span data-ttu-id="fd7e4-138">Fecha de caducidad opcional de perfiles y la hora.</span><span class="sxs-lookup"><span data-stu-id="fd7e4-138">Optional profile expiration date and time.</span></span>|
|<span data-ttu-id="fd7e4-139">payloadFileName</span><span class="sxs-lookup"><span data-stu-id="fd7e4-139">payloadFileName</span></span>|<span data-ttu-id="fd7e4-140">String</span><span class="sxs-lookup"><span data-stu-id="fd7e4-140">String</span></span>|<span data-ttu-id="fd7e4-141">Nombre de archivo de carga (\*.mobileprovision</span><span class="sxs-lookup"><span data-stu-id="fd7e4-141">Payload file name (\*.mobileprovision</span></span> | <span data-ttu-id="fd7e4-142">\*.xml).</span><span class="sxs-lookup"><span data-stu-id="fd7e4-142">\*.xml).</span></span>|
|<span data-ttu-id="fd7e4-143">carga útil</span><span class="sxs-lookup"><span data-stu-id="fd7e4-143">payload</span></span>|<span data-ttu-id="fd7e4-144">Binario</span><span class="sxs-lookup"><span data-stu-id="fd7e4-144">Binary</span></span>|<span data-ttu-id="fd7e4-145">Carga útil.</span><span class="sxs-lookup"><span data-stu-id="fd7e4-145">Payload.</span></span> <span data-ttu-id="fd7e4-146">(Matriz de bytes codificada UTF8)</span><span class="sxs-lookup"><span data-stu-id="fd7e4-146">(UTF8 encoded byte array)</span></span>|
|<span data-ttu-id="fd7e4-147">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="fd7e4-147">createdDateTime</span></span>|<span data-ttu-id="fd7e4-148">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="fd7e4-148">DateTimeOffset</span></span>|<span data-ttu-id="fd7e4-149">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="fd7e4-149">DateTime the object was created.</span></span>|
|<span data-ttu-id="fd7e4-150">descripción</span><span class="sxs-lookup"><span data-stu-id="fd7e4-150">description</span></span>|<span data-ttu-id="fd7e4-151">String</span><span class="sxs-lookup"><span data-stu-id="fd7e4-151">String</span></span>|<span data-ttu-id="fd7e4-152">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fd7e4-152">Admin provided description of the Device Configuration.</span></span>|
|<span data-ttu-id="fd7e4-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="fd7e4-153">lastModifiedDateTime</span></span>|<span data-ttu-id="fd7e4-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="fd7e4-154">DateTimeOffset</span></span>|<span data-ttu-id="fd7e4-155">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="fd7e4-155">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="fd7e4-156">displayName</span><span class="sxs-lookup"><span data-stu-id="fd7e4-156">displayName</span></span>|<span data-ttu-id="fd7e4-157">String</span><span class="sxs-lookup"><span data-stu-id="fd7e4-157">String</span></span>|<span data-ttu-id="fd7e4-158">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fd7e4-158">Admin provided name of the device configuration.</span></span>|
|<span data-ttu-id="fd7e4-159">versión</span><span class="sxs-lookup"><span data-stu-id="fd7e4-159">version</span></span>|<span data-ttu-id="fd7e4-160">Int32</span><span class="sxs-lookup"><span data-stu-id="fd7e4-160">Int32</span></span>|<span data-ttu-id="fd7e4-161">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fd7e4-161">Version of the device configuration.</span></span>|



## <a name="response"></a><span data-ttu-id="fd7e4-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fd7e4-162">Response</span></span>
<span data-ttu-id="fd7e4-163">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [iosLobAppProvisioningConfiguration](../resources/intune-apps-ioslobappprovisioningconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fd7e4-163">If successful, this method returns a `201 Created` response code and a [iosLobAppProvisioningConfiguration](../resources/intune-apps-ioslobappprovisioningconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fd7e4-164">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fd7e4-164">Example</span></span>
### <a name="request"></a><span data-ttu-id="fd7e4-165">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fd7e4-165">Request</span></span>
<span data-ttu-id="fd7e4-166">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fd7e4-166">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/iosLobAppProvisioningConfigurations
Content-type: application/json
Content-length: 377

{
  "@odata.type": "#microsoft.graph.iosLobAppProvisioningConfiguration",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "payloadFileName": "Payload File Name value",
  "payload": "cGF5bG9hZA==",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7
}
```

### <a name="response"></a><span data-ttu-id="fd7e4-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fd7e4-167">Response</span></span>
<span data-ttu-id="fd7e4-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fd7e4-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 485

{
  "@odata.type": "#microsoft.graph.iosLobAppProvisioningConfiguration",
  "id": "e2a23631-3631-e2a2-3136-a2e23136a2e2",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "payloadFileName": "Payload File Name value",
  "payload": "cGF5bG9hZA==",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7
}
```





