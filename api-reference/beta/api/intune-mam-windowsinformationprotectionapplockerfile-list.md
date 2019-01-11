---
title: Enumerar windowsInformationProtectionAppLockerFiles
description: Enumere las propiedades y las relaciones de los objetos windowsInformationProtectionAppLockerFile.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: af1c2d9346abc12ab8909aceb199eab60d87432a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27822928"
---
# <a name="list-windowsinformationprotectionapplockerfiles"></a><span data-ttu-id="7b774-103">Enumerar windowsInformationProtectionAppLockerFiles</span><span class="sxs-lookup"><span data-stu-id="7b774-103">List windowsInformationProtectionAppLockerFiles</span></span>

> <span data-ttu-id="7b774-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7b774-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7b774-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7b774-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7b774-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7b774-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7b774-107">Enumere las propiedades y las relaciones de los objetos [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md).</span><span class="sxs-lookup"><span data-stu-id="7b774-107">List properties and relationships of the [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7b774-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7b774-108">Prerequisites</span></span>
<span data-ttu-id="7b774-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7b774-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7b774-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7b774-111">Permission type</span></span>|<span data-ttu-id="7b774-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7b774-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7b774-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7b774-113">Delegated (work or school account)</span></span>|<span data-ttu-id="7b774-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="7b774-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="7b774-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7b774-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7b774-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7b774-116">Not supported.</span></span>|
|<span data-ttu-id="7b774-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7b774-117">Application</span></span>|<span data-ttu-id="7b774-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7b774-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7b774-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7b774-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/windowsInformationProtectionPolicies/{windowsInformationProtectionPolicyId}/exemptAppLockerFiles
GET /deviceAppManagement/windowsInformationProtectionPolicies/{windowsInformationProtectionPolicyId}/protectedAppLockerFiles
GET /deviceAppManagement/mdmWindowsInformationProtectionPolicies/{mdmWindowsInformationProtectionPolicyId}/exemptAppLockerFiles
GET /deviceAppManagement/mdmWindowsInformationProtectionPolicies/{mdmWindowsInformationProtectionPolicyId}/protectedAppLockerFiles
```

## <a name="request-headers"></a><span data-ttu-id="7b774-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7b774-120">Request headers</span></span>
|<span data-ttu-id="7b774-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7b774-121">Header</span></span>|<span data-ttu-id="7b774-122">Valor</span><span class="sxs-lookup"><span data-stu-id="7b774-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7b774-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="7b774-123">Authorization</span></span>|<span data-ttu-id="7b774-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7b774-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7b774-125">Accept</span><span class="sxs-lookup"><span data-stu-id="7b774-125">Accept</span></span>|<span data-ttu-id="7b774-126">application/json</span><span class="sxs-lookup"><span data-stu-id="7b774-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7b774-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7b774-127">Request body</span></span>
<span data-ttu-id="7b774-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7b774-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7b774-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7b774-129">Response</span></span>
<span data-ttu-id="7b774-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7b774-130">If successful, this method returns a `200 OK` response code and a collection of [windowsInformationProtectionAppLockerFile](../resources/intune-mam-windowsinformationprotectionapplockerfile.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7b774-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7b774-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="7b774-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7b774-132">Request</span></span>
<span data-ttu-id="7b774-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7b774-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/windowsInformationProtectionPolicies/{windowsInformationProtectionPolicyId}/exemptAppLockerFiles
```

### <a name="response"></a><span data-ttu-id="7b774-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7b774-134">Response</span></span>
<span data-ttu-id="7b774-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7b774-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 317

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windowsInformationProtectionAppLockerFile",
      "displayName": "Display Name value",
      "fileHash": "File Hash value",
      "file": "ZmlsZQ==",
      "id": "d81f0e40-0e40-d81f-400e-1fd8400e1fd8",
      "version": "Version value"
    }
  ]
}
```





