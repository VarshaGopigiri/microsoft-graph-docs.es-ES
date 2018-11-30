---
title: Eliminar deviceManagementScriptDeviceState
description: Elimina un deviceManagementScriptDeviceState.
ms.openlocfilehash: 1753be474e698331001ae5c53872f7a0d618a365
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086029"
---
# <a name="delete-devicemanagementscriptdevicestate"></a><span data-ttu-id="908b6-103">Eliminar deviceManagementScriptDeviceState</span><span class="sxs-lookup"><span data-stu-id="908b6-103">Delete deviceManagementScriptDeviceState</span></span>

> <span data-ttu-id="908b6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="908b6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="908b6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="908b6-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="908b6-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="908b6-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="908b6-107">Elimina un [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md).</span><span class="sxs-lookup"><span data-stu-id="908b6-107">Deletes a [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="908b6-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="908b6-108">Prerequisites</span></span>
<span data-ttu-id="908b6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="908b6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="908b6-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="908b6-111">Permission type</span></span>|<span data-ttu-id="908b6-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="908b6-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="908b6-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="908b6-113">Delegated (work or school account)</span></span>|<span data-ttu-id="908b6-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="908b6-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="908b6-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="908b6-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="908b6-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="908b6-116">Not supported.</span></span>|
|<span data-ttu-id="908b6-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="908b6-117">Application</span></span>|<span data-ttu-id="908b6-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="908b6-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="908b6-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="908b6-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}
DELETE /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/userRunStates/{deviceManagementScriptUserStateId}/deviceRunStates/{deviceManagementScriptDeviceStateId}
```

## <a name="request-headers"></a><span data-ttu-id="908b6-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="908b6-120">Request headers</span></span>
|<span data-ttu-id="908b6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="908b6-121">Header</span></span>|<span data-ttu-id="908b6-122">Valor</span><span class="sxs-lookup"><span data-stu-id="908b6-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="908b6-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="908b6-123">Authorization</span></span>|<span data-ttu-id="908b6-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="908b6-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="908b6-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="908b6-125">Accept</span></span>|<span data-ttu-id="908b6-126">application/json</span><span class="sxs-lookup"><span data-stu-id="908b6-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="908b6-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="908b6-127">Request body</span></span>
<span data-ttu-id="908b6-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="908b6-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="908b6-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="908b6-129">Response</span></span>
<span data-ttu-id="908b6-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="908b6-130">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="908b6-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="908b6-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="908b6-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="908b6-132">Request</span></span>
<span data-ttu-id="908b6-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="908b6-133">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/beta/deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}
```

### <a name="response"></a><span data-ttu-id="908b6-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="908b6-134">Response</span></span>
<span data-ttu-id="908b6-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="908b6-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```




