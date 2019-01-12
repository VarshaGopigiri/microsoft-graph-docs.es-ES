---
title: Permisos
description: 'Recupera una lista de los elementos recientemente eliminados que pertenecen al usuario especificado.  '
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: f02d6dccd005696c130c6bb4a1f42c603943e5c8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27960570"
---
# <a name="list-deleted-items-owned-by-a-user"></a><span data-ttu-id="34484-103">**Lista de los elementos eliminados que pertenecen a un usuario**</span><span class="sxs-lookup"><span data-stu-id="34484-103">**List deleted items owned by a user**</span></span>

<span data-ttu-id="34484-104">Recupera una lista de los elementos recientemente eliminados que pertenecen al usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="34484-104">Retrieves a list of recently deleted items owned by the specified user.</span></span>  

<span data-ttu-id="34484-105">Actualmente, la funcionalidad de elementos de lista eliminada sólo se admite para [agrupar](../resources/group.md) los recursos que pertenecen al usuario.</span><span class="sxs-lookup"><span data-stu-id="34484-105">Currently, list deleted items functionality is supported only for [group](../resources/group.md) resources owned by the user.</span></span>

<span data-ttu-id="34484-106">Se trata de una acción de servicio, lo que significa que no admite la paginación.</span><span class="sxs-lookup"><span data-stu-id="34484-106">This is a service action, which means it does not support pagination.</span></span>  <span data-ttu-id="34484-107">La API devuelve objetos eliminados hasta 1.000 que pertenecen al usuario, ordenado por identificador.</span><span class="sxs-lookup"><span data-stu-id="34484-107">The API returns up to 1,000 deleted objects owned by the user, sorted by ID.</span></span>  <span data-ttu-id="34484-108">Debe el usuario propietario de 1.000 o más elimina los objetos, la API devuelve nothing.</span><span class="sxs-lookup"><span data-stu-id="34484-108">Should the user own 1,000 or more deleted objects, the API returns nothing.</span></span>

## <a name="permissions"></a><span data-ttu-id="34484-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="34484-109">Permissions</span></span>

<span data-ttu-id="34484-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span><span class="sxs-lookup"><span data-stu-id="34484-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span></span>

| <span data-ttu-id="34484-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="34484-112">Permission type</span></span> | <span data-ttu-id="34484-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="34484-113">Permissions (from least to most privileged)</span></span> |
| --- | --- |
| <span data-ttu-id="34484-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="34484-114">Delegated (work or school account)</span></span> | <span data-ttu-id="34484-115">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="34484-115">Group.Read.All, Group.ReadWrite.All</span></span> |
| <span data-ttu-id="34484-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="34484-116">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="34484-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="34484-117">Not supported.</span></span> |
| <span data-ttu-id="34484-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="34484-118">Application</span></span> | <span data-ttu-id="34484-119">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="34484-119">Group.Read.All, Group.ReadWrite.All</span></span>  |

## <a name="http-request"></a><span data-ttu-id="34484-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="34484-120">HTTP request</span></span>

``` http
POST /directory/deletedItems/getUserOwnedObjects
```

## <a name="request-headers"></a><span data-ttu-id="34484-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="34484-121">Request headers</span></span>

| <span data-ttu-id="34484-122">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="34484-122">**Name**</span></span>      | <span data-ttu-id="34484-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="34484-123">**Description**</span></span>           |
| ------------- | ------------------------- |
| <span data-ttu-id="34484-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="34484-124">Authorization</span></span> | <span data-ttu-id="34484-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="34484-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="34484-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="34484-127">Request body</span></span>

```json
{
  "userId":"55ac777c-109e-4022-b58c-470c8fcb6892",
  "type":"group"
}
```

<span data-ttu-id="34484-128">El cuerpo de solicitud requiere los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="34484-128">The request body requires the following parameters:</span></span>

| <span data-ttu-id="34484-129">Parámetro</span><span class="sxs-lookup"><span data-stu-id="34484-129">Parameter</span></span>    | <span data-ttu-id="34484-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="34484-130">Type</span></span> |<span data-ttu-id="34484-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="34484-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="34484-132">userId</span><span class="sxs-lookup"><span data-stu-id="34484-132">userId</span></span>|<span data-ttu-id="34484-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="34484-133">String</span></span>|<span data-ttu-id="34484-134">Identificador del propietario.</span><span class="sxs-lookup"><span data-stu-id="34484-134">ID of the owner.</span></span>|
|<span data-ttu-id="34484-135">type</span><span class="sxs-lookup"><span data-stu-id="34484-135">type</span></span>|<span data-ttu-id="34484-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="34484-136">String</span></span>|<span data-ttu-id="34484-137">Tipo de objetos que posea para devolver; `Group` actualmente es el único valor admitido.</span><span class="sxs-lookup"><span data-stu-id="34484-137">Type of owned objects to return; `Group` is currently the only supported value.</span></span>|

## <a name="response"></a><span data-ttu-id="34484-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="34484-138">Response</span></span>

<span data-ttu-id="34484-139">Solicitudes correctas devuelven `200 OK` los códigos de respuesta; el objeto de respuesta incluye las propiedades del [directorio (elementos eliminados)](../resources/directory.md) .</span><span class="sxs-lookup"><span data-stu-id="34484-139">Successful requests return `200 OK` response codes; the response object includes [directory (deleted items)](../resources/directory.md) properties.</span></span>

## <a name="example"></a><span data-ttu-id="34484-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="34484-140">Example</span></span>

##### <a name="request"></a><span data-ttu-id="34484-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="34484-141">Request</span></span>

<span data-ttu-id="34484-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="34484-142">Here is an example of the request.</span></span>

``` http
POST https://graph.microsoft.com/beta/directory/deletedItems/getUserOwnedObjects
Content-type: application/json
```

``` json
{
  "userId":"55ac777c-109e-4022-b58c-470c8fcb6892",
  "type":"Group"
}
```

###### <a name="response"></a><span data-ttu-id="34484-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="34484-143">Response</span></span>

<span data-ttu-id="34484-144">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="34484-144">Here is an example of the response.</span></span> <span data-ttu-id="34484-145">Nota: Este objeto de respuesta es posible que esté truncada por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="34484-145">Note: This response object may be truncated for brevity.</span></span> <span data-ttu-id="34484-146">Se devuelven todas las propiedades admitidas de llamadas reales.</span><span class="sxs-lookup"><span data-stu-id="34484-146">All supported properties are returned from actual calls.</span></span>

``` http
HTTP/1.1 200
Content-type: application/json
Content-length: 1249

{
"value": [
          {
              "@odata.type": "#microsoft.graph.group",
              "id": "bfa7033a-7367-4644-85f5-95aaf385cbd7",
              "deletedDateTime": "2018-04-01T12:34:56Z",
              "classification": null,
              "createdDateTime": "2017-03-22T12:39:16Z",
              "description": null,
              "displayName": "Test",
              "groupTypes": [
                  "Unified"
              ],
              "mail": "Test@contoso.com",
              "mailEnabled": true,
              "mailNickname": "Test",
              "membershipRule": null,
              "membershipRuleProcessingState": null,
              "preferredDataLocation": null,
              "preferredLanguage": null,
              "proxyAddresses": [
                  "SMTP:Test@contoso.com"
              ],
              "renewedDateTime": "2017-09-22T22:30:39Z",
              "securityEnabled": false,
              "theme": null,
              "visibility": "Public"
          } 
        ]
 }
```


