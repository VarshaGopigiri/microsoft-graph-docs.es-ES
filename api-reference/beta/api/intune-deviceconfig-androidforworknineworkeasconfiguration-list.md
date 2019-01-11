---
title: Lista androidForWorkNineWorkEasConfigurations
description: Propiedades de la lista y relaciones de los objetos androidForWorkNineWorkEasConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 41b356e35aa9af41840361f58d3defe625dda8ec
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27878599"
---
# <a name="list-androidforworknineworkeasconfigurations"></a><span data-ttu-id="26435-103">Lista androidForWorkNineWorkEasConfigurations</span><span class="sxs-lookup"><span data-stu-id="26435-103">List androidForWorkNineWorkEasConfigurations</span></span>

> <span data-ttu-id="26435-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="26435-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="26435-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="26435-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="26435-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="26435-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="26435-107">Propiedades de la lista y relaciones de los objetos [androidForWorkNineWorkEasConfiguration](../resources/intune-deviceconfig-androidforworknineworkeasconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="26435-107">List properties and relationships of the [androidForWorkNineWorkEasConfiguration](../resources/intune-deviceconfig-androidforworknineworkeasconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="26435-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="26435-108">Prerequisites</span></span>
<span data-ttu-id="26435-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="26435-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="26435-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="26435-111">Permission type</span></span>|<span data-ttu-id="26435-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="26435-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="26435-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="26435-113">Delegated (work or school account)</span></span>|<span data-ttu-id="26435-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="26435-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="26435-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="26435-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="26435-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="26435-116">Not supported.</span></span>|
|<span data-ttu-id="26435-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="26435-117">Application</span></span>|<span data-ttu-id="26435-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="26435-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="26435-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="26435-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="26435-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="26435-120">Request headers</span></span>
|<span data-ttu-id="26435-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26435-121">Header</span></span>|<span data-ttu-id="26435-122">Valor</span><span class="sxs-lookup"><span data-stu-id="26435-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="26435-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="26435-123">Authorization</span></span>|<span data-ttu-id="26435-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="26435-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="26435-125">Accept</span><span class="sxs-lookup"><span data-stu-id="26435-125">Accept</span></span>|<span data-ttu-id="26435-126">application/json</span><span class="sxs-lookup"><span data-stu-id="26435-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="26435-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="26435-127">Request body</span></span>
<span data-ttu-id="26435-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="26435-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="26435-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="26435-129">Response</span></span>
<span data-ttu-id="26435-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [androidForWorkNineWorkEasConfiguration](../resources/intune-deviceconfig-androidforworknineworkeasconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="26435-130">If successful, this method returns a `200 OK` response code and a collection of [androidForWorkNineWorkEasConfiguration](../resources/intune-deviceconfig-androidforworknineworkeasconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="26435-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="26435-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="26435-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="26435-132">Request</span></span>
<span data-ttu-id="26435-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="26435-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="26435-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="26435-134">Response</span></span>
<span data-ttu-id="26435-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="26435-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 851

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.androidForWorkNineWorkEasConfiguration",
      "id": "f8ef19e0-19e0-f8ef-e019-eff8e019eff8",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "roleScopeTagIds": [
        "Role Scope Tag Ids value"
      ],
      "supportsScopeTags": true,
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "description": "Description value",
      "displayName": "Display Name value",
      "version": 7,
      "authenticationMethod": "certificate",
      "durationOfEmailToSync": "oneDay",
      "emailAddressSource": "primarySmtpAddress",
      "hostName": "Host Name value",
      "requireSsl": true,
      "usernameSource": "userPrincipalName",
      "syncCalendar": true,
      "syncContacts": true,
      "syncTasks": true
    }
  ]
}
```





