---
description: >-
  AEDT 與 Minerva 的連接旨在將客戶端的設置和修改與 Minerva
  存儲庫中的模擬同步。這樣可以讓用戶方便地保存和分享其工作，以及使多個用戶能夠協同工作，並在進行多個經過驗證的版本和變體的同時保持項目的一致性。
---

# AEDT連結

### AEDT當中設定欲連結之Minerva資料庫

在 AEDT 中，您可以設置要連接的 Ansys Minerva 資料庫。以下是相關步驟：

1. 從 AEDT 菜單欄中選擇「Ansys Minerva」>「設定」。
2. 在「Ansys Minerva 設定」對話框中，輸入 Ansys Minerva 伺服器的 URL 地址和要連接的資料庫名稱。
3. 輸入您的用戶名和密碼。
4. 點擊「確定」按鈕以連接到 Ansys Minerva。

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

### 與Minerva同步設計變更

用戶可以在客戶端中打開 Minerva 目錄中的文件，並將文件保存到 Minerva 目錄中。同時還可以使用 claim/unclaim 功能來釋放和獲取控制權，以確保項目的一致性。以下是相關操作的步驟：

打開 Minerva 目錄中的文件：

1. 從 AEDT 工具欄中，選擇「Ansys Minerva」>「打開 Ansys Minerva 存儲庫」。
2. 選擇要打開的項目，然後點擊「打開」。

將文件保存到 Minerva 目錄中：

1. 從 AEDT 工具欄中，選擇「Ansys Minerva」>「另存為到 Ansys Minerva 存儲庫」。
2. 輸入新文件名稱並選擇保存的位置，然後點擊「保存」。

釋放和獲取控制權：

1. 從 AEDT 工具欄中，選擇「Ansys Minerva」>「聲明項目」或「取消聲明項目」。
2. 當您完成對項目的編輯時，請取消聲明項目，以便其他用戶可以編輯該項目。

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
存檔會連同模擬結果以.aedtz壓縮檔格式存放在Minerva 保險庫當中。
{% endhint %}

{% hint style="info" %}
單純修改存檔並不會作版本控管，只有進入生命週期，經果審核的檔案才會加入版本號。
{% endhint %}
