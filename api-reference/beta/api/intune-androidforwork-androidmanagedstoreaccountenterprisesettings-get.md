---
title: Obtener androidManagedStoreAccountEnterpriseSettings
description: Leer las propiedades y las relaciones del objeto androidManagedStoreAccountEnterpriseSettings.
author: tfitzmac
ms.openlocfilehash: 5e47c9c1456d35932fb040561c8d54cdfd78932e
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27306646"
---
# <a name="get-androidmanagedstoreaccountenterprisesettings"></a><span data-ttu-id="139c7-103">Obtener androidManagedStoreAccountEnterpriseSettings</span><span class="sxs-lookup"><span data-stu-id="139c7-103">Get androidManagedStoreAccountEnterpriseSettings</span></span>

> <span data-ttu-id="139c7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="139c7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="139c7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="139c7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="139c7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="139c7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="139c7-107">Leer las propiedades y las relaciones del objeto [androidManagedStoreAccountEnterpriseSettings](../resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings.md) .</span><span class="sxs-lookup"><span data-stu-id="139c7-107">Read properties and relationships of the [androidManagedStoreAccountEnterpriseSettings](../resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="139c7-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="139c7-108">Prerequisites</span></span>
<span data-ttu-id="139c7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="139c7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="139c7-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="139c7-111">Permission type</span></span>|<span data-ttu-id="139c7-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="139c7-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="139c7-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="139c7-113">Delegated (work or school account)</span></span>|<span data-ttu-id="139c7-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="139c7-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="139c7-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="139c7-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="139c7-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="139c7-116">Not supported.</span></span>|
|<span data-ttu-id="139c7-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="139c7-117">Application</span></span>|<span data-ttu-id="139c7-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="139c7-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="139c7-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="139c7-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/androidManagedStoreAccountEnterpriseSettings
```

## <a name="optional-query-parameters"></a><span data-ttu-id="139c7-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="139c7-120">Optional query parameters</span></span>
<span data-ttu-id="139c7-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="139c7-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="139c7-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="139c7-122">Request headers</span></span>
|<span data-ttu-id="139c7-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="139c7-123">Header</span></span>|<span data-ttu-id="139c7-124">Valor</span><span class="sxs-lookup"><span data-stu-id="139c7-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="139c7-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="139c7-125">Authorization</span></span>|<span data-ttu-id="139c7-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="139c7-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="139c7-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="139c7-127">Accept</span></span>|<span data-ttu-id="139c7-128">application/json</span><span class="sxs-lookup"><span data-stu-id="139c7-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="139c7-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="139c7-129">Request body</span></span>
<span data-ttu-id="139c7-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="139c7-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="139c7-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="139c7-131">Response</span></span>
<span data-ttu-id="139c7-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [androidManagedStoreAccountEnterpriseSettings](../resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="139c7-132">If successful, this method returns a `200 OK` response code and [androidManagedStoreAccountEnterpriseSettings](../resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="139c7-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="139c7-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="139c7-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="139c7-134">Request</span></span>
<span data-ttu-id="139c7-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="139c7-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/androidManagedStoreAccountEnterpriseSettings
```

### <a name="response"></a><span data-ttu-id="139c7-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="139c7-136">Response</span></span>
<span data-ttu-id="139c7-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="139c7-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 635

{
  "value": {
    "@odata.type": "#microsoft.graph.androidManagedStoreAccountEnterpriseSettings",
    "id": "b71357c9-57c9-b713-c957-13b7c95713b7",
    "bindStatus": "bound",
    "lastAppSyncDateTime": "2016-12-31T23:57:22.8606813-08:00",
    "lastAppSyncStatus": "credentialsNotValid",
    "ownerUserPrincipalName": "Owner User Principal Name value",
    "ownerOrganizationName": "Owner Organization Name value",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "enrollmentTarget": "all",
    "targetGroupIds": [
      "Target Group Ids value"
    ],
    "deviceOwnerManagementEnabled": true
  }
}
```





