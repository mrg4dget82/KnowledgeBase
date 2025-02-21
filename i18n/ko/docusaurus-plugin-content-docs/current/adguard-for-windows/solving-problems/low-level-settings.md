---
title: 고급(로우 레벨) 설정 가이드
sidebar_position: 7
---

:::info

This article covers AdGuard for Windows, a multifunctional ad blocker that protects your device at the system level. To see how it works, [download the AdGuard app](https://adguard.com/download.html?auto=true)

:::

이전에는 로우 레벨 설정으로 알려진 고급 설정에는 대부분 평균적인 사용자 역량을 넘어서는 옵션이 포함되어 있으며 일상적인 사용에는 적용되지 않습니다. Windows용 AdGuard는 이러한 기능을 변경할 필요 없이 작동하도록 설계되었지만, 일부 특수한 경우나 흔하지 않은 문제를 해결할 때 추가 기능을 제공할 수 있습니다.

:::caution

*고급 설정*을 무심코 변경하면 AdGuard의 성능에 문제가 발생하거나 인터넷 연결이 끊어지거나 보안 및 개인정보가 손상될 수 있습니다. 이러한 설정은 본인이 무엇을 하고 있는지 알고 있거나 지원팀에서 요청하는 경우에만 변경하세요.

:::

## 고급 설정으로 이동하는 방법

*고급 설정*으로 이동하려면 기본 창에서 *설정 → 일반 설정* 을 클릭하고 아래로 스크롤하여 *고급 설정*으로 이동합니다. 또는 트레이 메뉴에서 *고급 → 고급 설정...* 을 선택합니다.

## 고급 설정

고급 설정을 열면 다음과 같은 옵션이 표시됩니다:

### TCP Fast Open 차단

이 기능을 활성화하면 AdGuard가 Edge 브라우저에서 TCP 빠른 열기를 차단합니다. 설정을 적용하려면 브라우저를 다시 시작해야 합니다.

### Encrypted ClientHello 사용

모든 암호화된 인터넷 연결에는 암호화되지 않은 부분이 있습니다. 이것은 연결하려는 서버의 이름이 포함된 첫 번째 패킷입니다. Encrypted Client Hello 기술은 이 문제를 해결하고 암호화되지 않은 마지막 비트의 정보를 암호화합니다. 이 기능을 사용하려면 *Encrypted ClientHello 사용* 옵션을 활성화하세요. It uses a local DNS proxy to look for the ECH configuration for the domain. ECH 구성이 발견되면 ClientHello 패킷이 암호화됩니다.

### 웹사이트의 인증서 투명성 확인

Chrome 인증서 투명성 정책에 따라 도메인의 모든 인증서를 확인합니다. If the certificate does not comply with the Chrome Certificate Transparency Policy, AdGuard will not filter the website. 반면에 Chrome은 이 사이트를 차단합니다.

### SSL/TLS 인증서 해지 확인 활성화

이 옵션을 활성화하면 비동기 OCSP 검사를 실행하여 웹사이트의 SSL/TLS 인증서가 해지되었는지 확인합니다.

최소 시간 제한 내에 OCSP 확인이 완료되면 AdGuard는 즉시 결과를 적용합니다. 인증서가 해지된 경우 연결을 차단하고 인증서가 유효한 경우 연결을 설정합니다.

확인에 시간이 너무 오래 걸리면 AdGuard가 연결을 설정하고 백그라운드에서 계속 확인합니다. 인증서가 해지되면 도메인에 대한 현재 및 향후 연결이 차단됩니다.

### 설정에서 AdGuard VPN 표시

이 옵션을 활성화하면 설정에 AdGuard VPN 탭이 표시되어 앱과 제품 웹사이트를 쉽게 열 수 있습니다.

### 전체 경로를 입력하여 필터링에서 앱 제외하기

특정 앱을 필터링하지 않도록 하기 위해서는 해당 앱의 전체 경로를 지정하면 해당 앱이 필터링에서 제외됩니다. 세미콜론으로 서로 다른 경로를 구분합니다.

### AdGuard 팝업 알림 활성화

이 기능을 활성화하면 AdGuard 팝업 알림을 볼 수 있습니다. 너무 자주 표시되지 않으며 중요한 정보만 포함되어 있습니다. 트레이 메뉴를 사용하여 마지막 팝업 알림을 불러올 수도 있습니다.

### 필터 구독 URL 자동 차단

AdGuard가 필터 구독 URL(예: `abp:subscribe` 등)을 자동으로 가로채고 사용자 정의 필터 설치 대화 상자를 열도록 하려면 이 기능을 활성화합니다.

### 리디렉션 드라이버 모드 사용

이 옵션을 활성화하면 AdGuard가 모든 트래픽을 가로채서 추가 필터링을 위해 로컬 프록시 서버로 리디렉션합니다.

이 기능이 활성화되지 않은 경우, AdGuard는 리디렉션 없이 모든 트래픽을 즉시 필터링합니다. 시스템은 인터넷에 연결되는 유일한 애플리케이션으로 AdGuard를 간주합니다(다른 애플리케이션은 AdGuard를 통해 라우팅됨). 단점은 시스템 방화벽의 효율성이 떨어질 수 있다는 것입니다. 장점은 이 접근 방식이 조금 더 빠르게 작동한다는 것입니다.

### 시스템 시작 시 메인 창 열기

이 옵션을 활성화하면 시스템이 로드된 후 기본 AdGuard 창이 열립니다. 이 설정은 *설정 → 일반 설정*에 있으며 실제 필터링 서비스가 실행되는지 여부에는 영향을 미치지 않습니다.

### 시스템 시작 시 필터링 활성화

7.12 버전부터 시스템 시작 시 AdGard 실행 옵션이 비활성화되어 있는 경우, 기본적으로 AdGard 서비스는 OS 시작 후 트래픽을 필터링하지 않습니다. 즉, AdGuard의 서비스는 '유휴' 모드에서 시작됩니다. 이 옵션을 활성화하면 앱이 실행되지 않은 상태에서도 AdGuard가 트래픽을 필터링하도록 설정할 수 있습니다.

:::note

Before v7.12, the AdGuard service started in filtering mode by default (even if the *Launch AdGuard at system start-up* was disabled). If you were satisfied with the old behavior, enable this option.

:::

### 로컬 호스트 필터링

AdGuard가 루프백 연결을 필터링하도록 하려면 확인란을 선택합니다. 이 옵션은 AdGuard VPN이 설치되어 있는 경우 항상 켜져 있으며, 그렇지 않으면 작동하지 않습니다.

### 필터링에서 지정된 IP 범위 제외

AdGuard가 특정 서브넷을 필터링하지 않도록 설정하려면 이 기능을 활성화하고 아래 **필터링에서 제외되는 IP 범위** 섹션에서 CIDR 표기법(예: 98.51.100.14/24)으로 IP 범위를 지정하세요.

### HAR 쓰기 활성화

이 옵션은 **디버깅 목적**으로만 활성화해야 합니다. 확인 표시를 선택하면 AdGuard가 필터링된 모든 HTTP 요청에 대한 정보가 포함된 HAR 1.2 형식의 파일을 생성합니다. 이 파일은 Fiddler 앱으로 분석할 수 있습니다. 웹 브라우징 속도가 상당히 느려질 수 있습니다.

### 일반 HTTP 요청에 추가 공백 추가

HTTP 메서드와 URL 사이에 공백을 추가하고 심층 패킷 검사를 피하기 위해 '호스트:' 필드 뒤에 공백을 제거합니다. 예를 들어,

`GET /foo/bar/ HTTP/1.1
Host: example.org 요청은`

다음과 같이 변환됩니다.

`GET  /foo/bar/ HTTP/1.1
Host: example.org`

이 설정은 스텔스 모드에서 *DP로부터 보호* 옵션이 활성화된 경우에만 적용됩니다.

### 초기 TLS 패킷의 조각화 크기 조정

심층 패킷 검사를 피하기 위해 TCP 패킷 조각화의 크기를 지정합니다. This option only affects secured (HTTPS) traffic.

이 옵션을 활성화하면 AdGuard는 초기 TLS 패킷(ClientHello 패킷)을 두 부분으로 분할합니다. 첫 번째 부분은 지정된 길이를 가지며 두 번째 부분은 나머지 길이(전체 초기 TLS 패킷의 길이까지)를 가집니다.

Valid values: 1–1500. 잘못된 크기를 지정하면 시스템에서 선택한 값이 사용됩니다. 이 설정은 스텔스 모드에서 *DP로부터 보호* 옵션이 활성화된 경우에만 적용됩니다.

### 일반 HTTP 조각 크기

HTTP 요청 조각화의 크기를 조정합니다. 이 옵션은 일반 HTTP 트래픽에만 영향을 줍니다. 이 옵션을 활성화하면 AdGuard는 초기 패킷을 두 부분으로 분할하여 첫 번째 패킷은 지정된 길이로, 두 번째 패킷은 전체 원본 패킷의 길이까지 나머지 부분을 차지합니다.

Valid values: 1–1500. 잘못된 크기를 지정하면 시스템에서 선택한 값이 사용됩니다. 이 설정은 스텔스 모드에서 *DP로부터 보호* 옵션이 활성화된 경우에만 적용됩니다.

### QUIC 보기

필터링 로그에 QUIC 프로토콜 레코드를 표시할 수 있습니다. 이 옵션은 차단된 요청에 대해서만 작동합니다.

### TCP 연결 유지 사용

유휴 연결을 통해 주기적으로 TCP 패킷을 전송하여 연결이 활성화되어 있는지 확인하고 NAT 시간 제한을 갱신합니다. 이 옵션은 일부 ISP가 사용하는 엄격한 NAT(네트워크 주소 변환) 설정을 우회하는 데 유용할 수 있습니다.

### TCP 연결 유지 간격

킵얼라이브 프로브를 보내기 전에 유휴 기간을 초 단위로 지정할 수 있습니다. If 0 is specified, the value selected by the system will be used.

:::note

This setting only works when the *Enable TCP keepalive* option is enabled.

:::

### TCP 연결 유지 시간 초과

Here you can specify time in seconds before sending another keepalive probe to an unresponsive peer. 0을 지정하면 시스템에서 선택한 값이 사용됩니다.

:::note

This setting only works when the *Enable TCP keepalive* option is enabled.

:::

### Java 차단

일부 웹사이트와 웹 서비스는 여전히 Java 플러그인을 지원합니다. Java 플러그인의 기반이 되는 API에는 심각한 보안 취약점이 있습니다. 보안을 위해 이러한 플러그인을 비활성화할 수 있습니다. 그러나 *Java 차단* 옵션을 사용하기로 결정하더라도 자바스크립트는 계속 활성화됩니다.

### DNS 서버 시간 초과 기간

이 필드에서 AdGuard가 폴백 DNS 서버를 사용하기 전에 선택한 DNS 서버의 응답을 기다리는 시간(밀리초)을 지정할 수 있습니다. 이 필드를 채우지 않거나 잘못된 값을 입력하면 5000이라는 값이 사용됩니다.

### DNS-over-HTTPS에 HTTP/3 사용

선택한 업스트림이 이 프로토콜을 지원하는 경우, DNS-over-HTTPS 업스트림에 HTTP/3을 활성화하여 연결을 가속화합니다. 즉, 이 옵션을 활성화해도 모든 DNS 요청이 HTTP/3을 통해 전송된다는 보장은 없습니다.

### 폴백 DNS 업스트림 사용

Normal queries will be redirected to the fallback upstream if all DNS requests to the selected upstreams fail.

### DNS 업스트림 쿼리를 병렬로 수행

All upstreams will be queried in parallel and the first response is returned. DNS 쿼리는 병렬로 이루어지므로 이 기능을 활성화하면 인터넷 속도가 빨라집니다.

### 실패한 DNS 쿼리에 항상 응답

전달된 각 업스트림과 폴백 도메인에서 주소 확인에 실패한 경우 DNS 요청에 대한 응답은 `SERVFAIL`이 됩니다.

### 보안 DNS 요청 필터링 사용

AdGuard will redirect secure DNS requests to the local DNS proxy, in addition to plain DNS requests.

### 호스트 규칙에 대한 차단 모드

[호스트 규칙 구문](https://adguard-dns.io/kb/general/dns-filtering-syntax/#etc-hosts-syntax)을 기반으로 DNS 규칙에 의해 차단된 도메인에 대해 AdGuard가 응답하는 방식을 선택할 수 있습니다.

* 'Refused' 오류로 회신
* 'NxDomain' 오류로 회신
* 사용자 정의 IP 주소로 회신

### adblock-style 규칙을 위한 차단 모드

여기에서 [adblock-style 구문](https://adguard-dns.io/kb/general/dns-filtering-syntax/#adblock-style-syntax)을 기반으로 DNS 규칙에 의해 차단된 도메인에 AdGuard가 응답하는 방식을 선택할 수 있습니다.

* 'Refused' 오류로 회신
* 'NxDomain' 오류로 회신
* 사용자 정의 IP 주소로 회신

### 사용자 정의 IPv4

호스트 규칙의 차단 모드 또는 adblock-style 규칙의 차단 모드에서 사용자 정의 IP 주소를 선택한 경우, 차단된 A 요청에 대한 응답으로 이 IP 주소가 반환됩니다. IP 주소가 지정되지 않은 경우 AdGuard는 기본 'Refused' 오류로 응답합니다.

### 사용자 지정 IPv6

호스트 규칙의 차단 모드 또는 adblock-style 규칙의 차단 모드에서 사용자 정의 IP 주소를 선택한 경우, 차단된 AAAA 요청에 대한 응답으로 이 IP 주소가 반환됩니다. IP 주소가 지정되지 않은 경우 AdGuard는 기본 'Refused' 오류로 응답합니다.

### 폴백 서버

여기에서 주 서버가 다음 섹션에서 지정한 시간 제한 기간 내에 응답하지 않을 경우, DNS 요청을 다시 라우팅할 대체 DNS 서버를 지정할 수 있습니다. 세 가지 옵션 중에서 선택할 수 있습니다.

* 폴백 서버를 사용하지 않음
* 시스템 기본 서버 사용
* 사용자 정의 서버 사용

### ECH 차단

이 옵션을 활성화하면 AdGuard는 응답에서 암호화된 클라이언트 헬로 매개변수를 제거합니다.

### 사용자 정의 폴백 서버 목록

AdGuard가 사용자 정의 폴백 서버를 사용하도록 하려면 이 섹션에 한 줄에 하나씩 나열하세요.

### 사용자 정의 부트스트랩 주소 목록

부트스트랩은 앞서 *DNS 보호*에서 선택한 보안 DNS 서버의 IP 주소를 가져오는 데 사용되는 중간 DNS 서버입니다. 이러한 '중간 지점'은 서버 주소를 문자로 표시하는 프로토콜(예: DNS-over-TLS)을 사용할 때 필요합니다. 이 경우 부트스트랩이 번역기 역할을 하여 문자를 시스템에서 이해할 수 있는 숫자로 변환합니다.

기본적으로 시스템 DNS DNS 리졸버가 사용되며 초기 부트스트랩 요청은 포트 53을 통해 이루어집니다. 이 방법이 적합하지 않은 경우 암호화된 DNS 서버의 주소를 확인하는 데 사용할 DNS 서버의 IP 주소를 여기에 나열하세요. 지정된 IP 주소는 나열된 순서대로 적용됩니다. 잘못된 주소를 지정하거나 주소를 전혀 지정하지 않으면 시스템 IP가 사용됩니다.

### DNS 예외

여기에 나열된 도메인에 대한 모든 DNS 요청은 앱 설정에 지정된 DNS 서버가 아닌 시스템 기본 DNS 서버로 리디렉션됩니다. 또한 이러한 요청에는 DNS 차단 규칙이 적용되지 않습니다.

### 지정된 Wi-Fi 네트워크 이름(SSID)을 DNS 필터링하지 않기

DNS protection will not include Wi-Fi networks listed in this section. Wi-Fi 네트워크 이름(SSID)을 한 줄에 하나씩 지정합니다. 특정 Wi-Fi 네트워크가 이미 AdGuard Home 또는 다른 DNS 보호 시스템에 의해 보호되고 있는 경우 유용할 수 있습니다. 이 경우 DNS 요청을 다시 필터링할 필요가 없습니다.
