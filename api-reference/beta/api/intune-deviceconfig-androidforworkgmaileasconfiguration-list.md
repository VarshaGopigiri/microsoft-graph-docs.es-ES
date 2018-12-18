---
title: Lista androidForWorkGmailEasConfigurations
description: Propiedades de la lista y relaciones de los objetos androidForWorkGmailEasConfiguration.
author: tfitzmac
ms.openlocfilehash: b227f09b13b8522d6e78cbee1f26743b9f82bc2a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27308081"
---
# <a name="list-androidforworkgmaileasconfigurations"></a><span data-ttu-id="3281d-103">Lista androidForWorkGmailEasConfigurations</span><span class="sxs-lookup"><span data-stu-id="3281d-103">List androidForWorkGmailEasConfigurations</span></span>

> <span data-ttu-id="3281d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3281d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3281d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3281d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="3281d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3281d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3281d-107">Propiedades de la lista y relaciones de los objetos [androidForWorkGmailEasConfiguration](../resources/intune-deviceconfig-androidforworkgmaileasconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="3281d-107">List properties and relationships of the [androidForWorkGmailEasConfiguration](../resources/intune-deviceconfig-androidforworkgmaileasconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3281d-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3281d-108">Prerequisites</span></span>
<span data-ttu-id="3281d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3281d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3281d-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3281d-111">Permission type</span></span>|<span data-ttu-id="3281d-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3281d-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3281d-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3281d-113">Delegated (work or school account)</span></span>|<span data-ttu-id="3281d-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="3281d-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="3281d-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3281d-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3281d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3281d-116">Not supported.</span></span>|
|<span data-ttu-id="3281d-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3281d-117">Application</span></span>|<span data-ttu-id="3281d-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3281d-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3281d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3281d-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="3281d-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3281d-120">Request headers</span></span>
|<span data-ttu-id="3281d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3281d-121">Header</span></span>|<span data-ttu-id="3281d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3281d-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3281d-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="3281d-123">Authorization</span></span>|<span data-ttu-id="3281d-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3281d-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3281d-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="3281d-125">Accept</span></span>|<span data-ttu-id="3281d-126">application/json</span><span class="sxs-lookup"><span data-stu-id="3281d-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3281d-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3281d-127">Request body</span></span>
<span data-ttu-id="3281d-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3281d-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3281d-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3281d-129">Response</span></span>
<span data-ttu-id="3281d-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [androidForWorkGmailEasConfiguration](../resources/intune-deviceconfig-androidforworkgmaileasconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3281d-130">If successful, this method returns a `200 OK` response code and a collection of [androidForWorkGmailEasConfiguration](../resources/intune-deviceconfig-androidforworkgmaileasconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3281d-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3281d-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="3281d-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3281d-132">Request</span></span>
<span data-ttu-id="3281d-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3281d-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="3281d-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3281d-134">Response</span></span>
<span data-ttu-id="3281d-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3281d-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 764

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.androidForWorkGmailEasConfiguration",
      "id": "2bafc891-c891-2baf-91c8-af2b91c8af2b",
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
  ]
}
```





