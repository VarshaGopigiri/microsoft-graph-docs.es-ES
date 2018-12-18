---
title: acción revokeAppleVppLicenses
description: Revocar todas las licencias de Apple Vpp para un dispositivo
author: tfitzmac
ms.openlocfilehash: 03a38821a4ca7c8675dbd97d89b157ae6dd88fd4
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27344901"
---
# <a name="revokeapplevpplicenses-action"></a><span data-ttu-id="f3150-103">acción revokeAppleVppLicenses</span><span class="sxs-lookup"><span data-stu-id="f3150-103">revokeAppleVppLicenses action</span></span>

> <span data-ttu-id="f3150-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f3150-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f3150-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f3150-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f3150-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f3150-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f3150-107">Revocar todas las licencias de Apple Vpp para un dispositivo</span><span class="sxs-lookup"><span data-stu-id="f3150-107">Revoke all Apple Vpp licenses for a device</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f3150-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f3150-108">Prerequisites</span></span>
<span data-ttu-id="f3150-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f3150-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f3150-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f3150-111">Permission type</span></span>|<span data-ttu-id="f3150-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f3150-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f3150-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f3150-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f3150-114">DeviceManagementManagedDevices.PriviligedOperation.All</span><span class="sxs-lookup"><span data-stu-id="f3150-114">DeviceManagementManagedDevices.PriviligedOperation.All</span></span>|
|<span data-ttu-id="f3150-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f3150-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f3150-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f3150-116">Not supported.</span></span>|
|<span data-ttu-id="f3150-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f3150-117">Application</span></span>|<span data-ttu-id="f3150-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f3150-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f3150-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f3150-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/managedDevices/{managedDeviceId}/revokeAppleVppLicenses
POST /deviceManagement/managedDevices/{managedDeviceId}/revokeAppleVppLicenses
POST /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/revokeAppleVppLicenses
POST /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}/revokeAppleVppLicenses
```

## <a name="request-headers"></a><span data-ttu-id="f3150-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f3150-120">Request headers</span></span>
|<span data-ttu-id="f3150-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3150-121">Header</span></span>|<span data-ttu-id="f3150-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f3150-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f3150-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="f3150-123">Authorization</span></span>|<span data-ttu-id="f3150-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f3150-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f3150-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f3150-125">Accept</span></span>|<span data-ttu-id="f3150-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f3150-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f3150-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f3150-127">Request body</span></span>
<span data-ttu-id="f3150-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f3150-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f3150-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f3150-129">Response</span></span>
<span data-ttu-id="f3150-130">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="f3150-130">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="f3150-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f3150-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="f3150-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f3150-132">Request</span></span>
<span data-ttu-id="f3150-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f3150-133">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/users/{usersId}/managedDevices/{managedDeviceId}/revokeAppleVppLicenses
```

### <a name="response"></a><span data-ttu-id="f3150-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f3150-134">Response</span></span>
<span data-ttu-id="f3150-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f3150-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```





