---
title: Enumerar managedAppConfigurations
description: Enumere las propiedades y las relaciones de los objetos managedAppConfiguration.
author: tfitzmac
ms.openlocfilehash: 1cb84794d52f202fae1abac40f4aa74dbdf65ae1
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27332154"
---
# <a name="list-managedappconfigurations"></a><span data-ttu-id="6dab1-103">Enumerar managedAppConfigurations</span><span class="sxs-lookup"><span data-stu-id="6dab1-103">List managedAppConfigurations</span></span>

> <span data-ttu-id="6dab1-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6dab1-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6dab1-105">Enumere las propiedades y las relaciones de los objetos [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="6dab1-105">List properties and relationships of the [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6dab1-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6dab1-106">Prerequisites</span></span>
<span data-ttu-id="6dab1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6dab1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6dab1-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6dab1-109">Permission type</span></span>|<span data-ttu-id="6dab1-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6dab1-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6dab1-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6dab1-111">Delegated (work or school account)</span></span>|<span data-ttu-id="6dab1-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="6dab1-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="6dab1-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6dab1-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6dab1-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6dab1-114">Not supported.</span></span>|
|<span data-ttu-id="6dab1-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6dab1-115">Application</span></span>|<span data-ttu-id="6dab1-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6dab1-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6dab1-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6dab1-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedAppPolicies
GET /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/appliedPolicies
GET /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/intendedPolicies
```

## <a name="request-headers"></a><span data-ttu-id="6dab1-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6dab1-118">Request headers</span></span>
|<span data-ttu-id="6dab1-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6dab1-119">Header</span></span>|<span data-ttu-id="6dab1-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6dab1-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6dab1-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="6dab1-121">Authorization</span></span>|<span data-ttu-id="6dab1-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6dab1-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6dab1-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6dab1-123">Accept</span></span>|<span data-ttu-id="6dab1-124">application/json</span><span class="sxs-lookup"><span data-stu-id="6dab1-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6dab1-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6dab1-125">Request body</span></span>
<span data-ttu-id="6dab1-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6dab1-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6dab1-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6dab1-127">Response</span></span>
<span data-ttu-id="6dab1-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6dab1-128">If successful, this method returns a `200 OK` response code and a collection of [managedAppConfiguration](../resources/intune-mam-managedappconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6dab1-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6dab1-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="6dab1-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6dab1-130">Request</span></span>
<span data-ttu-id="6dab1-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6dab1-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppPolicies
```

### <a name="response"></a><span data-ttu-id="6dab1-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6dab1-132">Response</span></span>
<span data-ttu-id="6dab1-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6dab1-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 592

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.managedAppConfiguration",
      "displayName": "Display Name value",
      "description": "Description value",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "id": "2ed27cb5-7cb5-2ed2-b57c-d22eb57cd22e",
      "version": "Version value",
      "customSettings": [
        {
          "@odata.type": "microsoft.graph.keyValuePair",
          "name": "Name value",
          "value": "Value value"
        }
      ]
    }
  ]
}
```



