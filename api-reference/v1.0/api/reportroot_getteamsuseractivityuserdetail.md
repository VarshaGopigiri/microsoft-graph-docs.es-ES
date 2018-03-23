# <a name="reportroot-getteamsuseractivityuserdetail"></a><span data-ttu-id="5a969-101">reportRoot: getTeamsUserActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="5a969-101">reportRoot: getTeamsUserActivityUserDetail</span></span>

<span data-ttu-id="5a969-102">Obtenga información sobre la actividad de usuario de Microsoft Teams por usuario.</span><span class="sxs-lookup"><span data-stu-id="5a969-102">Get details about Microsoft Teams user activity by user.</span></span>

## <a name="permissions"></a><span data-ttu-id="5a969-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="5a969-103">Permissions</span></span>

<span data-ttu-id="5a969-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="5a969-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="5a969-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5a969-106">Permission type</span></span>                        | <span data-ttu-id="5a969-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5a969-107">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="5a969-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5a969-108">Delegated (work or school account)</span></span>     | <span data-ttu-id="5a969-109">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5a969-109">Not supported.</span></span>                           |
| <span data-ttu-id="5a969-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5a969-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5a969-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5a969-111">Not supported.</span></span>                           |
| <span data-ttu-id="5a969-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5a969-112">Application</span></span>                            | <span data-ttu-id="5a969-113">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="5a969-113">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="5a969-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5a969-114">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /reports/getTeamsUserActivityUserDetail(period='{period_value}')
GET /reports/getTeamsUserActivityUserDetail(date={date_value})
```

## <a name="request-parameters"></a><span data-ttu-id="5a969-115">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5a969-115">Request parameters</span></span>

<span data-ttu-id="5a969-116">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="5a969-116">In the request URL, provide the following query parameter with a valid value.</span></span>

| <span data-ttu-id="5a969-117">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5a969-117">Parameter</span></span> | <span data-ttu-id="5a969-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="5a969-118">Type</span></span>   | <span data-ttu-id="5a969-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="5a969-119">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="5a969-120">period</span><span class="sxs-lookup"><span data-stu-id="5a969-120">period</span></span>    | <span data-ttu-id="5a969-121">cadena</span><span class="sxs-lookup"><span data-stu-id="5a969-121">string</span></span> | <span data-ttu-id="5a969-122">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="5a969-122">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="5a969-123">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="5a969-123">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="5a969-124">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante el que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="5a969-124">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="5a969-125">date</span><span class="sxs-lookup"><span data-stu-id="5a969-125">date</span></span>      | <span data-ttu-id="5a969-126">Fecha</span><span class="sxs-lookup"><span data-stu-id="5a969-126">Date</span></span>   | <span data-ttu-id="5a969-127">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="5a969-127">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="5a969-128">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="5a969-128">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="5a969-129">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="5a969-129">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="5a969-130">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="5a969-130">**Note:** You need to set either period or date in the URL.</span></span>

## <a name="request-headers"></a><span data-ttu-id="5a969-131">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5a969-131">Request headers</span></span>

| <span data-ttu-id="5a969-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="5a969-132">Name</span></span>          | <span data-ttu-id="5a969-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="5a969-133">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="5a969-134">Authorization</span><span class="sxs-lookup"><span data-stu-id="5a969-134">Authorization</span></span> | <span data-ttu-id="5a969-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5a969-p104">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="5a969-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5a969-137">Response</span></span>

<span data-ttu-id="5a969-138">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="5a969-138">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="5a969-139">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5a969-139">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="5a969-140">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="5a969-140">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="5a969-141">El archivo CSV tiene los siguientes encabezados de columna:</span><span class="sxs-lookup"><span data-stu-id="5a969-141">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="5a969-142">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="5a969-142">Report Refresh Date</span></span>
- <span data-ttu-id="5a969-143">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="5a969-143">User Principal Name</span></span>
- <span data-ttu-id="5a969-144">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="5a969-144">Last Activity Date</span></span>
- <span data-ttu-id="5a969-145">Eliminado</span><span class="sxs-lookup"><span data-stu-id="5a969-145">Is Deleted</span></span>
- <span data-ttu-id="5a969-146">Fecha de eliminación</span><span class="sxs-lookup"><span data-stu-id="5a969-146">Deleted Date</span></span>
- <span data-ttu-id="5a969-147">Productos asignados</span><span class="sxs-lookup"><span data-stu-id="5a969-147">Assigned Products</span></span>
- <span data-ttu-id="5a969-148">Recuento de mensajes de chat del equipo</span><span class="sxs-lookup"><span data-stu-id="5a969-148">Team Chat Message Count</span></span>
- <span data-ttu-id="5a969-149">Recuento de mensajes de chat privado</span><span class="sxs-lookup"><span data-stu-id="5a969-149">Private Chat Message Count</span></span>
- <span data-ttu-id="5a969-150">Recuento de llamadas</span><span class="sxs-lookup"><span data-stu-id="5a969-150">Call Count</span></span>
- <span data-ttu-id="5a969-151">Recuento de reuniones</span><span class="sxs-lookup"><span data-stu-id="5a969-151">Meeting Count</span></span>
- <span data-ttu-id="5a969-152">Tiene otra acción</span><span class="sxs-lookup"><span data-stu-id="5a969-152">Has Other Action</span></span>
- <span data-ttu-id="5a969-153">Período del informe</span><span class="sxs-lookup"><span data-stu-id="5a969-153">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="5a969-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5a969-154">Example</span></span>

#### <a name="request"></a><span data-ttu-id="5a969-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5a969-155">Request</span></span>

<span data-ttu-id="5a969-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5a969-156">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getteamsuseractivityuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getTeamsUserActivityUserDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="5a969-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5a969-157">Response</span></span>

<span data-ttu-id="5a969-158">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5a969-158">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="5a969-159">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="5a969-159">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Last Activity Date,Is Deleted,Deleted Date,Assigned Products,Team Chat Message Count,Private Chat Message Count,Call Count,Meeting Count,Has Other Action,Report Period
```
