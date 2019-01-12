---
title: Actualizar userAppInstallStatus
description: Actualizar las propiedades de un objeto userAppInstallStatus.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 677333a486d1798afe4cf0d004c5fa3af714bf46
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27968732"
---
# <a name="update-userappinstallstatus"></a><span data-ttu-id="085ca-103">Actualizar userAppInstallStatus</span><span class="sxs-lookup"><span data-stu-id="085ca-103">Update userAppInstallStatus</span></span>

> <span data-ttu-id="085ca-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="085ca-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="085ca-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="085ca-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="085ca-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="085ca-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="085ca-107">Actualizar las propiedades de un objeto [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="085ca-107">Update the properties of a [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="085ca-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="085ca-108">Prerequisites</span></span>
<span data-ttu-id="085ca-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="085ca-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="085ca-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="085ca-111">Permission type</span></span>|<span data-ttu-id="085ca-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="085ca-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="085ca-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="085ca-113">Delegated (work or school account)</span></span>|<span data-ttu-id="085ca-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="085ca-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="085ca-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="085ca-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="085ca-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="085ca-116">Not supported.</span></span>|
|<span data-ttu-id="085ca-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="085ca-117">Application</span></span>|<span data-ttu-id="085ca-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="085ca-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="085ca-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="085ca-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}
```

## <a name="request-headers"></a><span data-ttu-id="085ca-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="085ca-120">Request headers</span></span>
|<span data-ttu-id="085ca-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="085ca-121">Header</span></span>|<span data-ttu-id="085ca-122">Valor</span><span class="sxs-lookup"><span data-stu-id="085ca-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="085ca-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="085ca-123">Authorization</span></span>|<span data-ttu-id="085ca-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="085ca-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="085ca-125">Accept</span><span class="sxs-lookup"><span data-stu-id="085ca-125">Accept</span></span>|<span data-ttu-id="085ca-126">application/json</span><span class="sxs-lookup"><span data-stu-id="085ca-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="085ca-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="085ca-127">Request body</span></span>
<span data-ttu-id="085ca-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="085ca-128">In the request body, supply a JSON representation for the [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) object.</span></span>

<span data-ttu-id="085ca-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md).</span><span class="sxs-lookup"><span data-stu-id="085ca-129">The following table shows the properties that are required when you create the [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md).</span></span>

|<span data-ttu-id="085ca-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="085ca-130">Property</span></span>|<span data-ttu-id="085ca-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="085ca-131">Type</span></span>|<span data-ttu-id="085ca-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="085ca-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="085ca-133">id</span><span class="sxs-lookup"><span data-stu-id="085ca-133">id</span></span>|<span data-ttu-id="085ca-134">String</span><span class="sxs-lookup"><span data-stu-id="085ca-134">String</span></span>|<span data-ttu-id="085ca-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="085ca-135">Key of the entity.</span></span>|
|<span data-ttu-id="085ca-136">userName</span><span class="sxs-lookup"><span data-stu-id="085ca-136">userName</span></span>|<span data-ttu-id="085ca-137">String</span><span class="sxs-lookup"><span data-stu-id="085ca-137">String</span></span>|<span data-ttu-id="085ca-138">Nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="085ca-138">User name.</span></span>|
|<span data-ttu-id="085ca-139">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="085ca-139">userPrincipalName</span></span>|<span data-ttu-id="085ca-140">String</span><span class="sxs-lookup"><span data-stu-id="085ca-140">String</span></span>|<span data-ttu-id="085ca-141">Nombre Principal de usuario.</span><span class="sxs-lookup"><span data-stu-id="085ca-141">User Principal Name.</span></span>|
|<span data-ttu-id="085ca-142">installedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="085ca-142">installedDeviceCount</span></span>|<span data-ttu-id="085ca-143">Int32</span><span class="sxs-lookup"><span data-stu-id="085ca-143">Int32</span></span>|<span data-ttu-id="085ca-144">Número de dispositivos instalados.</span><span class="sxs-lookup"><span data-stu-id="085ca-144">Installed Device Count.</span></span>|
|<span data-ttu-id="085ca-145">failedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="085ca-145">failedDeviceCount</span></span>|<span data-ttu-id="085ca-146">Int32</span><span class="sxs-lookup"><span data-stu-id="085ca-146">Int32</span></span>|<span data-ttu-id="085ca-147">Número de dispositivos erróneos.</span><span class="sxs-lookup"><span data-stu-id="085ca-147">Failed Device Count.</span></span>|
|<span data-ttu-id="085ca-148">notInstalledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="085ca-148">notInstalledDeviceCount</span></span>|<span data-ttu-id="085ca-149">Int32</span><span class="sxs-lookup"><span data-stu-id="085ca-149">Int32</span></span>|<span data-ttu-id="085ca-150">Número de dispositivos no instalados.</span><span class="sxs-lookup"><span data-stu-id="085ca-150">Not installed device count.</span></span>|



## <a name="response"></a><span data-ttu-id="085ca-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="085ca-151">Response</span></span>
<span data-ttu-id="085ca-152">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="085ca-152">If successful, this method returns a `200 OK` response code and an updated [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="085ca-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="085ca-153">Example</span></span>
### <a name="request"></a><span data-ttu-id="085ca-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="085ca-154">Request</span></span>
<span data-ttu-id="085ca-155">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="085ca-155">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}
Content-type: application/json
Content-length: 180

{
  "userName": "User Name value",
  "userPrincipalName": "User Principal Name value",
  "installedDeviceCount": 4,
  "failedDeviceCount": 1,
  "notInstalledDeviceCount": 7
}
```

### <a name="response"></a><span data-ttu-id="085ca-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="085ca-156">Response</span></span>
<span data-ttu-id="085ca-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="085ca-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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





