---
title: 비즈니스용 Skype Online 플랜 1 구독을 새로운 Office 365 버전으로 마이그레이션 | 파트너 센터
ms.topic: article
ms.date: 03/15/2019
ms.service: partner-dashboard
ms.subservice: partnercenter-csp
Description: 비즈니스용 Skype Online 요금제 1 구독이 지원 되는 SKU 옵션으로 전환 되는 고객을 전환 합니다. 구독의 매년 종료 날짜 전에 새 구독으로 고객을 이동 하는 것이 좋습니다.
author: LauraBrenner
ms.author: labrenne
keywords: 비즈니스용 Skype 플랜, Skype 사용 중지, Office 365
ms.localizationpriority: medium
ms.custom: seodec18
ms.openlocfilehash: 2afe07797ca0e4e255e88a86149bfe532d29a426
ms.sourcegitcommit: dbaa6c2e8a0e6431f1420e024cca6d0dd54f1425
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/06/2019
ms.locfileid: "73654046"
---
# <a name="migrate-skype-for-business-online-plan-1-subscriptions-to-newer-office-365-versions"></a>비즈니스용 Skype Online 플랜 1 구독을 새로운 Office 365 버전으로 마이그레이션

**적용 대상**

- 파트너 센터

비즈니스용 Skype Online 플랜 1은 2018년 8월 1일 기준으로 사용 중지됩니다. 이 날짜 이후에 고객은 더 이상 새로운 비즈니스용 Skype Online 플랜 1 구독을 구입할 수 없으며 기존 구독이 만료되면 자동으로 갱신되지 않고 갱신 옵션도 제공하지 않습니다. 비즈니스용 Skype Online 플랜 1 구독의 세부 정보 페이지에서 구독 상태가 "[날짜]에 자동 갱신"에서 "[날짜]에 만료"로 변경되었습니다.  

고객에게 연속성을 보장하기 위해, 비즈니스용 Skype Online 플랜 1 구독이 곧 만료되는 고객을 아래에 나열된 지원되는 SKU 옵션으로 전환해야 합니다. 고객에 대 한 서비스 중단을 방지 하려면 구독의 연간 종료 날짜 이전에 새 구독으로 고객을 이동 하는 것이 좋습니다. 

>[!NOTE]
>비즈니스용 Skype Online 플랜 1 상용 및 정부 SKU는 모두 사용 중지됩니다.

API(CREST 또는 파트너 센터)를 사용하는 경우 auto renew = False 속성과 함께 구독의 종료 날짜를 확인하여 곧 만료되는 구독을 검색하세요. 비즈니스용 Skype Online 플랜 1 구독은 2018년 9월 1일에 auto renew=False로 설정됩니다. 언제든지 고객을 새 요금제로 이동할 수 있습니다. 

## <a name="skype-for-business-online-plan-1-replacement-plans"></a>비즈니스용 Skype Online 플랜 1 사용 중지 계획

새로운 요금제를 통해 고객은 Office 365의 새로운 기능을 활용할 수 있습니다. 가격 정보는 가격 목록에서 찾을 수 있으며 파트너 센터에 목록표가 제공됩니다. 

- 옵션 1: Office 365 Enterprise F1
- 옵션 2: Microsoft 365 Enterprise F1
- 옵션 3: Other Office 365 플랜

|**기능과**    |**옵션 1**   |**옵션 2**   |**옵션 3**   |
|:-----------------|:-----------------|:-------------|:------------|
|비즈니스용 Skype Online 플랜 1에 포함된 모든 기능 사용|예   |예   |예   |
|IM 및 상태 확인 |예   |예   |예   |
|IP를 통한 피어 투 피어 오디오 및 비디오|예   |예   |예   
|인증된 사용자로 회의 참여| 예   |예   |예   |

## <a name="transition-customers-to-new-product-plans"></a>새 제품 요금제로 고객 전환

Microsoft는 지속적으로 파트너에게 새 제품 및 서비스를 제공합니다. 다음과 같은 경우 파트너는 고객을 새 서비스로 업그레이드하거나 결국 종료될 SKU의 구독을 마이그레이션해야 할 수 있습니다. 사용 중지된 SKU에서 새 SKU로 고객을 마이그레이션하려면 다음 단계를 따라야 합니다.

- 새 구독 구매
- 현재 사용자 라이선스 다시 할당
- 이전 구독 취소

### <a name="migrate-your-customers-to-new-plans"></a>고객을 새 플랜으로 마이그레이션

1. 새 구독을 구입 하려면 **파트너 센터 메뉴**에서 **고객**을 선택 하 고 이동할 고객을 선택한 다음 **구독 추가**를 선택 합니다.

2. 카탈로그에서 구매할 구독을 선택하고(이 경우 아래 옵션 중 하나), 라이선스 수를 입력한 다음 **제출**을 선택합니다. 

이제 고객에 게 이전 구독과 새 구독, 이전에는 비즈니스용 Skype Online 계획 1 구독 및 새 ' 대상 ' 구독이 모두 포함 되어 있어야 합니다 (예: 옵션 1-Office 365 Enterprise F1).

3. 고객의 사용자 라이선스를 재할당 하려면 **파트너 센터** 메뉴에서 **고객**을 선택 하 고 이동 하는 고객을 선택한 다음 **사용자 및 라이선스**를 선택 합니다. 고객의 사용자 및 라이선스 페이지가 열립니다.

4. 사용자 라이선스를 다시 할당하려면 다시 할당할 사용자를 선택한 다음 **라이선스 관리**를 선택합니다.

5. **라이선스 관리** 페이지에서 비즈니스용 Skype Online 플랜 1 라이선스 확인란의 선택을 취소한 다음 고객을 이동할 구독의 새로운 서비스 요금제를 선택합니다.

6. **제출**을 선택합니다. 확인 페이지에 새 라이선스 할당이 나열됩니다. 라이센스 할당이 필요한 다른 사용자에 대해 이 프로세스를 계속합니다.

사용자 라이선스를 새 서비스로 이동한 후 고객 수준에서 사용 중지된 구독을 안전하게 취소할 수 있습니다.

7. **파트너 센터** 메뉴에서 **고객**을 선택 합니다. 구독 취소 중인 고객을 선택합니다.

8. 구독 세부 정보 페이지에서 구독을 **일시 중단됨**으로 설정합니다.

9. **제출**을 선택합니다.

이전 구독이 일시 중단되고 새 구독이 활성화됩니다. 일시 중단된 구독은 120일 후 자동으로 프로비전이 해제됩니다. 이전 구독에 대해서는 고객에게 추가 비용이 발생하지 않습니다.

