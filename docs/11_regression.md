# C-1
- DAG 그림
```mermaid
graph TD
    Exposure["주중 수면 부족 (8시간 미만)"] --> Outcome["주관적 학업성적"]

    SEX["성별"] --> Exposure
    SEX --> Outcome
    
    GRADE["학년"] --> Exposure
    GRADE --> Outcome
    
    SES["가정 경제 상태"] --> Exposure
    SES --> Outcome

    Exposure --> Stress["평상시 스트레스"]
    Stress --> Outcome
    
    Exposure --> StudyTime["주중 학습 목적 앉은 시간"]
    StudyTime --> Outcome

    Exposure --> Breakfast["아침식사 횟수"]
    Breakfast --> Outcome
