---
title: Obtener androidWorkProfileEasEmailProfileBase
description: Leer las propiedades y las relaciones del objeto androidWorkProfileEasEmailProfileBase.
ms.openlocfilehash: b0a0bd924bfc65267f9808c2e072693d7ea83879
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086942"
---
# <a name="get-androidworkprofileeasemailprofilebase"></a><span data-ttu-id="02c88-103">Obtener androidWorkProfileEasEmailProfileBase</span><span class="sxs-lookup"><span data-stu-id="02c88-103">Get androidWorkProfileEasEmailProfileBase</span></span>

> <span data-ttu-id="02c88-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="02c88-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="02c88-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="02c88-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="02c88-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="02c88-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="02c88-107">Leer las propiedades y las relaciones del objeto [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md) .</span><span class="sxs-lookup"><span data-stu-id="02c88-107">Read properties and relationships of the [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="02c88-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="02c88-108">Prerequisites</span></span>
<span data-ttu-id="02c88-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="02c88-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="02c88-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="02c88-111">Permission type</span></span>|<span data-ttu-id="02c88-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="02c88-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="02c88-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="02c88-113">Delegated (work or school account)</span></span>|<span data-ttu-id="02c88-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="02c88-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="02c88-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="02c88-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="02c88-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="02c88-116">Not supported.</span></span>|
|<span data-ttu-id="02c88-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="02c88-117">Application</span></span>|<span data-ttu-id="02c88-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="02c88-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="02c88-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="02c88-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="02c88-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="02c88-120">Optional query parameters</span></span>
<span data-ttu-id="02c88-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="02c88-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="02c88-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="02c88-122">Request headers</span></span>
|<span data-ttu-id="02c88-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="02c88-123">Header</span></span>|<span data-ttu-id="02c88-124">Valor</span><span class="sxs-lookup"><span data-stu-id="02c88-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="02c88-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="02c88-125">Authorization</span></span>|<span data-ttu-id="02c88-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="02c88-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="02c88-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="02c88-127">Accept</span></span>|<span data-ttu-id="02c88-128">application/json</span><span class="sxs-lookup"><span data-stu-id="02c88-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="02c88-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="02c88-129">Request body</span></span>
<span data-ttu-id="02c88-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="02c88-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="02c88-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="02c88-131">Response</span></span>
<span data-ttu-id="02c88-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="02c88-132">If successful, this method returns a `200 OK` response code and [androidWorkProfileEasEmailProfileBase](../resources/intune-deviceconfig-androidworkprofileeasemailprofilebase.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="02c88-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="02c88-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="02c88-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="02c88-134">Request</span></span>
<span data-ttu-id="02c88-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="02c88-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="02c88-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="02c88-136">Response</span></span>
<span data-ttu-id="02c88-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="02c88-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 718

{
  "value": {
    "@odata.type": "#microsoft.graph.androidWorkProfileEasEmailProfileBase",
    "id": "5d74f295-f295-5d74-95f2-745d95f2745d",
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
    "usernameSource": "userPrincipalName"
  }
}
```





