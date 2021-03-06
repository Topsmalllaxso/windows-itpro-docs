---
title: Score methods and properties
description: Retrieves your organization's exposure score, device secure score, and exposure score by machine group
keywords: apis, graph api, supported apis, score, exposure score, device secure score, exposure score by machine group
search.product: eADQiWindows 10XVcnh
ms.prod: w10
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dolmont
author: DulceMontemayor
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance 
ms.topic: article
---

# Score resource type

**Applies to:** [Microsoft Defender Advanced Threat Protection (Microsoft Defender ATP)](https://go.microsoft.com/fwlink/p/?linkid=2069559)

- Want to experience Microsoft Defender ATP? [Sign up for a free trial.](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Prerelease information](../../includes/prerelease.md)]

## Methods
Method |Return Type |Description
:---|:---|:---
[Get exposure score](get-exposure-score.md) | [Score](score.md) | Get the organizational exposure score.
[Get device secure score](get-device-secure-score.md) | [Score](score.md) | Get the organizational device secure score.
[List exposure score by machine group](get-machine-group-exposure-score.md)| [Score](score.md) | List scores by machine group.


## Properties
Property |	Type	|	Description
:---|:---|:---
Score | Double | The current score.
Time | DateTime | The date and time in which the call for this API was made.
RbacGroupId | Nullable Int | RBAC Group ID.


### Response example for getting machine groups score:

```
GET https://api.securitycenter.windows.com/api/exposureScore/byMachineGroups
```

```json
{
    "@odata.context": "https://api-us.securitycenter.windows.com/api/$metadata#ExposureScore",
    "value": [
        {
            "time": "2019-12-03T07:26:49.9376328Z",
            "score": 41.38041766305988,
            "rbacGroupId": 10
        },
        {
            "time": "2019-12-03T07:26:49.9376375Z",
            "score": 23.58823563070858,
            "rbacGroupId": 5
        },
        {
            "time": "2019-12-03T07:26:49.9376382Z",
            "score": 37.403726933165366,
            "rbacGroupId": 11
        },
        {
            "time": "2019-12-03T07:26:49.9376388Z",
            "score": 26.323200116475423,
            "rbacGroupId": 9
        }
    ]
}
 

```
