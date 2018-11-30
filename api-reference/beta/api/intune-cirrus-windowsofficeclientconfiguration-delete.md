---
title: Eliminar windowsOfficeClientConfiguration
description: Eliminar una directiva de seguridad que no sean específica.
ms.openlocfilehash: a7911fd7f0f4b2079f9396d29c6a690e5caea62c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088263"
---
# <a name="delete-windowsofficeclientconfiguration"></a><span data-ttu-id="9ef91-103">Eliminar windowsOfficeClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="9ef91-103">Delete windowsOfficeClientConfiguration</span></span>

> <span data-ttu-id="9ef91-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9ef91-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9ef91-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9ef91-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="9ef91-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9ef91-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9ef91-107">Eliminar una directiva de seguridad que no sean específica.</span><span class="sxs-lookup"><span data-stu-id="9ef91-107">Delete a specific non-security policy.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9ef91-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9ef91-108">Prerequisites</span></span>
<span data-ttu-id="9ef91-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9ef91-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9ef91-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9ef91-111">Permission type</span></span>|<span data-ttu-id="9ef91-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9ef91-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9ef91-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9ef91-113">Delegated (work or school account)</span></span>|<span data-ttu-id="9ef91-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9ef91-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="9ef91-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9ef91-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9ef91-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9ef91-116">Not supported.</span></span>|
|<span data-ttu-id="9ef91-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9ef91-117">Application</span></span>|<span data-ttu-id="9ef91-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9ef91-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9ef91-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9ef91-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /officeConfiguration/clientConfigurations/{key}
```

## <a name="request-headers"></a><span data-ttu-id="9ef91-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9ef91-120">Request headers</span></span>
|<span data-ttu-id="9ef91-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9ef91-121">Header</span></span>|<span data-ttu-id="9ef91-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9ef91-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9ef91-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="9ef91-123">Authorization</span></span>|<span data-ttu-id="9ef91-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9ef91-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9ef91-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="9ef91-125">Accept</span></span>|<span data-ttu-id="9ef91-126">application/json</span><span class="sxs-lookup"><span data-stu-id="9ef91-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9ef91-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9ef91-127">Request body</span></span>
<span data-ttu-id="9ef91-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9ef91-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9ef91-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9ef91-129">Response</span></span>
<span data-ttu-id="9ef91-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="9ef91-130">If successful, this method returns a `200 OK` response code.</span></span>

## <a name="example"></a><span data-ttu-id="9ef91-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9ef91-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="9ef91-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9ef91-132">Request</span></span>
<span data-ttu-id="9ef91-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9ef91-133">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/beta/officeConfiguration/clientConfigurations/{key}
```

### <a name="response"></a><span data-ttu-id="9ef91-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9ef91-134">Response</span></span>
<span data-ttu-id="9ef91-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9ef91-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
```



