# hw02
```mermaid
graph LR
    A[任務1: 研究計劃 - 1天] --> B[任務2: 任務分配 - 4天]
    A --> C[任務3: 取得硬體 - 17天]
    B --> D[任務4: 程式開發 - 70天]
    C --> E[任務5: 安裝硬體 - 10天]
    D --> F[任務6: 程式測試 - 30天]
    E --> G[任務7: 撰寫使用手冊 - 25天]
    E --> H[任務8: 轉換檔案 - 20天]
    F --> I[任務9: 系統測試 - 25天]
    G --> J[任務10: 使用者訓練 - 20天]
    H --> J
    I --> K[任務11: 使用者測試 - 25天]
    J --> K

    style A fill:#f9f,stroke:#333,stroke-width:4px
    style B fill:#f9f,stroke:#333,stroke-width:4px
    style D fill:#f9f,stroke:#333,stroke-width:4px
    style F fill:#f9f,stroke:#333,stroke-width:4px
    style I fill:#f9f,stroke:#333,stroke-width:4px
    style K fill:#f9f,stroke:#333,stroke-width:4px

```mermaid
gantt
    title Project Tasks Gantt Chart
    dateFormat  YYYY-MM-DD
    section Task 1
    Research Plan         :done,    t1, 2024-01-01, 1d
    Task Allocation       :done,    t2, 2024-01-02, 4d
    Hardware Acquisition  :done,    t3, 2024-01-06, 17d
    section Task 2
    Program Development   :active,  t4, 2024-01-23, 70d
    Hardware Installation :         t5, 2024-02-01, 10d
    Program Testing       :         t6, 2024-03-12, 30d
    User Manual Writing   :         t7, 2024-04-11, 25d
    Data Conversion       :         t8, 2024-04-06, 20d
    System Testing        :         t9, 2024-05-01, 25d
    User Training         :         t10, 2024-05-26, 20d
    User Testing          :         t11, 2024-06-15, 25d
```
