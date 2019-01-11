---
title: Eliminar deviceManagementScriptDeviceState
description: Elimina un deviceManagementScriptDeviceState.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: a133917e229f4144b146cb4efc1ab73f84a09b6c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27882750"
---
# <a name="delete-devicemanagementscriptdevicestate"></a><span data-ttu-id="dbc28-103">Eliminar deviceManagementScriptDeviceState</span><span class="sxs-lookup"><span data-stu-id="dbc28-103">Delete deviceManagementScriptDeviceState</span></span>

> <span data-ttu-id="dbc28-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dbc28-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dbc28-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dbc28-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="dbc28-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="dbc28-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="dbc28-107">Elimina un [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md).</span><span class="sxs-lookup"><span data-stu-id="dbc28-107">Deletes a [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="dbc28-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="dbc28-108">Prerequisites</span></span>
<span data-ttu-id="dbc28-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dbc28-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dbc28-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dbc28-111">Permission type</span></span>|<span data-ttu-id="dbc28-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dbc28-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="dbc28-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dbc28-113">Delegated (work or school account)</span></span>|<span data-ttu-id="dbc28-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="dbc28-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="dbc28-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dbc28-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="dbc28-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dbc28-116">Not supported.</span></span>|
|<span data-ttu-id="dbc28-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dbc28-117">Application</span></span>|<span data-ttu-id="dbc28-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dbc28-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="dbc28-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dbc28-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}
DELETE /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/userRunStates/{deviceManagementScriptUserStateId}/deviceRunStates/{deviceManagementScriptDeviceStateId}
```

## <a name="request-headers"></a><span data-ttu-id="dbc28-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dbc28-120">Request headers</span></span>
|<span data-ttu-id="dbc28-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dbc28-121">Header</span></span>|<span data-ttu-id="dbc28-122">Valor</span><span class="sxs-lookup"><span data-stu-id="dbc28-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="dbc28-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="dbc28-123">Authorization</span></span>|<span data-ttu-id="dbc28-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="dbc28-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="dbc28-125">Accept</span><span class="sxs-lookup"><span data-stu-id="dbc28-125">Accept</span></span>|<span data-ttu-id="dbc28-126">application/json</span><span class="sxs-lookup"><span data-stu-id="dbc28-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="dbc28-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dbc28-127">Request body</span></span>
<span data-ttu-id="dbc28-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="dbc28-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="dbc28-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dbc28-129">Response</span></span>
<span data-ttu-id="dbc28-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="dbc28-130">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="dbc28-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dbc28-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="dbc28-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dbc28-132">Request</span></span>
<span data-ttu-id="dbc28-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dbc28-133">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/beta/deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}
```

### <a name="response"></a><span data-ttu-id="dbc28-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dbc28-134">Response</span></span>
<span data-ttu-id="dbc28-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dbc28-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```





