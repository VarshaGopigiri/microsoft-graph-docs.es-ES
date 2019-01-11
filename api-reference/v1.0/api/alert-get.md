---
title: Get alert
description: " Recuperar las propiedades y relaciones de un objeto de alerta."
author: Preetikr
localization_priority: Normal
ms.openlocfilehash: 6e2bc95561dcfb87c54e684ad6f3991cbcd6e7f1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27857004"
---
# <a name="get-alert"></a><span data-ttu-id="44613-103">Get alert</span><span class="sxs-lookup"><span data-stu-id="44613-103">Get alert</span></span>

 <span data-ttu-id="44613-104">Recuperar las propiedades y relaciones de un objeto de [alerta](../resources/alert.md) .</span><span class="sxs-lookup"><span data-stu-id="44613-104">Retrieve the properties and relationships of an [alert](../resources/alert.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="44613-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="44613-105">Permissions</span></span>

<span data-ttu-id="44613-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="44613-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="44613-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="44613-108">Permission type</span></span>      | <span data-ttu-id="44613-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="44613-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="44613-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="44613-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="44613-111">SecurityEvents.Read.All, SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="44613-111">SecurityEvents.Read.All, SecurityEvents.ReadWrite.All</span></span>   |
|<span data-ttu-id="44613-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="44613-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="44613-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="44613-113">Not supported.</span></span>  |
|<span data-ttu-id="44613-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="44613-114">Application</span></span> | <span data-ttu-id="44613-115">SecurityEvents.Read.All, SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="44613-115">SecurityEvents.Read.All, SecurityEvents.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="44613-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="44613-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /security/alerts/{alert_id}
```

## <a name="request-headers"></a><span data-ttu-id="44613-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="44613-117">Request headers</span></span>

| <span data-ttu-id="44613-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="44613-118">Name</span></span>      |<span data-ttu-id="44613-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="44613-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="44613-120">Autorización</span><span class="sxs-lookup"><span data-stu-id="44613-120">Authorization</span></span>  | <span data-ttu-id="44613-p102">{código} del portador. Necesario.</span><span class="sxs-lookup"><span data-stu-id="44613-p102">Bearer {code}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="44613-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="44613-123">Request body</span></span>

<span data-ttu-id="44613-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="44613-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="44613-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="44613-125">Response</span></span>

<span data-ttu-id="44613-126">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto de **alerta** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="44613-126">If successful, this method returns a `200 OK` response code and an **alert** object in the response body.</span></span> <span data-ttu-id="44613-127">Si se devuelve un código de estado que no sea 2xx o 404 desde un proveedor o un proveedor de tiempo de espera, la respuesta será un `206 Partial Content` código de estado con la respuesta del proveedor en un encabezado de advertencia.</span><span class="sxs-lookup"><span data-stu-id="44613-127">If a status code other than 2xx or 404 is returned from a provider or if a provider times out, the response will be a `206 Partial Content` status code with the provider's response in a warning header.</span></span> <span data-ttu-id="44613-128">Para obtener más información, vea [respuestas de error de la API de seguridad de Microsoft Graph](../resources/security-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="44613-128">For more information, see [Microsoft Graph Security API error responses](../resources/security-error-codes.md).</span></span>

## <a name="example"></a><span data-ttu-id="44613-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="44613-129">Example</span></span>

### <a name="request"></a><span data-ttu-id="44613-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="44613-130">Request</span></span>

<span data-ttu-id="44613-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="44613-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_alert"
}-->

```http
GET https://graph.microsoft.com/v1.0/security/alerts/{alert_id}
```

### <a name="response"></a><span data-ttu-id="44613-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="44613-132">Response</span></span>

<span data-ttu-id="44613-133">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="44613-133">The following is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.alert"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "activityGroupName": "String",
  "assignedTo": "String",
  "azureSubscriptionId": "String",
  "azureTenantId": "String",
  "category": "String",
  "closedDateTime": "String (timestamp)",
  "cloudAppStates": [
    {
      "destinationServiceIp": "String",
      "destinationServiceName": "String",
      "riskScore": "String"
    }
  ],
  "comments": ["String"],
  "confidence": 1024,
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "detectionIds": ["String"],
  "eventDateTime": "String (timestamp)",
  "feedback": "@odata.type: microsoft.graph.alertFeedback",
  "fileStates": [
    {
      "fileHash": {
        "hashType": "@odata.type: microsoft.graph.fileHashType",
        "hashValue": "String"
      },
      "name": "String",
      "path": "String",
      "riskScore": "String"
    }
  ],
  "hostStates": [
    {
      "fqdn": "String",
      "isAzureAadJoined": true,
      "isAzureAadRegistered": true,
      "isHybridAzureDomainJoined": true,
      "netBiosName": "String",
      "os": "String",
      "privateIpAddress": "String",
      "publicIpAddress": "String",
      "riskScore": "String"
    }
  ],
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "malwareStates": [
    {
      "category": "String",
      "family": "String",
      "name": "String",
      "severity": "String",
      "wasRunning": true
    }
  ],
  "networkConnections": [
    {
      "applicationName": "String",
      "destinationAddress": "String",
      "destinationDomain": "String",
      "destinationPort": "String",
      "destinationUrl": "String",
      "direction": "@odata.type: microsoft.graph.connectionDirection",
      "domainRegisteredDateTime": "String (timestamp)",
      "localDnsName": "String",
      "natDestinationAddress": "String",
      "natDestinationPort": "String",
      "natSourceAddress": "String",
      "natSourcePort": "String",
      "protocol": "@odata.type: microsoft.graph.securityNetworkProtocol",
      "riskScore": "String",
      "sourceAddress": "String",
      "sourcePort": "String",
      "status": "@odata.type: microsoft.graph.connectionStatus",
      "urlParameters": "String"
    }
  ],
  "processes": [
    {
      "accountName": "String",
      "commandLine": "String",
      "createdDateTime": "String (timestamp)",
      "fileHash": {
        "hashType": "@odata.type: microsoft.graph.fileHashType",
        "hashValue": "String"
      },
      "integrityLevel": "@odata.type: microsoft.graph.processIntegrityLevel",
      "isElevated": true,
      "name": "String",
      "parentProcessCreatedDateTime": "String (timestamp)",
      "parentProcessId": 1024,
      "parentProcessName": "String",
      "path": "String",
      "processId": 1024
    }
  ],
  "recommendedActions": ["String"],
  "registryKeyStates": [
    {
      "hive": "@odata.type: microsoft.graph.registryHive",
      "key": "String",
      "oldKey": "String",
      "oldValueData": "String",
      "oldValueName": "String",
      "operation": "@odata.type: microsoft.graph.registryOperation",
      "processId": 1024,
      "valueData": "String",
      "valueName": "String",
      "valueType": "@odata.type: microsoft.graph.registryValueType"
    }
  ],
  "severity": "@odata.type: microsoft.graph.alertSeverity",
  "sourceMaterials": ["String"],
  "status": "@odata.type: microsoft.graph.alertStatus",
  "tags": ["String"],
  "title": "String",
  "triggers": [
    {
      "name": "String",
      "type": "String",
      "value": "String"
    }
  ],
  "userStates": [
    {
      "aadUserId": "String",
      "accountName": "String",
      "domainName": "String",
      "emailRole": "@odata.type: microsoft.graph.emailRole",
      "isVpn": true,
      "logonDateTime": "String (timestamp)",
      "logonId": "String",
      "logonIp": "String",
      "logonLocation": "String",
      "logonType": "@odata.type: microsoft.graph.logonType",
      "onPremisesSecurityIdentifier": "String",
      "riskScore": "String",
      "userAccountType": "@odata.type: microsoft.graph.userAccountSecurityType",
      "userPrincipalName": "String"
    }
  ],
  "vendorInformation": {
    "provider": "String",
    "providerVersion": "String",
    "subProvider": "String",
    "vendor": "String"
  },
  "vulnerabilityStates": [
    {
      "cve": "String",
      "severity": "String",
      "wasRunning": true
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get glert",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
