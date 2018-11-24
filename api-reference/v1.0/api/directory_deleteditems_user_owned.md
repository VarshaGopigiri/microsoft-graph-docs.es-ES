# <a name="list-deleted-items-owned-by-a-user"></a><span data-ttu-id="863c4-101">**Lista de los elementos eliminados que pertenecen a un usuario**</span><span class="sxs-lookup"><span data-stu-id="863c4-101">**List deleted items owned by a user**</span></span>

<span data-ttu-id="863c4-102">Recupera una lista de los elementos recientemente eliminados que pertenecen al usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="863c4-102">Retrieves a list of recently deleted items owned by the specified user.</span></span>  

<span data-ttu-id="863c4-103">Actualmente, la funcionalidad de elementos de lista eliminada sólo se admite para [agrupar](../resources/group.md) los recursos que pertenecen al usuario.</span><span class="sxs-lookup"><span data-stu-id="863c4-103">Currently, list deleted items functionality is supported only for [group](../resources/group.md) resources owned by the user.</span></span>

<span data-ttu-id="863c4-104">Se trata de una acción de servicio, lo que significa que no admite la paginación.</span><span class="sxs-lookup"><span data-stu-id="863c4-104">This is a service action, which means it does not support pagination.</span></span>  <span data-ttu-id="863c4-105">La API devuelve objetos eliminados hasta 1.000 que pertenecen al usuario, ordenado por identificador.</span><span class="sxs-lookup"><span data-stu-id="863c4-105">The API returns up to 1,000 deleted objects owned by the user, sorted by ID.</span></span>

## <a name="permissions"></a><span data-ttu-id="863c4-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="863c4-106">Permissions</span></span>

<span data-ttu-id="863c4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span><span class="sxs-lookup"><span data-stu-id="863c4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span></span>

| <span data-ttu-id="863c4-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="863c4-109">Permission type</span></span> | <span data-ttu-id="863c4-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="863c4-110">Permissions (from least to most privileged)</span></span> |
| --- | --- |
| <span data-ttu-id="863c4-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="863c4-111">Delegated (work or school account)</span></span> | <span data-ttu-id="863c4-112">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="863c4-112">Group.Read.All, Group.ReadWrite.All</span></span> |
| <span data-ttu-id="863c4-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="863c4-113">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="863c4-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="863c4-114">Not supported.</span></span> |
| <span data-ttu-id="863c4-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="863c4-115">Application</span></span> | <span data-ttu-id="863c4-116">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="863c4-116">Group.Read.All, Group.ReadWrite.All</span></span>  |

## <a name="http-request"></a><span data-ttu-id="863c4-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="863c4-117">HTTP request</span></span>

``` http
POST /directory/deletedItems/getUserOwnedObjects
```

## <a name="request-headers"></a><span data-ttu-id="863c4-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="863c4-118">Request headers</span></span>

| <span data-ttu-id="863c4-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="863c4-119">Name</span></span>          | <span data-ttu-id="863c4-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="863c4-120">Description</span></span>               |
| ------------- | ------------------------- |
| <span data-ttu-id="863c4-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="863c4-121">Authorization</span></span> | <span data-ttu-id="863c4-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="863c4-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="863c4-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="863c4-124">Request body</span></span>

```json
{
  "userId":"{id}",
  "type":"Group"
}
```

<span data-ttu-id="863c4-125">El cuerpo de solicitud requiere los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="863c4-125">The request body requires the following parameters:</span></span>

| <span data-ttu-id="863c4-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="863c4-126">Parameter</span></span>    | <span data-ttu-id="863c4-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="863c4-127">Type</span></span> |<span data-ttu-id="863c4-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="863c4-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="863c4-129">userId</span><span class="sxs-lookup"><span data-stu-id="863c4-129">userId</span></span>|<span data-ttu-id="863c4-130">String</span><span class="sxs-lookup"><span data-stu-id="863c4-130">String</span></span>|<span data-ttu-id="863c4-131">Identificador del propietario.</span><span class="sxs-lookup"><span data-stu-id="863c4-131">ID of the owner.</span></span>|
|<span data-ttu-id="863c4-132">type</span><span class="sxs-lookup"><span data-stu-id="863c4-132">type</span></span>|<span data-ttu-id="863c4-133">String</span><span class="sxs-lookup"><span data-stu-id="863c4-133">String</span></span>|<span data-ttu-id="863c4-134">Tipo de objetos que posea para devolver; `Group` actualmente es el único valor admitido.</span><span class="sxs-lookup"><span data-stu-id="863c4-134">Type of owned objects to return; `Group` is currently the only supported value.</span></span>|


## <a name="response"></a><span data-ttu-id="863c4-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="863c4-135">Response</span></span>

<span data-ttu-id="863c4-136">Solicitudes correctas devuelven `200 OK` los códigos de respuesta; el objeto de respuesta incluye las propiedades del [directorio (elementos eliminados)](../resources/directory.md) .</span><span class="sxs-lookup"><span data-stu-id="863c4-136">Successful requests return `200 OK` response codes; the response object includes [directory (deleted items)](../resources/directory.md) properties.</span></span>

## <a name="example"></a><span data-ttu-id="863c4-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="863c4-137">Example</span></span>

##### <a name="request"></a><span data-ttu-id="863c4-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="863c4-138">Request</span></span>

<span data-ttu-id="863c4-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="863c4-139">Here is an example of the request.</span></span>

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

###### <a name="response"></a><span data-ttu-id="863c4-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="863c4-140">Response</span></span>

<span data-ttu-id="863c4-141">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="863c4-141">Here is an example of the response.</span></span> <span data-ttu-id="863c4-142">Nota: Este objeto de respuesta es posible que esté truncada por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="863c4-142">Note: This response object may be truncated for brevity.</span></span> <span data-ttu-id="863c4-143">Se devuelven todas las propiedades admitidas de llamadas reales.</span><span class="sxs-lookup"><span data-stu-id="863c4-143">All supported properties are returned from actual calls.</span></span>

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


