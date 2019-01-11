---
title: 'synchronizationSchema: parseExpression'
description: '(.. / resources/synchronization_attributemappingsource.md) objeto. '
localization_priority: Normal
ms.openlocfilehash: dbde03b9ae85377801ad894c8b8ca22c6baebc85
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27811028"
---
# <a name="synchronizationschema-parseexpression"></a><span data-ttu-id="a8cfa-103">synchronizationSchema: parseExpression</span><span class="sxs-lookup"><span data-stu-id="a8cfa-103">synchronizationSchema: parseExpression</span></span>

> <span data-ttu-id="a8cfa-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a8cfa-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a8cfa-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a8cfa-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a8cfa-106">Analizar una expresión de cadena dada en un [attributeMappingSource | (.. / resources/synchronization_attributemappingsource.md) objeto.</span><span class="sxs-lookup"><span data-stu-id="a8cfa-106">Parse a given string expression into an [attributeMappingSource|(../resources/synchronization_attributemappingsource.md) object.</span></span> 

<span data-ttu-id="a8cfa-107">Para obtener más información acerca de las expresiones, vea [Escritura de expresiones para asignaciones de atributo de Active Directory de Azure](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-saas-writing-expressions-for-attribute-mappings).</span><span class="sxs-lookup"><span data-stu-id="a8cfa-107">For more information about expressions, see [Writing Expressions for Attribute Mappings in Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-saas-writing-expressions-for-attribute-mappings).</span></span>

## <a name="permissions"></a><span data-ttu-id="a8cfa-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="a8cfa-108">Permissions</span></span>
<span data-ttu-id="a8cfa-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a8cfa-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a8cfa-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a8cfa-111">Permission type</span></span>                        | <span data-ttu-id="a8cfa-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a8cfa-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="a8cfa-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a8cfa-113">Delegated (work or school account)</span></span>     |<span data-ttu-id="a8cfa-114">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a8cfa-114">Directory.ReadWrite.All</span></span>  |
|<span data-ttu-id="a8cfa-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a8cfa-115">Delegated (personal Microsoft account)</span></span> |<span data-ttu-id="a8cfa-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a8cfa-116">Not supported.</span></span>|
|<span data-ttu-id="a8cfa-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a8cfa-117">Application</span></span>                            |<span data-ttu-id="a8cfa-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a8cfa-118">Not supported.</span></span>| 

## <a name="http-request"></a><span data-ttu-id="a8cfa-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a8cfa-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /servicePrincipals/{id}/synchronization/jobs/{id}/schema/parseExpression
POST /servicePrincipals/{id}/synchronization/templates/{id}/schema/parseExpression

```
## <a name="request-headers"></a><span data-ttu-id="a8cfa-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a8cfa-120">Request headers</span></span>
| <span data-ttu-id="a8cfa-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="a8cfa-121">Name</span></span>       | <span data-ttu-id="a8cfa-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8cfa-122">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="a8cfa-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="a8cfa-123">Authorization</span></span>  | <span data-ttu-id="a8cfa-124">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="a8cfa-124">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="a8cfa-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a8cfa-125">Request body</span></span>
<span data-ttu-id="a8cfa-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="a8cfa-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="a8cfa-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="a8cfa-127">Parameter</span></span>    | <span data-ttu-id="a8cfa-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="a8cfa-128">Type</span></span>   |<span data-ttu-id="a8cfa-129">Description</span><span class="sxs-lookup"><span data-stu-id="a8cfa-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a8cfa-130">expresión</span><span class="sxs-lookup"><span data-stu-id="a8cfa-130">expression</span></span>               |<span data-ttu-id="a8cfa-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="a8cfa-131">String</span></span>               |<span data-ttu-id="a8cfa-132">Expresión para analizar.</span><span class="sxs-lookup"><span data-stu-id="a8cfa-132">Expression to parse.</span></span>|
|<span data-ttu-id="a8cfa-133">testInputObject</span><span class="sxs-lookup"><span data-stu-id="a8cfa-133">testInputObject</span></span>          |[<span data-ttu-id="a8cfa-134">expressionInputObject</span><span class="sxs-lookup"><span data-stu-id="a8cfa-134">expressionInputObject</span></span>](../resources/synchronization-expressioninputobject.md)|<span data-ttu-id="a8cfa-135">Objeto de datos de prueba para evaluar la expresión con respecto a.</span><span class="sxs-lookup"><span data-stu-id="a8cfa-135">Test data object to evaluate expression against.</span></span> <span data-ttu-id="a8cfa-136">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a8cfa-136">Optional.</span></span>|
|<span data-ttu-id="a8cfa-137">targetAttributeDefinition</span><span class="sxs-lookup"><span data-stu-id="a8cfa-137">targetAttributeDefinition</span></span>|[<span data-ttu-id="a8cfa-138">attributeDefinition</span><span class="sxs-lookup"><span data-stu-id="a8cfa-138">attributeDefinition</span></span>](../resources/synchronization-attributedefinition.md) |<span data-ttu-id="a8cfa-139">Definición del atributo que se va a asignar a esta expresión.</span><span class="sxs-lookup"><span data-stu-id="a8cfa-139">Definition of the attribute that will be mapped to this expression.</span></span> <span data-ttu-id="a8cfa-140">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a8cfa-140">Optional.</span></span>|

## <a name="response"></a><span data-ttu-id="a8cfa-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a8cfa-141">Response</span></span>
<span data-ttu-id="a8cfa-142">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [parseExpressionResponse](../resources/synchronization-parseexpressionresponse.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a8cfa-142">If successful, this method returns a `200 OK` response code and a [parseExpressionResponse](../resources/synchronization-parseexpressionresponse.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a8cfa-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a8cfa-143">Example</span></span>

##### <a name="request"></a><span data-ttu-id="a8cfa-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a8cfa-144">Request</span></span>
<span data-ttu-id="a8cfa-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a8cfa-145">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "synchronizationschema_parseexpression"
}-->
```http
POST https://graph.microsoft.com/beta/servicePrincipals/{id}/synchronization/jobs/{id}/schema/parseExpression
Content-type: application/json

{
    "expression":"Replace([preferredLanguage], \"-\", , , \"_\", ,  )",
    "targetAttributeDefinition":null,
    "testInputObject": {
        definition: null,
        properties:[
            { key: "objectId", value : "66E4A8CC-1B7B-435E-95F8-F06CEA133828" },
            { key: "IsSoftDeleted", value: "false"},
            { key: "accountEnabled", value: "true"},
            { key: "streetAddress", value: "1 Redmond Way"},
            { key: "city", value: "Redmond"},
            { key: "state", value: "WA"},
            { key: "postalCode", value: "98052"},
            { key: "country", value: "USA"},
            { key: "department", value: "Sales"},
            { key: "displayName", value: "John Smith"},
            { key: "extensionAttribute1", value: "Sample 1"},
            { key: "extensionAttribute2", value: "Sample 2"},
            { key: "extensionAttribute3", value: "Sample 3"},
            { key: "extensionAttribute4", value: "Sample 4"},
            { key: "extensionAttribute5", value: "Sample 5"},
            { key: "extensionAttribute6", value: "Sample 6"},
            { key: "extensionAttribute7", value: "Sample 1"},
            { key: "extensionAttribute8", value: "Sample 1"},
            { key: "extensionAttribute9", value: "Sample 1"},
            { key: "extensionAttribute10", value: "Sample 1"},
            { key: "extensionAttribute11", value: "Sample 1"},
            { key: "extensionAttribute12", value: "Sample 1"},
            { key: "extensionAttribute13", value: "Sample 1"},
            { key: "extensionAttribute14", value: "Sample 1"},
            { key: "extensionAttribute15", value: "Sample 1"},
            { key: "givenName", value: "John"},
            { key: "jobTitle", value: "Finance manager"},
            { key: "mail", value: "johns@contoso.com"},
            { key: "mailNickname", value: "johns"},
            { key: "manager", value: "maxs@contoso.com"},
            { key: "mobile", value: "425-555-0010"},
            { key: "onPremisesSecurityIdentifier", value: "66E4A8CC-1B7B-435E-95F8-F06CEA133828"},
            { key: "passwordProfile.password", value: ""},
            { key: "physicalDeliveryOfficeName", value: "Main Office"},
            { key: "preferredLanguage", value: "EN-US"},
            { key: "proxyAddresses", value: ""},
            { key: "surname", value: "Smith"},
            { key: "telephoneNumber", value: "425-555-0011"},
            { key: "userPrincipalName", value: "johns@contoso.com"},
            { key: "appRoleAssignments", "value@odata.type":"#Collection(String)", value: ["Default Assignment"] }
        ]
    }
}
```

##### <a name="response"></a><span data-ttu-id="a8cfa-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a8cfa-146">Response</span></span>
<span data-ttu-id="a8cfa-147">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a8cfa-147">The following is an example of the response.</span></span> 

><span data-ttu-id="a8cfa-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a8cfa-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.parseExpressionResponse"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "error": null,
    "evaluationSucceeded": true,
    "evaluationResult": [
        "EN_US"
    ],
    "parsedExpression": {
        "expression": "Replace([preferredLanguage], \"-\", , , \"_\", , )",
        "name": "Replace",
        "parameters": [
            {
                "key": "source",
                "value": {
                    "expression": "[preferredLanguage]",
                    "name": "preferredLanguage",
                    "parameters": [],
                    "type": "Attribute"
                }
            },
            {
                "key": "Find",
                "value": {
                    "expression": "\"-\"",
                    "name": "-",
                    "parameters": [],
                    "type": "Constant"
                }
            },
            {
                "key": "Replacement",
                "value": {
                    "expression": "\"_\"",
                    "name": "_",
                    "parameters": [],
                    "type": "Constant"
                }
            }
        ],
        "type": "Function"
    },
    "parsingSucceeded": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "synchronizationSchema: parseExpression",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
