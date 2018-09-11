# Lab

## 01. 管理訂閱與資源群組

### a. 加入使用者與設定權限

1. 選擇要加入使用者的訂用帳戶

    ![Select Subscription](https://i.imgur.com/LOr4rHw.png)

2. 點選: 存取控制(IAM)

    ![IAM](https://i.imgur.com/ezGCMvR.png)

3.  點選: 新增

    ![New](https://i.imgur.com/JVjIMDn.png)

4.  選擇欲指派之腳色與人員

    ![Role and User](https://i.imgur.com/cVOWI9D.png)

5. 完成後，該使用者即可依照所被指派之權限處理相關事務

### b. 資源群組

1. 從 Azure Portal 選擇資源群組，並點選: 新增

    ![Resource Group](https://i.imgur.com/iFR4ov2.png)

2.  填寫名稱、訂用帳戶與選擇資源群組欲置放所在之資料中心

    ![New](https://i.imgur.com/mxzMEW4.png)

3.  完成後，點進去會如下圖所示

     ![Complete](https://i.imgur.com/l5SRMjQ.png) 

### c. 建立資源鎖定

1. 點選: 鎖定，然後點選: 新增，填寫相關設定資訊
    ![New Lock](https://i.imgur.com/WPabqDY.png)
    ![Result](https://i.imgur.com/JbGYBrf.png)

2. 當被觸發時會如下顯示
    ![Try Delete](https://i.imgur.com/tgR98B4.png)

## 01. 儲存體

### a. 建立儲存體帳戶

1. 點選儲存體帳戶後，點擊新增
    ![Storage](https://i.imgur.com/jQdMFZi.png)

2. 填寫相關資訊與設定
    ![New](https://i.imgur.com/NOh9poG.png)

3. 點選建立即可完成
    ![Complete](https://i.imgur.com/IuRom6z.png)

### b. 上傳檔案

1. 安裝 Microsoft Azure Storage Explorer 並開啟，連結：[Azure Storage Explorer](https://azure.microsoft.com/en-us/features/storage-explorer/)
    ![Microsoft Azure Storage Explorer](https://i.imgur.com/UmhSqNN.png)

2. 連結至 Storage Account
    i. 透過 Microsoft Account 登入
        ![Microsoft Account](https://i.imgur.com/nNjEaSz.png)

    ii. 透過 Storage Account Name 與 Key
        ![Storage Account](https://i.imgur.com/eQ5GQeg.png)

3. 連結至 Storage 後，展開到 Blob Container 並新建一個 Container
    ![New Container](https://i.imgur.com/Ymc2ZuP.png)

4. 透過介面上傳檔案 (Demo.jpg)
    ![Upload](https://i.imgur.com/mBzr5yv.png)
    ![Upload Complete](https://i.imgur.com/72yoNyA.png)

5. 透過網址可以檢視檔案
    結構：https://{StorageAccountName}.blob.core.windows.net/{ContainerName}/{BlobName}
    連結：https://test20180912.blob.core.windows.net/images/Demo.jpg
    ![Image](https://i.imgur.com/s47HIF8.png)
    > 注意 Access Level 或是使用 S.H.A.

### c. 使用 CDN

1. 建立 Azure CDN 並與 Storage 連結
    ![CDN](https://i.imgur.com/zxuxUQA.png)

2. 檢視結果
    ![CdnResult](https://i.imgur.com/H8SjXv8.png)

3. 比較差異，使用：<https://www.cdnplanet.com/tools/cdnperfcheck>
    ![StorageTest](https://i.imgur.com/ocxO8i1.png)
    ![CdnTest](https://i.imgur.com/D0zg3FG.png)

### d. 使用儲存體來架設靜態網站

1. 開啟靜態網站功能
    ![EnableStaticSite](https://i.imgur.com/MG9hUgb.png)

2. 同時間 Storage 會自動新增兩個 Container
    ![WebContainer](https://i.imgur.com/epQXssf.png)

3. 將靜態網站原始碼上傳至 $web
    ![UploadHtml](https://i.imgur.com/W680Buw.png)

4. 設定靜態網站進入點等相關資訊
    ![EntryPoint](https://i.imgur.com/gPuwddJ.png)

5. 開啟主要端點連結檢視成果
    ![Result](https://i.imgur.com/kzjhPS9.png)

> 文件名稱會區分大小寫，因此必須完全相符儲存體中的檔案名稱。
> 也可自訂網域

### e. Azure File

## 02. 虛擬機器與相關設定

### a. 建立虛擬機器

1. 於 Azure Portal 選擇建立資源，以 Windows Server 2016 Datacenter 為範例

    ![New Resource](https://i.imgur.com/Od2IusO.png)

2. 填寫基本資訊

    ![Info](https://i.imgur.com/9xmouZt.png)

3. 選擇 VM 等級

    ![VM Size](https://i.imgur.com/XghCv36.png)

4. 填寫相關設定

    ![Settings](https://i.imgur.com/ZYO71dL.png)

5. 確認資訊無誤後，按下確認來執行建立 VM 動作

    ![Create](https://i.imgur.com/w6woCp0.png)

6. 等待 VM 建立完成

### b. 網路設定

1. 點選網路
    ![Network](https://i.imgur.com/1z8PEeL.png)

2. 設定 NSG
    ![NSG](https://i.imgur.com/kxxT1fe.png)

3. 設定 DNS Name
    ![DNS Name](https://i.imgur.com/GxTfLHN.png)

4. 遠端連線至主機
 
### c. 磁碟設定

1. 新增資料磁碟
    ![NewDisk](https://i.imgur.com/JaUYoYK.png)
    i. 建立受控磁碟
        ![NewManagedDisk](https://i.imgur.com/NUWwH1M.png)

2. 進入作業系統設定  
 
### d. 其他設定

1. 延伸模組
    ![clipboard](https://i.imgur.com/wia3DrO.png)

2. 自動關機、自動開機
    ![AutoShutdown](https://i.imgur.com/S0IwuTT.png)

3. 備份
    ![Backup](https://i.imgur.com/WGb4qqU.png)

4. 災害復原
    ![Site Recovery](https://i.imgur.com/fAWr6GF.png)

6. 更新管理
    ![Update](https://i.imgur.com/ABDexkM.png)

6. 圖表
    ![Diagram](https://i.imgur.com/VT932et.png)

## 03. VM 擴展集



