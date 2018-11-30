---
title: Eliminar managedDeviceMobileAppConfigurationUserStatus
description: Elimina un managedDeviceMobileAppConfigurationUserStatus
ms.openlocfilehash: 01bb4c6519efcc3cfaf05210d508fcdf2623e9a5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029995"
---
# <a name="delete-manageddevicemobileappconfigurationuserstatus"></a><span data-ttu-id="dc407-103">Eliminar managedDeviceMobileAppConfigurationUserStatus</span><span class="sxs-lookup"><span data-stu-id="dc407-103">Delete managedDeviceMobileAppConfigurationUserStatus</span></span>

> <span data-ttu-id="dc407-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="dc407-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="dc407-105">Elimina un [managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md)</span><span class="sxs-lookup"><span data-stu-id="dc407-105">Deletes a [managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="dc407-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="dc407-106">Prerequisites</span></span>
<span data-ttu-id="dc407-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dc407-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dc407-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dc407-109">Permission type</span></span>|<span data-ttu-id="dc407-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dc407-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="dc407-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dc407-111">Delegated (work or school account)</span></span>|<span data-ttu-id="dc407-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="dc407-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="dc407-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dc407-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="dc407-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dc407-114">Not supported.</span></span>|
|<span data-ttu-id="dc407-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dc407-115">Application</span></span>|<span data-ttu-id="dc407-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dc407-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="dc407-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dc407-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/userStatuses/{managedDeviceMobileAppConfigurationUserStatusId}
```

## <a name="request-headers"></a><span data-ttu-id="dc407-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dc407-118">Request headers</span></span>
|<span data-ttu-id="dc407-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dc407-119">Header</span></span>|<span data-ttu-id="dc407-120">Valor</span><span class="sxs-lookup"><span data-stu-id="dc407-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="dc407-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="dc407-121">Authorization</span></span>|<span data-ttu-id="dc407-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="dc407-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="dc407-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="dc407-123">Accept</span></span>|<span data-ttu-id="dc407-124">application/json</span><span class="sxs-lookup"><span data-stu-id="dc407-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="dc407-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dc407-125">Request body</span></span>
<span data-ttu-id="dc407-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="dc407-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="dc407-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dc407-127">Response</span></span>
<span data-ttu-id="dc407-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="dc407-128">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="dc407-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dc407-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="dc407-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dc407-130">Request</span></span>
<span data-ttu-id="dc407-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dc407-131">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/v1.0/deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/userStatuses/{managedDeviceMobileAppConfigurationUserStatusId}
```

### <a name="response"></a><span data-ttu-id="dc407-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dc407-132">Response</span></span>
<span data-ttu-id="dc407-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dc407-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



