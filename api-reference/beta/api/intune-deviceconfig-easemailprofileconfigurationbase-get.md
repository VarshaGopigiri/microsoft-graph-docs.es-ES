---
title: Obtener easEmailProfileConfigurationBase
description: Leer las propiedades y las relaciones del objeto easEmailProfileConfigurationBase.
ms.openlocfilehash: 53a31647634a6c3e3393d6613d198419a973f715
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089940"
---
# <a name="get-easemailprofileconfigurationbase"></a><span data-ttu-id="c88e4-103">Obtener easEmailProfileConfigurationBase</span><span class="sxs-lookup"><span data-stu-id="c88e4-103">Get easEmailProfileConfigurationBase</span></span>

> <span data-ttu-id="c88e4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c88e4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c88e4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c88e4-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c88e4-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c88e4-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c88e4-107">Leer las propiedades y las relaciones del objeto [easEmailProfileConfigurationBase](../resources/intune-deviceconfig-easemailprofileconfigurationbase.md) .</span><span class="sxs-lookup"><span data-stu-id="c88e4-107">Read properties and relationships of the [easEmailProfileConfigurationBase](../resources/intune-deviceconfig-easemailprofileconfigurationbase.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c88e4-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c88e4-108">Prerequisites</span></span>
<span data-ttu-id="c88e4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c88e4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c88e4-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c88e4-111">Permission type</span></span>|<span data-ttu-id="c88e4-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c88e4-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c88e4-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c88e4-113">Delegated (work or school account)</span></span>|<span data-ttu-id="c88e4-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="c88e4-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="c88e4-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c88e4-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c88e4-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c88e4-116">Not supported.</span></span>|
|<span data-ttu-id="c88e4-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c88e4-117">Application</span></span>|<span data-ttu-id="c88e4-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c88e4-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c88e4-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c88e4-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="c88e4-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c88e4-120">Optional query parameters</span></span>
<span data-ttu-id="c88e4-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c88e4-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="c88e4-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c88e4-122">Request headers</span></span>
|<span data-ttu-id="c88e4-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c88e4-123">Header</span></span>|<span data-ttu-id="c88e4-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c88e4-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c88e4-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="c88e4-125">Authorization</span></span>|<span data-ttu-id="c88e4-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c88e4-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c88e4-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c88e4-127">Accept</span></span>|<span data-ttu-id="c88e4-128">application/json</span><span class="sxs-lookup"><span data-stu-id="c88e4-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c88e4-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c88e4-129">Request body</span></span>
<span data-ttu-id="c88e4-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c88e4-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c88e4-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c88e4-131">Response</span></span>
<span data-ttu-id="c88e4-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [easEmailProfileConfigurationBase](../resources/intune-deviceconfig-easemailprofileconfigurationbase.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c88e4-132">If successful, this method returns a `200 OK` response code and [easEmailProfileConfigurationBase](../resources/intune-deviceconfig-easemailprofileconfigurationbase.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c88e4-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c88e4-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="c88e4-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c88e4-134">Request</span></span>
<span data-ttu-id="c88e4-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c88e4-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="c88e4-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c88e4-136">Response</span></span>
<span data-ttu-id="c88e4-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c88e4-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 671

{
  "value": {
    "@odata.type": "#microsoft.graph.easEmailProfileConfigurationBase",
    "id": "a3f96310-6310-a3f9-1063-f9a31063f9a3",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "roleScopeTagIds": [
      "Role Scope Tag Ids value"
    ],
    "supportsScopeTags": true,
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "displayName": "Display Name value",
    "version": 7,
    "usernameSource": "primarySmtpAddress",
    "usernameAADSource": "primarySmtpAddress",
    "userDomainNameSource": "netBiosDomainName",
    "customDomainName": "Custom Domain Name value"
  }
}
```




