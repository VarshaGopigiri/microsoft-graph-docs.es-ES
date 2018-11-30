---
title: Obtener mobileAppIntentAndState
description: Leer las propiedades y las relaciones del objeto mobileAppIntentAndState.
ms.openlocfilehash: 837165f713aea00061b721a41003adc479a46b4d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085704"
---
# <a name="get-mobileappintentandstate"></a><span data-ttu-id="18fce-103">Obtener mobileAppIntentAndState</span><span class="sxs-lookup"><span data-stu-id="18fce-103">Get mobileAppIntentAndState</span></span>

> <span data-ttu-id="18fce-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="18fce-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="18fce-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="18fce-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="18fce-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="18fce-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="18fce-107">Leer las propiedades y las relaciones del objeto [mobileAppIntentAndState](../resources/intune-troubleshooting-mobileappintentandstate.md) .</span><span class="sxs-lookup"><span data-stu-id="18fce-107">Read properties and relationships of the [mobileAppIntentAndState](../resources/intune-troubleshooting-mobileappintentandstate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="18fce-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="18fce-108">Prerequisites</span></span>
<span data-ttu-id="18fce-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="18fce-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="18fce-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="18fce-111">Permission type</span></span>|<span data-ttu-id="18fce-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="18fce-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="18fce-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="18fce-113">Delegated (work or school account)</span></span>|<span data-ttu-id="18fce-114">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="18fce-114">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="18fce-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="18fce-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="18fce-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="18fce-116">Not supported.</span></span>|
|<span data-ttu-id="18fce-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="18fce-117">Application</span></span>|<span data-ttu-id="18fce-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="18fce-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="18fce-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="18fce-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /users/{usersId}/mobileAppIntentAndStates/{mobileAppIntentAndStateId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="18fce-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="18fce-120">Optional query parameters</span></span>
<span data-ttu-id="18fce-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="18fce-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="18fce-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="18fce-122">Request headers</span></span>
|<span data-ttu-id="18fce-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="18fce-123">Header</span></span>|<span data-ttu-id="18fce-124">Valor</span><span class="sxs-lookup"><span data-stu-id="18fce-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="18fce-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="18fce-125">Authorization</span></span>|<span data-ttu-id="18fce-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="18fce-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="18fce-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="18fce-127">Accept</span></span>|<span data-ttu-id="18fce-128">application/json</span><span class="sxs-lookup"><span data-stu-id="18fce-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="18fce-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="18fce-129">Request body</span></span>
<span data-ttu-id="18fce-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="18fce-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="18fce-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="18fce-131">Response</span></span>
<span data-ttu-id="18fce-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [mobileAppIntentAndState](../resources/intune-troubleshooting-mobileappintentandstate.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="18fce-132">If successful, this method returns a `200 OK` response code and [mobileAppIntentAndState](../resources/intune-troubleshooting-mobileappintentandstate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="18fce-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="18fce-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="18fce-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="18fce-134">Request</span></span>
<span data-ttu-id="18fce-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="18fce-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/users/{usersId}/mobileAppIntentAndStates/{mobileAppIntentAndStateId}
```

### <a name="response"></a><span data-ttu-id="18fce-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="18fce-136">Response</span></span>
<span data-ttu-id="18fce-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="18fce-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 943

{
  "value": {
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
}
```





