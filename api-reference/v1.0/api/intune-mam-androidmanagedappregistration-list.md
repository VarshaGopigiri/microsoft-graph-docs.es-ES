---
title: Enumerar androidManagedAppRegistrations
description: Enumere las propiedades y las relaciones de los objetos androidManagedAppRegistration.
ms.openlocfilehash: e281cc17c14a9c1df0015289f138d7f5a870bad3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030446"
---
# <a name="list-androidmanagedappregistrations"></a><span data-ttu-id="cc5a5-103">Enumerar androidManagedAppRegistrations</span><span class="sxs-lookup"><span data-stu-id="cc5a5-103">List androidManagedAppRegistrations</span></span>

> <span data-ttu-id="cc5a5-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cc5a5-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cc5a5-105">Enumere las propiedades y las relaciones de los objetos [androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="cc5a5-105">List properties and relationships of the [androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cc5a5-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cc5a5-106">Prerequisites</span></span>
<span data-ttu-id="cc5a5-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cc5a5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cc5a5-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cc5a5-109">Permission type</span></span>|<span data-ttu-id="cc5a5-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cc5a5-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="cc5a5-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cc5a5-111">Delegated (work or school account)</span></span>|<span data-ttu-id="cc5a5-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="cc5a5-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="cc5a5-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cc5a5-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="cc5a5-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cc5a5-114">Not supported.</span></span>|
|<span data-ttu-id="cc5a5-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cc5a5-115">Application</span></span>|<span data-ttu-id="cc5a5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cc5a5-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="cc5a5-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cc5a5-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedAppRegistrations
```

## <a name="request-headers"></a><span data-ttu-id="cc5a5-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cc5a5-118">Request headers</span></span>
|<span data-ttu-id="cc5a5-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cc5a5-119">Header</span></span>|<span data-ttu-id="cc5a5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="cc5a5-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="cc5a5-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="cc5a5-121">Authorization</span></span>|<span data-ttu-id="cc5a5-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="cc5a5-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="cc5a5-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="cc5a5-123">Accept</span></span>|<span data-ttu-id="cc5a5-124">application/json</span><span class="sxs-lookup"><span data-stu-id="cc5a5-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="cc5a5-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cc5a5-125">Request body</span></span>
<span data-ttu-id="cc5a5-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="cc5a5-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="cc5a5-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cc5a5-127">Response</span></span>
<span data-ttu-id="cc5a5-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cc5a5-128">If successful, this method returns a `200 OK` response code and a collection of [androidManagedAppRegistration](../resources/intune-mam-androidmanagedappregistration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cc5a5-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cc5a5-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="cc5a5-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cc5a5-130">Request</span></span>
<span data-ttu-id="cc5a5-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cc5a5-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppRegistrations
```

### <a name="response"></a><span data-ttu-id="cc5a5-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cc5a5-132">Response</span></span>
<span data-ttu-id="cc5a5-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cc5a5-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 862

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.androidManagedAppRegistration",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
      "applicationVersion": "Application Version value",
      "managementSdkVersion": "Management Sdk Version value",
      "platformVersion": "Platform Version value",
      "deviceType": "Device Type value",
      "deviceTag": "Device Tag value",
      "deviceName": "Device Name value",
      "flaggedReasons": [
        "rootedDevice"
      ],
      "userId": "User Id value",
      "appIdentifier": {
        "@odata.type": "microsoft.graph.androidMobileAppIdentifier",
        "packageId": "Package Id value"
      },
      "id": "0e064997-4997-0e06-9749-060e9749060e",
      "version": "Version value"
    }
  ]
}
```



