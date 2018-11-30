---
title: acción assignUserToDevice
description: Asigna el usuario a los dispositivos de piloto automático.
ms.openlocfilehash: 7e3152b4ac158714d37f5d5eb1b830a21dd3745d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086070"
---
# <a name="assignusertodevice-action"></a><span data-ttu-id="6e6a5-103">acción assignUserToDevice</span><span class="sxs-lookup"><span data-stu-id="6e6a5-103">assignUserToDevice action</span></span>

> <span data-ttu-id="6e6a5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6e6a5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6e6a5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6e6a5-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6e6a5-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6e6a5-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6e6a5-107">Asigna el usuario a los dispositivos de piloto automático.</span><span class="sxs-lookup"><span data-stu-id="6e6a5-107">Assigns user to Autopilot devices.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6e6a5-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6e6a5-108">Prerequisites</span></span>
<span data-ttu-id="6e6a5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6e6a5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6e6a5-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6e6a5-111">Permission type</span></span>|<span data-ttu-id="6e6a5-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6e6a5-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6e6a5-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6e6a5-113">Delegated (work or school account)</span></span>|<span data-ttu-id="6e6a5-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6e6a5-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="6e6a5-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6e6a5-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6e6a5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6e6a5-116">Not supported.</span></span>|
|<span data-ttu-id="6e6a5-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6e6a5-117">Application</span></span>|<span data-ttu-id="6e6a5-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6e6a5-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6e6a5-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6e6a5-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/windowsAutopilotDeviceIdentities/{windowsAutopilotDeviceIdentityId}/assignUserToDevice
POST /deviceManagement/windowsAutopilotDeviceIdentities/{windowsAutopilotDeviceIdentityId}/deploymentProfile/assignedDevices/{windowsAutopilotDeviceIdentityId}/assignUserToDevice
```

## <a name="request-headers"></a><span data-ttu-id="6e6a5-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6e6a5-120">Request headers</span></span>
|<span data-ttu-id="6e6a5-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e6a5-121">Header</span></span>|<span data-ttu-id="6e6a5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6e6a5-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6e6a5-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="6e6a5-123">Authorization</span></span>|<span data-ttu-id="6e6a5-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6e6a5-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6e6a5-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6e6a5-125">Accept</span></span>|<span data-ttu-id="6e6a5-126">application/json</span><span class="sxs-lookup"><span data-stu-id="6e6a5-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6e6a5-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6e6a5-127">Request body</span></span>
<span data-ttu-id="6e6a5-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="6e6a5-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="6e6a5-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="6e6a5-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="6e6a5-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6e6a5-130">Property</span></span>|<span data-ttu-id="6e6a5-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e6a5-131">Type</span></span>|<span data-ttu-id="6e6a5-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e6a5-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6e6a5-133">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="6e6a5-133">userPrincipalName</span></span>|<span data-ttu-id="6e6a5-134">String</span><span class="sxs-lookup"><span data-stu-id="6e6a5-134">String</span></span>|<span data-ttu-id="6e6a5-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="6e6a5-135">Not yet documented</span></span>|
|<span data-ttu-id="6e6a5-136">addressableUserName</span><span class="sxs-lookup"><span data-stu-id="6e6a5-136">addressableUserName</span></span>|<span data-ttu-id="6e6a5-137">String</span><span class="sxs-lookup"><span data-stu-id="6e6a5-137">String</span></span>|<span data-ttu-id="6e6a5-138">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="6e6a5-138">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="6e6a5-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6e6a5-139">Response</span></span>
<span data-ttu-id="6e6a5-140">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="6e6a5-140">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="6e6a5-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6e6a5-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="6e6a5-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6e6a5-142">Request</span></span>
<span data-ttu-id="6e6a5-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6e6a5-143">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/windowsAutopilotDeviceIdentities/{windowsAutopilotDeviceIdentityId}/assignUserToDevice

Content-type: application/json
Content-length: 113

{
  "userPrincipalName": "User Principal Name value",
  "addressableUserName": "Addressable User Name value"
}
```

### <a name="response"></a><span data-ttu-id="6e6a5-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6e6a5-144">Response</span></span>
<span data-ttu-id="6e6a5-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6e6a5-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```





