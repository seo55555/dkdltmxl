# C-1
- DAG 그림
```mermaid
flowchart LR
    %% 교란변수 (위쪽: 노출과 결과의 공통 원인 / 보정 대상)
    C["성별, 학년, 경제상태\n학습 목적 앉아있는 시간"] --> X["평일 수면시간\n(노출)"]
    C --> Y["학업성적\n(결과)"]

    %% 노출 -> 결과 직접 경로
    X --> Y

    %% 매개변수 (아래쪽: 노출 ➔ 매개 ➔ 결과)
    X --> M["평상시 스트레스 인지\n아침식사 횟수"]
    M --> Y

    %% 스타일링 (템플릿 색상 및 형태 반영)
    style C fill:#d1ecf1,stroke:#bee5eb,stroke-width:2px
    style X fill:#ffffff,stroke:#333333,stroke-width:2px
    style Y fill:#ffffff,stroke:#333333,stroke-width:2px
    style M fill:#fff3cd,stroke:#ffeeba,stroke-dasharray: 5 5,stroke-width:2px
