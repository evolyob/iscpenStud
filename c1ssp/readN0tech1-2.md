ch.1 治理的原則和策略
```
完整性:訪問控制、身分驗證、IDS、encrypt、hash、接口限制、輸出入功能檢查、培訓

縱身防禦 : 分層、分類、分區、分域、隔離、孤島、分段、格結構、保護環

數據隱藏； 防止應用程序直接放問儲存硬件，無法直接查看或訪問位置
第三方治理:通常外部人員或稽核員有湖符合安全目標、需求、法規、合同義務
COBIT 信息與相關技術控制目標 ((制定綜合安全解決方案
-->計畫與組織、獲得與實施、交付與支持、監測與評估

-->創造價值、整理分析、動態地治理系統、治理不同於管理、需求量身定做、端到端治理系統、保持真實性和問責制

文件審查 :  無果交換文件不完整不準確不充分 現場審查將會推遲到文件被更新，因為導致操作授權ATO丟失或失效
最有效益處理安全管理計畫是上而下: 高層啟動定義策略、中層落實標準基線指導方針程序、操作人員時限規定配置
戰略strategic長期有效期限大約五年 目標願景風險評估、定義安全目標、功能
戰術tactical 中期有效期限約一年規劃和安排實現目標所需的任務細節而制定
操作operational短期、高度詳細計畫、短時間內有效須經常更換每月每季，保持戰術計畫一致性

ROI return on investment投資報酬率:收購產品固有風險、威脅最小化、減少安全管理成本及違規行為
現場觀察觀察工作人員操作習慣，文件數據交換方式評估審查、策略審查的過程、事件響應
SLA服務水平協議 確保服務合同包含相關安全規定
SLR服務級別需求 製作軟件或提供服務的定義 變更控制管理

高級管理者:必須在所有策略問題上簽字，負責總體成功或失敗
安全專業人員: 落實高級管理指下達指令保證安全性包括編寫和執行安全策略
資產所有者 asset owner 通常為高級管理者 最終對資產保護負責，實際管理託付給託管員
託管員 custodian 執行安全策略及高級管理員規定，執行測試、備份、驗證數據、用戶訪問權限與工作相關並期限制
審計人員 auditor 出具合規性有效性報告，高級管理再把問題分配給安全專業人員或託管員

CEO要求CISO評估合理與否、安全報告應提交給CISO
CIO 確保信息被有效地用於實現業務目標

NIST SP 800-53 美國提供通用性建議
CIS 對操作系統、應用程序和硬件的安全配置指南
NIST RMF 強制性要求六階段 分類、選擇、實施、評估、授權、監控
NIST CSF 基礎設施及商業組織 識別、保護、檢查、響應、恢復構成

ITIL 信息技術基礎設施庫 IT安全需求如何與組織目標進行集成並保持一致、安全解決方案的起點
-->可接受使用的策略 定義可接受的級別及期望行為和活動，若不遵守得到告警處罰或解聘

威脅建模 識別淺在危害、發生可能性、關注優先、減少消除威脅 (SD3+C)
識別威脅 關注資產價值即面臨威脅、關注攻擊者動機目標或策略技術程序(TTP)

###微軟的 安全開發生命週期SDL：設計安全、默認安全
分類   微軟開發威些分類方案 STRIDE
Spoofing              欺騙 透過偽造身分進行攻擊 通常能繞過過濾器跟封鎖
Tampering             竄改 傳輸或儲存的數據未授權更改或操作
Repudiation           否認 否認執行動作能力 還可以讓善意第三人被指責違反規定
Information Disclosure 信息洩漏 發送外部或未授權實體
DoS                   拒絕服務  阻止資源授權使用 通常利用過載貨爆發流量進行
Elevation of Privilge  特權提升 將有限用戶帳號轉換更大特權

分析  PSATA 攻擊模擬和威脅分析過程、
七階段已風險為核心選擇要保護資產價值相關的方護措施
1.定義目標      ||2.定義技術範圍
3分解分析應用程序||4威脅分析
5弱點脆弱性分析  ||6攻擊建模仿真
7風險分析管理

VAST 可視化敏捷和簡單威脅  : 基於敏捷項管理編成建模概念，將威脅和風險回應到敏捷編成環境中

簡化分析 信任邊界、數據流路徑、輸入點、特權操作、安全聲明和方法細節
##補丁或版本更新管理是安全管理重要組成

DERAD 評級解決方案 每個威脅有五個問向
淺在破壞   若成真帶來損害多嚴重
可再現性   復現攻擊過程有多複雜
可利用性   實施攻擊難度有多大
受影響用戶 多少人可能收到攻擊%%%
可發現性   攻擊發現弱點有多難

SCRM 供應鏈風險管理 評估硬件軟體和服務相關風險的第三方評估監控，設定最低安全要求和強制執行服務級別需求
```
ch2 人員跟風管
```
資安長  定義並實施整個組織的安全
安全審計員 管理安全日志記錄並檢查身繫軌跡已追蹤合規或違規跡象
託管員  是安全腳色從所有者資產、依據所有者指定分類、提供適當安全保護的容器

安全框架
-->安全策略 ：定義所需的安全範圍、需要的保護、安全解決方案提供必要保護程度
-->標準 ：對軟硬件、技術和安全控制方法一致定義強制性要求
-->基線 ：
-->程序 ：詳細分步實施文檔、實現特定安全機制、控制或解決所需具體操作
-->指南 ：如何實現安全需求的建議、並是安全專業人員和用戶的操作指南

IAM  身分和訪問管理  提供帳戶分配必要的特權和訪問權限，能完成工作任務最小原則
AUP 可接受的使用策略 確認候選人以閱讀並理解相關文件並簽名 遵守預期工作相關的必要策略
NDA 保密協議 防止在職或已離職洩漏，可能會被要求在離職重新簽屬保密協議、減少未來的安全問題。

員工監管
1強制休假 了解其他人員如何執行其工作
2職責分離
3崗位輪換交叉培訓
UBA 用戶行為分析  UEBA用戶與實體行為分析  特定行為不一定有直接相關，但可能與漏洞偵查入侵破壞漏洞利用事件相關
-->監控收集信息可用改人員安全策略程序培訓相關安全監督計畫
人員調動可以被視為開除重新雇用，通常進用前員工帳戶會保留數月在規定期間沒有發現相關事件才可能Iam系統完全刪除

離職人員應處理 移除或禁用帳戶、歸還所有公司設備用品、監督收拾個人物品、無護送情形無法再次進入大樓、
-->新員工安排工作區域內、允許解雇信息告訴媒體

VMS 供應商管理系統  提供便利訂購、訂單分發、訂單培訓、統一計費，安全性可以通信合同保密為乎相關事情詳細活動日志
PII 防止未授權未同意不之情況下被訪問、觀察、監視或檢查
-->歐盟認為  IP和MAC地址在某些情況視為PII
HIPAA、SOX、FERPA、GDPR都對隱私要求必須遵守所有政府規定。

風險管理兩要素 風險評估和風險響應
asset資產、資產估值(資產價值AV)、threat威脅不良非預期、
-->威脅主體有目的利用脆弱性通常是人員、
-->威脅事件對脆弱性意外或有意利用、
-->威脅向量遭成傷害或採用的路徑或手段
脆弱性 vulnerability 防護措施缺乏造成傷害的缺陷、漏洞、疏忽、錯誤、侷限、過失
暴露   exposure 遭破壞可能損害存在性，暴露因子EF值
風險   risk   利用脆弱性可能造成損害的嚴重程度或機率
風險=威脅*脆弱性    風險=損害可能性*損害嚴重程度

威脅-->脆弱性-->暴露-->風險-->防護措施-->保護資產 -->威脅
防護現有資產成分析-->評估防護跟控制-->買保險提供總體靜值-->準確了解存在風險-->促進法遵和內部安全策略

風險評估是高層管理者的職責-->執行任務是IT和安全部門
-->結果回應給高級管理人員
定性風險分析包括判斷直覺經驗: 情境版、焦點小組、調查、問卷、檢查清單、一對伊會議、採訪、場景、delphi技術(匿名)
場景 威脅如何產生對組織對特定資產帶來麼引響，場景分配威脅級別高中低
-->將所有反饋彙總一分報告給高級管理層

Delphi技術 匿名反貴響應過程得到誠實提交給風險分析小組進行評估。
-->定性風險評估、達到匿名共識

定量風險分析  (危害可能 嚴重程度 發生頻率 可能性)
AV 資產價值分配，面臨所有威脅形成 威脅組合
EF 暴露因子 每個威脅組合計算EF，特定資產造成破壞遭到損失百分比
SLE單一損失期望 每個威脅組合計算SLE
SLE= AV*EF
ARO每年發生率 威脅分析每個威在在一年內實際發生的可能性
ALE年度損失期望  每個威脅可能帶來總損失
ALE= SLE(=AV*EF)*ARO
每種威脅控制措施研究 成本效益分析，為每個威脅選擇適合防護

風險響應 種類
降低緩解、轉讓或轉移、威攝、規避、接受、拒絕或忽略
風險緩解 risk mitigation  一種控制措施、有時可以完全消除或還是存在一些風險
風險轉讓 risk assignment  轉移給第三方、常見買保險外包
風險威攝 risk deterrence  對違規者實施威攝 CCTV 警語 保全
風險規避 risk avoidance   選擇替代品，躲避高風險
風險接受 risk acceptance  高級管理層接受風險造成的後果並書面陳述簽名
風險拒絕 risk rejection   否認存在希望不發生，不是有效風險響應方式。
-->威脅*脆弱*資產價值=總風險
-->總風險-殘餘風險=控制間隙

防護措施年度成本 ACS annual cost of the safegard
:購買、開發、許可、實施、制定、年度營運、維護、管理費用、年度修理、升級成本、生產率提高降低、環境改變、測試評估成本。
-->防護前ALE- 防護後ALE - ACS =防護措施對公司價值

選擇實施安全對策
低於資產價值、低於控制措施收益、對攻擊者稱本高於收益、控制措施真實可解決問題方案、收益是可檢測驗證、提供一致性保護、
-->只需要最低限度人為干預、防竄改控制錯 施、只有特權操作員才能全面訪問控制措施、提供故障安全或保護選項。

管理控制  合規法遵、策略、背調、數據分類標籤、安全意識培訓、報告審查、工作監督、人員控制測試
邏輯/技術  軟硬控制機制、訪問權限、加密、限制接口ACL、防火牆、IDS/IPS、閥值級別
物理控制   保安、圍欄、感測器、上鎖、蜜蜂、燈光、徽章、刷卡、看們狗、警報器

適用控制類型  (對已知的)
預防控制 身分驗證、鎖、欄、報警、職責分離、崗位輪調、DLP、PT、加密、審計、安全策略、培訓、AV、FW、IPS
威攝控制 安全意識培訓、鎖、欄、安全標誌'保安、CCTV、訪問管控門廳
檢測控制 保安、感應器、logs、輪調、強制休假、密罐、密網、IDS、違規報告、用戶行為監控、事件調查
補償控制 故障轉移替換的補充或替換選項
糾正控制 終止惡意活動或重新啟動可恢復可修正資源、功能和能力。換感應器、檢查完整性工具
恢復控制 糾正的擴展對於業務持續和災難恢復的解決方案
指示控制 強制或鼓勵遵守安全策略

安全控制評估 SCA 作為PT漏洞補充內容
監事和測量 識別安全重大改變帶來新控制措施花費合理
風險報告和文檔  已識別、評故嚴重性及優先、制定減少或消除、跟蹤緩解的進度
持續改進 RMM風險成熟度模型、ERM評估企業風險管理
***
RMM風險成熟度模型
1.初始級 ad hoc     開始進行風險管理混亂狀態、選項未列出
2.預備級preliminary 嘗試遵守風險管理流程但各部門評估不相同
3.定義級defined     範圍內採用通用標準化風險框架
4.集成級intrgrated  集成到業務流程，收集有效數據並視為業務戰略決策
5.優化級optimized   實現目標不是只對外部威脅回應、增加戰略規劃為了業務成功不是只避免事故、吸取經驗納入風險管理過程

***風險管理框架 RMF
1.準備 對安全跟隱私對組織跟系統角度執行RMF
2.分類 損失影響系統處理、儲存、傳輸進行分類
3.選擇 系統選擇一組依需求制訂控制並降低到可接受水平
4.實施 實施並描述如何在環境中使用控制
5.評估 是否被正確實施，是否按預期值結果的要求
6.授權 確認面臨風險是可接受的基礎授權系統或共同控制。
7.監控 評估控制有效性並紀錄系統操作環境變化的風險評和影響分析

安全意識教育培訓計畫
安全意識  自身安全責任和義務 通用安全認知基線、不特定對象內部執行
培訓     具有類似崗位職能的員工經過培訓才會遵守安全策略所有的標準、指南、程序、有效性量測，
教育     安全人員需要掌握大量安全知識對組織環境廣泛了解而不侷限具體工作任務、不是雇主主辦
改進
有效性評估  驗證手段、隨時間推進測驗、監控安全事件發生率、判定培訓是否有效
```
