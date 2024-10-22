# hw02

## 工作分解結構清單
| 任務 | 說明        | 需時 (天) | 前置任務  |
| :----: | :-----------: | :---------: | :---------: |
| 1    | 研擬計畫    | 1         | -         |
| 2    | 任務分配    | 4         | 1         |
| 3    | 取得硬體    | 17        | 1         |
| 4    | 程式開發    | 70        | 2         |
| 5    | 安裝硬體    | 10        | 3         |
| 6    | 程式測試    | 30        | 4         |
| 7    | 撰寫使用手冊| 25        | 5         |
| 8    | 轉換檔案    | 20        | 5         |
| 9    | 系統測試    | 25        | 6         |
| 10   | 使用者訓練  | 20        | 7,8       |
| 11   | 使用者測試  | 25        | 9,10      |


## PERT/CPM圖
```mermaid
graph TD;
    A1(任務1：研擬計畫<br>開始日期：2024/10/01<br>結束日期：2024/10/01<br>時長：1天) --> A2(任務2：任務分配<br>開始日期：2024/10/02<br>結束日期：2024/10/05<br>時長：4天)
    A1 --> A3(任務3：取得硬體<br>開始日期：2024/10/06<br>結束日期：2024/10/22<br>時長：17天)
    A2 --> A4(任務4：程式開發<br>開始日期：2024/10/06<br>結束日期：2024/12/14<br>時長：70天)
    A3 --> A5(任務5：安裝硬體<br>開始日期：2024/10/23<br>結束日期：2024/11/01<br>時長：10天)
    A4 --> A6(任務6：程式測試<br>開始日期：2024/12/15<br>結束日期：2025/01/13<br>時長：30天)
    A5 --> A7(任務7：撰寫使用手冊<br>開始日期：2024/11/02<br>結束日期：2024/11/26<br>時長：25天)
    A5 --> A8(任務8：轉換檔案<br>開始日期：2024/11/02<br>結束日期：2024/11/21<br>時長：20天)
    A6 --> A9(任務9：系統測試<br>開始日期：2025/01/14<br>結束日期：2025/02/07<br>時長：25天)
    A7 --> A10(任務10：使用者訓練<br>開始日期：2024/11/27<br>結束日期：2024/12/16<br>時長：20天)
    A8 --> A10
    A9 --> A11(任務11：使用者測試<br>開始日期：2025/02/08<br>結束日期：2025/03/04<br>時長：25天)
    A10 --> A11
```

## 甘特圖
```mermaid
gantt
    title 專案甘特圖
    dateFormat  YYYY-MM-DD
    section 計畫研擬
    研擬計畫         :done, task1, 2024-10-01, 1d
    section 任務分配
    任務分配         :task2, after task1, 4d
    section 硬體取得
    取得硬體         :task3, after task1, 17d
    section 程式開發
    程式開發         :task4, after task2, 70d
    section 硬體安裝
    安裝硬體         :task5, after task3, 10d
    section 程式測試
    程式測試         :task6, after task4, 30d
    section 使用手冊撰寫
    撰寫使用手冊     :task7, after task5, 25d
    section 檔案轉換
    轉換檔案         :task8, after task5, 20d
    section 系統測試
    系統測試         :task9, after task6, 25d
    section 使用者訓練
    使用者訓練       :task10, after task7, 20d
    section 使用者測試
    使用者測試       :task11, after task9, 25d
```


## 關鍵路徑圖

```mermaid
graph TD;
    A1[研擬計畫] --> A2[任務分配];
    A1 --> A3[取得硬體];
    A2 --> A4[程式開發];
    A3 --> A5[安裝硬體];
    A4 --> A6[程式測試];
    A5 --> A7[撰寫使用手冊];
    A5 --> A8[轉換檔案];
    A6 --> A9[系統測試];
    A7 --> A10[使用者訓練];
    A8 --> A10;
    A9 --> A11[使用者測試];
    A10 --> A11;
   
    style A1 fill:#f9f,stroke:#333,stroke-width:2px;
    style A2 fill:#f9f,stroke:#333,stroke-width:2px;
    style A4 fill:#f9f,stroke:#333,stroke-width:2px;
    style A6 fill:#f9f,stroke:#333,stroke-width:2px;
    style A9 fill:#f9f,stroke:#333,stroke-width:2px;
    style A11 fill:#f9f,stroke:#333,stroke-width:2px;

