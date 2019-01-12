---
title: Obtener deviceManagementTroubleshootingEvent
description: Lea las propiedades y las relaciones del objeto deviceManagementTroubleshootingEvent.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 2f1a11b1c494ca5d233bcf962d053a11379edce3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27975830"
---
# <a name="get-devicemanagementtroubleshootingevent"></a><span data-ttu-id="da2bf-103">Obtener deviceManagementTroubleshootingEvent</span><span class="sxs-lookup"><span data-stu-id="da2bf-103">Get deviceManagementTroubleshootingEvent</span></span>

> <span data-ttu-id="da2bf-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="da2bf-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="da2bf-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="da2bf-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="da2bf-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="da2bf-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="da2bf-107">Lea las propiedades y las relaciones del objeto [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="da2bf-107">Read properties and relationships of the [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="da2bf-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="da2bf-108">Prerequisites</span></span>
<span data-ttu-id="da2bf-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="da2bf-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="da2bf-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="da2bf-111">Permission type</span></span>|<span data-ttu-id="da2bf-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="da2bf-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="da2bf-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="da2bf-113">Delegated (work or school account)</span></span>|<span data-ttu-id="da2bf-114">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="da2bf-114">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="da2bf-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="da2bf-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="da2bf-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="da2bf-116">Not supported.</span></span>|
|<span data-ttu-id="da2bf-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="da2bf-117">Application</span></span>|<span data-ttu-id="da2bf-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="da2bf-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="da2bf-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="da2bf-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/troubleshootingEvents/{deviceManagementTroubleshootingEventId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="da2bf-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="da2bf-120">Optional query parameters</span></span>
<span data-ttu-id="da2bf-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="da2bf-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="da2bf-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="da2bf-122">Request headers</span></span>
|<span data-ttu-id="da2bf-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="da2bf-123">Header</span></span>|<span data-ttu-id="da2bf-124">Valor</span><span class="sxs-lookup"><span data-stu-id="da2bf-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="da2bf-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="da2bf-125">Authorization</span></span>|<span data-ttu-id="da2bf-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="da2bf-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="da2bf-127">Accept</span><span class="sxs-lookup"><span data-stu-id="da2bf-127">Accept</span></span>|<span data-ttu-id="da2bf-128">application/json</span><span class="sxs-lookup"><span data-stu-id="da2bf-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="da2bf-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="da2bf-129">Request body</span></span>
<span data-ttu-id="da2bf-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="da2bf-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="da2bf-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="da2bf-131">Response</span></span>
<span data-ttu-id="da2bf-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="da2bf-132">If successful, this method returns a `200 OK` response code and [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="da2bf-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="da2bf-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="da2bf-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="da2bf-134">Request</span></span>
<span data-ttu-id="da2bf-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="da2bf-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/troubleshootingEvents/{deviceManagementTroubleshootingEventId}
```

### <a name="response"></a><span data-ttu-id="da2bf-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="da2bf-136">Response</span></span>
<span data-ttu-id="da2bf-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="da2bf-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 255

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceManagementTroubleshootingEvent",
    "id": "fb26dcee-dcee-fb26-eedc-26fbeedc26fb",
    "eventDateTime": "2016-12-31T23:59:23.3984029-08:00",
    "correlationId": "Correlation Id value"
  }
}
```





