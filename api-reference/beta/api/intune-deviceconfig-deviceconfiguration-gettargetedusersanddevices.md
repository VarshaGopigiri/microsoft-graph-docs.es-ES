---
title: acción getTargetedUsersAndDevices
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: b0893a3942b3423d2bcb1aebeb77c893b0098b50
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27357641"
---
# <a name="gettargetedusersanddevices-action"></a><span data-ttu-id="513a6-103">acción getTargetedUsersAndDevices</span><span class="sxs-lookup"><span data-stu-id="513a6-103">getTargetedUsersAndDevices action</span></span>

> <span data-ttu-id="513a6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="513a6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="513a6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="513a6-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="513a6-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="513a6-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="513a6-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="513a6-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="513a6-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="513a6-108">Prerequisites</span></span>
<span data-ttu-id="513a6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="513a6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="513a6-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="513a6-111">Permission type</span></span>|<span data-ttu-id="513a6-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="513a6-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="513a6-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="513a6-113">Delegated (work or school account)</span></span>|<span data-ttu-id="513a6-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="513a6-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="513a6-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="513a6-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="513a6-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="513a6-116">Not supported.</span></span>|
|<span data-ttu-id="513a6-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="513a6-117">Application</span></span>|<span data-ttu-id="513a6-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="513a6-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="513a6-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="513a6-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations/getTargetedUsersAndDevices
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/getTargetedUsersAndDevices
```

## <a name="request-headers"></a><span data-ttu-id="513a6-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="513a6-120">Request headers</span></span>
|<span data-ttu-id="513a6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="513a6-121">Header</span></span>|<span data-ttu-id="513a6-122">Valor</span><span class="sxs-lookup"><span data-stu-id="513a6-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="513a6-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="513a6-123">Authorization</span></span>|<span data-ttu-id="513a6-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="513a6-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="513a6-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="513a6-125">Accept</span></span>|<span data-ttu-id="513a6-126">application/json</span><span class="sxs-lookup"><span data-stu-id="513a6-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="513a6-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="513a6-127">Request body</span></span>
<span data-ttu-id="513a6-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="513a6-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="513a6-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="513a6-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="513a6-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="513a6-130">Property</span></span>|<span data-ttu-id="513a6-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="513a6-131">Type</span></span>|<span data-ttu-id="513a6-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="513a6-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="513a6-133">deviceConfigurationIds</span><span class="sxs-lookup"><span data-stu-id="513a6-133">deviceConfigurationIds</span></span>|<span data-ttu-id="513a6-134">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="513a6-134">String collection</span></span>|<span data-ttu-id="513a6-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="513a6-135">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="513a6-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="513a6-136">Response</span></span>
<span data-ttu-id="513a6-137">Si tiene éxito, esta acción devuelve un `200 OK` código de respuesta y una colección de [deviceConfigurationTargetedUserAndDevice](../resources/intune-deviceconfig-deviceconfigurationtargeteduseranddevice.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="513a6-137">If successful, this action returns a `200 OK` response code and a [deviceConfigurationTargetedUserAndDevice](../resources/intune-deviceconfig-deviceconfigurationtargeteduseranddevice.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="513a6-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="513a6-138">Example</span></span>
### <a name="request"></a><span data-ttu-id="513a6-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="513a6-139">Request</span></span>
<span data-ttu-id="513a6-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="513a6-140">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/getTargetedUsersAndDevices

Content-type: application/json
Content-length: 78

{
  "deviceConfigurationIds": [
    "Device Configuration Ids value"
  ]
}
```

### <a name="response"></a><span data-ttu-id="513a6-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="513a6-141">Response</span></span>
<span data-ttu-id="513a6-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="513a6-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 409

{
  "value": [
    {
      "@odata.type": "microsoft.graph.deviceConfigurationTargetedUserAndDevice",
      "deviceId": "Device Id value",
      "deviceName": "Device Name value",
      "userId": "User Id value",
      "userDisplayName": "User Display Name value",
      "userPrincipalName": "User Principal Name value",
      "lastCheckinDateTime": "2017-01-01T00:02:46.0431416-08:00"
    }
  ]
}
```





