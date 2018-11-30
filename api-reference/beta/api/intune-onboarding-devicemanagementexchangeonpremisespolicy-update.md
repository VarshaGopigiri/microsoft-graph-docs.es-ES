---
title: Actualizar deviceManagementExchangeOnPremisesPolicy
description: Actualizar las propiedades de un objeto deviceManagementExchangeOnPremisesPolicy.
ms.openlocfilehash: afc3df27d79b2cefab434126da8971f0fff5c8e4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084342"
---
# <a name="update-devicemanagementexchangeonpremisespolicy"></a><span data-ttu-id="31fd5-103">Actualizar deviceManagementExchangeOnPremisesPolicy</span><span class="sxs-lookup"><span data-stu-id="31fd5-103">Update deviceManagementExchangeOnPremisesPolicy</span></span>

> <span data-ttu-id="31fd5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="31fd5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="31fd5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="31fd5-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="31fd5-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="31fd5-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="31fd5-107">Actualizar las propiedades de un objeto [deviceManagementExchangeOnPremisesPolicy](../resources/intune-onboarding-devicemanagementexchangeonpremisespolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="31fd5-107">Update the properties of a [deviceManagementExchangeOnPremisesPolicy](../resources/intune-onboarding-devicemanagementexchangeonpremisespolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="31fd5-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="31fd5-108">Prerequisites</span></span>
<span data-ttu-id="31fd5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="31fd5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="31fd5-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="31fd5-111">Permission type</span></span>|<span data-ttu-id="31fd5-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="31fd5-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="31fd5-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="31fd5-113">Delegated (work or school account)</span></span>|<span data-ttu-id="31fd5-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="31fd5-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="31fd5-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="31fd5-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="31fd5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="31fd5-116">Not supported.</span></span>|
|<span data-ttu-id="31fd5-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="31fd5-117">Application</span></span>|<span data-ttu-id="31fd5-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="31fd5-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="31fd5-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="31fd5-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/exchangeOnPremisesPolicy
PATCH /deviceManagement/exchangeOnPremisesPolicies/{deviceManagementExchangeOnPremisesPolicyId}
```

## <a name="request-headers"></a><span data-ttu-id="31fd5-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="31fd5-120">Request headers</span></span>
|<span data-ttu-id="31fd5-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31fd5-121">Header</span></span>|<span data-ttu-id="31fd5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="31fd5-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="31fd5-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="31fd5-123">Authorization</span></span>|<span data-ttu-id="31fd5-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="31fd5-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="31fd5-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="31fd5-125">Accept</span></span>|<span data-ttu-id="31fd5-126">application/json</span><span class="sxs-lookup"><span data-stu-id="31fd5-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="31fd5-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="31fd5-127">Request body</span></span>
<span data-ttu-id="31fd5-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [deviceManagementExchangeOnPremisesPolicy](../resources/intune-onboarding-devicemanagementexchangeonpremisespolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="31fd5-128">In the request body, supply a JSON representation for the [deviceManagementExchangeOnPremisesPolicy](../resources/intune-onboarding-devicemanagementexchangeonpremisespolicy.md) object.</span></span>

<span data-ttu-id="31fd5-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [deviceManagementExchangeOnPremisesPolicy](../resources/intune-onboarding-devicemanagementexchangeonpremisespolicy.md).</span><span class="sxs-lookup"><span data-stu-id="31fd5-129">The following table shows the properties that are required when you create the [deviceManagementExchangeOnPremisesPolicy](../resources/intune-onboarding-devicemanagementexchangeonpremisespolicy.md).</span></span>

|<span data-ttu-id="31fd5-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="31fd5-130">Property</span></span>|<span data-ttu-id="31fd5-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="31fd5-131">Type</span></span>|<span data-ttu-id="31fd5-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="31fd5-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="31fd5-133">id</span><span class="sxs-lookup"><span data-stu-id="31fd5-133">id</span></span>|<span data-ttu-id="31fd5-134">String</span><span class="sxs-lookup"><span data-stu-id="31fd5-134">String</span></span>|<span data-ttu-id="31fd5-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="31fd5-135">Not yet documented</span></span>|
|<span data-ttu-id="31fd5-136">notificationContent</span><span class="sxs-lookup"><span data-stu-id="31fd5-136">notificationContent</span></span>|<span data-ttu-id="31fd5-137">Binario</span><span class="sxs-lookup"><span data-stu-id="31fd5-137">Binary</span></span>|<span data-ttu-id="31fd5-138">Texto de notificación que se van a enviar a los usuarios en cuarentena por esta directiva.</span><span class="sxs-lookup"><span data-stu-id="31fd5-138">Notification text that will be sent to users quarantined by this policy.</span></span> <span data-ttu-id="31fd5-139">Se trata de una matriz de bytes codificada con UTF8 HTML.</span><span class="sxs-lookup"><span data-stu-id="31fd5-139">This is UTF8 encoded byte array HTML.</span></span>|
|<span data-ttu-id="31fd5-140">defaultAccessLevel</span><span class="sxs-lookup"><span data-stu-id="31fd5-140">defaultAccessLevel</span></span>|[<span data-ttu-id="31fd5-141">deviceManagementExchangeAccessLevel</span><span class="sxs-lookup"><span data-stu-id="31fd5-141">deviceManagementExchangeAccessLevel</span></span>](../resources/intune-onboarding-devicemanagementexchangeaccesslevel.md)|<span data-ttu-id="31fd5-142">Estado de acceso predeterminado en Exchange.</span><span class="sxs-lookup"><span data-stu-id="31fd5-142">Default access state in Exchange.</span></span> <span data-ttu-id="31fd5-143">Esta regla se aplica globalmente a toda la organización de Exchange.</span><span class="sxs-lookup"><span data-stu-id="31fd5-143">This rule applies globally to the entire Exchange organization.</span></span> <span data-ttu-id="31fd5-144">Los valores posibles son: `none`, `allow`, `block` y `quarantine`.</span><span class="sxs-lookup"><span data-stu-id="31fd5-144">Possible values are: `none`, `allow`, `block`, `quarantine`.</span></span>|
|<span data-ttu-id="31fd5-145">accessRules</span><span class="sxs-lookup"><span data-stu-id="31fd5-145">accessRules</span></span>|<span data-ttu-id="31fd5-146">colección de [deviceManagementExchangeAccessRule](../resources/intune-onboarding-devicemanagementexchangeaccessrule.md)</span><span class="sxs-lookup"><span data-stu-id="31fd5-146">[deviceManagementExchangeAccessRule](../resources/intune-onboarding-devicemanagementexchangeaccessrule.md) collection</span></span>|<span data-ttu-id="31fd5-147">La lista de acceso de los dispositivos de reglas en Exchange.</span><span class="sxs-lookup"><span data-stu-id="31fd5-147">The list of device access rules in Exchange.</span></span> <span data-ttu-id="31fd5-148">Las reglas de acceso se aplican globalmente a toda la organización de Exchange</span><span class="sxs-lookup"><span data-stu-id="31fd5-148">The access rules apply globally to the entire Exchange organization</span></span>|
|<span data-ttu-id="31fd5-149">knownDeviceClasses</span><span class="sxs-lookup"><span data-stu-id="31fd5-149">knownDeviceClasses</span></span>|<span data-ttu-id="31fd5-150">colección de [deviceManagementExchangeDeviceClass](../resources/intune-onboarding-devicemanagementexchangedeviceclass.md)</span><span class="sxs-lookup"><span data-stu-id="31fd5-150">[deviceManagementExchangeDeviceClass](../resources/intune-onboarding-devicemanagementexchangedeviceclass.md) collection</span></span>|<span data-ttu-id="31fd5-151">La lista de clases de dispositivo conocidos para Exchange</span><span class="sxs-lookup"><span data-stu-id="31fd5-151">The list of device classes known to Exchange</span></span>|



## <a name="response"></a><span data-ttu-id="31fd5-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="31fd5-152">Response</span></span>
<span data-ttu-id="31fd5-153">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [deviceManagementExchangeOnPremisesPolicy](../resources/intune-onboarding-devicemanagementexchangeonpremisespolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="31fd5-153">If successful, this method returns a `200 OK` response code and an updated [deviceManagementExchangeOnPremisesPolicy](../resources/intune-onboarding-devicemanagementexchangeonpremisespolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="31fd5-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="31fd5-154">Example</span></span>
### <a name="request"></a><span data-ttu-id="31fd5-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="31fd5-155">Request</span></span>
<span data-ttu-id="31fd5-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="31fd5-156">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/exchangeOnPremisesPolicy
Content-type: application/json
Content-length: 586

{
  "notificationContent": "bm90aWZpY2F0aW9uQ29udGVudA==",
  "defaultAccessLevel": "allow",
  "accessRules": [
    {
      "@odata.type": "microsoft.graph.deviceManagementExchangeAccessRule",
      "deviceClass": {
        "@odata.type": "microsoft.graph.deviceManagementExchangeDeviceClass",
        "name": "Name value",
        "type": "model"
      },
      "accessLevel": "allow"
    }
  ],
  "knownDeviceClasses": [
    {
      "@odata.type": "microsoft.graph.deviceManagementExchangeDeviceClass",
      "name": "Name value",
      "type": "model"
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="31fd5-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="31fd5-157">Response</span></span>
<span data-ttu-id="31fd5-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="31fd5-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 714

{
  "@odata.type": "#microsoft.graph.deviceManagementExchangeOnPremisesPolicy",
  "id": "16e76336-6336-16e7-3663-e7163663e716",
  "notificationContent": "bm90aWZpY2F0aW9uQ29udGVudA==",
  "defaultAccessLevel": "allow",
  "accessRules": [
    {
      "@odata.type": "microsoft.graph.deviceManagementExchangeAccessRule",
      "deviceClass": {
        "@odata.type": "microsoft.graph.deviceManagementExchangeDeviceClass",
        "name": "Name value",
        "type": "model"
      },
      "accessLevel": "allow"
    }
  ],
  "knownDeviceClasses": [
    {
      "@odata.type": "microsoft.graph.deviceManagementExchangeDeviceClass",
      "name": "Name value",
      "type": "model"
    }
  ]
}
```





