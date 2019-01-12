---
title: acción revokeDeviceLicense
description: REVOKE asignado iOS VPP dispositivo licencia para dada la aplicación.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 83d15f542799fb604a3d82d5ac6989087ff75bcf
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27979099"
---
# <a name="revokedevicelicense-action"></a><span data-ttu-id="1cc47-103">acción revokeDeviceLicense</span><span class="sxs-lookup"><span data-stu-id="1cc47-103">revokeDeviceLicense action</span></span>

> <span data-ttu-id="1cc47-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1cc47-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1cc47-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1cc47-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1cc47-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1cc47-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1cc47-107">REVOKE asignado iOS VPP dispositivo licencia para dada la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1cc47-107">Revoke assigned iOS VPP device license for given app.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1cc47-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1cc47-108">Prerequisites</span></span>
<span data-ttu-id="1cc47-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1cc47-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1cc47-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1cc47-111">Permission type</span></span>|<span data-ttu-id="1cc47-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1cc47-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1cc47-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1cc47-113">Delegated (work or school account)</span></span>|<span data-ttu-id="1cc47-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1cc47-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="1cc47-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1cc47-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1cc47-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1cc47-116">Not supported.</span></span>|
|<span data-ttu-id="1cc47-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1cc47-117">Application</span></span>|<span data-ttu-id="1cc47-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1cc47-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1cc47-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1cc47-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps/{mobileAppId}/revokeDeviceLicense
POST /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app/revokeDeviceLicense
POST /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app/revokeDeviceLicense
```

## <a name="request-headers"></a><span data-ttu-id="1cc47-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1cc47-120">Request headers</span></span>
|<span data-ttu-id="1cc47-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1cc47-121">Header</span></span>|<span data-ttu-id="1cc47-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1cc47-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1cc47-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="1cc47-123">Authorization</span></span>|<span data-ttu-id="1cc47-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1cc47-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1cc47-125">Accept</span><span class="sxs-lookup"><span data-stu-id="1cc47-125">Accept</span></span>|<span data-ttu-id="1cc47-126">application/json</span><span class="sxs-lookup"><span data-stu-id="1cc47-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1cc47-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1cc47-127">Request body</span></span>
<span data-ttu-id="1cc47-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="1cc47-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="1cc47-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="1cc47-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="1cc47-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1cc47-130">Property</span></span>|<span data-ttu-id="1cc47-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="1cc47-131">Type</span></span>|<span data-ttu-id="1cc47-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="1cc47-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1cc47-133">managedDeviceId</span><span class="sxs-lookup"><span data-stu-id="1cc47-133">managedDeviceId</span></span>|<span data-ttu-id="1cc47-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="1cc47-134">String</span></span>|<span data-ttu-id="1cc47-135">DeviceId para quienes licencia de aplicaciones asignado es que se desea revocar</span><span class="sxs-lookup"><span data-stu-id="1cc47-135">DeviceId for whom assigned app license is to be revoked</span></span>|
|<span data-ttu-id="1cc47-136">notifyManagedDevices</span><span class="sxs-lookup"><span data-stu-id="1cc47-136">notifyManagedDevices</span></span>|<span data-ttu-id="1cc47-137">Booleano</span><span class="sxs-lookup"><span data-stu-id="1cc47-137">Boolean</span></span>|<span data-ttu-id="1cc47-138">Valor Boolean que indica si se debe enviar notificación de revoke para dispositivos</span><span class="sxs-lookup"><span data-stu-id="1cc47-138">Boolean that indicates if revoke notification should be sent to device</span></span>|



## <a name="response"></a><span data-ttu-id="1cc47-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1cc47-139">Response</span></span>
<span data-ttu-id="1cc47-140">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="1cc47-140">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="1cc47-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1cc47-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="1cc47-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1cc47-142">Request</span></span>
<span data-ttu-id="1cc47-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1cc47-143">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/revokeDeviceLicense

Content-type: application/json
Content-length: 85

{
  "managedDeviceId": "Managed Device Id value",
  "notifyManagedDevices": true
}
```

### <a name="response"></a><span data-ttu-id="1cc47-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1cc47-144">Response</span></span>
<span data-ttu-id="1cc47-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1cc47-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```





