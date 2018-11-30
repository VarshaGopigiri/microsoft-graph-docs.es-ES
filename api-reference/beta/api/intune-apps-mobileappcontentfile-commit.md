---
title: Acción commit
description: Confirma un archivo de una aplicación determinada.
ms.openlocfilehash: 923bd9cc74d377cc61a466dfda12148c84d706c3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084971"
---
# <a name="commit-action"></a><span data-ttu-id="ab59f-103">Acción commit</span><span class="sxs-lookup"><span data-stu-id="ab59f-103">commit action</span></span>

> <span data-ttu-id="ab59f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ab59f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ab59f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ab59f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ab59f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ab59f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ab59f-107">Confirma un archivo de una aplicación determinada.</span><span class="sxs-lookup"><span data-stu-id="ab59f-107">Commits a file of a given app.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ab59f-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ab59f-108">Prerequisites</span></span>
<span data-ttu-id="ab59f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ab59f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ab59f-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ab59f-111">Permission type</span></span>|<span data-ttu-id="ab59f-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ab59f-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ab59f-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ab59f-113">Delegated (work or school account)</span></span>|<span data-ttu-id="ab59f-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ab59f-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="ab59f-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ab59f-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ab59f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ab59f-116">Not supported.</span></span>|
|<span data-ttu-id="ab59f-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ab59f-117">Application</span></span>|<span data-ttu-id="ab59f-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ab59f-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ab59f-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ab59f-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/files/{mobileAppContentFileId}/commit
```

## <a name="request-headers"></a><span data-ttu-id="ab59f-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ab59f-120">Request headers</span></span>
|<span data-ttu-id="ab59f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab59f-121">Header</span></span>|<span data-ttu-id="ab59f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ab59f-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ab59f-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="ab59f-123">Authorization</span></span>|<span data-ttu-id="ab59f-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ab59f-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ab59f-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ab59f-125">Accept</span></span>|<span data-ttu-id="ab59f-126">application/json</span><span class="sxs-lookup"><span data-stu-id="ab59f-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ab59f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ab59f-127">Request body</span></span>
<span data-ttu-id="ab59f-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="ab59f-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="ab59f-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="ab59f-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="ab59f-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ab59f-130">Property</span></span>|<span data-ttu-id="ab59f-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="ab59f-131">Type</span></span>|<span data-ttu-id="ab59f-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab59f-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ab59f-133">fileEncryptionInfo</span><span class="sxs-lookup"><span data-stu-id="ab59f-133">fileEncryptionInfo</span></span>|[<span data-ttu-id="ab59f-134">fileEncryptionInfo</span><span class="sxs-lookup"><span data-stu-id="ab59f-134">fileEncryptionInfo</span></span>](../resources/intune-apps-fileencryptioninfo.md)|<span data-ttu-id="ab59f-135">Clave de parámetro de información de cifrado del archivo.</span><span class="sxs-lookup"><span data-stu-id="ab59f-135">File encryption info parameter key.</span></span>|



## <a name="response"></a><span data-ttu-id="ab59f-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ab59f-136">Response</span></span>
<span data-ttu-id="ab59f-137">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="ab59f-137">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="ab59f-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ab59f-138">Example</span></span>
### <a name="request"></a><span data-ttu-id="ab59f-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ab59f-139">Request</span></span>
<span data-ttu-id="ab59f-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ab59f-140">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/files/{mobileAppContentFileId}/commit

Content-type: application/json
Content-length: 399

{
  "fileEncryptionInfo": {
    "@odata.type": "microsoft.graph.fileEncryptionInfo",
    "encryptionKey": "ZW5jcnlwdGlvbktleQ==",
    "initializationVector": "aW5pdGlhbGl6YXRpb25WZWN0b3I=",
    "mac": "bWFj",
    "macKey": "bWFjS2V5",
    "profileIdentifier": "Profile Identifier value",
    "fileDigest": "ZmlsZURpZ2VzdA==",
    "fileDigestAlgorithm": "File Digest Algorithm value"
  }
}
```

### <a name="response"></a><span data-ttu-id="ab59f-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ab59f-141">Response</span></span>
<span data-ttu-id="ab59f-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ab59f-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```





