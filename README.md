# Technical-Interview-Qns

```mermaid
flowchart TD
    Start([Start: nums = [2, 3, 5, 7], target = 8]) --> LoopI[Outer Loop: i = 0 to 3]

    %% i = 0
    LoopI --> CheckI0["i = 0 (nums[0] = 2)"]
    CheckI0 --> LoopJ0["Inner Loop: j = 1 to 3"]

    LoopJ0 --> Step1["j = 1: nums[0] + nums[1] = 2 + 3 = 5 ≠ 8"]
    Step1 --> Step2["j = 2: nums[0] + nums[2] = 2 + 5 = 7 ≠ 8"]
    Step2 --> Step3["j = 3: nums[0] + nums[3] = 2 + 7 = 9 ≠ 8"]

    %% i = 1
    Step3 --> CheckI1["i = 1 (nums[1] = 3)"]
    CheckI1 --> LoopJ1["Inner Loop: j = 2 to 3"]

    LoopJ1 --> Step4["j = 2: nums[1] + nums[2] = 3 + 5 = 8 == target ✓"]
    Step4 --> Match([Return [1, 2]])

    style Step4 fill:#2ea44f,stroke:#238636,color:#ffffff
    style Match fill:#2ea44f,stroke:#238636,color:#ffffff
```