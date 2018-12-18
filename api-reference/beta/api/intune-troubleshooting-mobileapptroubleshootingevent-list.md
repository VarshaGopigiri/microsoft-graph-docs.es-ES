---
title: Lista mobileAppTroubleshootingEvents
description: Propiedades de la lista y relaciones de los objetos mobileAppTroubleshootingEvent.
author: tfitzmac
ms.openlocfilehash: cee6872731977fedddced00f3bad678d3b3e42da
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27308676"
---
# <a name="list-mobileapptroubleshootingevents"></a><span data-ttu-id="f9ab5-103">Lista mobileAppTroubleshootingEvents</span><span class="sxs-lookup"><span data-stu-id="f9ab5-103">List mobileAppTroubleshootingEvents</span></span>

> <span data-ttu-id="f9ab5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f9ab5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f9ab5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f9ab5-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f9ab5-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f9ab5-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f9ab5-107">Propiedades de la lista y relaciones de los objetos [mobileAppTroubleshootingEvent](../resources/intune-troubleshooting-mobileapptroubleshootingevent.md) .</span><span class="sxs-lookup"><span data-stu-id="f9ab5-107">List properties and relationships of the [mobileAppTroubleshootingEvent](../resources/intune-troubleshooting-mobileapptroubleshootingevent.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f9ab5-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f9ab5-108">Prerequisites</span></span>
<span data-ttu-id="f9ab5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f9ab5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f9ab5-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f9ab5-111">Permission type</span></span>|<span data-ttu-id="f9ab5-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f9ab5-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f9ab5-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f9ab5-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f9ab5-114">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="f9ab5-114">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="f9ab5-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f9ab5-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f9ab5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f9ab5-116">Not supported.</span></span>|
|<span data-ttu-id="f9ab5-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f9ab5-117">Application</span></span>|<span data-ttu-id="f9ab5-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f9ab5-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f9ab5-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f9ab5-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /users/{usersId}/mobileAppTroubleshootingEvents
```

## <a name="request-headers"></a><span data-ttu-id="f9ab5-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f9ab5-120">Request headers</span></span>
|<span data-ttu-id="f9ab5-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9ab5-121">Header</span></span>|<span data-ttu-id="f9ab5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f9ab5-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f9ab5-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="f9ab5-123">Authorization</span></span>|<span data-ttu-id="f9ab5-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f9ab5-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f9ab5-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f9ab5-125">Accept</span></span>|<span data-ttu-id="f9ab5-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f9ab5-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f9ab5-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f9ab5-127">Request body</span></span>
<span data-ttu-id="f9ab5-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f9ab5-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f9ab5-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9ab5-129">Response</span></span>
<span data-ttu-id="f9ab5-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [mobileAppTroubleshootingEvent](../resources/intune-troubleshooting-mobileapptroubleshootingevent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f9ab5-130">If successful, this method returns a `200 OK` response code and a collection of [mobileAppTroubleshootingEvent](../resources/intune-troubleshooting-mobileapptroubleshootingevent.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f9ab5-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f9ab5-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="f9ab5-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f9ab5-132">Request</span></span>
<span data-ttu-id="f9ab5-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f9ab5-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/users/{usersId}/mobileAppTroubleshootingEvents
```

### <a name="response"></a><span data-ttu-id="f9ab5-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9ab5-134">Response</span></span>
<span data-ttu-id="f9ab5-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f9ab5-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 623

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.mobileAppTroubleshootingEvent",
      "id": "77943c10-3c10-7794-103c-9477103c9477",
      "eventDateTime": "2016-12-31T23:59:23.3984029-08:00",
      "correlationId": "Correlation Id value",
      "managedDeviceIdentifier": "Managed Device Identifier value",
      "userId": "User Id value",
      "applicationId": "Application Id value",
      "history": [
        {
          "@odata.type": "microsoft.graph.mobileAppTroubleshootingHistoryItem",
          "occurrenceDateTime": "2017-01-01T00:03:20.8380798-08:00"
        }
      ]
    }
  ]
}
```





