# 본사 및 지사 보안 인프라 구축

## 초기 네트워크 구성도
![image](https://github.com/user-attachments/assets/7d3b8118-b0e3-4c97-858a-57b4e97df17d)

## 본사 네트워크 구성도
![image](https://github.com/user-attachments/assets/c67f944c-ba75-448e-9b82-5b91e1c68d0b)


## 지사 네트워크 구성도
![image](https://github.com/user-attachments/assets/c2e56271-f665-4e6b-a485-77a19b4ec114)


## 초기 DMZ 구성도
![image](https://github.com/user-attachments/assets/57bcb36b-5e95-4b6a-9275-b348627569ec)


## 최종 네트워크 구성도
![image](https://github.com/user-attachments/assets/2324bbd2-da47-4f1b-828b-4cb766a23f9f)


## VPN 구성도
![image](https://github.com/user-attachments/assets/76acbb67-3748-49a4-9e03-502acecd97e4)


### IPSEC을 활용한 VPN 구축

- **인증**: Pre-share key 사용
- **암호화 알고리즘**: AES 128
- **인증 헤더 프로토콜 (AH)**:
  - **알고리즘**: HMAC-MD5
  - AH는 데이터 무결성을 제공하지만, 암호화는 제공하지 않음.

- **캡슐화 보안 페이로드 (ESP)**:
  - **알고리즘**: AES
  - ESP는 데이터 암호화와 무결성을 모두 제공.

## 모니터링 결과
![image](https://github.com/user-attachments/assets/5f200114-654e-424f-a05f-d4ec0bd7543d)
![image](https://github.com/user-attachments/assets/9f563328-54e4-4f85-948f-285b399657b4)


### Zabbix - 서버 및 에이전트 구축

- Zabbix 서버와 에이전트를 설정하여 실시간 모니터링을 수행.

## 테스트 환경
![image](https://github.com/user-attachments/assets/8f15f32d-5d22-4756-9894-ff410763c5d8)
- **ZABBIX SERVER ( Monitoring 수집 서버) : 192.168.11.129**
- **ZABBIX AGENT( Monitoring 대상 서버) : 192.168.11.130**



### Zabbix 웹 설정
![image](https://github.com/user-attachments/assets/3d5a4168-3f82-4f18-a74f-04ef3649c740)

1. **대시보드**: 설정 후 처음으로 보이는 대시보드 화면.
   ![image](https://github.com/user-attachments/assets/c8b9de13-40a8-4a32-9571-a41ee64e71ab)
3. **호스트 추가**: 새로운 호스트를 Zabbix 서버에 추가.
   ![image](https://github.com/user-attachments/assets/c08db2fc-0d1f-409b-84a0-69e6bfd71c09)
5. **등록된 호스트**: 모니터링 중인 모든 등록된 호스트 목록.
![image](https://github.com/user-attachments/assets/c67c77da-ea89-4679-a5fe-32a20f69c1a4)

## TEST
![image](https://github.com/user-attachments/assets/60f9b948-e8ae-4137-a4e8-bff7738215c7)

## 고찰

보완해야 할 점 : 이중화(GLBP)를 활용한 안전성 증가, ASA장비를 이용한 방화벽 DMZ 강화,
프록시 서버를 활용한 네트워크 효율성 증가, 네트워크 공격 탐지 기능 추가 
