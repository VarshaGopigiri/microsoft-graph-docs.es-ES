---
title: acción createGooglePlayWebToken
description: Genera un token de web que se usa en un componente puede incrustar.
ms.openlocfilehash: 26b58e5973063a74cac69d0bb70aa02adde7093f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088417"
---
# <a name="creategoogleplaywebtoken-action"></a><span data-ttu-id="6e943-103">acción createGooglePlayWebToken</span><span class="sxs-lookup"><span data-stu-id="6e943-103">createGooglePlayWebToken action</span></span>

> <span data-ttu-id="6e943-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6e943-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6e943-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6e943-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6e943-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6e943-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6e943-107">Genera un token de web que se usa en un componente puede incrustar.</span><span class="sxs-lookup"><span data-stu-id="6e943-107">Generates a web token that is used in an embeddable component.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6e943-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6e943-108">Prerequisites</span></span>
<span data-ttu-id="6e943-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6e943-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6e943-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6e943-111">Permission type</span></span>|<span data-ttu-id="6e943-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6e943-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6e943-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6e943-113">Delegated (work or school account)</span></span>|<span data-ttu-id="6e943-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6e943-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="6e943-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6e943-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6e943-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6e943-116">Not supported.</span></span>|
|<span data-ttu-id="6e943-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6e943-117">Application</span></span>|<span data-ttu-id="6e943-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6e943-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6e943-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6e943-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/androidManagedStoreAccountEnterpriseSettings/createGooglePlayWebToken
```

## <a name="request-headers"></a><span data-ttu-id="6e943-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6e943-120">Request headers</span></span>
|<span data-ttu-id="6e943-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e943-121">Header</span></span>|<span data-ttu-id="6e943-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6e943-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6e943-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="6e943-123">Authorization</span></span>|<span data-ttu-id="6e943-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6e943-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6e943-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6e943-125">Accept</span></span>|<span data-ttu-id="6e943-126">application/json</span><span class="sxs-lookup"><span data-stu-id="6e943-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6e943-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6e943-127">Request body</span></span>
<span data-ttu-id="6e943-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="6e943-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="6e943-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="6e943-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="6e943-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6e943-130">Property</span></span>|<span data-ttu-id="6e943-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e943-131">Type</span></span>|<span data-ttu-id="6e943-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e943-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6e943-133">parentUri</span><span class="sxs-lookup"><span data-stu-id="6e943-133">parentUri</span></span>|<span data-ttu-id="6e943-134">String</span><span class="sxs-lookup"><span data-stu-id="6e943-134">String</span></span>|<span data-ttu-id="6e943-135">La ruta de acceso https de la página que hospeda el componente.</span><span class="sxs-lookup"><span data-stu-id="6e943-135">The https path of the page hosting the component.</span></span>|



## <a name="response"></a><span data-ttu-id="6e943-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6e943-136">Response</span></span>
<span data-ttu-id="6e943-137">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `200 OK` y un objeto String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6e943-137">If successful, this action returns a `200 OK` response code and a String in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6e943-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6e943-138">Example</span></span>
### <a name="request"></a><span data-ttu-id="6e943-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6e943-139">Request</span></span>
<span data-ttu-id="6e943-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6e943-140">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/androidManagedStoreAccountEnterpriseSettings/createGooglePlayWebToken

Content-type: application/json
Content-length: 39

{
  "parentUri": "Parent Uri value"
}
```

### <a name="response"></a><span data-ttu-id="6e943-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6e943-141">Response</span></span>
<span data-ttu-id="6e943-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6e943-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 53

{
  "value": "Create Google Play Web Token value"
}
```





