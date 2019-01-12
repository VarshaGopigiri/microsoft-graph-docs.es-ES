---
title: Obtener targetedManagedAppConfiguration
description: Lea las propiedades y las relaciones del objeto targetedManagedAppConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 4907f142cb7b4526d284952b84598206dd37550a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27951477"
---
# <a name="get-targetedmanagedappconfiguration"></a><span data-ttu-id="71b6e-103">Obtener targetedManagedAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="71b6e-103">Get targetedManagedAppConfiguration</span></span>

> <span data-ttu-id="71b6e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="71b6e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="71b6e-105">Lea las propiedades y las relaciones del objeto [targetedManagedAppConfiguration](../resources/intune-mam-targetedmanagedappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="71b6e-105">Read properties and relationships of the [targetedManagedAppConfiguration](../resources/intune-mam-targetedmanagedappconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="71b6e-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="71b6e-106">Prerequisites</span></span>
<span data-ttu-id="71b6e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="71b6e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="71b6e-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="71b6e-109">Permission type</span></span>|<span data-ttu-id="71b6e-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="71b6e-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="71b6e-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="71b6e-111">Delegated (work or school account)</span></span>|<span data-ttu-id="71b6e-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="71b6e-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="71b6e-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="71b6e-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="71b6e-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="71b6e-114">Not supported.</span></span>|
|<span data-ttu-id="71b6e-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="71b6e-115">Application</span></span>|<span data-ttu-id="71b6e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="71b6e-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="71b6e-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="71b6e-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="71b6e-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="71b6e-118">Optional query parameters</span></span>
<span data-ttu-id="71b6e-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71b6e-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="71b6e-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="71b6e-120">Request headers</span></span>
|<span data-ttu-id="71b6e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71b6e-121">Header</span></span>|<span data-ttu-id="71b6e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="71b6e-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="71b6e-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="71b6e-123">Authorization</span></span>|<span data-ttu-id="71b6e-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="71b6e-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="71b6e-125">Accept</span><span class="sxs-lookup"><span data-stu-id="71b6e-125">Accept</span></span>|<span data-ttu-id="71b6e-126">application/json</span><span class="sxs-lookup"><span data-stu-id="71b6e-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="71b6e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="71b6e-127">Request body</span></span>
<span data-ttu-id="71b6e-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="71b6e-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="71b6e-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71b6e-129">Response</span></span>
<span data-ttu-id="71b6e-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [targetedManagedAppConfiguration](../resources/intune-mam-targetedmanagedappconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71b6e-130">If successful, this method returns a `200 OK` response code and [targetedManagedAppConfiguration](../resources/intune-mam-targetedmanagedappconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="71b6e-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="71b6e-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="71b6e-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="71b6e-132">Request</span></span>
<span data-ttu-id="71b6e-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="71b6e-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}
```

### <a name="response"></a><span data-ttu-id="71b6e-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71b6e-134">Response</span></span>
<span data-ttu-id="71b6e-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="71b6e-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 611

{
  "value": {
    "@odata.type": "#microsoft.graph.targetedManagedAppConfiguration",
    "displayName": "Display Name value",
    "description": "Description value",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "id": "2444e029-e029-2444-29e0-442429e04424",
    "version": "Version value",
    "customSettings": [
      {
        "@odata.type": "microsoft.graph.keyValuePair",
        "name": "Name value",
        "value": "Value value"
      }
    ],
    "deployedAppCount": 0,
    "isAssigned": true
  }
}
```



