# Job

在ANSYS Minerva中，Job指的是一個計算任務或工作，包括模擬、仿真或分析等。它是由用戶提交到系統的一個指令集合，用於在高性能計算（HPC）集群上執行複雜的計算或模擬工作。

一個Job可能包含多個步驟或階段，例如設置模型參數、網格劃分、求解和後處理等。在提交Job之前，通常需要為它指定適當的計算資源（例如節點、處理器和內存等）和執行條件（例如運行時間和優先級等）。

Job的執行進度和結果可以通過ANSYS Minerva中的作業監視器（Job Monitor）進行監控和管理。在Job完成後，系統會自動將結果保存到指定的輸出文件中，並可通過系統界面或API接口進行後續的數據分析和處理等工作。

### Job Template

工作模板是用於提交批次作業到遠端HPC群集或運行本地應用程序的模板。Ansys Minerva包含了Ansys Electronics Desktop、Fluent、Icepak、LS-DYNA、Mechanical APDL、optiSLang、SpaceClaim和Workbench的內建作業模板。為了更大的靈活性，您可以自定義這些模板，或創建新模板。最小的努力和編碼是需要的。

