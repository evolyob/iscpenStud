
防護能力/存取控制
```
系統存取可對各種類型帳戶的權限，應採用最小權限原則來限制使用者、設備(包含其他資訊系統)存取系統
-->> 密碼原則、失敗鎖定、GPO組態設定及強制派送檢查、員工離職後立即禁用其使用者帳號和密碼
-->> 管理特定員工才能使用機敏應用程式或資料、存取前須經過身分認證 
-->> 防止非特權用戶執行特權活動或記錄非特權用戶使用管理者權限的狀況 
-->> 資安政策有提供行動設備（如：筆電、平板和手機）使用指南及存取公司網路和資訊

對遠端(無線)存取進行監控與控制權限，並定義管理遠端網路存取需考量哪些風險因素 
-->> 只允許經過公司資安配置設定或使用VPN來進行遠端連線，基於TLS的VPN機制並有自動監控確保符合組織政策
-->> 連接無線網路之前都需要經過授權，無線存取採用加密保護(WPA2)，不活動後會終止所有使用者的Session連線
```
防護能力/配置管理
```
可識別資訊系統使用者和使用者所執行的程式或設備，使用前驗證帳戶、程式或設備的身份。
-->> 設置身分認證系統，員工都有唯一帳號識別每個人，定期盤點任何閒置帳戶。
-->> 第一次登錄時必須更改他們的臨時密碼及有限制個人使用重複密碼的頻率
```
防護能力/系統和通訊保護
```
外部邊界和關鍵內部邊界監視、控制和保護組織通訊，並滿足與內部網路分離 
-->> 防火牆規則預設為原則禁止、例外允許並定期查看防火牆規則。
-->> 檢查伺服器上TLS、VPN配置是安全性及監控未授權使用VoIP
-->> 設置DMZ(非軍事區 )、Vlan 網段、單獨安全區保護敏感資料。

任何帳戶權限在進行網路連線存取時身份驗證機制，並建置、部屬和管理加密金鑰
-->> 啟用傳輸層安全性(TLS)以存取並使用SSH2協定，
-->> 針對特權用戶使用多因素身份驗證(MFA)或使用公鑰基礎設施(PKI)或一次性密碼(OTP)

使用者功能與系統管理功能分開並採用SSDLC、實體和虛擬隔離系統安全技術。
-->> 使用獨立管理通道進行維護，重要系統隔離到單獨安全區及採用加密技術保護靜態資料。
-->> 專責人員負責制定強化組織資安、工程設計原則文件，應定期檢查軟、硬體升級需求。
-->> 系統管理員只能從特權帳戶執行系統管理功能，不允許一般用戶執行系統管理功能
-->> 定期執行作業系統的資安強化作業及驗證作業系統設置正確性。
```
防護能力/系統和資訊完整性
```
使用與受保護資訊和系統相關的威脅指標資訊，以及從外部組織獲得的有效緩解措施、即時辨識、報告、糾正和漏洞
-->>團隊定期接受及掌握來自商業、公開TTP威脅情資、外部ISAC的資安情資(TWCERT/CC、廠商平台通知)

系統的重要位置上佈署惡意程式防護分析系統行為來偵測，潛在惡意行為的指令和腳本於正常系統上執行。
-->> 部署端點偵測和回應方案(EDR)到組織端點設備，持續偵測攻擊和攻擊指標。
-->> antiV 閒置一小時後開始更新及掃描排程
path: \\\Microsoft\Windows\Windows Defender
mail存取入口和出口點採用垃圾郵件保護機制。 
-->> 有垃圾郵件入站(阻擋垃圾郵件)、出站(避免發送垃圾郵件)防護機制定期查看和改進過濾規則 
-->> 實施電子郵件保護阻止偽造寄件者位址(DKIM、SPF和DMARC)
```

防護能力/資安意識與訓練
```
確保管理者、系統管理員和組織系統使用者，了解與其操作相關的安全風險，人員接受其所分配的資訊安全相關職責訓練內容設有資安專業培訓預算
-->>資安意識提升活動、有提供培訓材料，使企業研發人員對社交工程攻擊有感 
-->>基於員工角色與職責及定制內部威脅指標培訓課程 
```

防護能力/資安維護
```
組織系統上執行維護管理 
-->> 定期糾正性修復技術、預防性更新、適應性操作環境的變化、完善性改進操作
-->> 進行系統維護的流程都需要獲得批准
-->> 供應商執行維護活動時只提供臨時授權、結束後失效 
```

防護能力/媒體防護
```
將受管制資訊的存取權限，限制為僅允許授權用戶
-->>只有特權員工才能存取實體儲存安全區，存有管制資料的所有媒體應有標記
-->>所有存取儲存媒介的人都可記錄追蹤完整借閱和歸還流程並禁止使用未知所有者的可攜式設備 
-->>設置可攜式媒體的管制政策，任何非授權的軟體在安裝之前須執行掃描 
```

防護能力/人員安全
```
確保在人員操作期間和操作之後（例如：離職和轉職），皆應保護含有受管制資料的系統。 
-->>能夠存取管制資料的人員必須經過適當的篩選流程 
-->>離職收回所有公司IT設備、員工證、門禁卡和/或鑰匙。
-->>進行離職面談會提醒員工保密義務、刪除對所有授予的存取權限。
```

防護能力/實體保護
```
限制授權人員對組織資訊系統、設備和相應操作環境的實體存取。 
-->>定義檢討哪些人員才能獲得實體存取設備，哪些實體設施配有存取控制措施。
-->>員工和訪客要有記錄訪問公司設施的日誌，訪客需員工陪同。

異地辦公需執行受管制資料的保護措施。 
-->>遠端作業的電腦都安裝漏洞管理和防毒軟體保護
-->>採用多因子身份驗證來驗證用戶身份，存取內部網路時需要VPN連接

```

偵測能力/稽核和可歸責性
```
組織可查看稽核記錄並了解每台機器的活動和系統時間同步。
-->>將稽核記錄功能的管理權限，限縮給特定的特權帳戶
-->>日誌採用通用格式(用戶ID 、來源IP、目標IP、時間戳)匯集到一台或多台集中式儲存伺服器。
-->>提供系統錯誤、備份和還原、配置變更事件、存取控制成功或失敗事件描述。
-->>審核資訊紀錄失敗時告警，重新啟動日誌記錄機制並驗證它確實運作。
 
識別未回報的資產稽核紀錄，並確保組織定義的系統有被適當的記錄下來
-->>有定期確認資產回報日誌狀態，當發現有尚未回報將發送通知。
-->>正確配置日誌記錄，確認儲存空間充足 
-->>指向NTP Server利用FW policy123 port特定來源

```

回應能力/事件通報
```
應具備事件處理的能力，包括準備、檢測、分析、遏制、修復和回報 
-->>建置事件中IT人員需要聯繫對象、通報事件的方式
-->>分析以決定要採取的措施 

事先定義好的程序，建立並實施應變措施 
-->>可分析事件類型、影響程度、優先級劃分、不同優先順序給予通報方案 
-->>應變流程含停止或控制損壞、含與使用者溝通方法、含實施控制措施

組織可偵測和回報事件
-->> 主動追蹤網路資安事件、蒐集內部員工的異常通報並可以在24小時內回應安全事件

網路事件發生時，應收集系統上的事件證據，並確保鑑識資料的安全 
-->>資安事件處理者會調查、收集並記錄初步發現，SOC與事件回應團隊有建議直接溝通管道。
-->>當確認事件發生有建立一個團隊(事件調查、IT技術、系統管理和實體安全等人員)來管理事件。
```

復原能力/復原
```
定期執行資料備份及資料回復驗證程序，滿足組織定義的資訊安全連續性，備援性和可用性要求。 
-->>定期安排備份，建立備份後定期進行測試，至少有一份完整系統備份離線儲存異機/異地。
-->>備份資料只有授權人員存取 
-->>切換備援主機時間間隔在組織可容忍範圍內
```

識別能力/資產管理
```
識別庫存中的元件屬性，以便在發生漏洞時快速識別並找出問題發生點，如此可將修補程式快速部署或進行網路隔離 
-->>執行軟體版本盤點及用來執行修補程式安裝 

```

識別能力/風險管理
```
根據企業需要制定和更新風險管理計劃，涉及企業資料處理、儲存或傳輸，以及組織營運的系統、資產與個人。
-->>定義核心資產、資訊分級標準及執行資產清查，根據風險分級標準，對每項資產/資訊定義其風險值。
-->>制定並定期更新IT供應鏈管理計畫、辨識和評估供應商的風險、適當緩解措施。

定期執行風險評估，以根據定義的風險類別、來源和衡量標準確定優先等級，定期掃描組織系統和應用程式中的漏洞並評估修補漏洞 。
-->> 定義組織功能、所需的IT資產、可能面臨的威脅的嚴重性和影響性來定義風險並分析威脅以確定發生的可能性。
-->> 審閱漏洞評估的優先排序列表並制定緩解計劃，並持續追蹤尚未修補的漏洞。
-->> 對連網資產有定期產出漏洞掃描並且使用的工具為最新版本。

分開管理不受供應商支持的產品（例如，壽命終止），並根據需要進行限制以降低風險。 
-->> 網路中隔離EndofService的產品，有規劃EndofService的產品執行升級、更換或報廢的時程。

對組織的Internet或其他網路連線的跨網閘道器上執行掃描。
-->>有記錄網路邊界安全配置狀態及驗證配置的正確性。

```

識別能力/資安評估
```
組織可定期評估組織系統中的安全控制，以確定這些控制在其應用中是否有效，
定期更新系統安全計劃，這些計劃描述系統邊界、系統運行環境、安全要求的實現方式，以及與其他系統的關係。
-->>制定組織如何實施安全要求之文件、角色、職責 、權責、聯繫及定期更新
-->>有描述深度防禦策略、允許的Port和網路協定，記錄安全控制評估結果、新發現的風險。

針對內部開發、內部使用的企業軟體進行資安評估，並持續監控安全控制措施。
-->> 組織軟體都有執行程式碼審查，定期舉行會議評估控制措施缺口、風險及第三方安全評估員進行評估。
```
