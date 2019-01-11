---
title: Enumerar managedAppRegistrations
description: Enumere las propiedades y las relaciones de los objetos managedAppRegistration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: d9676a082269d450ad1dd5b5267d45733f47803b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27822298"
---
# <a name="list-managedappregistrations"></a><span data-ttu-id="caed4-103">Enumerar managedAppRegistrations</span><span class="sxs-lookup"><span data-stu-id="caed4-103">List managedAppRegistrations</span></span>

> <span data-ttu-id="caed4-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="caed4-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="caed4-105">Enumere las propiedades y las relaciones de los objetos [managedAppRegistration](../resources/intune-mam-managedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="caed4-105">List properties and relationships of the [managedAppRegistration](../resources/intune-mam-managedappregistration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="caed4-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="caed4-106">Prerequisites</span></span>
<span data-ttu-id="caed4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="caed4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="caed4-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="caed4-109">Permission type</span></span>|<span data-ttu-id="caed4-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="caed4-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="caed4-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="caed4-111">Delegated (work or school account)</span></span>|<span data-ttu-id="caed4-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="caed4-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="caed4-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="caed4-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="caed4-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="caed4-114">Not supported.</span></span>|
|<span data-ttu-id="caed4-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="caed4-115">Application</span></span>|<span data-ttu-id="caed4-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="caed4-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="caed4-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="caed4-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedAppRegistrations
```

## <a name="request-headers"></a><span data-ttu-id="caed4-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="caed4-118">Request headers</span></span>
|<span data-ttu-id="caed4-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="caed4-119">Header</span></span>|<span data-ttu-id="caed4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="caed4-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="caed4-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="caed4-121">Authorization</span></span>|<span data-ttu-id="caed4-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="caed4-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="caed4-123">Accept</span><span class="sxs-lookup"><span data-stu-id="caed4-123">Accept</span></span>|<span data-ttu-id="caed4-124">application/json</span><span class="sxs-lookup"><span data-stu-id="caed4-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="caed4-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="caed4-125">Request body</span></span>
<span data-ttu-id="caed4-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="caed4-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="caed4-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="caed4-127">Response</span></span>
<span data-ttu-id="caed4-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [managedAppRegistration](../resources/intune-mam-managedappregistration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="caed4-128">If successful, this method returns a `200 OK` response code and a collection of [managedAppRegistration](../resources/intune-mam-managedappregistration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="caed4-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="caed4-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="caed4-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="caed4-130">Request</span></span>
<span data-ttu-id="caed4-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="caed4-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppRegistrations
```

### <a name="response"></a><span data-ttu-id="caed4-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="caed4-132">Response</span></span>
<span data-ttu-id="caed4-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="caed4-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 806

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.managedAppRegistration",
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
        "@odata.type": "microsoft.graph.mobileAppIdentifier"
      },
      "id": "5496aa60-aa60-5496-60aa-965460aa9654",
      "version": "Version value"
    }
  ]
}
```



