ch.1
```
業務需求
--根據需求通信流量類型、外部攻擊性質和強度並相應調整安全基線
--不違背安全規範情況下提升營運能力
>>> functional：設備流程或員工完成業務目標所需、
>>> non-functional 希望滿足的一些附加要素
***現有狀態業務需求、業務影響分析BIA賦予優先級並考慮損失對組織作用
>>>採訪業務職能經理、用戶、高層管理繩、客戶需求
>>>收集網路流量、清點資產、財務記錄、保險紀錄、市場數據及強制性合規要求

收益量化和機會成本
--減少資本性支出 Capital expenditure CapEx
>>>無法滿足所有時段有效使用或超出負荷、突發使用要求
>>>雲環境只需要支付實際使用資源費用的可計量服務特性、成本節約避免高昂業務風險
--降低人工成本   為滿足內部需求雇用及培訓費用、可降低資深員工的僱用比例
--減少營運性費用 通過計算拉精確支付統一匯總費率進行計價而非運營活動強度增加而增加

--轉移部分監管成本 滿足特定行業可互安全控制項 PCIDSS強制監管要求而不是單獨付費
>>>不能把無意或惡意洩露PII相關風險或責任轉嫁給第三方，需承擔最終全部責任
--減少數據歸檔服務 Data Archival備份服務的成本、異地備份較好成本收益選擇、增強BC/DR戰略

預期影響 成本效益計算由業務需求驅動並考慮安全因素，高層決定遷移到雲端是否合理

運計算標誌特性
--彈性  Elasticity    當需求立即使用資源可按需分配資源，避免浪費及資源閒置產生額外成本
--簡單化  Simplicity  可任意使用除要履行職責必須部分，很少與供應商頻繁互動．
--可伸縮性 Scalability 計算能力需求會發生變化分配新資源不需要增加成本輕鬆滿足這些需求．

--> NaaS networking  網路即服務
--> CaaS compliance  合規即服務
--> DSaaS Data Science 數據科學及服務
```
```
雲計算服務模型
--IaaS  連通刀片式硬件
>>>雲服務只提供設備的物理資源，其餘軟體邏輯資源由客戶自行管理
>>>DR/BC的角度是溫站warm Site有完備物理空間測試正常網路連接，可使用任何類型配置加載業務需求任何數據
>>>DR/BC對於增加強數據安全控制權可能是最適合模型

--PaaS  操作系統 MS linux unix
>>>雲供應商負責需對系統補丁負責管理和更新操作系統、
***DevOps可在相對獨立測試軟件不破壞正式環境功能

--SaaS  客戶關係管理系統、託管HR系統、電子郵件
>>>額外提供建案程序並負責管理及更新軟件、客戶負責上傳及處理業務數據
>>>對最終用戶是完全透明也只能能看見他們購買的應用

雲部屬模型
--公有雲 public   由供應商擁有和經營並出售或租任給任何人
>>>特定公司擁有根據合同提供對外AWS Azure
--私有雲 private  專供自己客戶和使用者的私有環境intranet、透過web方式或遠程方問連接的傳統環境
>>>僅允許該組織授權用戶使用，通常是託管形式共享應用系統
--社區雲 community 共同目標或利益多個組織擁有和營運的基礎架構和處理能力以某種方式聚集起來執行聯合任務和公能
>>>例如遊戲社區託管網路身份和管理IAM任務、或形數字版權管理DRM任務處理某一遊戲、而用戶在本地處理任務和處理．

--混合雲 Hybrid 希望保留部分私有雲資源、租用公有雲DevOps測試、降低正式區崩潰風險．

角色和責任
--雲服務提供商 CSP 擁有數據中心、員工、管理資源、提供服務和安全及客戶數據處理需求幫助
--雲客戶 customer 購買或租任雲服務的組資或個人
--雲訪問安全代理商 CASB 提供獨立身份和訪問管理IAM、單點登入SSO、證書管理和密鑰託管
--監管機構 regulator 確保組織尊循規章制度框架、HIPAA GLBA PCIDSS SOX FTC(聯邦貿易委員) SEC(證卷交易)
```
```
雲計算的定義
--Apache Cloud stack 利用IaaS通過雲環境提供相關功能組件、更方便創建部署和管理雲服務
--業務需求 requirement 遷移決策驅動因素也是風險管理輸入項
--雲計算APP 雲應用系統、可能是用戶設備安裝代理或小程序
--雲計算架構師 architect 基礎架構設計和部署專家
--雲備份 backup      基於遠程服務器將數據備份可訪問形式儲存
--雲計算 computing   可保證計算資源來處理應用系統、通常是軍事或研究設施服務、提供個性化或支持逼真遊戲
--雲計算經銷商 reseller 購買託管服務然後再轉賣給他們自己客戶
--雲遷移 migration    全部或部分數據應用系統從公司內部轉移到雲端的過程、雲服務案需求提供
--雲操作系統 OS      PaaS模型用語
--雲可移植性 portablility 兩個雲服務提供商之間遷移應用系統或相關數據的能力
--雲服務提供商 provider 公共網路提供存儲或軟體解決方案的供應商並決定使用的技術和維運流程
--雲服務代理商 CSB     第三方實體公司透過多朵雲服務供應商的商業關係之間仲介、為每個客戶選擇最佳雲服務和相關持續監控


--雲儲存 Storage    可訪問形式儲存在雲上、而雲由多個分佈並連接資源組成
--雲測試 Testing    負載和性能測試在供應商的應用系統和服務進行、確保多種條件實現最佳性能和可伸縮性
--雲社區 community  特定社區專門設計、有相同考慮、業務和安全要求
--企業應用系統 enterprise application 企業所用 解決企業問題的應用系統或軟體
--Eucalyptus  私有雲使用的、開源雲計算和IaaS平台
--FIPS 140-2 列出經過認證和不再使用的密碼體制
--混合雲 Hybrid cloud 多種模型元素的雲計算解決方案

--託管服務提供商 managed service provider 由雲客戶指定技術和維運流程的服務、根據合同執行管理和維運支持
--多租戶 multi-tenant  多個客戶使用相同雲環境
--NIST 800-53 滿足適當安全要求和控制項

--TCI可信雲計算參考模型 TCI物理設施和網路邏輯佈局和需求、讓客戶放心和自信購買使用雲服務
--**供應商綁定vendor lock-in  客戶由於技術或非技術限制而無法遷移到另一個雲服務的狀況
--供應商鎖定vendor lock-out 服務商破產或由其他方式離開試場導致無法恢復自己的數據 

雲CIA
>>>confidentiality機密性 避免未經授權訪問
>>>integrity完整性 信息不被未經授權竄改
>>>availability可用性 確保授權用戶可在允許情況下訪問

```

```
敏感數據 risk appetite 
--雲宮應用必須提供方法讓客戶根據數據的敏感程度進行分類categorization和分級classification確保得到相應的保護
虛擬化技術 virtual machine 
--利用快照snapshot保存單個文件保存在某個位址當用戶再次請求可以恢復離開前的情景
加密技術 提供一定程度的安全保證
--可在到達雲端前進行加密、必要時解密，可緩解竊聽攔截的威脅

合規與持續審計 on going audit
--在已知經測試的整體方案符合PCIDSS、GLBA、HIPAA控制集合和步驟概要
--但供應商不願開放物理訪問許可分享網路部署和安全控制列表、維護這些內下的幾密性可增強公應傷整體安全水平
--很難確定哪個設備承載哪個客戶數據、通常提供他們自己審計成功聲明 SSAE SOC3

雲服務提供商合同 SLA
--每個參與方負責的服務內容、採取哪種服務形式、出現問題如何解決
--一訂時間範圍為這些服務設置特定量化的目標和相應配置
--確保客戶能持續不間斷訪問自己的數據儲存資源、未能滿足所受懲罰

```

```
--
--
>>>
--
>>>
>>>
--
--
>>>
>>>
--
--


```

```
--
--
>>>
--
>>>
>>>
--
--
>>>
>>>
--
--


```
