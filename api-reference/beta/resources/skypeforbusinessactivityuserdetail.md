---
title: tipo de recurso skypeForBusinessActivityUserDetail
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: e847cbf469db3be55c8c12ebf31056a262962886
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27828654"
---
# <a name="skypeforbusinessactivityuserdetail-resource-type"></a>tipo de recurso skypeForBusinessActivityUserDetail

## <a name="properties"></a>Propiedades

| Propiedad                                 | Tipo              |
| :--------------------------------------- | :---------------- |
| totalPeerToPeerSessionCount              | Int64             |
| totalOrganizedConferenceCount            | Int64             |
| totalParticipatedConferenceCount         | Int64             |
| peerToPeerLastActivityDate               | Fecha              |
| organizedConferenceLastActivityDate      | Fecha              |
| participatedConferenceLastActivityDate   | Fecha              |
| peerToPeerIMCount                        | Int64             |
| peerToPeerAudioCount                     | Int64             |
| peerToPeerAudioMinutes                   | Int64             |
| peerToPeerVideoCount                     | Int64             |
| peerToPeerVideoMinutes                   | Int64             |
| peerToPeerAppSharingCount                | Int64             |
| peerToPeerFileTransferCount              | Int64             |
| organizedConferenceIMCount               | Int64             |
| organizedConferenceAudioVideoCount       | Int64             |
| organizedConferenceAudioVideoMinutes     | Int64             |
| organizedConferenceAppSharingCount       | Int64             |
| organizedConferenceWebCount              | Int64             |
| organizedConferenceDialInOut3rdPartyCount | Int64             |
| organizedConferenceCloudDialInOutMicrosoftCount | Int64             |
| organizedConferenceCloudDialInMicrosoftMinutes | Int64             |
| organizedConferenceCloudDialOutMicrosoftMinutes | Int64             |
| participatedConferenceIMCount           | Int64             |
| participatedConferenceAudioVideoCount   | Int64             |
| participatedConferenceAudioVideoMinutes | Int64             |
| participatedConferenceAppSharingCount   | Int64             |
| participatedConferenceWebCount          | Int64             |
| participatedConferenceDialInOut3rdPartyCount | Int64             |
| reportRefreshDate                        | Fecha              |
| userPrincipalName                        | Cadena            |
| isDeleted                                | Booleano           |
| deletedDate                              | Fecha              |
| lastActivityDate                         | Fecha              |
| assignedProducts                         | Colección String |
| reportPeriod                             | String            |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.skypeForBusinessActivityUserDetail"
} -->

```json
{
  "totalPeerToPeerSessionCount": 1024, 
  "totalOrganizedConferenceCount": 1024, 
  "totalParticipatedConferenceCount": 1024, 
  "peerToPeerLastActivityDate": "Date", 
  "organizedConferenceLastActivityDate": "Date", 
  "participatedConferenceLastActivityDate": "Date", 
  "peerToPeerIMCount": 1024, 
  "peerToPeerAudioCount": 1024, 
  "peerToPeerAudioMinutes": 1024, 
  "peerToPeerVideoCount": 1024, 
  "peerToPeerVideoMinutes": 1024, 
  "peerToPeerAppSharingCount": 1024, 
  "peerToPeerFileTransferCount": 1024, 
  "organizedConferenceIMCount": 1024, 
  "organizedConferenceAudioVideoCount": 1024, 
  "organizedConferenceAudioVideoMinutes": 1024, 
  "organizedConferenceAppSharingCount": 1024, 
  "organizedConferenceWebCount": 1024, 
  "organizedConferenceDialInOut3rdPartyCount": 1024, 
  "organizedConferenceCloudDialInOutMicrosoftCount": 1024, 
  "organizedConferenceCloudDialInMicrosoftMinutes": 1024, 
  "organizedConferenceCloudDialOutMicrosoftMinutes": 1024, 
  "participatedConferenceIMCount": 1024, 
  "participatedConferenceAudioVideoCount": 1024, 
  "participatedConferenceAudioVideoMinutes": 1024, 
  "participatedConferenceAppSharingCount": 1024, 
  "participatedConferenceWebCount": 1024, 
  "participatedConferenceDialInOut3rdPartyCount": 1024, 
  "reportRefreshDate": "Date", 
  "userPrincipalName": "String", 
  "isDeleted": true, 
  "deletedDate": "Date", 
  "lastActivityDate": "Date", 
  "assignedProducts": ["String"], 
  "reportPeriod": "String"
}
```
