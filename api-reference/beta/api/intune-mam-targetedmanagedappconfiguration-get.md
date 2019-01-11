---
title: Obtener targetedManagedAppConfiguration
description: Lea las propiedades y las relaciones del objeto targetedManagedAppConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: ffdd605fe531982756541e9cf8d7b0f1ef1cde2e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27862632"
---
# <a name="get-targetedmanagedappconfiguration"></a><span data-ttu-id="36221-103">Obtener targetedManagedAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="36221-103">Get targetedManagedAppConfiguration</span></span>

> <span data-ttu-id="36221-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="36221-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="36221-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="36221-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="36221-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="36221-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="36221-107">Lea las propiedades y las relaciones del objeto [targetedManagedAppConfiguration](../resources/intune-mam-targetedmanagedappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="36221-107">Read properties and relationships of the [targetedManagedAppConfiguration](../resources/intune-mam-targetedmanagedappconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="36221-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="36221-108">Prerequisites</span></span>
<span data-ttu-id="36221-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="36221-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="36221-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="36221-111">Permission type</span></span>|<span data-ttu-id="36221-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="36221-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="36221-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="36221-113">Delegated (work or school account)</span></span>|<span data-ttu-id="36221-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="36221-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="36221-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="36221-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="36221-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="36221-116">Not supported.</span></span>|
|<span data-ttu-id="36221-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="36221-117">Application</span></span>|<span data-ttu-id="36221-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="36221-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="36221-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="36221-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="36221-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="36221-120">Optional query parameters</span></span>
<span data-ttu-id="36221-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="36221-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="36221-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="36221-122">Request headers</span></span>
|<span data-ttu-id="36221-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="36221-123">Header</span></span>|<span data-ttu-id="36221-124">Valor</span><span class="sxs-lookup"><span data-stu-id="36221-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="36221-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="36221-125">Authorization</span></span>|<span data-ttu-id="36221-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="36221-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="36221-127">Accept</span><span class="sxs-lookup"><span data-stu-id="36221-127">Accept</span></span>|<span data-ttu-id="36221-128">application/json</span><span class="sxs-lookup"><span data-stu-id="36221-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="36221-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="36221-129">Request body</span></span>
<span data-ttu-id="36221-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="36221-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="36221-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="36221-131">Response</span></span>
<span data-ttu-id="36221-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [targetedManagedAppConfiguration](../resources/intune-mam-targetedmanagedappconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="36221-132">If successful, this method returns a `200 OK` response code and [targetedManagedAppConfiguration](../resources/intune-mam-targetedmanagedappconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="36221-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="36221-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="36221-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="36221-134">Request</span></span>
<span data-ttu-id="36221-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="36221-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}
```

### <a name="response"></a><span data-ttu-id="36221-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="36221-136">Response</span></span>
<span data-ttu-id="36221-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="36221-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





