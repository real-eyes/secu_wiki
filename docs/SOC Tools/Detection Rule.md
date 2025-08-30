## Snort Rule / Suricata
네트워크 탐지 정책으로 IPS, IDS 그리고 NGFW 등에 사용됩니다. 실질적인 Device에 도달하기 전에 탐지 및 차단하는 것이 목적이기 때문에 Blue Team이 알아야 할 탐지 정책 중 하나입니다.

대체로 악성 트래픽을 잡고자 하는 니즈가 많을텐데 취약점 개념 증명, 실질적인 정책 테스트는 어떻게 해야할까요? 관련 정책을 획득하고 싶을 때 아래의 사이트를 참고하면 좋습니다.

- [CISCO Talos, Snort](https://www.snort.org/)
    - Sourcefire를 인수한 CISCO에서 위협 인텔리전스팀 Talos에 편입 후 관리 중입니다. 무료로도 사용 할 수 있지만, 유료로 사용한다면 최신 정책을 획득 할 수 있습니다. 제가 생각하기로는 그 가격조차 비싸다고 판단되지 않습니다.
- [Proofpoint Emerging Threats Rules](https://rules.emergingthreatspro.com/open/)
    - Proofpoint에서 제공하는 정책입니다. 대체로 Suricata를 통한 IDS를 구현할 때 많이 쓰이며, Snort Rule과 Suricata Rule 둘 다 제공하는 모습을 보입니다.
    - 다만, 유료 정책은 알 수 없습니다.

## Yara Rule
쉽게 말해 악성파일 탐지 정책으로 주로, 악성코드를 식별하기 위해 사용합니다. 관련 솔루션으로는 AV(Anti-Virus), EDR(Endpoint Detection and Response), Email Security 솔루션 등에 쓰입니다.

Yara Rule은 아쉽게도 위의 Snort Rule처럼 특정 기업이 관리하는 사이트를 찾을 수 없었습니다. 

- [Github, Yara-Rules/rules](https://github.com/Yara-Rules/rules): 대표적인 Yara rule 기본 저장소입니다.
- [Github, Awesome YARA](https://github.com/InQuest/awesome-yara): Yara Rule 관련된 저장소를 공유해주는 사이트입니다.

## Sigma Rule
Sigma Rule은 개념이 좀 다른데요, 네트워크를 담당하는 Snort Rule, 파일을 탐지하는 Yara Rule과 다르게 SIEM 정책처럼 로그 기반 탐지 포맷으로 이해하면 될 것 같습니다.

관리 주체는 [SigmaHQ](https://sigmahq.io/)이며, 이 분야의 상업적으로 사용하는 대표 주자는 [SOC Prime](https://socprime.com/)입니다.

- [SigmaHQ/sigma](https://github.com/SigmaHQ/sigma): 약 2,000개에 가까운 정책이 있습니다. 참고하면 좋은 자료들이 많습니다.

Q. 근데 왜 이런 포맷을 만든걸까요?
A. 저는 좋은 정보보안 시스템을 구축하고 유지보수 하는 것은 천재 혼자서 이룩할 수 없다고 생각을 합니다. 만약에 괜찮은 정책이 있어서 공유를 하려는데 제가 알지 못하는 kql, spl, elastic query 등을 통해서 공유를 받았다고 합시다. 그걸 써먹으려면 타 SIEM에 종속된 쿼리를 알아야하고 테스트까지 수행해야 하는데 이는 많은 공수가 들어갑니다. 이러한 표준 체계를 만듦으로써 공유된 정책에 인사이트를 얻고 정책 적용하는데 수고가 덜 들어 갈 것으로 보입니다.

하지만, 현업에 계신 분도 Sigma Rule을 당장 알 필요는 없다고 생각합니다.

## Open SIEM Rules
벤더사에서도 SIEM 정책을 Open한 케이스를 소개합니다.

- Splunk
    - [Splunk, Github](https://github.com/splunk/security_content)
    - [Splunk, Detections](https://research.splunk.com/detections/)
- Elastic
    - [Elastic, Github](https://github.com/elastic/detection-rules)
    - [Elastic](https://www.elastic.co/guide/en/security/current/prebuilt-rules.html)
- Google SecOps
    - [Chronicle/detection-rules](https://github.com/chronicle/detection-rules)
- Microsoft Azure-Sentinel
    - [Azure Sentinel](https://github.com/Azure/Azure-Sentinel)
- Fortinet(Sigma Rule을 Fortinet Query로 변환)
    - [Fortinet](https://filestore.fortinet.com/docs.fortinet.com/fsiem/Public_Resource_Access/7_3_0/rules/rule_descriptions.htm)