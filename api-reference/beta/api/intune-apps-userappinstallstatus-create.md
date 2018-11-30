---
title: Crear userAppInstallStatus
description: Crear un nuevo objeto userAppInstallStatus.
ms.openlocfilehash: 4096bd5223869dba2e692c9d8dcc87e01b5a004e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089314"
---
# <a name="create-userappinstallstatus"></a><span data-ttu-id="42fe9-103">Crear userAppInstallStatus</span><span class="sxs-lookup"><span data-stu-id="42fe9-103">Create userAppInstallStatus</span></span>

> <span data-ttu-id="42fe9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="42fe9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="42fe9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="42fe9-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="42fe9-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="42fe9-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="42fe9-107">Crear un nuevo objeto [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="42fe9-107">Create a new [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="42fe9-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="42fe9-108">Prerequisites</span></span>
<span data-ttu-id="42fe9-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="42fe9-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="42fe9-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="42fe9-111">Permission type</span></span>|<span data-ttu-id="42fe9-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="42fe9-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="42fe9-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="42fe9-113">Delegated (work or school account)</span></span>|<span data-ttu-id="42fe9-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="42fe9-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="42fe9-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="42fe9-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="42fe9-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="42fe9-116">Not supported.</span></span>|
|<span data-ttu-id="42fe9-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="42fe9-117">Application</span></span>|<span data-ttu-id="42fe9-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="42fe9-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="42fe9-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="42fe9-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses
```

## <a name="request-headers"></a><span data-ttu-id="42fe9-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="42fe9-120">Request headers</span></span>
|<span data-ttu-id="42fe9-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42fe9-121">Header</span></span>|<span data-ttu-id="42fe9-122">Valor</span><span class="sxs-lookup"><span data-stu-id="42fe9-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="42fe9-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="42fe9-123">Authorization</span></span>|<span data-ttu-id="42fe9-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="42fe9-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="42fe9-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="42fe9-125">Accept</span></span>|<span data-ttu-id="42fe9-126">application/json</span><span class="sxs-lookup"><span data-stu-id="42fe9-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="42fe9-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="42fe9-127">Request body</span></span>
<span data-ttu-id="42fe9-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto userAppInstallStatus.</span><span class="sxs-lookup"><span data-stu-id="42fe9-128">In the request body, supply a JSON representation for the userAppInstallStatus object.</span></span>

<span data-ttu-id="42fe9-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el userAppInstallStatus.</span><span class="sxs-lookup"><span data-stu-id="42fe9-129">The following table shows the properties that are required when you create the userAppInstallStatus.</span></span>

|<span data-ttu-id="42fe9-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="42fe9-130">Property</span></span>|<span data-ttu-id="42fe9-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="42fe9-131">Type</span></span>|<span data-ttu-id="42fe9-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="42fe9-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="42fe9-133">id</span><span class="sxs-lookup"><span data-stu-id="42fe9-133">id</span></span>|<span data-ttu-id="42fe9-134">String</span><span class="sxs-lookup"><span data-stu-id="42fe9-134">String</span></span>|<span data-ttu-id="42fe9-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="42fe9-135">Key of the entity.</span></span>|
|<span data-ttu-id="42fe9-136">userName</span><span class="sxs-lookup"><span data-stu-id="42fe9-136">userName</span></span>|<span data-ttu-id="42fe9-137">String</span><span class="sxs-lookup"><span data-stu-id="42fe9-137">String</span></span>|<span data-ttu-id="42fe9-138">Nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="42fe9-138">User name.</span></span>|
|<span data-ttu-id="42fe9-139">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="42fe9-139">userPrincipalName</span></span>|<span data-ttu-id="42fe9-140">String</span><span class="sxs-lookup"><span data-stu-id="42fe9-140">String</span></span>|<span data-ttu-id="42fe9-141">Nombre Principal de usuario.</span><span class="sxs-lookup"><span data-stu-id="42fe9-141">User Principal Name.</span></span>|
|<span data-ttu-id="42fe9-142">installedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="42fe9-142">installedDeviceCount</span></span>|<span data-ttu-id="42fe9-143">Int32</span><span class="sxs-lookup"><span data-stu-id="42fe9-143">Int32</span></span>|<span data-ttu-id="42fe9-144">Número de dispositivos instalados.</span><span class="sxs-lookup"><span data-stu-id="42fe9-144">Installed Device Count.</span></span>|
|<span data-ttu-id="42fe9-145">failedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="42fe9-145">failedDeviceCount</span></span>|<span data-ttu-id="42fe9-146">Int32</span><span class="sxs-lookup"><span data-stu-id="42fe9-146">Int32</span></span>|<span data-ttu-id="42fe9-147">Número de dispositivos erróneos.</span><span class="sxs-lookup"><span data-stu-id="42fe9-147">Failed Device Count.</span></span>|
|<span data-ttu-id="42fe9-148">notInstalledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="42fe9-148">notInstalledDeviceCount</span></span>|<span data-ttu-id="42fe9-149">Int32</span><span class="sxs-lookup"><span data-stu-id="42fe9-149">Int32</span></span>|<span data-ttu-id="42fe9-150">Número de dispositivos no instalados.</span><span class="sxs-lookup"><span data-stu-id="42fe9-150">Not installed device count.</span></span>|



## <a name="response"></a><span data-ttu-id="42fe9-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="42fe9-151">Response</span></span>
<span data-ttu-id="42fe9-152">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="42fe9-152">If successful, this method returns a `201 Created` response code and a [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="42fe9-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="42fe9-153">Example</span></span>
### <a name="request"></a><span data-ttu-id="42fe9-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="42fe9-154">Request</span></span>
<span data-ttu-id="42fe9-155">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="42fe9-155">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/userStatuses
Content-type: application/json
Content-length: 239

{
  "@odata.type": "#microsoft.graph.userAppInstallStatus",
  "userName": "User Name value",
  "userPrincipalName": "User Principal Name value",
  "installedDeviceCount": 4,
  "failedDeviceCount": 1,
  "notInstalledDeviceCount": 7
}
```

### <a name="response"></a><span data-ttu-id="42fe9-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="42fe9-156">Response</span></span>
<span data-ttu-id="42fe9-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="42fe9-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 288

{
  "@odata.type": "#microsoft.graph.userAppInstallStatus",
  "id": "14959a2a-9a2a-1495-2a9a-95142a9a9514",
  "userName": "User Name value",
  "userPrincipalName": "User Principal Name value",
  "installedDeviceCount": 4,
  "failedDeviceCount": 1,
  "notInstalledDeviceCount": 7
}
```





