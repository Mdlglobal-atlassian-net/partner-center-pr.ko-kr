---
title: 사용 빈도 기반 조정 파일 | 파트너 센터
ms.topic: article
ms.date: 01/14/2020
description: 사용 빈도 기반 조정 파일의 모든 항목은 예제와 함께 설명 됩니다.
ms.assetid: ''
author: LauraBrenner
ms.author: labrenne
ms.localizationpriority: medium
ms.openlocfilehash: e4ce3427f52ccde8f61fa553f3fa0af79bff0a95
ms.sourcegitcommit: fc43ee25d405ef3dc673edd884c877bfc62ad6aa
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/15/2020
ms.locfileid: "76021747"
---
# <a name="usage-based-file-fields"></a>사용량 기준 파일 필드

적용 대상:

- 파트너 센터
- Microsoft Cloud for US Government 파트너 센터

고객의 사용량과 요금을 조정 하려면 **ResellerID**, **ResellerName**및 **ResellerBillableAccount** 를 조정 파일에서 파트너 센터의 **고객 이름** 및 **구독 ID** 와 비교 합니다.

## <a name="fields-in-usage-based-reconciliation-files"></a>사용량 기반 조정 파일의 필드

다음 필드에서는 사용된 서비스와 요금을 설명합니다.

| Column | 설명 | 샘플 값 |
| ------ | ----------- | ------------ |
| PartnerId | GUID 형식의 파트너 식별자입니다. | *DA41BC5F-C52D-4464-8A8D-8C8DCC43503B* |
| PartnerName | 파트너 이름입니다. | *Contoso, l t d.* |
| PartnerBillableAccountId | 파트너 계정 식별자입니다. | *1010578050* |
| CustomerCompanyName | 파트너 센터에 보고 된 고객의 조직 이름입니다. *시스템 정보를 사용 하 여 송장을 조정 하는 데 매우 중요 합니다.* | *고객 테스트* |
| MpnId | CSP 파트너의 MPN 식별자입니다. | *4390934* |
| ResellerMpnId | 구독에 대 한 레코드 대리점의 MPN 식별자입니다.  |
| InvoiceNumber | 지정한 트랜잭션이 표시되는 송장 번호입니다. | *D020001IVK* |
| ChargeStartDate | 이전에 청구되지 않은 잠재 사용량 데이터 날짜(이전 청구 주기)를 표시할 경우를 제외하고 청구 주기의 시작 날짜입니다. 시간은 항상 해당하는 날의 시작인 0:00입니다. | *2/1/2019 0:00* |
| ChargeEndDate | 이전에 청구되지 않은 잠재 사용량 데이터 날짜(이전 청구 주기)를 표시할 경우를 제외하고 청구 주기의 종료 날짜입니다. 시간은 항상 해당 일의 마지막인 23:59입니다. | *2/28/2019 23:59* |
| SubscriptionId | Microsoft 청구 플랫폼에서 구독의 고유 식별자. 지원에 문의할 때 구독을 식별 하는 데 유용할 수 있습니다. 조정에 사용 되지 않습니다. *파트너 관리 콘솔의 **구독 ID** 와 동일 하지 않습니다.* | *usCBMgAAAAAAAAIA* |
| SubscriptionName | 서비스 제공의 애칭입니다. | *Microsoft Azure* |
| SubscriptionDescription | LOB(기간 업무) 서비스 제공입니다. | *Microsoft Azure* |
| OrderID | Microsoft 청구 플랫폼에서 주문의 고유 식별자입니다. 지원에 문의할 때 구독을 식별 하는 데 유용할 수 있습니다. 조정에 사용 되지 않습니다. | *566890604832738111* |
| ServiceName | 해당 Azure 서비스의 이름 | *가상 컴퓨터* |
| ServiceType | Azure 서비스의 특정 유형입니다. | *Service Bus – 개별 또는 Pack*, *SQL Azure database – Business 또는 Web Edition* |
| ResourceGuid | 모든 서비스 데이터 및 가격 책정 구조에 대한 특정 고유 식별자 | *DA41BC5F-C52D-4464-8A8D-8C8DCC43503B* |
| ResourceName | Azure 리소스의 이름 | *데이터 전송 (GB)* , *데이터 송신(GB)* |
| 국가 | 사용이 적용 되는 지역입니다. 요금은 지역에 따라 달라 지므로 데이터 전송에 속도를 할당 하는 데 주로 사용 됩니다. | *아시아 태평양*, *유럽*, *라틴 아메리카*, *북아메리카* |
| Sku | 제안에 대 한 고유한 Microsoft 식별자입니다. | *7UD-00001* |
| DetailLineItemId | 지정 된 청구 기간에 서비스 또는 리소스에 대해 서로 다른 비율을 지정 하는 식별자 및 수량입니다. Azure 계층화 된 가격 책정의 경우 청구 가능 단위의 특정 수량에 대해 하나의 요금이 청구 된 후 해당 수량 이후 다른 요금이 청구 될 수 있습니다. | *1* |
| ConsumedQuantity | 보고 기간 동안 사용 된 서비스의 양 (예: 시간 또는 GB)입니다. 이전 보고 기간의 미청구 사용량도 포함됩니다. | *11* |
| IncludedQuantity | 제품의 일부로 포함된 단위. 일반적으로 CSP에는 표시 되지 않습니다. | *0* |
| OverageQuantity | 제품의 일부로 포함 되지 않은 단위입니다. 파트너는이를 지불 해야 합니다. **ConsumedQuantity** 마이너스 **IncludedQuantity**와 같습니다. | *11* |
| ListPrice | 제공 가격은 구독의 시작 날짜에 적용 됩니다. | *$0.0808* |
| PretaxCharges | 가장 가까운 센트로 반올림 된 **List3| st** 를 곱한 **값과 같습니다**. | *$0.085* |
| TaxAmount | 세금 청구 금액입니다. 시장의 세금 규칙 및 특정 상황을 기준으로 합니다. | *$0.08* |
| PostTaxTotal | 세금을 적용할 수 있는 경우 세금을 적용한 후의 총액 | *$0.93* |
| Currency | 통화 형식. 각 청구 엔터티의 통화는 한 가지만 가능합니다. 첫 번째 청구서와 일치 하는지 확인 한 후 주요 청구 플랫폼 업데이트 후에 확인 합니다. | *EUR* |
| PretaxEffectiveRate | 세전 단가. **PretaxCharges** **로 나눈 값이 가장**가까운 센트로 반올림 됩니다. | *$0.08* |
| PostTaxEffectiveRate | 세후 단가. **PostTaxTotal** **로 나눈 값이 가장**가까운 센트로 반올림 됩니다. 또는 가장 가까운 센트로 반올림 된 **PretaxEffectiveRate** 와 같음 (unit tax)과 동일 합니다. | *$0.08* |
| ChargeType | 요금 또는 조정 [의 유형](recon-file-charge-types.md) 입니다. | [요금 청구 유형](recon-file-charge-types.md)을 참조 하세요. |
| CustomerId | GUID 형식의 고객에 대 한 고유한 Microsoft 식별자입니다. | *ORDDC52E52FDEF405786F0642DD0108BE4* |
| DomainName | 고객의 도메인 이름입니다. 두 번째 청구 주기가 될 때까지 이 필드는 빈 상태로 나타날 수 있습니다. | *example.onmicrosoft.com* |
| BillingCycleType | 시간 청구 빈도.| **매월**  |
| Unit | 리소스 **이름의**단위입니다. | *GB* 또는 *시간* |
| CustomerBillableAccount | Microsoft 청구 플랫폼의 고유 계정 식별자입니다. | *1280018095* |
| UsageDate | 서비스 배포 날짜 | *2/1/2019 0:00* |
| MeteredRegion | 해당 지역 내에서 데이터 센터의 위치를 식별 합니다 (이 값이 적용 되 고 채워진 서비스의 경우). | *동아시아*, *남부 동아시아*, *유럽*, *유럽 서부* *, 미국 중 북부, 미국* 중 *북부* |
| MeteredService | **ServiceName** 열에서 구체적으로 식별 되지 않은 개별 Azure 서비스 사용을 식별 합니다. 예를 들어 데이터 전송은 **ServiceName** 열에 *Microsoft Azure-All Services* 로 보고 됩니다. | *Accesscontrol-namespace*, *CDN*, *계산*, *데이터베이스*, *ServiceBus*, *저장소* |
| MeteredServiceType | Azure 서비스 사용에 대 한 추가 설명을 제공 하는 **MeteredService** 필드에 대 한 부제목입니다. | *외부* |
| 프로젝트 | 해당 서비스 인스턴스에 대한 사용자 정의 이름입니다. | *ORDDC52E52FDEF405786F0642DD0108BE4* |
| ServiceInfo | 지정 된 날짜에 프로 비전 되 고 사용 된 Azure Service Bus 연결의 수입니다. | *1.000000 연결/30 일* (30 일 동안 개별적으로 프로 비전 한 경우), *25 개의 연결/30 일 – 사용 됨: 1.000000* (프로 비전 된 Service Bus 연결의 25 개 팩이 있고 해당 날짜에 1을 사용 하는 경우) |
