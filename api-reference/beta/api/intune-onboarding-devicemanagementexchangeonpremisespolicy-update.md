---
title: Actualizar deviceManagementExchangeOnPremisesPolicy
description: Actualizar las propiedades de un objeto deviceManagementExchangeOnPremisesPolicy.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 5cd001f6935836537fe06bd44af20ca9e6a6aa7b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27873972"
---
# <a name="update-devicemanagementexchangeonpremisespolicy"></a><span data-ttu-id="8fc57-103">Actualizar deviceManagementExchangeOnPremisesPolicy</span><span class="sxs-lookup"><span data-stu-id="8fc57-103">Update deviceManagementExchangeOnPremisesPolicy</span></span>

> <span data-ttu-id="8fc57-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8fc57-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8fc57-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8fc57-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8fc57-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8fc57-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8fc57-107">Actualizar las propiedades de un objeto [deviceManagementExchangeOnPremisesPolicy](../resources/intune-onboarding-devicemanagementexchangeonpremisespolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="8fc57-107">Update the properties of a [deviceManagementExchangeOnPremisesPolicy](../resources/intune-onboarding-devicemanagementexchangeonpremisespolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8fc57-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8fc57-108">Prerequisites</span></span>
<span data-ttu-id="8fc57-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8fc57-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8fc57-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8fc57-111">Permission type</span></span>|<span data-ttu-id="8fc57-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8fc57-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8fc57-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8fc57-113">Delegated (work or school account)</span></span>|<span data-ttu-id="8fc57-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8fc57-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="8fc57-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8fc57-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8fc57-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8fc57-116">Not supported.</span></span>|
|<span data-ttu-id="8fc57-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8fc57-117">Application</span></span>|<span data-ttu-id="8fc57-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8fc57-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8fc57-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8fc57-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/exchangeOnPremisesPolicy
PATCH /deviceManagement/exchangeOnPremisesPolicies/{deviceManagementExchangeOnPremisesPolicyId}
```

## <a name="request-headers"></a><span data-ttu-id="8fc57-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8fc57-120">Request headers</span></span>
|<span data-ttu-id="8fc57-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8fc57-121">Header</span></span>|<span data-ttu-id="8fc57-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8fc57-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8fc57-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="8fc57-123">Authorization</span></span>|<span data-ttu-id="8fc57-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8fc57-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8fc57-125">Accept</span><span class="sxs-lookup"><span data-stu-id="8fc57-125">Accept</span></span>|<span data-ttu-id="8fc57-126">application/json</span><span class="sxs-lookup"><span data-stu-id="8fc57-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8fc57-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8fc57-127">Request body</span></span>
<span data-ttu-id="8fc57-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [deviceManagementExchangeOnPremisesPolicy](../resources/intune-onboarding-devicemanagementexchangeonpremisespolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="8fc57-128">In the request body, supply a JSON representation for the [deviceManagementExchangeOnPremisesPolicy](../resources/intune-onboarding-devicemanagementexchangeonpremisespolicy.md) object.</span></span>

<span data-ttu-id="8fc57-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [deviceManagementExchangeOnPremisesPolicy](../resources/intune-onboarding-devicemanagementexchangeonpremisespolicy.md).</span><span class="sxs-lookup"><span data-stu-id="8fc57-129">The following table shows the properties that are required when you create the [deviceManagementExchangeOnPremisesPolicy](../resources/intune-onboarding-devicemanagementexchangeonpremisespolicy.md).</span></span>

|<span data-ttu-id="8fc57-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8fc57-130">Property</span></span>|<span data-ttu-id="8fc57-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="8fc57-131">Type</span></span>|<span data-ttu-id="8fc57-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="8fc57-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8fc57-133">id</span><span class="sxs-lookup"><span data-stu-id="8fc57-133">id</span></span>|<span data-ttu-id="8fc57-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="8fc57-134">String</span></span>|<span data-ttu-id="8fc57-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="8fc57-135">Not yet documented</span></span>|
|<span data-ttu-id="8fc57-136">notificationContent</span><span class="sxs-lookup"><span data-stu-id="8fc57-136">notificationContent</span></span>|<span data-ttu-id="8fc57-137">Binario</span><span class="sxs-lookup"><span data-stu-id="8fc57-137">Binary</span></span>|<span data-ttu-id="8fc57-138">Texto de notificación que se van a enviar a los usuarios en cuarentena por esta directiva.</span><span class="sxs-lookup"><span data-stu-id="8fc57-138">Notification text that will be sent to users quarantined by this policy.</span></span> <span data-ttu-id="8fc57-139">Se trata de una matriz de bytes codificada con UTF8 HTML.</span><span class="sxs-lookup"><span data-stu-id="8fc57-139">This is UTF8 encoded byte array HTML.</span></span>|
|<span data-ttu-id="8fc57-140">defaultAccessLevel</span><span class="sxs-lookup"><span data-stu-id="8fc57-140">defaultAccessLevel</span></span>|[<span data-ttu-id="8fc57-141">deviceManagementExchangeAccessLevel</span><span class="sxs-lookup"><span data-stu-id="8fc57-141">deviceManagementExchangeAccessLevel</span></span>](../resources/intune-onboarding-devicemanagementexchangeaccesslevel.md)|<span data-ttu-id="8fc57-142">Estado de acceso predeterminado en Exchange.</span><span class="sxs-lookup"><span data-stu-id="8fc57-142">Default access state in Exchange.</span></span> <span data-ttu-id="8fc57-143">Esta regla se aplica globalmente a toda la organización de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8fc57-143">This rule applies globally to the entire Exchange organization.</span></span> <span data-ttu-id="8fc57-144">Los valores posibles son: `none`, `allow`, `block` y `quarantine`.</span><span class="sxs-lookup"><span data-stu-id="8fc57-144">Possible values are: `none`, `allow`, `block`, `quarantine`.</span></span>|
|<span data-ttu-id="8fc57-145">accessRules</span><span class="sxs-lookup"><span data-stu-id="8fc57-145">accessRules</span></span>|<span data-ttu-id="8fc57-146">colección de [deviceManagementExchangeAccessRule](../resources/intune-onboarding-devicemanagementexchangeaccessrule.md)</span><span class="sxs-lookup"><span data-stu-id="8fc57-146">[deviceManagementExchangeAccessRule](../resources/intune-onboarding-devicemanagementexchangeaccessrule.md) collection</span></span>|<span data-ttu-id="8fc57-147">La lista de acceso de los dispositivos de reglas en Exchange.</span><span class="sxs-lookup"><span data-stu-id="8fc57-147">The list of device access rules in Exchange.</span></span> <span data-ttu-id="8fc57-148">Las reglas de acceso se aplican globalmente a toda la organización de Exchange</span><span class="sxs-lookup"><span data-stu-id="8fc57-148">The access rules apply globally to the entire Exchange organization</span></span>|
|<span data-ttu-id="8fc57-149">knownDeviceClasses</span><span class="sxs-lookup"><span data-stu-id="8fc57-149">knownDeviceClasses</span></span>|<span data-ttu-id="8fc57-150">colección de [deviceManagementExchangeDeviceClass](../resources/intune-onboarding-devicemanagementexchangedeviceclass.md)</span><span class="sxs-lookup"><span data-stu-id="8fc57-150">[deviceManagementExchangeDeviceClass](../resources/intune-onboarding-devicemanagementexchangedeviceclass.md) collection</span></span>|<span data-ttu-id="8fc57-151">La lista de clases de dispositivo conocidos para Exchange</span><span class="sxs-lookup"><span data-stu-id="8fc57-151">The list of device classes known to Exchange</span></span>|



## <a name="response"></a><span data-ttu-id="8fc57-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8fc57-152">Response</span></span>
<span data-ttu-id="8fc57-153">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [deviceManagementExchangeOnPremisesPolicy](../resources/intune-onboarding-devicemanagementexchangeonpremisespolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8fc57-153">If successful, this method returns a `200 OK` response code and an updated [deviceManagementExchangeOnPremisesPolicy](../resources/intune-onboarding-devicemanagementexchangeonpremisespolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8fc57-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8fc57-154">Example</span></span>
### <a name="request"></a><span data-ttu-id="8fc57-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8fc57-155">Request</span></span>
<span data-ttu-id="8fc57-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8fc57-156">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="8fc57-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8fc57-157">Response</span></span>
<span data-ttu-id="8fc57-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8fc57-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





