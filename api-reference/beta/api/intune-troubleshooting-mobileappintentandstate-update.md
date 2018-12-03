---
title: Actualizar mobileAppIntentAndState
description: Actualizar las propiedades de un objeto mobileAppIntentAndState.
ms.openlocfilehash: 36bbfa2ea41f68b84ae711204fcbdafb3c309aa2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086684"
---
# <a name="update-mobileappintentandstate"></a><span data-ttu-id="4ef47-103">Actualizar mobileAppIntentAndState</span><span class="sxs-lookup"><span data-stu-id="4ef47-103">Update mobileAppIntentAndState</span></span>

> <span data-ttu-id="4ef47-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4ef47-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4ef47-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4ef47-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="4ef47-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4ef47-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4ef47-107">Actualizar las propiedades de un objeto [mobileAppIntentAndState](../resources/intune-troubleshooting-mobileappintentandstate.md) .</span><span class="sxs-lookup"><span data-stu-id="4ef47-107">Update the properties of a [mobileAppIntentAndState](../resources/intune-troubleshooting-mobileappintentandstate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4ef47-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4ef47-108">Prerequisites</span></span>
<span data-ttu-id="4ef47-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4ef47-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4ef47-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4ef47-111">Permission type</span></span>|<span data-ttu-id="4ef47-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4ef47-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4ef47-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4ef47-113">Delegated (work or school account)</span></span>|<span data-ttu-id="4ef47-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4ef47-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="4ef47-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4ef47-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4ef47-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4ef47-116">Not supported.</span></span>|
|<span data-ttu-id="4ef47-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4ef47-117">Application</span></span>|<span data-ttu-id="4ef47-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4ef47-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4ef47-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4ef47-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /users/{usersId}/mobileAppIntentAndStates/{mobileAppIntentAndStateId}
```

## <a name="request-headers"></a><span data-ttu-id="4ef47-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4ef47-120">Request headers</span></span>
|<span data-ttu-id="4ef47-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4ef47-121">Header</span></span>|<span data-ttu-id="4ef47-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4ef47-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4ef47-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="4ef47-123">Authorization</span></span>|<span data-ttu-id="4ef47-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4ef47-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4ef47-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="4ef47-125">Accept</span></span>|<span data-ttu-id="4ef47-126">application/json</span><span class="sxs-lookup"><span data-stu-id="4ef47-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4ef47-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4ef47-127">Request body</span></span>
<span data-ttu-id="4ef47-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [mobileAppIntentAndState](../resources/intune-troubleshooting-mobileappintentandstate.md) .</span><span class="sxs-lookup"><span data-stu-id="4ef47-128">In the request body, supply a JSON representation for the [mobileAppIntentAndState](../resources/intune-troubleshooting-mobileappintentandstate.md) object.</span></span>

<span data-ttu-id="4ef47-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [mobileAppIntentAndState](../resources/intune-troubleshooting-mobileappintentandstate.md).</span><span class="sxs-lookup"><span data-stu-id="4ef47-129">The following table shows the properties that are required when you create the [mobileAppIntentAndState](../resources/intune-troubleshooting-mobileappintentandstate.md).</span></span>

|<span data-ttu-id="4ef47-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4ef47-130">Property</span></span>|<span data-ttu-id="4ef47-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="4ef47-131">Type</span></span>|<span data-ttu-id="4ef47-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="4ef47-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4ef47-133">id</span><span class="sxs-lookup"><span data-stu-id="4ef47-133">id</span></span>|<span data-ttu-id="4ef47-134">String</span><span class="sxs-lookup"><span data-stu-id="4ef47-134">String</span></span>|<span data-ttu-id="4ef47-135">UUID para el objeto</span><span class="sxs-lookup"><span data-stu-id="4ef47-135">UUID for the object</span></span>|
|<span data-ttu-id="4ef47-136">managedDeviceIdentifier</span><span class="sxs-lookup"><span data-stu-id="4ef47-136">managedDeviceIdentifier</span></span>|<span data-ttu-id="4ef47-137">String</span><span class="sxs-lookup"><span data-stu-id="4ef47-137">String</span></span>|<span data-ttu-id="4ef47-138">Identificador del dispositivo creado o recopilado por Intune.</span><span class="sxs-lookup"><span data-stu-id="4ef47-138">Device identifier created or collected by Intune.</span></span>|
|<span data-ttu-id="4ef47-139">userId</span><span class="sxs-lookup"><span data-stu-id="4ef47-139">userId</span></span>|<span data-ttu-id="4ef47-140">String</span><span class="sxs-lookup"><span data-stu-id="4ef47-140">String</span></span>|<span data-ttu-id="4ef47-141">Identificador del usuario que intentó inscribir el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4ef47-141">Identifier for the user that tried to enroll the device.</span></span>|
|<span data-ttu-id="4ef47-142">mobileAppList</span><span class="sxs-lookup"><span data-stu-id="4ef47-142">mobileAppList</span></span>|<span data-ttu-id="4ef47-143">colección de [mobileAppIntentAndStateDetail](../resources/intune-troubleshooting-mobileappintentandstatedetail.md)</span><span class="sxs-lookup"><span data-stu-id="4ef47-143">[mobileAppIntentAndStateDetail](../resources/intune-troubleshooting-mobileappintentandstatedetail.md) collection</span></span>|<span data-ttu-id="4ef47-144">La lista de calidades de carga y Estados para el inquilino.</span><span class="sxs-lookup"><span data-stu-id="4ef47-144">The list of payload intents and states for the tenant.</span></span>|



## <a name="response"></a><span data-ttu-id="4ef47-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4ef47-145">Response</span></span>
<span data-ttu-id="4ef47-146">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [mobileAppIntentAndState](../resources/intune-troubleshooting-mobileappintentandstate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4ef47-146">If successful, this method returns a `200 OK` response code and an updated [mobileAppIntentAndState](../resources/intune-troubleshooting-mobileappintentandstate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4ef47-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4ef47-147">Example</span></span>
### <a name="request"></a><span data-ttu-id="4ef47-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4ef47-148">Request</span></span>
<span data-ttu-id="4ef47-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4ef47-149">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/users/{usersId}/mobileAppIntentAndStates/{mobileAppIntentAndStateId}
Content-type: application/json
Content-length: 769

{
  "managedDeviceIdentifier": "Managed Device Identifier value",
  "userId": "User Id value",
  "mobileAppList": [
    {
      "@odata.type": "microsoft.graph.mobileAppIntentAndStateDetail",
      "applicationId": "Application Id value",
      "displayName": "Display Name value",
      "mobileAppIntent": "notAvailable",
      "displayVersion": "Display Version value",
      "installState": "failed",
      "supportedDeviceTypes": [
        {
          "@odata.type": "microsoft.graph.mobileAppSupportedDeviceType",
          "type": "windowsRT",
          "minimumOperatingSystemVersion": "Minimum Operating System Version value",
          "maximumOperatingSystemVersion": "Maximum Operating System Version value"
        }
      ]
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="4ef47-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4ef47-150">Response</span></span>
<span data-ttu-id="4ef47-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4ef47-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 880

{
  "@odata.type": "#microsoft.graph.mobileAppIntentAndState",
  "id": "45a775d6-75d6-45a7-d675-a745d675a745",
  "managedDeviceIdentifier": "Managed Device Identifier value",
  "userId": "User Id value",
  "mobileAppList": [
    {
      "@odata.type": "microsoft.graph.mobileAppIntentAndStateDetail",
      "applicationId": "Application Id value",
      "displayName": "Display Name value",
      "mobileAppIntent": "notAvailable",
      "displayVersion": "Display Version value",
      "installState": "failed",
      "supportedDeviceTypes": [
        {
          "@odata.type": "microsoft.graph.mobileAppSupportedDeviceType",
          "type": "windowsRT",
          "minimumOperatingSystemVersion": "Minimum Operating System Version value",
          "maximumOperatingSystemVersion": "Maximum Operating System Version value"
        }
      ]
    }
  ]
}
```




