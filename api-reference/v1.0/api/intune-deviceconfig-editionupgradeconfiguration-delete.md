---
title: Eliminar editionUpgradeConfiguration
description: Elimina un editionUpgradeConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 5cb91c0fe87f79ef814d0bd047964134da3c5a29
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805330"
---
# <a name="delete-editionupgradeconfiguration"></a><span data-ttu-id="d09f5-103">Eliminar editionUpgradeConfiguration</span><span class="sxs-lookup"><span data-stu-id="d09f5-103">Delete editionUpgradeConfiguration</span></span>

> <span data-ttu-id="d09f5-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d09f5-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d09f5-105">Elimina un [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="d09f5-105">Deletes a [editionUpgradeConfiguration](../resources/intune-deviceconfig-editionupgradeconfiguration.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d09f5-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d09f5-106">Prerequisites</span></span>
<span data-ttu-id="d09f5-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d09f5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d09f5-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d09f5-109">Permission type</span></span>|<span data-ttu-id="d09f5-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d09f5-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d09f5-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d09f5-111">Delegated (work or school account)</span></span>|<span data-ttu-id="d09f5-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d09f5-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="d09f5-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d09f5-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d09f5-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d09f5-114">Not supported.</span></span>|
|<span data-ttu-id="d09f5-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d09f5-115">Application</span></span>|<span data-ttu-id="d09f5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d09f5-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d09f5-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d09f5-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="d09f5-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d09f5-118">Request headers</span></span>
|<span data-ttu-id="d09f5-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d09f5-119">Header</span></span>|<span data-ttu-id="d09f5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d09f5-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d09f5-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="d09f5-121">Authorization</span></span>|<span data-ttu-id="d09f5-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d09f5-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d09f5-123">Accept</span><span class="sxs-lookup"><span data-stu-id="d09f5-123">Accept</span></span>|<span data-ttu-id="d09f5-124">application/json</span><span class="sxs-lookup"><span data-stu-id="d09f5-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d09f5-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d09f5-125">Request body</span></span>
<span data-ttu-id="d09f5-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d09f5-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d09f5-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d09f5-127">Response</span></span>
<span data-ttu-id="d09f5-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="d09f5-128">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="d09f5-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d09f5-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="d09f5-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d09f5-130">Request</span></span>
<span data-ttu-id="d09f5-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d09f5-131">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="d09f5-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d09f5-132">Response</span></span>
<span data-ttu-id="d09f5-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d09f5-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



