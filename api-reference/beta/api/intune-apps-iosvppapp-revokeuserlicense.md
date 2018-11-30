---
title: acción revokeUserLicense
description: Licencia de usuario de REVOKE asignado iOS VPP para dado app.
ms.openlocfilehash: 0222623ba5e1f3de0122a632a3ea9554bbd2c0ea
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083952"
---
# <a name="revokeuserlicense-action"></a><span data-ttu-id="ba8dd-103">acción revokeUserLicense</span><span class="sxs-lookup"><span data-stu-id="ba8dd-103">revokeUserLicense action</span></span>

> <span data-ttu-id="ba8dd-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ba8dd-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ba8dd-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ba8dd-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ba8dd-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ba8dd-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ba8dd-107">Licencia de usuario de REVOKE asignado iOS VPP para dado app.</span><span class="sxs-lookup"><span data-stu-id="ba8dd-107">Revoke assigned iOS VPP user license for given app.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ba8dd-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ba8dd-108">Prerequisites</span></span>
<span data-ttu-id="ba8dd-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ba8dd-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ba8dd-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ba8dd-111">Permission type</span></span>|<span data-ttu-id="ba8dd-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ba8dd-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ba8dd-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ba8dd-113">Delegated (work or school account)</span></span>|<span data-ttu-id="ba8dd-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ba8dd-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="ba8dd-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ba8dd-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ba8dd-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ba8dd-116">Not supported.</span></span>|
|<span data-ttu-id="ba8dd-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ba8dd-117">Application</span></span>|<span data-ttu-id="ba8dd-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ba8dd-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ba8dd-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ba8dd-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps/{mobileAppId}/revokeUserLicense
POST /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/app/revokeUserLicense
POST /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}/app/revokeUserLicense
```

## <a name="request-headers"></a><span data-ttu-id="ba8dd-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ba8dd-120">Request headers</span></span>
|<span data-ttu-id="ba8dd-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba8dd-121">Header</span></span>|<span data-ttu-id="ba8dd-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ba8dd-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ba8dd-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="ba8dd-123">Authorization</span></span>|<span data-ttu-id="ba8dd-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ba8dd-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ba8dd-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ba8dd-125">Accept</span></span>|<span data-ttu-id="ba8dd-126">application/json</span><span class="sxs-lookup"><span data-stu-id="ba8dd-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ba8dd-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ba8dd-127">Request body</span></span>
<span data-ttu-id="ba8dd-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="ba8dd-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="ba8dd-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="ba8dd-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="ba8dd-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ba8dd-130">Property</span></span>|<span data-ttu-id="ba8dd-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="ba8dd-131">Type</span></span>|<span data-ttu-id="ba8dd-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba8dd-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ba8dd-133">userId</span><span class="sxs-lookup"><span data-stu-id="ba8dd-133">userId</span></span>|<span data-ttu-id="ba8dd-134">String</span><span class="sxs-lookup"><span data-stu-id="ba8dd-134">String</span></span>|<span data-ttu-id="ba8dd-135">UserId para quienes licencia de aplicaciones asignado es que se desea revocar</span><span class="sxs-lookup"><span data-stu-id="ba8dd-135">UserId for whom assigned app license is to be revoked</span></span>|
|<span data-ttu-id="ba8dd-136">notifyManagedDevices</span><span class="sxs-lookup"><span data-stu-id="ba8dd-136">notifyManagedDevices</span></span>|<span data-ttu-id="ba8dd-137">Booleano</span><span class="sxs-lookup"><span data-stu-id="ba8dd-137">Boolean</span></span>|<span data-ttu-id="ba8dd-138">Valor Boolean que indica si se debe enviar notificación de revoke para dispositivos</span><span class="sxs-lookup"><span data-stu-id="ba8dd-138">Boolean that indicates if revoke notification should be sent to device</span></span>|



## <a name="response"></a><span data-ttu-id="ba8dd-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ba8dd-139">Response</span></span>
<span data-ttu-id="ba8dd-140">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="ba8dd-140">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="ba8dd-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ba8dd-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="ba8dd-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ba8dd-142">Request</span></span>
<span data-ttu-id="ba8dd-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ba8dd-143">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/revokeUserLicense

Content-type: application/json
Content-length: 66

{
  "userId": "User Id value",
  "notifyManagedDevices": true
}
```

### <a name="response"></a><span data-ttu-id="ba8dd-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ba8dd-144">Response</span></span>
<span data-ttu-id="ba8dd-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ba8dd-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```




