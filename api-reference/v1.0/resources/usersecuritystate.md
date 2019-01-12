---
title: tipo de recurso userSecurityState
description: Contiene información de estado acerca de la cuenta de usuario.
author: dkershaw10
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 9f451f2bc42500eee15bd59809c124a79186916f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27992059"
---
# <a name="usersecuritystate-resource-type"></a><span data-ttu-id="d4cdb-103">tipo de recurso userSecurityState</span><span class="sxs-lookup"><span data-stu-id="d4cdb-103">userSecurityState resource type</span></span>

<span data-ttu-id="d4cdb-104">Contiene información de estado acerca de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="d4cdb-104">Contains stateful information about the user account.</span></span>

## <a name="properties"></a><span data-ttu-id="d4cdb-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d4cdb-105">Properties</span></span>

| <span data-ttu-id="d4cdb-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d4cdb-106">Property</span></span>   | <span data-ttu-id="d4cdb-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="d4cdb-107">Type</span></span> |<span data-ttu-id="d4cdb-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4cdb-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d4cdb-109">aadUserId</span><span class="sxs-lookup"><span data-stu-id="d4cdb-109">aadUserId</span></span>|<span data-ttu-id="d4cdb-110">String</span><span class="sxs-lookup"><span data-stu-id="d4cdb-110">String</span></span>|<span data-ttu-id="d4cdb-111">AAD usuario identificador (GUID) - objeto representa la entidad de usuario físicos/multi-account.</span><span class="sxs-lookup"><span data-stu-id="d4cdb-111">AAD User object identifier (GUID) - represents the physical/multi-account user entity.</span></span>|
|<span data-ttu-id="d4cdb-112">accountName</span><span class="sxs-lookup"><span data-stu-id="d4cdb-112">accountName</span></span>|<span data-ttu-id="d4cdb-113">String</span><span class="sxs-lookup"><span data-stu-id="d4cdb-113">String</span></span>|<span data-ttu-id="d4cdb-114">Nombre de cuenta de la cuenta de usuario (sin dominio de Active Directory o dominio DNS) - (también denominada `mailNickName`).</span><span class="sxs-lookup"><span data-stu-id="d4cdb-114">Account name of user account (without Active Directory domain or DNS domain) - (also called `mailNickName`).</span></span>|
|<span data-ttu-id="d4cdb-115">domainName</span><span class="sxs-lookup"><span data-stu-id="d4cdb-115">domainName</span></span>|<span data-ttu-id="d4cdb-116">String</span><span class="sxs-lookup"><span data-stu-id="d4cdb-116">String</span></span>|<span data-ttu-id="d4cdb-117">Dominio de NetBIOS o Active Directory de la cuenta de usuario (es decir, el formato dominio\cuenta).</span><span class="sxs-lookup"><span data-stu-id="d4cdb-117">NetBIOS/Active Directory domain of user account (that is, domain\account format).</span></span>|
|<span data-ttu-id="d4cdb-118">emailRole</span><span class="sxs-lookup"><span data-stu-id="d4cdb-118">emailRole</span></span>|<span data-ttu-id="d4cdb-119">emailRole</span><span class="sxs-lookup"><span data-stu-id="d4cdb-119">emailRole</span></span>|<span data-ttu-id="d4cdb-120">Para las alertas relacionadas con el correo electrónico - correo electrónico de una cuenta de usuario 'rol'.</span><span class="sxs-lookup"><span data-stu-id="d4cdb-120">For email-related alerts - user account's email 'role'.</span></span> <span data-ttu-id="d4cdb-121">Los valores posibles son: `unknown`, `sender` y `recipient`.</span><span class="sxs-lookup"><span data-stu-id="d4cdb-121">Possible values are: `unknown`, `sender`, `recipient`.</span></span>|
|<span data-ttu-id="d4cdb-122">isVpn</span><span class="sxs-lookup"><span data-stu-id="d4cdb-122">isVpn</span></span>|<span data-ttu-id="d4cdb-123">Booleano</span><span class="sxs-lookup"><span data-stu-id="d4cdb-123">Boolean</span></span>|<span data-ttu-id="d4cdb-124">Indica si el usuario se conectó a través de una red privada virtual.</span><span class="sxs-lookup"><span data-stu-id="d4cdb-124">Indicates whether the user logged on through a VPN.</span></span>|
|<span data-ttu-id="d4cdb-125">logonDateTime</span><span class="sxs-lookup"><span data-stu-id="d4cdb-125">logonDateTime</span></span>|<span data-ttu-id="d4cdb-126">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d4cdb-126">DateTimeOffset</span></span>|<span data-ttu-id="d4cdb-127">Hora a la que el inicio de sesión se produjo.</span><span class="sxs-lookup"><span data-stu-id="d4cdb-127">Time at which the sign-in occurred.</span></span> <span data-ttu-id="d4cdb-128">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="d4cdb-128">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="d4cdb-129">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="d4cdb-129">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="d4cdb-130">ID de registro</span><span class="sxs-lookup"><span data-stu-id="d4cdb-130">logonId</span></span>|<span data-ttu-id="d4cdb-131">String</span><span class="sxs-lookup"><span data-stu-id="d4cdb-131">String</span></span>|<span data-ttu-id="d4cdb-132">Identificador de usuario de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="d4cdb-132">User sign-in ID.</span></span>|
|<span data-ttu-id="d4cdb-133">logonIp</span><span class="sxs-lookup"><span data-stu-id="d4cdb-133">logonIp</span></span>|<span data-ttu-id="d4cdb-134">String</span><span class="sxs-lookup"><span data-stu-id="d4cdb-134">String</span></span>|<span data-ttu-id="d4cdb-135">Dirección IP de. que la solicitud de inicio de sesión se originó.</span><span class="sxs-lookup"><span data-stu-id="d4cdb-135">IP Address the sign-in request originated from.</span></span>|
|<span data-ttu-id="d4cdb-136">logonLocation</span><span class="sxs-lookup"><span data-stu-id="d4cdb-136">logonLocation</span></span>|<span data-ttu-id="d4cdb-137">String</span><span class="sxs-lookup"><span data-stu-id="d4cdb-137">String</span></span>|<span data-ttu-id="d4cdb-138">Ubicación (mediante la asignación de direcciones IP) asociado a un evento de inicio de sesión de usuario por este usuario.</span><span class="sxs-lookup"><span data-stu-id="d4cdb-138">Location (by IP address mapping) associated with a user sign-in event by this user.</span></span>|
|<span data-ttu-id="d4cdb-139">logonType</span><span class="sxs-lookup"><span data-stu-id="d4cdb-139">logonType</span></span>|<span data-ttu-id="d4cdb-140">logonType</span><span class="sxs-lookup"><span data-stu-id="d4cdb-140">logonType</span></span>|<span data-ttu-id="d4cdb-141">Método de inicio de sesión de usuario en.</span><span class="sxs-lookup"><span data-stu-id="d4cdb-141">Method of user sign in.</span></span> <span data-ttu-id="d4cdb-142">Los valores posibles son: `unknown`, `interactive`, `remoteInteractive`, `network`, `batch`, `service`.</span><span class="sxs-lookup"><span data-stu-id="d4cdb-142">Possible values are: `unknown`, `interactive`, `remoteInteractive`, `network`, `batch`, `service`.</span></span>|
|<span data-ttu-id="d4cdb-143">onPremisesSecurityIdentifier</span><span class="sxs-lookup"><span data-stu-id="d4cdb-143">onPremisesSecurityIdentifier</span></span>|<span data-ttu-id="d4cdb-144">String</span><span class="sxs-lookup"><span data-stu-id="d4cdb-144">String</span></span>|<span data-ttu-id="d4cdb-145">Active Directory (local) identificador de seguridad (SID) del usuario.</span><span class="sxs-lookup"><span data-stu-id="d4cdb-145">Active Directory (on-premises) Security Identifier (SID) of the user.</span></span>|
|<span data-ttu-id="d4cdb-146">riskScore</span><span class="sxs-lookup"><span data-stu-id="d4cdb-146">riskScore</span></span>|<span data-ttu-id="d4cdb-147">String</span><span class="sxs-lookup"><span data-stu-id="d4cdb-147">String</span></span>|<span data-ttu-id="d4cdb-148">Puntuación de proveedor generado/calculada en el riesgo de la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="d4cdb-148">Provider-generated/calculated risk score of the user account.</span></span> <span data-ttu-id="d4cdb-149">Valor recomendado el rango de 0-1, lo que equivale a un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="d4cdb-149">Recommended value range of 0-1, which equates to a percentage.</span></span>|
|<span data-ttu-id="d4cdb-150">userAccountType</span><span class="sxs-lookup"><span data-stu-id="d4cdb-150">userAccountType</span></span>|<span data-ttu-id="d4cdb-151">userAccountSecurityType</span><span class="sxs-lookup"><span data-stu-id="d4cdb-151">userAccountSecurityType</span></span>|<span data-ttu-id="d4cdb-152">Tipo de cuenta de usuario (pertenencia a grupos), por definición de Windows.</span><span class="sxs-lookup"><span data-stu-id="d4cdb-152">User account type (group membership), per Windows definition.</span></span> <span data-ttu-id="d4cdb-153">Los valores posibles son: `unknown`, `standard`, `power` y `administrator`.</span><span class="sxs-lookup"><span data-stu-id="d4cdb-153">Possible values are: `unknown`, `standard`, `power`, `administrator`.</span></span>|
|<span data-ttu-id="d4cdb-154">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d4cdb-154">userPrincipalName</span></span>|<span data-ttu-id="d4cdb-155">String</span><span class="sxs-lookup"><span data-stu-id="d4cdb-155">String</span></span>|<span data-ttu-id="d4cdb-156">Inicio de sesión de nombre de usuario - formato de internet: (nombre de cuenta de usuario) @(nombre de dominio DNS de cuenta de usuario).</span><span class="sxs-lookup"><span data-stu-id="d4cdb-156">User sign-in name - internet format: (user account name)@(user account DNS domain name).</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d4cdb-157">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d4cdb-157">JSON representation</span></span>

<span data-ttu-id="d4cdb-158">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d4cdb-158">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.userSecurityState"
}-->

```json
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

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "userSecurityState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
