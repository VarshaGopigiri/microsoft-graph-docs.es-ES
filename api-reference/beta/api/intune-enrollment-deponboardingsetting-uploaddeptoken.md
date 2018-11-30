---
title: acción uploadDepToken
description: Carga un nuevo token de programa de inscripción de dispositivo
ms.openlocfilehash: 0230717d84e5d73834f8ce82a73e076f1b2e7142
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087494"
---
# <a name="uploaddeptoken-action"></a><span data-ttu-id="fdca4-103">acción uploadDepToken</span><span class="sxs-lookup"><span data-stu-id="fdca4-103">uploadDepToken action</span></span>

> <span data-ttu-id="fdca4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fdca4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fdca4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fdca4-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="fdca4-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fdca4-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fdca4-107">Carga un nuevo token de programa de inscripción de dispositivo</span><span class="sxs-lookup"><span data-stu-id="fdca4-107">Uploads a new Device Enrollment Program token</span></span>
## <a name="prerequisites"></a><span data-ttu-id="fdca4-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fdca4-108">Prerequisites</span></span>
<span data-ttu-id="fdca4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fdca4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fdca4-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fdca4-111">Permission type</span></span>|<span data-ttu-id="fdca4-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fdca4-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="fdca4-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fdca4-113">Delegated (work or school account)</span></span>|<span data-ttu-id="fdca4-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fdca4-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="fdca4-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fdca4-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="fdca4-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fdca4-116">Not supported.</span></span>|
|<span data-ttu-id="fdca4-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fdca4-117">Application</span></span>|<span data-ttu-id="fdca4-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fdca4-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="fdca4-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fdca4-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/uploadDepToken
```

## <a name="request-headers"></a><span data-ttu-id="fdca4-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fdca4-120">Request headers</span></span>
|<span data-ttu-id="fdca4-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fdca4-121">Header</span></span>|<span data-ttu-id="fdca4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="fdca4-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="fdca4-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="fdca4-123">Authorization</span></span>|<span data-ttu-id="fdca4-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="fdca4-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="fdca4-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="fdca4-125">Accept</span></span>|<span data-ttu-id="fdca4-126">application/json</span><span class="sxs-lookup"><span data-stu-id="fdca4-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="fdca4-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fdca4-127">Request body</span></span>
<span data-ttu-id="fdca4-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="fdca4-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="fdca4-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="fdca4-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="fdca4-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fdca4-130">Property</span></span>|<span data-ttu-id="fdca4-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="fdca4-131">Type</span></span>|<span data-ttu-id="fdca4-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="fdca4-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fdca4-133">Id. de Apple</span><span class="sxs-lookup"><span data-stu-id="fdca4-133">appleId</span></span>|<span data-ttu-id="fdca4-134">String</span><span class="sxs-lookup"><span data-stu-id="fdca4-134">String</span></span>|<span data-ttu-id="fdca4-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="fdca4-135">Not yet documented</span></span>|
|<span data-ttu-id="fdca4-136">depToken</span><span class="sxs-lookup"><span data-stu-id="fdca4-136">depToken</span></span>|<span data-ttu-id="fdca4-137">String</span><span class="sxs-lookup"><span data-stu-id="fdca4-137">String</span></span>|<span data-ttu-id="fdca4-138">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="fdca4-138">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="fdca4-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fdca4-139">Response</span></span>
<span data-ttu-id="fdca4-140">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="fdca4-140">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="fdca4-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fdca4-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="fdca4-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fdca4-142">Request</span></span>
<span data-ttu-id="fdca4-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fdca4-143">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/uploadDepToken

Content-type: application/json
Content-length: 69

{
  "appleId": "Apple Id value",
  "depToken": "Dep Token value"
}
```

### <a name="response"></a><span data-ttu-id="fdca4-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fdca4-144">Response</span></span>
<span data-ttu-id="fdca4-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fdca4-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```





