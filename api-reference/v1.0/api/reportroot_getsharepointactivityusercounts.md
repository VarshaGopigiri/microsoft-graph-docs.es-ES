# <a name="reportroot-getsharepointactivityusercounts"></a><span data-ttu-id="f7621-101">reportRoot: getSharePointActivityUserCounts</span><span class="sxs-lookup"><span data-stu-id="f7621-101">reportRoot: getSharePointActivityUserCounts</span></span>

<span data-ttu-id="f7621-102">Obtiene la tendencia del número de usuarios activos.</span><span class="sxs-lookup"><span data-stu-id="f7621-102">Get the trend in the number of active users.</span></span> <span data-ttu-id="f7621-103">Un usuario se considera activo si ejecutó una actividad de archivos (guardar, sincronizar, modificar o compartir), o bien si visitó una página dentro del período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="f7621-103">A user is considered active if he or she has executed a file activity (save, sync, modify, or share) or visited a page within the specified time period.</span></span>

> <span data-ttu-id="f7621-104">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de SharePoint](https://support.office.com/client/SharePoint-activity-a91c958f-1279-499d-9959-12f0de08dc8f).</span><span class="sxs-lookup"><span data-stu-id="f7621-104">**Note:** For details about different report views and names, see [Office 365 Reports - SharePoint activity](https://support.office.com/client/SharePoint-activity-a91c958f-1279-499d-9959-12f0de08dc8f).</span></span>

## <a name="permissions"></a><span data-ttu-id="f7621-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="f7621-105">Permissions</span></span>

<span data-ttu-id="f7621-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f7621-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="f7621-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f7621-108">Permission type</span></span>                        | <span data-ttu-id="f7621-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f7621-109">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="f7621-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f7621-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="f7621-111">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="f7621-111">Reports.Read.All</span></span>                         |
| <span data-ttu-id="f7621-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f7621-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f7621-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f7621-113">Not supported.</span></span>                           |
| <span data-ttu-id="f7621-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f7621-114">Application</span></span>                            | <span data-ttu-id="f7621-115">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="f7621-115">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="f7621-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f7621-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSharePointActivityUserCounts(period='{period_value}')
```

## <a name="request-parameters"></a><span data-ttu-id="f7621-117">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f7621-117">Request parameters</span></span>

<span data-ttu-id="f7621-118">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="f7621-118">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="f7621-119">Parámetro</span><span class="sxs-lookup"><span data-stu-id="f7621-119">Parameter</span></span> | <span data-ttu-id="f7621-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="f7621-120">Type</span></span>   | <span data-ttu-id="f7621-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7621-121">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="f7621-122">period</span><span class="sxs-lookup"><span data-stu-id="f7621-122">period</span></span>    | <span data-ttu-id="f7621-123">cadena</span><span class="sxs-lookup"><span data-stu-id="f7621-123">string</span></span> | <span data-ttu-id="f7621-124">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="f7621-124">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="f7621-125">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="f7621-125">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="f7621-126">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="f7621-126">These values follow the format D   where    represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="f7621-127">Necesario.</span><span class="sxs-lookup"><span data-stu-id="f7621-127">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="f7621-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f7621-128">Request headers</span></span>

| <span data-ttu-id="f7621-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7621-129">Name</span></span>          | <span data-ttu-id="f7621-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7621-130">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="f7621-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="f7621-131">Authorization</span></span> | <span data-ttu-id="f7621-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f7621-p104">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="f7621-134">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="f7621-134">If-None-Match</span></span> | <span data-ttu-id="f7621-135">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="f7621-135">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="f7621-136">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f7621-136">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="f7621-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f7621-137">Response</span></span>

<span data-ttu-id="f7621-138">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="f7621-138">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="f7621-139">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f7621-139">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="f7621-140">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="f7621-140">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="f7621-141">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="f7621-141">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="f7621-142">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="f7621-142">Report Refresh Date</span></span>
- <span data-ttu-id="f7621-143">Página visitada</span><span class="sxs-lookup"><span data-stu-id="f7621-143">Visited Page</span></span>
- <span data-ttu-id="f7621-144">Visto o editado</span><span class="sxs-lookup"><span data-stu-id="f7621-144">Viewed Or Edited</span></span>
- <span data-ttu-id="f7621-145">Sincronizado</span><span class="sxs-lookup"><span data-stu-id="f7621-145">Synced</span></span>
- <span data-ttu-id="f7621-146">Compartido internamente</span><span class="sxs-lookup"><span data-stu-id="f7621-146">Shared Internally</span></span>
- <span data-ttu-id="f7621-147">Compartido externamente</span><span class="sxs-lookup"><span data-stu-id="f7621-147">Shared Externally</span></span>
- <span data-ttu-id="f7621-148">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="f7621-148">Report Date</span></span>
- <span data-ttu-id="f7621-149">Período del informe</span><span class="sxs-lookup"><span data-stu-id="f7621-149">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="f7621-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f7621-150">Example</span></span>

#### <a name="request"></a><span data-ttu-id="f7621-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f7621-151">Request</span></span>

<span data-ttu-id="f7621-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f7621-152">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getsharepointactivityusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getSharePointActivityUserCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="f7621-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f7621-153">Response</span></span>

<span data-ttu-id="f7621-154">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f7621-154">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="f7621-155">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="f7621-155">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Visited Page,Viewed Or Edited,Synced,Shared Internally,Shared Externally,Report Date,Report Period
```
