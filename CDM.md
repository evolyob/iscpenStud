identify
```
asset
1. 可保護行動設備的資料機密性,定義處理受管制的處理過程
// 敏感資料放置在可管理的環境,設置存取控制方法,傳輸過程中保護資料
2. 有執行軟體版本盤點的報告,可將修補程式快速部署或進行網路隔離

RM
1. 涉及企業資料處理、儲存或傳輸，以及組織營運的系統、資產與個人組織資產和個人進行風險評估
2. 定期掃描組織系統和應用程式中的漏洞,每次執行掃描時，所使用的工具為最新版本
3. 定義的風險類別、風險來源和風險衡量標準確定風險，以及優先等級緩解計劃,人員,資源。
4. 分類並定期更新威脅剖繪(Profiles)和駭客的戰術、技術、流程(TTP)。
// 定期更新駭客威脅概況(駭客工具、技術和流程),註冊威脅情報服務,持續累積威脅配置文件或知識庫
5. 威脅情資整合到整個系統開發生命週期的風險管理流程之中，並為系統提供資訊。
// 使用威脅文件(TTP)為組織規劃網路防禦保護組織
6. 織的Internet 或其他網路連線的跨網閘道器上執行掃描,定期掃描各個網段邊界的資產
//  nmap portscan, 記錄網路邊界安全配置狀態,正確性
7. 分開管理不受供應商支持的產品,網路中隔離,執行升級、更換或報廢的時程
8. 根據新獲得的威脅情報評估組織防禦能力,資安配置的更改有納入SOP和改善的時間表
9. 制定和更新供應鏈風險管理計劃,有辨識和評估供應商的風險,風險緩解措施

資安評估
1. 定期更新系統安全計劃，這些計劃描述系統邊界、系統運行環境、安全要求的實現方式，以及與其他系統的關係，或與其他系統的連接
// 實施安全要求之文件,人員的角色、職責,深度防禦策略,定期更新
2. 安全控制在其應用中是否有效。(註：安全控制如：防火牆、網段隔離、防毒…等)
3. 制定並實施行動計劃，以糾正資安缺陷
// 定義特定人負責確保計劃的執行，以及計劃的責任歸屬,明確且可行的步驟
4.持續監控安全控制措施，以確保控制措施的持續有效性。
// 第三方安全評估員進行評估,定期評估每個控制措施
5. 定期執行滲透測試, 定期執行紅隊測試
6. 每個軟體更新都有執行程式碼審查



```
protect
```
AC
1. 唯一帳號密碼，離職即禁用
2. 系統登入前法規聲明通知
3. **可攜式設備政策、身份識別、使用範圍的最小權限
4. **管理功能僅特權帳號使用
5. 登入失敗嚐試次數
// AD GPO限制, 底層設定
6. 閒置Session locks, 條件終止或Session timeout
// keepalive_time = 1800
7. **可使用角色、登入前授權、允許設備需經授權、行動設備批准、監控、紀錄
// intranet,wifi,intrasystem,VPN(ipsec),extranet
8. 職權分離、開發測試隔離、日誌記錄非特權使用管理狀況
9. wireless access 身份驗證、WAP2等級(AES)以上、
// mac綁定

10. 敏感資料專區、需身份驗證、定期檢查更新存取清單批准、監控、紀錄
// ad group, sudoers , time_status
11. **FW,Proxy for IPDS UTM

Aware training
1. **管理者、系統管理員和組織系統使用者，了解與其操作相關的安全風險，包含系統安全性相關的規範，標準和流程
//資安意識提升活動、海報和電子郵件宣導資安政策
2. **特定角色定制內部威脅指標培訓課程
// 社交工程的威脅(social engineering)、進階持續性威脅(advanced persistent threat actors)、安全漏洞以及可疑的行為; 並且至少每年一次或威脅發生重大變化時更新訓練課程內容
// 研發人員對社交工程攻擊有感,針對式網路釣魚演練,設有資安專業培訓預算

Configration
1. **有記錄系統的軟體和組態設定、記錄系統與元件在網路中的位置、其他特殊規格
// 角色和最低要求功能, 刪除不需要的軟體, 禁用未使用的協定和網路服務
2. **使用管理流程或自動化方法管理使用者安裝的軟體,最嚴格的組態設定
3. 追蹤、查看、核准或不核准等配置變更記錄皆應記錄
//  定期召開白名單組態變更設定
4. **系統配置應定義、記錄、核准和實施與組織系統變更相關的實體和邏輯存取限制
// 經過主管核可, 特定IP特定時間才能對系統軟體更新, 
5. **限制所有不必要的通訊埠(port)、協定(protocols)和服務
// fw policy, iptable
6. **止未經授權的軟體執行,透過白名單或黑名單來管制程式執行
//  軟體進入到白名單之前會先驗證
7. 重要伺服器有使用安全晶片進行安全啟動驗證
// 終端設備，經IT人員配置為安全啟動後才將設備提供給員工

PAM
1. **有設置身分認證系統,都有唯一帳號識別每個人
// 新密碼需符合一定的複雜度,最少字元限制,禁止在規定的時間內設定重複的密碼
2. 所有密碼在儲存和傳遞時，都必須以加密方式進行保護
3. 身份驗證資訊時的反饋資訊模糊化
// 遮碼
4. 針對特權用戶、使用者啟動遠端存取時使用多因素身份驗證 (MFA)
5. 啟用傳輸層安全性 (TLS) 、公鑰基礎設施 (PKI)、或一次性密碼 (OTP) 
6. 定期盤點任何閒置帳戶




sys communication
1. 禁止設備遠端啟用鏡頭、麥克風
// Microsoft Defender  SOFTWARE\Policies\Microsoft\AppHVSI
2. SSH 協定管理網路設備
// disable weak cipher , enable ssh2
3. 採用資安架構設計、軟體安全開發技術和系統安全工程原理
// Config hardening, develop Document, ver. chk 
4. 共享系統資源進行未經授權傳輸,驗證設置正確。
5. 定期查看FW policy chk確保沒有授權的更改
6. 禁止分割通道
7. 採加密方式傳輸受管制的資料TLS ,PKI policy
8. Mobile Code必須是受信任的來源，並且進行數位簽章認證
9. VoIP使用限制和實施指南

10. MFA,TLS,VPN configration,Session的清除機制
11. 保護靜態資料的機密性
//  encryt key、簽核流程、單獨安全區域(異地異機)
12. **定義高價值網路架構跟伺服器系統、隔離措施
// vlan, DMZ, HA, 單獨通道管理
13. **FW, SW, WebProxy 信任邊界
// 進出封包側錄保存三個月、未知封包阻擋
14.實施域名系統（DNS）過濾服務
// DoH, FW設定, Web Proxy

系統和資訊完整性
1. 禁止在公開網站上發布受管制資料的政策
2. **專人執行資安情資收集IoC、公開TTP威脅情資
3. **新版本發佈時，自動更新到最新版本更新惡意程式保護機制
4. 部署端點偵測和回應方案 (EDR)到組織端點設備
5. 垃圾郵件出入站防護機制 SPAM過濾規則定期查看
6. 電子郵件偽造保護 DKIM、SPF 和 DMARC


```
detect
```
1. 組織有專責人員定期收集最新的網路威脅情資,加入產業或政府提供的威脅情資共享聯盟
2. 立並維護網路威脅獵捕功能，以搜尋組織系統中的威脅入侵指標(indicators of compromise)，並偵測、追蹤和破壞那些可逃避現有控制措施的威脅。
//  善用日誌分析、網路流量分析和威脅情資工具,事件處理完畢後，團隊會建立威脅入侵指標
//  威脅情資採用自動化方式介接，提高反應速度

3. **確保可以追溯單一系統操作的使用者，以便他們對其操作負責
// 日誌資訊有用戶ID, 來源IP, 目標IP, 時間戳
4. 定期檢查識別可能的安全事件，
5. 日誌記錄機制一驗證失效告警，立即通知資安專責人員,重新啟動日誌記錄機制並驗證它確實運作
6. 系統能提供系統錯誤事件描述, 備份和還原事件描述, 配置變更事件描述
// oscce, siem
7. **同步標準時間與內部系統時間的時間同步系統以生成稽核紀錄的時間戳記
// ntp , fw policy 123 port
8. 日誌採用通用格式匯集到一台或多台集中式儲存伺服器, 支援自動化分析功能
9. 定期確認資產回報日誌狀態,尚未回報日誌將發送通知進行調查
// 確認儲存空間充足, 唯讀模式，不會被刪除或更改,只有獲得授權個人才能查

10. 稽核記錄功能的管理權限，限縮給特定的特權帳戶
//  網路基礎架構人員無法查看、刪除與修改日誌
11. **定期檢查日誌文件是否已被更改，或有異常跡象
12. 調查和通報非法、未經授權、可疑或異常活動的跡象
//  有專門執行日誌分析團隊, 安全日誌可提供簡單可視化圖表
13. 自動分析審核記錄，並識別關鍵指標或組織定義的可疑活動並對其採取對應措施
//  日誌分析採用自動化工具(自動處理告警、產生完整報告)

14. 了解每台機器的活動，以及大範圍的機器活動
//  有跨系統進行資安事件調查能力,每台異常設備進行深度調查

```
respond
```
1. **組織系統內事件處理的能力，包括準備、檢測、分析、遏制、修復和回報
// 聯繫的內部、外部人員,建立通報事件,採取的措施,
2. 運用駭客的技術和手法等相關背景知識，規劃事件通報執行作法,駭客攻擊劇本
// 定期收到產業相關的防禦報告, 改進組織的事件回應計劃
// 查看管理流程、防護技術和實體控制方面的弱點,現有的回應計劃是否有效

3. 使用中央日誌收集工具，配置到組織的所有端點設備
// 建立事件收集環境端點,SOC可存取安裝在端點程式進行取證
4. **主動追蹤網路資安事件、蒐集內部員工的異常通報、針對事件分析與評估
// 分析事件類型和影響程度, 優先級劃分, 不同優先順序給予通報方案
5. **事先定義好的程序，建立並實施應變措施
// 停止或控制損壞方法,使用者溝通方法,利益關係人溝通,實施控制措施,跨不同職能團隊組成
6. 建立和維護有24/7安全性監視功能的安全中心
// 自建或委外的SOC中心, 與事件回應團隊有建議直接溝通管道


```
recover
```
1. 定期執行資料備份及資料回復驗證程序
// 定期執行系統備份,備份離線儲存在不同的位置, 異地備份在不同的位置
2. 資訊處理設施滿足組織定義的資訊安全連續性，備援性和可用性要求
// 重要安全設施存在備援系統,AS,切換備援主機時間間隔在組織可容忍範圍內
```