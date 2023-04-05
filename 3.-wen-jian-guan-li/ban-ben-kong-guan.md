# 版本控管

在 ANSYS Minerva 中，當文件或文件夾被創建時（通過拖放、手動上傳或由應用程序自動上傳），該對象（稱為項目）自動被放置在版本控制下。這允許保存其更改的歷史記錄，因為對該項目的修改可能意味著文件的新版本。版本控制使用兩個數字來標識對象的版本：主版本號和次版本號。

主版本號表示數據中的重大更改，通常由釋放過程觸發。釋放過程是一種正式流程，用於審查和批准對文件或一組文件的更改。一旦釋放過程完成，主版本號就會增加。

次版本號則表示較小的更改，通常用於捕捉給定文件的“快照”。例如，次版本號可能用於在對文件進行一系列小更改之前捕捉文件的狀態。次版本號通常在每次對文件進行更改時自動增加。

通過在 ANSYS Minerva 中使用主版本號和次版本號，用戶可以輕鬆跟踪其文件和文件夾的更改歷史記錄，並在需要時輕鬆訪問文件的先前版本。這在科學研究或工程項目等需要保持數據完整性和可追溯性的情況下尤其重要。

當打開一個文件時，它的版本是可以訪問的。

版本面板顯示了文件的“歷史”，包括所有之前的版本和更改的性質。這個對話框公開了進一步的功能，如創建新的分支、比較不同的版本或清除（刪除）舊版本。這樣的功能使得用戶可以輕鬆地查看和管理文件的歷史版本，進一步提高了文件管理的效率和可靠性。

當點擊較舊版本的版本號時，對應的文件會在新的標籤頁中打開。一個標誌表明該文件不是最新版本。

點擊較舊版本的版本號可以查看文件的先前版本，方便用戶進行比較或查看文件的演進過程。標誌指示這個打開的文件是一個舊版本，而不是當前的版本。這可以幫助用戶避免在編輯或更改文件時意外覆蓋了最新的版本。

在 ANSYS Minerva 中，所有對象都由項目（Item）表示。這些項目可以是不同性質的。項目的定義由項目類型（ItemType）管理。文件、文件夾和快捷方式由名為 Ans\_Data 的 ItemType 表示。默認情況下（當不存在特定配置時），Ans\_Data ItemType 是唯一啟用版本控制的 ItemType。這意味著只有 Ans\_Data ItemType 的對象才會有版本控制功能。

當一個進程（例如本地應用程序啟動或作業提交）正在處理任務的輸入時，這些輸入被“凍結”。此外，所有輸入都被釋放。

對於僅在該任務上使用的輸入，它們會被移動到已發布的狀態。對於在其他地方使用的輸入（例如在 /Data 視圖中），會創建一個快照。這意味著會創建一個被取代的次要版本。

注意：當已發布的項目再次被修改時，會創建主要版本。釋放過程是由用戶觸發的操作。

在 Ansys Minerva 中，可以建立分支。例如，當需要分析相同設計的不同變體時，可以建立分支。分支可以從先前版本中創建。

為了滿足不同的業務需求，實現了兩種不同的分支方案。可以從版本窗口中創建分支：“切換到新分支”將使新分支成為活動分支，“保留兩個分支”將創建兩個不同的項目，每個項目都屬於其自己的分支。

分支也是特定的對象，可以根據需要訪問和修改。認領一個對象會鎖定它，使其他用戶仍然可以訪問它但不能修改它（只讀訪問）。

取消認領對象會釋放它，使其他用戶可以認領它。