# 作業模板(Job Template)

Job模板用於向遠程HPC集群提交批處理作業或運行本地應用程序。Ansys Minerva內建了用於Ansys Electronics Desktop、Fluent、Icepak、LS-DYNA、Mechanical APDL、optiSLang、SpaceClaim和Workbench的內置Job模板。為了更大的靈活性，您可以自定義這些模板，或創建新模板。需要進行最小的工作量和編程。

以下是創建自定義Job模板的步驟：&#x20;

1. 定義需求&#x20;
2. 建立一個Job模板項目類型&#x20;
3. 定義用戶界面&#x20;
4. 建立服務器方法&#x20;
5. 建立應用程序定義

這些步驟旨在幫助您自定義Job模板，以便更好地支持您的特定應用程序和工作負載。這需要一定的技術和編程能力，但通常情況下，這些步驟的要求都是最小的。

### 定義需求

在創建自定義模板之前，請先思考您希望模板具有的功能和佈局。您需要了解JavaScript和C＃編程語言來定義模板。考慮以下幾點：

* Goal: 介面布局
* 輸入: 在作業提交界面中，輸入被分為以下幾個部分：輸入文件、求解器設置、硬件設置（僅限批處理作業模板）和輸出文件。
* 輸出: 當作業完成時，輸出會自動複製到提交作業時創建的任務的輸出選項卡中。它們也可以從作業項目中查看：

### 建立一個Job模板項目類型

創建自定義Job模板的第一步是創建一個用於該模板的項目類型。

1. 選擇 Administration → Item Types。
2. 在ItemTypes窗格中，Create New Item Type。
3. 在ItemType表單上，指定一個名稱以識別數據庫中的模板。 我們在此示例中使用了ans\_JobTemplate\_Fluent：
4. 在下面的窗格中，為每個所需的用戶輸入定義屬性。

### 定義用戶界面

您可以使用純JavaScript、Ansys Minerva表單或UI庫（如React / Angular）來設計作業提交用戶界面（UI）。

在我們的示例中，我們使用Ansys Minerva表單來設計自定義UI。表單包括一些基本元素，可幫助您開始設計，並需要最少的編程來創建設計。有關表單的更多信息，請參閱Aras Innovator指南。

### 創建服務器方法

對於高級模板驗證、構造複雜的命令行參數字符串或其他用例，請考慮創建服務器方法。

對於我們的Fluent示例，創建了一個名為ans\_Job\_SubmitFluent的服務器方法。為確保調用此方法，請確保在Submit按鈕控件的配置中指定它（p. 203）。

### 創建應用程序定義&#x20;

創建自定義作業模板的最後一步是創建應用程序定義，並將其與作業模板關聯。

要創建應用程序定義：

1. 在內容窗格中，選擇Administration → Job Management → Applications。
2. 在Applications窗格中，點擊Create New Application。
3. 使用應用程序表單定義應用程序類型。&#x20;
   1.  以下應用程序設置是關鍵的： •

       * 可執行文件路徑。運行應用程序的路徑。對於利用Ansys Solver Execution Controller（SEC）腳本的作業，請使用變量${Agent.Ansys.SecScript}。&#x20;
       * Arguments。要傳遞給應用程序的命令行參數。對於SEC作業，請留空。&#x20;
       * Job Template。選擇作業模板項目類型（在我們的示例中為ans\_JobTemplate\_Fluent）。 •
       * Solver Tag。僅適用於利用Ansys Solver Execution Controller（SEC）腳本的“Batch”應用程序。對於不使用SEC的批處理應用程序以及僅與應用程序啟動器一起使用的應用程序，此設置可以保持空白。&#x20;

       如果您有特定的文件傳輸要求（例如，從傳輸中排除某些文件類型），請使用Export File Definition和Import File Definition設置來指定適當的文件傳輸定義。請參閱Creating File Transfer Definitions。
   2. 在文件類型選項卡中，選擇用戶可以運行此應用程序的文件類型。在此示例中，當用戶選擇Ansys Fluent .cas，.cas.gz和.cas.h5文件時，Fluent作業模板將可用。
   3. 在腳本選項卡中，指定要使用的腳本。腳本可用於指定每次運行應用程序時應可用的文件（批處理腳本、日誌文件等）。腳本可以引用存儲在資料庫中的文件，或者文本文件的內容可以內嵌存儲。路徑表示文件可用的相對路徑（包括文件名）。
   4. 在環境變量選項卡中，設置應用程序運行時要使用的環境變量。環境變量的值可以是應用程序變量。
   5. 在變量選項卡中，指定模板變量。請參閱應用程序變量（p.211）。

