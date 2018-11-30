---
title: Obtener targetedManagedAppConfiguration
description: Lea las propiedades y las relaciones del objeto targetedManagedAppConfiguration.
ms.openlocfilehash: 5150fe9e4198f46a89a1fcf6ea9cc01da1ec3e80
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032295"
---
# <a name="get-targetedmanagedappconfiguration"></a><span data-ttu-id="74228-103">Obtener targetedManagedAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="74228-103">Get targetedManagedAppConfiguration</span></span>

> <span data-ttu-id="74228-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="74228-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="74228-105">Lea las propiedades y las relaciones del objeto [targetedManagedAppConfiguration](../resources/intune-mam-targetedmanagedappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="74228-105">Read properties and relationships of the [targetedManagedAppConfiguration](../resources/intune-mam-targetedmanagedappconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="74228-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="74228-106">Prerequisites</span></span>
<span data-ttu-id="74228-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="74228-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="74228-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="74228-109">Permission type</span></span>|<span data-ttu-id="74228-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="74228-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="74228-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="74228-111">Delegated (work or school account)</span></span>|<span data-ttu-id="74228-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="74228-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="74228-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="74228-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="74228-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="74228-114">Not supported.</span></span>|
|<span data-ttu-id="74228-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="74228-115">Application</span></span>|<span data-ttu-id="74228-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="74228-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="74228-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="74228-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="74228-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="74228-118">Optional query parameters</span></span>
<span data-ttu-id="74228-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="74228-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="74228-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="74228-120">Request headers</span></span>
|<span data-ttu-id="74228-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74228-121">Header</span></span>|<span data-ttu-id="74228-122">Valor</span><span class="sxs-lookup"><span data-stu-id="74228-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="74228-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="74228-123">Authorization</span></span>|<span data-ttu-id="74228-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="74228-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="74228-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="74228-125">Accept</span></span>|<span data-ttu-id="74228-126">application/json</span><span class="sxs-lookup"><span data-stu-id="74228-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="74228-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="74228-127">Request body</span></span>
<span data-ttu-id="74228-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="74228-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="74228-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="74228-129">Response</span></span>
<span data-ttu-id="74228-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [targetedManagedAppConfiguration](../resources/intune-mam-targetedmanagedappconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="74228-130">If successful, this method returns a `200 OK` response code and [targetedManagedAppConfiguration](../resources/intune-mam-targetedmanagedappconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="74228-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="74228-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="74228-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="74228-132">Request</span></span>
<span data-ttu-id="74228-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="74228-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}
```

### <a name="response"></a><span data-ttu-id="74228-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="74228-134">Response</span></span>
<span data-ttu-id="74228-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="74228-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



