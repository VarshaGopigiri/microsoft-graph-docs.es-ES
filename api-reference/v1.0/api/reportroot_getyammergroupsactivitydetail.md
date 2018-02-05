# <a name="reportroot-getyammergroupsactivitydetail"></a><span data-ttu-id="490e0-101">reportRoot: getYammerGroupsActivityDetail</span><span class="sxs-lookup"><span data-stu-id="490e0-101">reportRoot: getYammerGroupsActivityDetail</span></span>

<span data-ttu-id="490e0-102">Obtiene información sobre la actividad de grupos de Yammer por grupo.</span><span class="sxs-lookup"><span data-stu-id="490e0-102">Get details about Yammer groups activity by group.</span></span>

> <span data-ttu-id="490e0-103">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de grupos de Yammer](https://support.office.com/client/Yammer-groups-activity-report-94dd92ec-ea73-43c6-b51f-2a11fd78aa31).</span><span class="sxs-lookup"><span data-stu-id="490e0-103">**Note:** For details about different report views and names, see [Office 365 Reports - Yammer groups activity](https://support.office.com/client/Yammer-groups-activity-report-94dd92ec-ea73-43c6-b51f-2a11fd78aa31).</span></span>

## <a name="permissions"></a><span data-ttu-id="490e0-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="490e0-104">Permissions</span></span>

<span data-ttu-id="490e0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="490e0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="490e0-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="490e0-107">Permission type</span></span>                        | <span data-ttu-id="490e0-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="490e0-108">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="490e0-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="490e0-109">Delegated (work or school account)</span></span>     | <span data-ttu-id="490e0-110">No admitida.</span><span class="sxs-lookup"><span data-stu-id="490e0-110">Not supported.</span></span>                           |
| <span data-ttu-id="490e0-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="490e0-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="490e0-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="490e0-112">Not supported.</span></span>                           |
| <span data-ttu-id="490e0-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="490e0-113">Application</span></span>                            | <span data-ttu-id="490e0-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="490e0-114">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="490e0-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="490e0-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getYammerGroupsActivityDetail(period='{period_value}')
GET /reports/getYammerGroupsActivityDetail(date={date_value})
```

## <a name="request-parameters"></a><span data-ttu-id="490e0-116">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="490e0-116">Request parameters</span></span>

<span data-ttu-id="490e0-117">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="490e0-117">In the request URL, provide the following query parameter with a valid value.</span></span>

| <span data-ttu-id="490e0-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="490e0-118">Parameter</span></span> | <span data-ttu-id="490e0-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="490e0-119">Type</span></span>   | <span data-ttu-id="490e0-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="490e0-120">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="490e0-121">period</span><span class="sxs-lookup"><span data-stu-id="490e0-121">period</span></span>    | <span data-ttu-id="490e0-122">cadena</span><span class="sxs-lookup"><span data-stu-id="490e0-122">string</span></span> | <span data-ttu-id="490e0-123">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="490e0-123">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="490e0-124">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="490e0-124">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="490e0-125">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante el que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="490e0-125">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="490e0-126">date</span><span class="sxs-lookup"><span data-stu-id="490e0-126">date</span></span>      | <span data-ttu-id="490e0-127">Fecha</span><span class="sxs-lookup"><span data-stu-id="490e0-127">Date</span></span>   | <span data-ttu-id="490e0-128">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="490e0-128">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="490e0-129">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="490e0-129">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="490e0-130">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="490e0-130">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="490e0-131">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="490e0-131">**Note:** You need to set either period or date in the URL.</span></span>

## <a name="request-headers"></a><span data-ttu-id="490e0-132">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="490e0-132">Request headers</span></span>

| <span data-ttu-id="490e0-133">Nombre</span><span class="sxs-lookup"><span data-stu-id="490e0-133">Name</span></span>          | <span data-ttu-id="490e0-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="490e0-134">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="490e0-135">Authorization</span><span class="sxs-lookup"><span data-stu-id="490e0-135">Authorization</span></span> | <span data-ttu-id="490e0-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="490e0-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="490e0-138">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="490e0-138">If-None-Match</span></span> | <span data-ttu-id="490e0-139">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="490e0-139">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="490e0-140">Opcional.</span><span class="sxs-lookup"><span data-stu-id="490e0-140">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="490e0-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="490e0-141">Response</span></span>

<span data-ttu-id="490e0-142">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="490e0-142">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="490e0-143">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="490e0-143">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="490e0-144">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="490e0-144">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="490e0-145">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="490e0-145">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="490e0-146">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="490e0-146">Report Refresh Date</span></span>
- <span data-ttu-id="490e0-147">Nombre para mostrar del grupo</span><span class="sxs-lookup"><span data-stu-id="490e0-147">Group Display Name</span></span>
- <span data-ttu-id="490e0-148">Eliminado</span><span class="sxs-lookup"><span data-stu-id="490e0-148">Is Deleted</span></span>
- <span data-ttu-id="490e0-149">Nombre principal de propietario</span><span class="sxs-lookup"><span data-stu-id="490e0-149">Owner Principal Name</span></span>
- <span data-ttu-id="490e0-150">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="490e0-150">Last Activity Date</span></span>
- <span data-ttu-id="490e0-151">Tipo de grupo</span><span class="sxs-lookup"><span data-stu-id="490e0-151">Group Type</span></span>
- <span data-ttu-id="490e0-152">Office 365 conectado</span><span class="sxs-lookup"><span data-stu-id="490e0-152">Office 365 Connected</span></span>
- <span data-ttu-id="490e0-153">Número de miembros</span><span class="sxs-lookup"><span data-stu-id="490e0-153">Member Count</span></span>
- <span data-ttu-id="490e0-154">Número de publicaciones</span><span class="sxs-lookup"><span data-stu-id="490e0-154">Posted Count</span></span>
- <span data-ttu-id="490e0-155">Número de lecturas</span><span class="sxs-lookup"><span data-stu-id="490e0-155">Read Count</span></span>
- <span data-ttu-id="490e0-156">Número de etiquetados como “Me gusta”</span><span class="sxs-lookup"><span data-stu-id="490e0-156">Liked Count</span></span>
- <span data-ttu-id="490e0-157">Período del informe</span><span class="sxs-lookup"><span data-stu-id="490e0-157">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="490e0-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="490e0-158">Example</span></span>

#### <a name="request"></a><span data-ttu-id="490e0-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="490e0-159">Request</span></span>

<span data-ttu-id="490e0-160">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="490e0-160">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getyammergroupsactivityuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getYammerGroupsActivityDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="490e0-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="490e0-161">Response</span></span>

<span data-ttu-id="490e0-162">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="490e0-162">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="490e0-163">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="490e0-163">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Group Display Name,Is Deleted,Owner Principal Name,Last Activity Date,Group Type,Office 365 Connected,Member Count,Posted Count,Read Count,Liked Count,Report Period
```
