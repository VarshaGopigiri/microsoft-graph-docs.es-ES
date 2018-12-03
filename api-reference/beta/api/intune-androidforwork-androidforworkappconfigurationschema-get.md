---
title: Obtener androidForWorkAppConfigurationSchema
description: Lea las propiedades y las relaciones del objeto androidForWorkAppConfigurationSchema.
ms.openlocfilehash: 9ece3217670089575ea596dd8fa7b02571cd527b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086165"
---
# <a name="get-androidforworkappconfigurationschema"></a><span data-ttu-id="afbfa-103">Obtener androidForWorkAppConfigurationSchema</span><span class="sxs-lookup"><span data-stu-id="afbfa-103">Get androidForWorkAppConfigurationSchema</span></span>

> <span data-ttu-id="afbfa-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="afbfa-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="afbfa-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="afbfa-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="afbfa-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="afbfa-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="afbfa-107">Lea las propiedades y las relaciones del objeto [androidForWorkAppConfigurationSchema](../resources/intune-androidforwork-androidforworkappconfigurationschema.md).</span><span class="sxs-lookup"><span data-stu-id="afbfa-107">Read properties and relationships of the [androidForWorkAppConfigurationSchema](../resources/intune-androidforwork-androidforworkappconfigurationschema.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="afbfa-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="afbfa-108">Prerequisites</span></span>
<span data-ttu-id="afbfa-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="afbfa-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="afbfa-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="afbfa-111">Permission type</span></span>|<span data-ttu-id="afbfa-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="afbfa-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="afbfa-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="afbfa-113">Delegated (work or school account)</span></span>|<span data-ttu-id="afbfa-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="afbfa-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="afbfa-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="afbfa-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="afbfa-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="afbfa-116">Not supported.</span></span>|
|<span data-ttu-id="afbfa-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="afbfa-117">Application</span></span>|<span data-ttu-id="afbfa-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="afbfa-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="afbfa-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="afbfa-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/androidForWorkAppConfigurationSchemas/{androidForWorkAppConfigurationSchemaId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="afbfa-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="afbfa-120">Optional query parameters</span></span>
<span data-ttu-id="afbfa-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="afbfa-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="afbfa-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="afbfa-122">Request headers</span></span>
|<span data-ttu-id="afbfa-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="afbfa-123">Header</span></span>|<span data-ttu-id="afbfa-124">Valor</span><span class="sxs-lookup"><span data-stu-id="afbfa-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="afbfa-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="afbfa-125">Authorization</span></span>|<span data-ttu-id="afbfa-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="afbfa-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="afbfa-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="afbfa-127">Accept</span></span>|<span data-ttu-id="afbfa-128">application/json</span><span class="sxs-lookup"><span data-stu-id="afbfa-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="afbfa-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="afbfa-129">Request body</span></span>
<span data-ttu-id="afbfa-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="afbfa-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="afbfa-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="afbfa-131">Response</span></span>
<span data-ttu-id="afbfa-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [androidForWorkAppConfigurationSchema](../resources/intune-androidforwork-androidforworkappconfigurationschema.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="afbfa-132">If successful, this method returns a `200 OK` response code and [androidForWorkAppConfigurationSchema](../resources/intune-androidforwork-androidforworkappconfigurationschema.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="afbfa-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="afbfa-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="afbfa-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="afbfa-134">Request</span></span>
<span data-ttu-id="afbfa-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="afbfa-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/androidForWorkAppConfigurationSchemas/{androidForWorkAppConfigurationSchemaId}
```

### <a name="response"></a><span data-ttu-id="afbfa-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="afbfa-136">Response</span></span>
<span data-ttu-id="afbfa-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="afbfa-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 913

{
  "value": {
    "@odata.type": "#microsoft.graph.androidForWorkAppConfigurationSchema",
    "id": "c1230dc6-0dc6-c123-c60d-23c1c60d23c1",
    "exampleJson": "ZXhhbXBsZUpzb24=",
    "schemaItems": [
      {
        "@odata.type": "microsoft.graph.androidForWorkAppConfigurationSchemaItem",
        "schemaItemKey": "Schema Item Key value",
        "displayName": "Display Name value",
        "description": "Description value",
        "defaultBoolValue": true,
        "defaultIntValue": 15,
        "defaultStringValue": "Default String Value value",
        "defaultStringArrayValue": [
          "Default String Array Value value"
        ],
        "dataType": "integer",
        "selections": [
          {
            "@odata.type": "microsoft.graph.keyValuePair",
            "name": "Name value",
            "value": "Value value"
          }
        ]
      }
    ]
  }
}
```




