---
title: Actualizar deviceManagementScriptUserState
description: Actualizar las propiedades de un objeto deviceManagementScriptUserState.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: e5c3f991a8deaa3a68e7434426cc51c7ea205ef3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27806912"
---
# <a name="update-devicemanagementscriptuserstate"></a><span data-ttu-id="78c30-103">Actualizar deviceManagementScriptUserState</span><span class="sxs-lookup"><span data-stu-id="78c30-103">Update deviceManagementScriptUserState</span></span>

> <span data-ttu-id="78c30-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="78c30-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="78c30-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="78c30-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="78c30-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="78c30-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="78c30-107">Actualizar las propiedades de un objeto [deviceManagementScriptUserState](../resources/intune-devices-devicemanagementscriptuserstate.md) .</span><span class="sxs-lookup"><span data-stu-id="78c30-107">Update the properties of a [deviceManagementScriptUserState](../resources/intune-devices-devicemanagementscriptuserstate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="78c30-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="78c30-108">Prerequisites</span></span>
<span data-ttu-id="78c30-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="78c30-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="78c30-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="78c30-111">Permission type</span></span>|<span data-ttu-id="78c30-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="78c30-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="78c30-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="78c30-113">Delegated (work or school account)</span></span>|<span data-ttu-id="78c30-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="78c30-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="78c30-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="78c30-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="78c30-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="78c30-116">Not supported.</span></span>|
|<span data-ttu-id="78c30-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="78c30-117">Application</span></span>|<span data-ttu-id="78c30-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="78c30-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="78c30-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="78c30-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/userRunStates/{deviceManagementScriptUserStateId}
```

## <a name="request-headers"></a><span data-ttu-id="78c30-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="78c30-120">Request headers</span></span>
|<span data-ttu-id="78c30-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="78c30-121">Header</span></span>|<span data-ttu-id="78c30-122">Valor</span><span class="sxs-lookup"><span data-stu-id="78c30-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="78c30-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="78c30-123">Authorization</span></span>|<span data-ttu-id="78c30-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="78c30-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="78c30-125">Accept</span><span class="sxs-lookup"><span data-stu-id="78c30-125">Accept</span></span>|<span data-ttu-id="78c30-126">application/json</span><span class="sxs-lookup"><span data-stu-id="78c30-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="78c30-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="78c30-127">Request body</span></span>
<span data-ttu-id="78c30-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [deviceManagementScriptUserState](../resources/intune-devices-devicemanagementscriptuserstate.md) .</span><span class="sxs-lookup"><span data-stu-id="78c30-128">In the request body, supply a JSON representation for the [deviceManagementScriptUserState](../resources/intune-devices-devicemanagementscriptuserstate.md) object.</span></span>

<span data-ttu-id="78c30-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [deviceManagementScriptUserState](../resources/intune-devices-devicemanagementscriptuserstate.md).</span><span class="sxs-lookup"><span data-stu-id="78c30-129">The following table shows the properties that are required when you create the [deviceManagementScriptUserState](../resources/intune-devices-devicemanagementscriptuserstate.md).</span></span>

|<span data-ttu-id="78c30-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="78c30-130">Property</span></span>|<span data-ttu-id="78c30-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="78c30-131">Type</span></span>|<span data-ttu-id="78c30-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="78c30-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="78c30-133">id</span><span class="sxs-lookup"><span data-stu-id="78c30-133">id</span></span>|<span data-ttu-id="78c30-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="78c30-134">String</span></span>|<span data-ttu-id="78c30-135">Clave de la entidad de estado de usuario de secuencia de comandos de dispositivo administración.</span><span class="sxs-lookup"><span data-stu-id="78c30-135">Key of the device management script user state entity.</span></span>|
|<span data-ttu-id="78c30-136">successDeviceCount</span><span class="sxs-lookup"><span data-stu-id="78c30-136">successDeviceCount</span></span>|<span data-ttu-id="78c30-137">Int32</span><span class="sxs-lookup"><span data-stu-id="78c30-137">Int32</span></span>|<span data-ttu-id="78c30-138">Recuento de éxito de dispositivo para el usuario específico.</span><span class="sxs-lookup"><span data-stu-id="78c30-138">Success device count for specific user.</span></span>|
|<span data-ttu-id="78c30-139">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="78c30-139">errorDeviceCount</span></span>|<span data-ttu-id="78c30-140">Int32</span><span class="sxs-lookup"><span data-stu-id="78c30-140">Int32</span></span>|<span data-ttu-id="78c30-141">Número de dispositivo de error de usuario específico.</span><span class="sxs-lookup"><span data-stu-id="78c30-141">Error device count for specific user.</span></span>|
|<span data-ttu-id="78c30-142">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="78c30-142">userPrincipalName</span></span>|<span data-ttu-id="78c30-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="78c30-143">String</span></span>|<span data-ttu-id="78c30-144">Nombre de principio de usuario del usuario específico.</span><span class="sxs-lookup"><span data-stu-id="78c30-144">User principle name of specific user.</span></span>|



## <a name="response"></a><span data-ttu-id="78c30-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="78c30-145">Response</span></span>
<span data-ttu-id="78c30-146">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [deviceManagementScriptUserState](../resources/intune-devices-devicemanagementscriptuserstate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="78c30-146">If successful, this method returns a `200 OK` response code and an updated [deviceManagementScriptUserState](../resources/intune-devices-devicemanagementscriptuserstate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="78c30-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="78c30-147">Example</span></span>
### <a name="request"></a><span data-ttu-id="78c30-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="78c30-148">Request</span></span>
<span data-ttu-id="78c30-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="78c30-149">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/userRunStates/{deviceManagementScriptUserStateId}
Content-type: application/json
Content-length: 110

{
  "successDeviceCount": 2,
  "errorDeviceCount": 0,
  "userPrincipalName": "User Principal Name value"
}
```

### <a name="response"></a><span data-ttu-id="78c30-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="78c30-150">Response</span></span>
<span data-ttu-id="78c30-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="78c30-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 229

{
  "@odata.type": "#microsoft.graph.deviceManagementScriptUserState",
  "id": "d5a29103-9103-d5a2-0391-a2d50391a2d5",
  "successDeviceCount": 2,
  "errorDeviceCount": 0,
  "userPrincipalName": "User Principal Name value"
}
```





