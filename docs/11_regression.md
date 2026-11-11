# C-1
- DAG 그림
```mermaid
[graph TD
    %% 노출과 결과
    Exposure["주중 수면 부족 (<8시간, 노출)"] --> Outcome["주관적 학업성적 (결과)"]

    %% 교란변수 (공통 선행 원인)
    SEX["성별 (SEX)"] --> Exposure
    SEX --> Outcome
    GRADE["학년 (GRADE)"] --> Exposure
    GRADE --> Outcome
    SES["가정 경제 상태 (E_SES)"] --> Exposure
    SES --> Outcome

    %% 매개변수 및 생활습관 경로 (노출의 결과이면서 결과의 원인)
    Exposure --> Stress["평상시 스트레스 인지 (M_STR)"]
    Stress --> Outcome
    
    Exposure --> StudyTime["주중 학습 목적 앉은 시간 (PA_SWD_S)"]
    StudyTime --> Outcome

    Exposure --> Breakfast["아침식사 횟수 (F_BR)"]
    Breakfast --> Outcome]
