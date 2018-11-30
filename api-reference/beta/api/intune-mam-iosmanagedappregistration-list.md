---
title: Enumerar iosManagedAppRegistrations
description: Enumere las propiedades y las relaciones de los objetos iosManagedAppRegistration.
ms.openlocfilehash: 2ca0ec9d669f8778754f74a9d6d056da368bb086
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087447"
---
# <a name="list-iosmanagedappregistrations"></a><span data-ttu-id="1b755-103">Enumerar iosManagedAppRegistrations</span><span class="sxs-lookup"><span data-stu-id="1b755-103">List iosManagedAppRegistrations</span></span>

> <span data-ttu-id="1b755-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1b755-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1b755-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1b755-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1b755-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1b755-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1b755-107">Enumere las propiedades y las relaciones de los objetos [iosManagedAppRegistration](../resources/intune-mam-iosmanagedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="1b755-107">List properties and relationships of the [iosManagedAppRegistration](../resources/intune-mam-iosmanagedappregistration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1b755-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1b755-108">Prerequisites</span></span>
<span data-ttu-id="1b755-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1b755-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1b755-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1b755-111">Permission type</span></span>|<span data-ttu-id="1b755-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1b755-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1b755-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1b755-113">Delegated (work or school account)</span></span>|<span data-ttu-id="1b755-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="1b755-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="1b755-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1b755-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1b755-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1b755-116">Not supported.</span></span>|
|<span data-ttu-id="1b755-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1b755-117">Application</span></span>|<span data-ttu-id="1b755-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1b755-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1b755-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1b755-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedAppRegistrations
```

## <a name="request-headers"></a><span data-ttu-id="1b755-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1b755-120">Request headers</span></span>
|<span data-ttu-id="1b755-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1b755-121">Header</span></span>|<span data-ttu-id="1b755-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1b755-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1b755-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="1b755-123">Authorization</span></span>|<span data-ttu-id="1b755-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1b755-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1b755-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1b755-125">Accept</span></span>|<span data-ttu-id="1b755-126">application/json</span><span class="sxs-lookup"><span data-stu-id="1b755-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1b755-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1b755-127">Request body</span></span>
<span data-ttu-id="1b755-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1b755-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1b755-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1b755-129">Response</span></span>
<span data-ttu-id="1b755-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [iosManagedAppRegistration](../resources/intune-mam-iosmanagedappregistration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1b755-130">If successful, this method returns a `200 OK` response code and a collection of [iosManagedAppRegistration](../resources/intune-mam-iosmanagedappregistration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1b755-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1b755-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="1b755-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1b755-132">Request</span></span>
<span data-ttu-id="1b755-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1b755-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/managedAppRegistrations
```

### <a name="response"></a><span data-ttu-id="1b755-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1b755-134">Response</span></span>
<span data-ttu-id="1b755-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1b755-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1060

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.iosManagedAppRegistration",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
      "applicationVersion": "Application Version value",
      "managementSdkVersion": "Management Sdk Version value",
      "platformVersion": "Platform Version value",
      "deviceType": "Device Type value",
      "deviceTag": "Device Tag value",
      "deviceName": "Device Name value",
      "managedDeviceId": "Managed Device Id value",
      "azureADDeviceId": "Azure ADDevice Id value",
      "deviceModel": "Device Model value",
      "deviceManufacturer": "Device Manufacturer value",
      "flaggedReasons": [
        "rootedDevice"
      ],
      "userId": "User Id value",
      "appIdentifier": {
        "@odata.type": "microsoft.graph.iosMobileAppIdentifier",
        "bundleId": "Bundle Id value"
      },
      "id": "47632c19-2c19-4763-192c-6347192c6347",
      "version": "Version value"
    }
  ]
}
```





