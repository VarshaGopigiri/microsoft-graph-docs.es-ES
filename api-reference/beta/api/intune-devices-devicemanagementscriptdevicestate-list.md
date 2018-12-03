---
title: Lista deviceManagementScriptDeviceStates
description: Propiedades de la lista y relaciones de los objetos deviceManagementScriptDeviceState.
ms.openlocfilehash: 1c419663960c14a834360839861c6adaff146935
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083791"
---
# <a name="list-devicemanagementscriptdevicestates"></a><span data-ttu-id="47c79-103">Lista deviceManagementScriptDeviceStates</span><span class="sxs-lookup"><span data-stu-id="47c79-103">List deviceManagementScriptDeviceStates</span></span>

> <span data-ttu-id="47c79-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="47c79-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="47c79-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="47c79-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="47c79-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="47c79-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="47c79-107">Propiedades de la lista y relaciones de los objetos [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md) .</span><span class="sxs-lookup"><span data-stu-id="47c79-107">List properties and relationships of the [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="47c79-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="47c79-108">Prerequisites</span></span>
<span data-ttu-id="47c79-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="47c79-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="47c79-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="47c79-111">Permission type</span></span>|<span data-ttu-id="47c79-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="47c79-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="47c79-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="47c79-113">Delegated (work or school account)</span></span>|<span data-ttu-id="47c79-114">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="47c79-114">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="47c79-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="47c79-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="47c79-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="47c79-116">Not supported.</span></span>|
|<span data-ttu-id="47c79-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="47c79-117">Application</span></span>|<span data-ttu-id="47c79-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="47c79-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="47c79-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="47c79-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates
GET /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/userRunStates/{deviceManagementScriptUserStateId}/deviceRunStates
```

## <a name="request-headers"></a><span data-ttu-id="47c79-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="47c79-120">Request headers</span></span>
|<span data-ttu-id="47c79-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="47c79-121">Header</span></span>|<span data-ttu-id="47c79-122">Valor</span><span class="sxs-lookup"><span data-stu-id="47c79-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="47c79-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="47c79-123">Authorization</span></span>|<span data-ttu-id="47c79-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="47c79-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="47c79-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="47c79-125">Accept</span></span>|<span data-ttu-id="47c79-126">application/json</span><span class="sxs-lookup"><span data-stu-id="47c79-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="47c79-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="47c79-127">Request body</span></span>
<span data-ttu-id="47c79-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="47c79-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="47c79-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="47c79-129">Response</span></span>
<span data-ttu-id="47c79-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="47c79-130">If successful, this method returns a `200 OK` response code and a collection of [deviceManagementScriptDeviceState](../resources/intune-devices-devicemanagementscriptdevicestate.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="47c79-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="47c79-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="47c79-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="47c79-132">Request</span></span>
<span data-ttu-id="47c79-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="47c79-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates
```

### <a name="response"></a><span data-ttu-id="47c79-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="47c79-134">Response</span></span>
<span data-ttu-id="47c79-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="47c79-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 391

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceManagementScriptDeviceState",
      "id": "39440cba-0cba-3944-ba0c-4439ba0c4439",
      "runState": "success",
      "resultMessage": "Result Message value",
      "lastStateUpdateDateTime": "2017-01-01T00:02:58.4418045-08:00",
      "errorCode": 9,
      "errorDescription": "Error Description value"
    }
  ]
}
```




