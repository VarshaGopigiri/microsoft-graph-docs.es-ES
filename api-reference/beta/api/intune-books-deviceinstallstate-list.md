---
title: Enumerar deviceInstallStates
description: Enumere las propiedades y las relaciones de los objetos deviceInstallState.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 0352a70246726437961435b75feebfbd6af24f71
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27883128"
---
# <a name="list-deviceinstallstates"></a><span data-ttu-id="12ad5-103">Enumerar deviceInstallStates</span><span class="sxs-lookup"><span data-stu-id="12ad5-103">List deviceInstallStates</span></span>

> <span data-ttu-id="12ad5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="12ad5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="12ad5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="12ad5-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="12ad5-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="12ad5-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="12ad5-107">Enumere las propiedades y las relaciones de los objetos [deviceInstallState](../resources/intune-books-deviceinstallstate.md).</span><span class="sxs-lookup"><span data-stu-id="12ad5-107">List properties and relationships of the [deviceInstallState](../resources/intune-books-deviceinstallstate.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="12ad5-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="12ad5-108">Prerequisites</span></span>
<span data-ttu-id="12ad5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="12ad5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="12ad5-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="12ad5-111">Permission type</span></span>|<span data-ttu-id="12ad5-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="12ad5-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="12ad5-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="12ad5-113">Delegated (work or school account)</span></span>|<span data-ttu-id="12ad5-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="12ad5-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="12ad5-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="12ad5-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="12ad5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="12ad5-116">Not supported.</span></span>|
|<span data-ttu-id="12ad5-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="12ad5-117">Application</span></span>|<span data-ttu-id="12ad5-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="12ad5-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="12ad5-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="12ad5-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedEBooks/{managedEBookId}/deviceStates
GET /deviceAppManagement/managedEBooks/{managedEBookId}/userStateSummary/{userInstallStateSummaryId}/deviceStates
```

## <a name="request-headers"></a><span data-ttu-id="12ad5-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="12ad5-120">Request headers</span></span>
|<span data-ttu-id="12ad5-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12ad5-121">Header</span></span>|<span data-ttu-id="12ad5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="12ad5-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="12ad5-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="12ad5-123">Authorization</span></span>|<span data-ttu-id="12ad5-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="12ad5-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="12ad5-125">Accept</span><span class="sxs-lookup"><span data-stu-id="12ad5-125">Accept</span></span>|<span data-ttu-id="12ad5-126">application/json</span><span class="sxs-lookup"><span data-stu-id="12ad5-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="12ad5-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="12ad5-127">Request body</span></span>
<span data-ttu-id="12ad5-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="12ad5-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="12ad5-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="12ad5-129">Response</span></span>
<span data-ttu-id="12ad5-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceInstallState](../resources/intune-books-deviceinstallstate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="12ad5-130">If successful, this method returns a `200 OK` response code and a collection of [deviceInstallState](../resources/intune-books-deviceinstallstate.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="12ad5-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="12ad5-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="12ad5-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="12ad5-132">Request</span></span>
<span data-ttu-id="12ad5-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="12ad5-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/managedEBooks/{managedEBookId}/deviceStates
```

### <a name="response"></a><span data-ttu-id="12ad5-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="12ad5-134">Response</span></span>
<span data-ttu-id="12ad5-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="12ad5-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 496

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceInstallState",
      "id": "b9feb68f-b68f-b9fe-8fb6-feb98fb6feb9",
      "deviceName": "Device Name value",
      "deviceId": "Device Id value",
      "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
      "installState": "installed",
      "errorCode": "Error Code value",
      "osVersion": "Os Version value",
      "osDescription": "Os Description value",
      "userName": "User Name value"
    }
  ]
}
```





