---
title: Acción resetPasscode
description: Restablecer código de acceso
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: be84428cde043885d67509a6e023f16cccd03f64
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27882176"
---
# <a name="resetpasscode-action"></a><span data-ttu-id="32a2a-103">Acción resetPasscode</span><span class="sxs-lookup"><span data-stu-id="32a2a-103">resetPasscode action</span></span>

> <span data-ttu-id="32a2a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="32a2a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="32a2a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="32a2a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="32a2a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="32a2a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="32a2a-107">Restablecer código de acceso</span><span class="sxs-lookup"><span data-stu-id="32a2a-107">Reset passcode</span></span>
## <a name="prerequisites"></a><span data-ttu-id="32a2a-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="32a2a-108">Prerequisites</span></span>
<span data-ttu-id="32a2a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="32a2a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="32a2a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="32a2a-111">Permission type</span></span>|<span data-ttu-id="32a2a-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="32a2a-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="32a2a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="32a2a-113">Delegated (work or school account)</span></span>|<span data-ttu-id="32a2a-114">DeviceManagementManagedDevices.PriviligedOperation.All</span><span class="sxs-lookup"><span data-stu-id="32a2a-114">DeviceManagementManagedDevices.PriviligedOperation.All</span></span>|
|<span data-ttu-id="32a2a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="32a2a-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="32a2a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="32a2a-116">Not supported.</span></span>|
|<span data-ttu-id="32a2a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="32a2a-117">Application</span></span>|<span data-ttu-id="32a2a-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="32a2a-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="32a2a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="32a2a-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/managedDevices/{managedDeviceId}/resetPasscode
POST /deviceManagement/managedDevices/{managedDeviceId}/resetPasscode
POST /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/resetPasscode
POST /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}/resetPasscode
```

## <a name="request-headers"></a><span data-ttu-id="32a2a-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="32a2a-120">Request headers</span></span>
|<span data-ttu-id="32a2a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="32a2a-121">Header</span></span>|<span data-ttu-id="32a2a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="32a2a-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="32a2a-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="32a2a-123">Authorization</span></span>|<span data-ttu-id="32a2a-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="32a2a-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="32a2a-125">Accept</span><span class="sxs-lookup"><span data-stu-id="32a2a-125">Accept</span></span>|<span data-ttu-id="32a2a-126">application/json</span><span class="sxs-lookup"><span data-stu-id="32a2a-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="32a2a-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="32a2a-127">Request body</span></span>
<span data-ttu-id="32a2a-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="32a2a-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="32a2a-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="32a2a-129">Response</span></span>
<span data-ttu-id="32a2a-130">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="32a2a-130">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="32a2a-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="32a2a-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="32a2a-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="32a2a-132">Request</span></span>
<span data-ttu-id="32a2a-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="32a2a-133">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/users/{usersId}/managedDevices/{managedDeviceId}/resetPasscode
```

### <a name="response"></a><span data-ttu-id="32a2a-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="32a2a-134">Response</span></span>
<span data-ttu-id="32a2a-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="32a2a-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```





