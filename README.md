# NeprWeapon 3.1.0.8 — DungreedEnemies 호환 핫픽스

[DungreedEnemies 1.3.0](https://github.com/Xetsumei/DungreedEnemies/releases/tag/1.3.0)과 병용할 때 혈액 축제 회복 처리와 드론 피해 처리에서 발생할 수 있는 두 패치 초기화 충돌을 수정했습니다.

- 혈액 축제: 상대 모드의 회복 함수와 이펙트를 유지하면서 기존 강화 장갑의 회복량 보정을 적용하고, 예외 영역 종료 위치를 보존합니다.
- 드론 피해: 상대 모드의 피해 제한 패치 뒤에 보정을 적용하며, 재적용 때 중복으로 삽입하지 않습니다.

[NeprWeapon v3.1.0.8 다운로드](https://github.com/JYGOOD00/NeprWeapon/releases/tag/v3.1.0.8)

공개 3.1.0.7 기준의 Weapon 전용 변경입니다. NeprItem 공개 버전은 2.1.0.12로 유지합니다. 무기 ID·밸런스 수치·리소스는 변경하지 않았습니다. 기존 ID 이전에 관한 새 런 안내는 그대로 적용됩니다. 멀티플레이 참가자는 NeprWeapon 3.1.0.8 / NeprItem 2.1.0.12 및 다른 모드 구성을 맞춰 주세요.

검증: native/HarmonyX 빌드 성공, 자체 회귀 각 4,247개 통과(총 8,494 PASS). 실제 게임 병용·호스트·게스트 검증과 제보 원본 로그 확인은 아직 완료되지 않았습니다. 이번 검증은 두 패치의 구조적 충돌에 한정합니다.

ZIP SHA-256: `081948565f42232bc4645299c52d536f8c1d7b313a9fa3300afcbf63ced89855`
빌드 소스 fingerprint: `35f31288206c68d09384b131bd9291ca5708f9f459bd7eaf00d0eb5ac5710c0f`

---

## 이전 3.1.0.7 배포 기록

# NeprWeapon 3.1.0.7 — 충돌 및 기존 항목 오류 핫픽스

- 기존 무기의 고정 ID, 강화 연결, 조회와 네트워크 참조를 일관된 별도 대역으로 이전합니다.
- 광범위한 구형 권총 ID 별칭 처리를 제거하고 자기 모드 무기 참조의 소유 상태를 확인하도록 수정합니다.
- 등록 충돌/실패 시 다른 모드 객체를 보존하면서 자기 등록·패치·프리팹 상태를 정리하도록 수정합니다.
- 업데이트 알림을 HUD 로그 준비 뒤 표시하고, 완료 알림이 표시되기 전에 상태가 지워지는 문제를 수정합니다.

기존 공개 무기의 수치·효과·태그를 기준으로 합니다. 새 preset/UI, 드론 추종 변경과 로켓 드론 donor 동작 변경 등 별도의 기능/밸런스 변경은 포함하지 않습니다.

두 모드를 함께 업데이트하고 **새 런으로 시작하세요.** 멀티플레이 참가자는 NeprItem 2.1.0.12 / NeprWeapon 3.1.0.7 및 다른 모드 구성을 맞춰 주세요. 이전 숫자 ID 런의 자동 변환은 제공하지 않습니다.

두 Harmony 환경의 빌드, 공개 정의·자산 보존과 등록 충돌·참조·선별 오류의 정적/모의 검사를 확인했습니다. 실게임 호스트/게스트와 실제 설치 후 자동 업데이트 확인은 별도입니다.

이전 공개 버전: [NeprWeapon v3.1.0.1](https://github.com/JYGOOD00/NeprWeapon/releases/tag/v3.1.0.1) · [NeprItem v2.1.0.1](https://github.com/JYGOOD00/NeprItem/releases/tag/v2.1.0.1)

초기 검증 실행에서는 1,037개 검사를 확인한 뒤 Tests.exe의 IL 비교기가 ID 파생 상수·배열 초기화 데이터를 처리하지 못해 일반 관리 코드 단언 오류로 종료했습니다. 초기 실행 전체가 통과한 것은 아닙니다. 실제 Harmony detour나 게임 DLL 실행은 없었습니다. 전체 실패 경로를 중단하고 수정한 별도 정적 비교(2개), 최종 패키지 검사(357개), ZIP 해시 검증을 확인했습니다.

---

# NeprWeapon
Sephiria weapon mod for HorayModAPI. Releases and automatic updates.


