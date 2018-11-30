---
title: Permissions
description: 'Recupera una lista de los elementos recientemente eliminados que pertenecen al usuario especificado.  '
ms.openlocfilehash: affdd67d48056c4459e651fd5c64168d8356abe8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029160"
---
# <a name="list-deleted-items-owned-by-a-user"></a><span data-ttu-id="fbec5-103">**Lista de los elementos eliminados que pertenecen a un usuario**</span><span class="sxs-lookup"><span data-stu-id="fbec5-103">**List deleted items owned by a user**</span></span>

<span data-ttu-id="fbec5-104">Recupera una lista de los elementos recientemente eliminados que pertenecen al usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="fbec5-104">Retrieves a list of recently deleted items owned by the specified user.</span></span>  

<span data-ttu-id="fbec5-105">Actualmente, la funcionalidad de elementos de lista eliminada sólo se admite para [agrupar](../resources/group.md) los recursos que pertenecen al usuario.</span><span class="sxs-lookup"><span data-stu-id="fbec5-105">Currently, list deleted items functionality is supported only for [group](../resources/group.md) resources owned by the user.</span></span>

<span data-ttu-id="fbec5-106">Se trata de una acción de servicio, lo que significa que no admite la paginación.</span><span class="sxs-lookup"><span data-stu-id="fbec5-106">This is a service action, which means it does not support pagination.</span></span>  <span data-ttu-id="fbec5-107">La API devuelve objetos eliminados hasta 1.000 que pertenecen al usuario, ordenado por identificador.</span><span class="sxs-lookup"><span data-stu-id="fbec5-107">The API returns up to 1,000 deleted objects owned by the user, sorted by ID.</span></span>

## <a name="permissions"></a><span data-ttu-id="fbec5-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="fbec5-108">Permissions</span></span>

<span data-ttu-id="fbec5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span><span class="sxs-lookup"><span data-stu-id="fbec5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span></span>

| <span data-ttu-id="fbec5-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fbec5-111">Permission type</span></span> | <span data-ttu-id="fbec5-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fbec5-112">Permissions (from least to most privileged)</span></span> |
| --- | --- |
| <span data-ttu-id="fbec5-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fbec5-113">Delegated (work or school account)</span></span> | <span data-ttu-id="fbec5-114">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fbec5-114">Group.Read.All, Group.ReadWrite.All</span></span> |
| <span data-ttu-id="fbec5-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fbec5-115">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="fbec5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fbec5-116">Not supported.</span></span> |
| <span data-ttu-id="fbec5-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fbec5-117">Application</span></span> | <span data-ttu-id="fbec5-118">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fbec5-118">Group.Read.All, Group.ReadWrite.All</span></span>  |

## <a name="http-request"></a><span data-ttu-id="fbec5-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fbec5-119">HTTP request</span></span>

``` http
POST /directory/deletedItems/getUserOwnedObjects
```

## <a name="request-headers"></a><span data-ttu-id="fbec5-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fbec5-120">Request headers</span></span>

| <span data-ttu-id="fbec5-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="fbec5-121">Name</span></span>          | <span data-ttu-id="fbec5-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="fbec5-122">Description</span></span>               |
| ------------- | ------------------------- |
| <span data-ttu-id="fbec5-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="fbec5-123">Authorization</span></span> | <span data-ttu-id="fbec5-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fbec5-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="fbec5-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fbec5-126">Request body</span></span>

```json
{
  "userId":"{id}",
  "type":"Group"
}
```

<span data-ttu-id="fbec5-127">El cuerpo de solicitud requiere los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="fbec5-127">The request body requires the following parameters:</span></span>

| <span data-ttu-id="fbec5-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="fbec5-128">Parameter</span></span>    | <span data-ttu-id="fbec5-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="fbec5-129">Type</span></span> |<span data-ttu-id="fbec5-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="fbec5-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="fbec5-131">userId</span><span class="sxs-lookup"><span data-stu-id="fbec5-131">userId</span></span>|<span data-ttu-id="fbec5-132">String</span><span class="sxs-lookup"><span data-stu-id="fbec5-132">String</span></span>|<span data-ttu-id="fbec5-133">Identificador del propietario.</span><span class="sxs-lookup"><span data-stu-id="fbec5-133">ID of the owner.</span></span>|
|<span data-ttu-id="fbec5-134">type</span><span class="sxs-lookup"><span data-stu-id="fbec5-134">type</span></span>|<span data-ttu-id="fbec5-135">String</span><span class="sxs-lookup"><span data-stu-id="fbec5-135">String</span></span>|<span data-ttu-id="fbec5-136">Tipo de objetos que posea para devolver; `Group` actualmente es el único valor admitido.</span><span class="sxs-lookup"><span data-stu-id="fbec5-136">Type of owned objects to return; `Group` is currently the only supported value.</span></span>|


## <a name="response"></a><span data-ttu-id="fbec5-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fbec5-137">Response</span></span>

<span data-ttu-id="fbec5-138">Solicitudes correctas devuelven `200 OK` los códigos de respuesta; el objeto de respuesta incluye las propiedades del [directorio (elementos eliminados)](../resources/directory.md) .</span><span class="sxs-lookup"><span data-stu-id="fbec5-138">Successful requests return `200 OK` response codes; the response object includes [directory (deleted items)](../resources/directory.md) properties.</span></span>

## <a name="example"></a><span data-ttu-id="fbec5-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fbec5-139">Example</span></span>

##### <a name="request"></a><span data-ttu-id="fbec5-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fbec5-140">Request</span></span>

<span data-ttu-id="fbec5-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fbec5-141">Here is an example of the request.</span></span>

``` http
POST https://graph.microsoft.com/v1.0/directory/deletedItems/getUserOwnedObjects
Content-type: application/json
```

``` json
{
  "userId":"55ac777c-109e-4022-b58c-470c8fcb6892",
  "type":"group"
}
```

###### <a name="response"></a><span data-ttu-id="fbec5-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fbec5-142">Response</span></span>

<span data-ttu-id="fbec5-143">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fbec5-143">Here is an example of the response.</span></span> <span data-ttu-id="fbec5-144">Nota: Este objeto de respuesta es posible que esté truncada por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="fbec5-144">Note: This response object may be truncated for brevity.</span></span> <span data-ttu-id="fbec5-145">Se devuelven todas las propiedades admitidas de llamadas reales.</span><span class="sxs-lookup"><span data-stu-id="fbec5-145">All supported properties are returned from actual calls.</span></span>

``` http
HTTP/1.1 200
Content-type: application/json
Content-length: 1249

{
"value": [
          {
              "@odata.type": "#microsoft.graph.group",
              "id": "bfa7033a-7367-4644-85f5-95aaf385cbd7",
              "deletedDateTime": 2018-04-01T12:39:16Z,
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


