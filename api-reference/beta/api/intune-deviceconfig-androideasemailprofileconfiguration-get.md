---
title: Obtener androidEasEmailProfileConfiguration
description: Leer las propiedades y las relaciones del objeto androidEasEmailProfileConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: b00a3aa67646abe9c2d8263ab1ddda088f200e9c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27879495"
---
# <a name="get-androideasemailprofileconfiguration"></a><span data-ttu-id="9b756-103">Obtener androidEasEmailProfileConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b756-103">Get androidEasEmailProfileConfiguration</span></span>

> <span data-ttu-id="9b756-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9b756-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9b756-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9b756-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="9b756-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9b756-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9b756-107">Leer las propiedades y las relaciones del objeto [androidEasEmailProfileConfiguration](../resources/intune-deviceconfig-androideasemailprofileconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="9b756-107">Read properties and relationships of the [androidEasEmailProfileConfiguration](../resources/intune-deviceconfig-androideasemailprofileconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9b756-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9b756-108">Prerequisites</span></span>
<span data-ttu-id="9b756-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9b756-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9b756-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9b756-111">Permission type</span></span>|<span data-ttu-id="9b756-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9b756-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9b756-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9b756-113">Delegated (work or school account)</span></span>|<span data-ttu-id="9b756-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="9b756-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="9b756-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9b756-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9b756-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b756-116">Not supported.</span></span>|
|<span data-ttu-id="9b756-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9b756-117">Application</span></span>|<span data-ttu-id="9b756-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b756-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9b756-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9b756-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="9b756-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="9b756-120">Optional query parameters</span></span>
<span data-ttu-id="9b756-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b756-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="9b756-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9b756-122">Request headers</span></span>
|<span data-ttu-id="9b756-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b756-123">Header</span></span>|<span data-ttu-id="9b756-124">Valor</span><span class="sxs-lookup"><span data-stu-id="9b756-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9b756-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="9b756-125">Authorization</span></span>|<span data-ttu-id="9b756-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9b756-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9b756-127">Accept</span><span class="sxs-lookup"><span data-stu-id="9b756-127">Accept</span></span>|<span data-ttu-id="9b756-128">application/json</span><span class="sxs-lookup"><span data-stu-id="9b756-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9b756-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9b756-129">Request body</span></span>
<span data-ttu-id="9b756-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9b756-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9b756-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b756-131">Response</span></span>
<span data-ttu-id="9b756-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [androidEasEmailProfileConfiguration](../resources/intune-deviceconfig-androideasemailprofileconfiguration.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b756-132">If successful, this method returns a `200 OK` response code and [androidEasEmailProfileConfiguration](../resources/intune-deviceconfig-androideasemailprofileconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9b756-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9b756-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="9b756-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9b756-134">Request</span></span>
<span data-ttu-id="9b756-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9b756-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="9b756-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b756-136">Response</span></span>
<span data-ttu-id="9b756-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9b756-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1036

{
  "value": {
    "@odata.type": "#microsoft.graph.androidEasEmailProfileConfiguration",
    "id": "ee5e5610-5610-ee5e-1056-5eee10565eee",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "roleScopeTagIds": [
      "Role Scope Tag Ids value"
    ],
    "supportsScopeTags": true,
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "displayName": "Display Name value",
    "version": 7,
    "accountName": "Account Name value",
    "authenticationMethod": "certificate",
    "syncCalendar": true,
    "syncContacts": true,
    "syncTasks": true,
    "syncNotes": true,
    "durationOfEmailToSync": "oneDay",
    "emailAddressSource": "primarySmtpAddress",
    "emailSyncSchedule": "asMessagesArrive",
    "hostName": "Host Name value",
    "requireSmime": true,
    "requireSsl": true,
    "usernameSource": "userPrincipalName",
    "userDomainNameSource": "netBiosDomainName",
    "customDomainName": "Custom Domain Name value"
  }
}
```





