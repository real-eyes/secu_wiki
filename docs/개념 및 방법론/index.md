
## 프레임워크 모음

### Platform(하드웨어 및 소프트웨어 버전, 릴리즈 관리 체계)

- CPE (Common Platform Enumeration)
    - [NIST](https://nvd.nist.gov/products/cpe): 2025년 기준 현재 관리 주체
    - [MITRE](https://cpe.mitre.org/): 관리 주체가 NIST로 이관


### Vulnerabilities (취약점 관리 체계)
- **CVE (Common Vulnerabilities and Exposures)**
    - 마이터(MITRE)에서 개발했으며, 사실상 표준 취약점 관리 체계
    - [MITRE](https://www.cve.org/): https://www.cve.org/
    - [NIST](https://nvd.nist.gov/vuln/search#/nvd/home?resultType=records): https://nvd.nist.gov/vuln/search#/nvd/home?resultType=records
- KVE
    - 하드웨어/소프트웨어 공급사 공지를 확인
- [CNVD (China National Vulnerability Database)](https://www.cnvd.org.cn/)
    - 실제 관제를 수행함에 있어 중국의 프레임워크를 참고해야 할 수 있다.
- [JVN (Japan Vulnerability Notes)](https://jvn.jp/en/)
    - JPCERT와 IPA에서 운영되는 취약점 정보 및 해결책을 제공, 일본 제품군을 사용한다면 확인
    - 참고로, TrendMicro는 일본회사이기 때문에 JVN에 관련 취약점 목록이 나온다.
- [EUVD (European Vulnerability Database)](https://euvd.enisa.europa.eu/)
    - ENISA에서 운영 중인 취약점 분류 체계로 사이트에 들어가면 CVE와 GSD 등 취약점 체계와 매핑이 되어 있음을 알 수 있다.
- [OSV (Open Source Vulnerabilities)](https://osv.dev/)
    - 구글이 주도하는 오픈 소스 소프트웨어의 취약점 데이터베이스, 해당 사이트에 오픈소스 취약점 스캐너 또한 제공한다.
- [GSD (Global Security Database)](https://github.com/cloudsecurityalliance/gsd-database/)
    - 2025년에 확인 결과 취약점 매핑 등이 이루어지지 않는 것을 보아서는 중단 또는 정체된 프로젝트로 보임. 관리 주체가 없기 때문에 사실상 성공하기 힘든 것으로 보인다.

### 보안 약점 프레임워크
- [**CWE (Common Weakness Enumeration)**](https://cwe.mitre.org/)
    - 공통 보안 약점 목록, https://cwe.mitre.org/
    - 공격을 받는 입장으로써 공격 분류를 CWE로 하는 경우가 있다.

### 보안 공격 프레임워크
- [**CAPEC (Common Attack Pattern Enumeration and Classification)**](https://capec.mitre.org/)
    - 공통 보안 공격 패턴 목록 및 분류, https://capec.mitre.org/
    - 보안관제에서 공격을 받는 입장이지만, 공격 수행을 기준으로 CAPEC으로 공격 분류를 하는 경우가 있다.

### 보안 전략/전술/절차(TTP) 체계
- [**MITRE ATT&CK (Adversarial Tactics, Techniques, and Common Knowledge)**](https://attack.mitre.org/)
    - 악의적 보안 전략, 기술, 공통 지식, https://attack.mitre.org/
- [Cyber Kill Chain](https://www.lockheedmartin.com/en-us/capabilities/cyber/cyber-kill-chain.html)
    - 미국 군수업체인 록히드 마틴(Lockheed Martin)의 킬체인을 사이버 보안으로 재해석한 Kill Chain

### Application(애플리케이션) 보안
- [**OWASP (Open Worldwide Application Security Project)**](https://owasp.org/)
    - OWASP Top 10으로 유명한 비영리 보안 프로젝트, https://owasp.org/
    - 현재는 AI, API 보안에도 영향력을 끼치고 있다.
- [Application Security Tactics & Techniques Matrix](https://app-attack-matrix.com/)
    - 2025년 기준 새로 나온 프레임워크로 4개의 라이프사이클과 6개의 전략(Tatics)으로 구성되어 있다.
    - AppSec에 대한 내용이다.
    - https://app-attack-matrix.com/

### Threat Modeling (위협 모델링)
- [**Microsoft, STRIDE**](https://learn.microsoft.com/en-us/azure/security/develop/threat-modeling-tool-threats)
    - Microsoft에서 보안 위협을 식별하기 위한 모델, 1999년에 나온 개념이다.([Wikipedia](https://en.wikipedia.org/wiki/STRIDE_model))
- [**Lockheed Martin, STRIDE-LM** (PDF)](https://www.lockheedmartin.com/content/dam/lockheed-martin/rms/documents/cyber/LM-White-Paper-Threat-Driven-Approach.pdf)
    - 록히드 마틴(Lockheed Martin)에서 기존 STRIDE는 소프트웨어 공학/개발을 초점으로 두었기 때문에 Lateral Movement(내부 확산)을 추가한 위협 모델링이다.
    - 활용사례
        - [CSF, STRIDE-LM Threat Model](https://csf.tools/reference/stride-lm/)

