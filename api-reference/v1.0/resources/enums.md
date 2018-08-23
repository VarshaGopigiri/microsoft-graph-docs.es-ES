
### <a name="timezonestandard-values"></a>valores de timeZoneStandard

| Valor
|:-----------------
| windows
| iana


### <a name="freebusystatus-values"></a>valores de freeBusyStatus

| Miembro            |Valor
|:------------------|:-------
| free (libre)              | 0
| tentative (provisional)         | 1
| busy (ocupado)              | 2
| oof (fuera de la oficina)               | 3
| workingElsewhere (trabajando en otro lugar)  | 4
| unknown (desconocido)           | -1


### <a name="attendeetype-values"></a>valores de attendeeType

| Valor
|:-------------------------
| obligatorio
| opcional
| recurso


### <a name="externalaudiencescope-values"></a>valores de externalAudienceScope

| Valor
|:-------------------------
| none (ninguno)
| contactsOnly (solo contactos)
| all (todos)


### <a name="automaticrepliesstatus-values"></a>valores de automaticRepliesStatus

| Valor
|:-------------------------
| disabled (deshabilitado)
| alwaysEnabled (siempre habilitado)
| scheduled (programado)


### <a name="calendarcolor-values"></a>valores de calendarColor

| Miembro     | Valor
|:-----------|:----------
| auto       | -1
| lightBlue (azul claro)  | 0
| lightGreen (verde claro) | 1
| lightOrange (naranja claro)| 2
| lightGray (gris claro)  | 3
| lightYellow (amarillo claro)| 4
| lightTeal (verde azulado claro)  | 5
| lightPink (rosa claro)  | 6
| lightBrown (marrón claro) | 7
| lightRed (rojo claro)   | 8
| maxColor   | 9


### <a name="educationexternalsource-values"></a>valores de educationExternalSource

| Valor
|:-------------------------
| sis
| manual
| unknownFutureValue


### <a name="educationgender-values"></a>valores de educationGender

| Valor
|:-------------------------
| female (femenino)
| male (masculino)
| other (otro)
| unknownFutureValue


### <a name="eventtype-values"></a>valores de eventType

| Valor
|:-------------------------
| singleInstance (única instancia)
| occurrence (evento recurrente)
| exception (excepción)
| seriesMaster


### <a name="sensitivity-values"></a>valores de sensibilidad

| Valor
|:-------------------------
| normal
| personal
| private (privado)
| confidential (confidencial)


### <a name="importance-values"></a>valores de importance

| Valor
|:-------------------------
| low (baja)
| normal
| high (alta)


### <a name="educationuserrole-values"></a>valores de educationUserRole
| Valor
|:---------------------
| student (estudiante)
| teacher (docente)
| none (ninguno)
| unknownFutureValue


### <a name="meetingmessagetype-values"></a>valores de meetingMessageType

| Valor
|:-----------------
| none (ninguno)
| meetingRequest (solicitado)
| meetingCancelled (cancelado)
| meetingAccepted (aceptado)
| meetingTentativelyAccepted (provisionalmente aceptado)
| meetingDeclined (rechazado)


### <a name="followupflagstatus-values"></a>valores de followupFlagStatus

| Valor
|:-------------------------
| notFlagged (sin marcar)
| complete (completado)
| flagged (marcado)


### <a name="inferenceclassificationtype-values"></a>valores de inferenceClassificationType

| Valor
|:-----------------
| focused (centrado)
| other (otro)


### <a name="iosnotificationalerttype-values"></a>valores de iosNotificationAlertType

| Valor
|:-------------------------
| deviceDefault (predeterminado)
| banner
| modal
| none (ninguno)

### <a name="deviceenrollmentfailurereason-values"></a>valores de deviceEnrollmentFailureReason

| Valor
|:-------------
| unknown (desconocido)
| authentication (autenticación)
| authorization (autorización)
| accountValidation (validación de la cuenta)
| userValidation (validación del usuario)
| deviceNotSupported (dispositivo no compatible)
| inMaintenance (en mantenimiento)
| badRequest (solicitud errónea)
| featureNotSupported (característica no soportada)
| enrollmentRestrictionsEnforced (restricciones de inscripción)
| clientDisconnected (cliente desconectado)


### <a name="bodytype-values"></a>valores de bodyType
| Valor
|:---------
| text (texto)
| html


### <a name="locationtype-values"></a>valores de locationType

| Valor
|:-------------------------
| default (predeterminado)
| conferenceRoom (sala de conferencias)
| homeAddress (domicilio)
| businessAddress (dirección empresarial)
| geoCoordinates (coordenadas geográficas)
| streetAddress (dirección)
| hotel
| restaurant (restaurante)
| localBusiness (empresa local)
| postalAddress (dirección postal)

### <a name="locationuniqueidtype-values"></a>valores de locationUniqueIdType

| Valor
|:-------------------------
| unknown (desconocido)
| locationStore (almacén de ubicación)
| directory (directorio)
| private (privado)
| bing


### <a name="messageactionflag-values"></a>valores de messageActionFlag

| Valor
|:-------------------------
| any (cualquiera)
| call (llamada)
| doNotForward (no reenviar)
| followUp (seguimiento)
| fyi (para su información)
| forward (reenviar)
| noResponseNecessary (respuesta no necesaria)
| read (leído)
| reply (responder)
| replyToAll (responder a todos)
| review (revisar)


### <a name="onenoteuserrole-values"></a>valores de onenoteUserRole

| Miembro      | Valor
|:------------|:------------
| Owner (propietario)       | 0
| Contributor (colaborador) | 1
| Reader (lector)      | 2
| None (ninguno)        | -1


### <a name="operationstatus-values"></a>valores de operationStatus

| Valor
|:-----------------
| NotStarted (no empezada)
| Running (en ejecución)
| Completed (completada)
| Failed (fallada)


### <a name="onenotepatchactiontype-values"></a>valores de onenotePatchActionType

| Valor
|:-------------------------
| Replace (reemplazar)
| Append (añadir)
| Delete (eliminar)
| Insert (insertar)
| Prepend (anteponer)

### <a name="onenotepatchinsertposition-values"></a>valores de onenotePatchInsertPosition

| Valor
|:-------------------------
| After (después)
| Before (antes)


### <a name="phonetype-values"></a>valores de phoneType

| Valor
|:-------------------------
| home (casa)
| business (empresa)
| mobile (móvil)
| other (otro)
| assistant (ayudante)
| homeFax (fax personal)
| businessFax (fax de empresa)
| otherFax (otro fax)
| pager (localizador)
| radio


### <a name="plannerpreviewtype-values"></a>valores de plannerPreviewType

| Valor
|:-------------------------
| automatic (automático)
| noPreview (sin vista previa)
| checklist (lista de comprobación)
| description (descripción)
| reference (referencia)


### <a name="status-values"></a>valores de Status

| Valor
|:-----------------
| active (activo)
| updated (actualizado)
| deleted (eliminado)
| ignored (ignorados)
| unknownFutureValue


### <a name="weekindex-values"></a>valores de weekIndex

| Valor
|:-------------------------
| first (primera)
| second (segunda)
| third (tercera)
| fourth (cuarta)
| last (última)


### <a name="dayofweek-values"></a>valores de dayOfWeek

| Valor
|:-------------------------
| sunday (domingo)
| monday (lunes)
| tuesday (martes)
| wednesday (miércoles)
| thursday (jueves)
| friday (viernes)
| saturday (sábado)

### <a name="recurrencepatterntype-values"></a>valores de recurrencePatternType

| Valor
|:-------------------------
| daily (diariamente)
| weekly (semanalmente)
| absoluteMonthly (absoluto mensualmente)
| relativeMonthly (relativo mensualmente)
| absoluteYearly (absoluto anualmente)
| relativeYearly (relativo anualmente)


### <a name="recurrencerangetype-values"></a>valores de recurrenceRangeType

| Valor
|:-------------------------
| endDate (fecha final)
| NoEnd (sin final)
| numbered (numerado)


### <a name="onenotesourceservice-values"></a>valores de onenoteSourceService
| Valor
|:---------------------
| Unknown (desconocido)
| OneDrive
| oneDriveForBusiness
| OnPremOneDriveForBusiness


### <a name="responsetype-values"></a>valores de responseType

| Valor
|:-------------------------
| none (ninguna)
| organizer (organizador)
| tentativelyAccepted (aceptada provisionalmente)
| accepted (aceptada)
| declined (rechazada)
| notResponded (sin respuesta)


### <a name="activitydomain-values"></a>valores de activityDomain

| Valor
|:-------------------------
| unknown (desconocido)
| work (trabajo)
| personal
| unrestricted (sin restricciones)


### <a name="websitetype-values"></a>valores de websiteType

| Valor
|:-------------------------
| other (otro)
| home (casa)
| work (trabajo)
| blog
| ata-id="undefined" class="unusedGlossaryTerm">blog


### <a name="categorycolor-values"></a>valores de categoryColor

| Miembro   |Valor    
|:---------|:--------
| none (ninguno)     | -1      
| preset0  | 0       
| preset1  | 1       
| preset2  | 2       
| preset3  | 3       
| preset4  | 4       
| preset5  | 5       
| preset6  | 6       
| preset7  | 7       
| preset8  | 8       
| preset9  | 9       
| preset10 | 10      
| preset11 | 11      
| preset12 | 12      
| preset13 | 13      
| preset14 | 14      
| preset15 | 15      
| preset16 | 16      
| preset17 | 17      
| preset18 | 18      
| preset19 | 19      
| preset20 | 20      
| preset21 | 21      
| preset22 | 22      
| preset23 | 23      
| preset24 | 24      