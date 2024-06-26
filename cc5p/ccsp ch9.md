ch.9 運營管理

```

--持續監控
-->操作系統日誌 OS logging 集成持續監控性能和事件的工具、還可設定日誌便於容量利用率接近限度或性能下降超出SLA範圍
-->硬件的持續監控 Hardware CPU溫度、風扇轉速、電壓、負載、時間速度、驅動溫度的指標  
-->網路的持續監控 Network 間空佈線和SDN控制平面、確保滿足當前量需求和新增需求、對靈活性和可擴展性不會出現超載或延遲

--環境溫溼度影響 ASHRAE TC 9.9(2016)推薦
-->64~81F(18~27C)、相對濕度60%＋特定產品性能參數的環境因素的意見

維護 
--通用維護概念   一直處於維護模式、特定組建和系統持續維護和正常運行是必要的且不中斷
-->維護前所有操作實例都從系統設備移出  維護前將特定系統和設備內的VM遷出
-->防止所有新的登入  避免客戶登入受影響的系統和設備
-->確保日誌持續性並開啟增強日誌記錄  紀錄管理員活動的速率和詳細級別更高、維運模式是一種管理功能更需增強日誌記錄功能

更新 遵守供應商指導建議並作紀錄是履行應盡職責
-->紀錄如何、何時及何發起更新  詳細說明：日期、更新代碼或號碼、說明和理由
-->通過變更管理CM流程進行更新  更新前應沙鄉測試作為CM一部分  
->> 將系統和設備設置維護模式、更新到必要的系統和設備(資產清單添加注釋)、確認所有必要系統設備已更新
->> 驗證修改確保預期結果並能與其他部分進行適當交互、恢復正常操作恢復正常業務

->>update更新：現有系統和組件 
->>upgrade升級：替換舊元素、紀錄資產清單的變化、安全移除舊元素

--補丁管理 軟件相關更新、為了即時響應給定需求(漏洞)和滿足常規目的(修復、增強)

時機
>>>不部署補丁視為使用產品客戶給予“應盡關注”
->>急於解決問題、補丁往往不夠完美可能削弱交互性或街口能力導致新漏洞或影響其他系統
->>可能會根據其他競爭對手部署補丁確定效果和結果再執行、但客戶可依沒像其他服務供應商那樣旅行增進職責造成索賠的額外風險

實施
>>>自動  更快分法多目標系統、補丁工具可能包括報告功能著名哪些已獲補釘與資產清單互相參照通知哪些遺漏、
->>     可能被錯誤應用、報告可能不準確或描述不準確地完成狀態有誤
>>>手動  比工具更可靠、更了解例外活動、但可能漏一些目標和比自動化滿得多可能不夠徹底

日期時區時鐘  推送到整個環境、實際時間和時戳可能成為重要且具有誤導性問題(如果沒有打補丁時沒有運行就會延後下一個自然日執行)
->>不僅限於自動，這些目標系統可能收度補丁或管理員沒有意識到、
->>兩者並用、手動監督有助於補丁的實用性和測試補丁在環境是否適用、自動工具可用於傳播補丁和應用一至性

```
變更和配置管理 change management configuration management
```
配置、版本、偏差、例外、緣由
--基線 一種準確描述所期望的標準狀態方法、所需功能和安全性、對網路和系統的通用映射、說明每個控制項目的、依賴關西和支持理由
-->通過CM流程修改環境充分了解風險管理、是否增加任何風險、是風需增家補償性控制來管理新風險
->>如果擁有多個基線、須確保每個不同建構之前的互相操作性、覆蓋範圍的合理性
->>偏離基線應被調查和紀錄

--偏差和例外 任合有意無意、授權未授權的偏差必須記錄和審查、可能錯誤補丁管理流程、外部攻擊、不佳版本
-->被分配CM角色人員有責任確認事故原因和後續行動、確保機線是靈活實用、例外請求過程是即時
->>安全人員的工作是支持運營不是阻礙生產的人員、若足夠多例外請求相同或類似修改可能需要改變基線

--角色與流程 
-->CMB CM委員會組成、詳細流程、文件要求、請求例外的說明、
->>分配CM任務(驗證掃描、分析和偏差通知)、處理檢測的偏差過程、採取措施和責任
->>CMB由各利益相關方組成或組織認為有用的參與者
->>CMB負責審查變更和例外請求、決定變更是否可以增強功能和提高生產效能、
->>>>變更是否得到資助、是否產生潛在安全影響、需要資金、培訓、安全人員採取額外措施確保變更是合理成功
->>CMB **應經常招開會議、避免變更和例外請求被過度延遲，變更和例外請求到達一定閥值才安排臨時開會
->>>> 風險和收益的權衡、組織應作出相應的決定

->>全面資產清單 組織擁有的資產至關重要、可由其他來源(BIA)提供信息補助完成
->>制定基線 正式行動、包括CMB所有成員(影響相關部門將來所有的工作)、根據成本效益和風險分析進行協商
->>>> 使用已有來源通知此次協商、包括風險管理框架、企業和安全架構

->>確立安全基線 由CMB編寫定建立基線版本
->>部署新資產 常用於配置管理、獲得新資產根據CM策略和規程及CMB指導意見、需在相應資產上完成基線配置

變更管理CM流程
>>>會議 CMB開會審議、分析變更和例外請求、 CMB可批准或駁回請求、事前作業：潛在影響的詳細的安全性分析
->>>> CMB確定請求需要額外培訓、管理和安全控制、CMB可能要求者準備額外資金預算
>>>CM測試 如果CMB請求批准、必須在部署前對新修改進行測試、通常發生隔離沙箱網路中
->>>> 該網路模擬正式網路所有架構、流量和過程、測試應確認修改是否對安全性、互操作性或預期功能產生不良影響

->>部署 安照相對指導進行修改、完成後向CBM匯報
->>文檔紀錄  所有修改需要紀錄在案、並反映在資產清單中並向CMB報告

```

業務持續性和災難恢復BC/DR
```
--業務持續性：工作涉及任何服務中斷期間維持關鍵業務
--災難復原：  災難發生中斷後恢復運營、很多組織都合併成一項工作
--事件：    對操作環境計畫外的負面影響
->>>> 差異持續的時間，事件影響持續三天內、災難影響更長時間．事件可能成為災難

--主要關注事項 人員健康和安全放在第一位
->>>> BC/DR工作應將通知、疏散、保護和出口放在優先位置、對象取決可能受上這種情況的影響

-->保證人員離開  不應有障礙或延誤、緊急通道應立即打開(內向外打開)足夠應急照明
-->保證人員安全離開  出口路線上佈置足夠噴水滅火系統、必須有額外控制(持續開關)
->>>> 向所有人通報應急計劃並培訓了解執行計畫．
-->設計保護  滿足當地要求、承受或抵禦環境危害

營運連續性 客戶合同和SLA通常會指出關鍵操作便確定支持關鍵所需元素、
->>>> BIA能告訴哪些資產丟失或中斷將產生最大的不例影響、制定資產清單考慮支持關鍵功能所有元素
--
BC/DR計畫 策略應規定角色、計畫條款、實施和執行
>>>BC/DR列出改計畫和所有響應活動的有線、簡化、直接的程序,被引用描敘每類文件使用方式和時機
->>>> BC/DR過程、檢查清單目的描述必要具體行動、可按執行順序排列、可在活動完成後行程紀錄
->>>> BC/DR 未接受計畫培訓無經驗也允許實施適當行動、有受訓更好，因為災難期間相應角色並非總是可用

->>資產清單視為關鍵條目的列表  必要軟硬件和介質、版本控制數據和適用補丁程序
->>宣布發生事件或災難的情況    管理功能和事件災難響應應區分開來避免影響生產效率
->>>> BC/DR過於響應頻繁則生產效率會受到不必要的不利、或過於謹慎響應則可能延誤而阻礙響應

->>授權宣布  需指定授權方避免允許任何人起動正式響應導致過度可能性、
->>>> BC/DR確保知情有資格受過培惲和負責任的人來做決定、
->>>> BC/DR再充分保證所有安全和健康危害操作和風險已恢復正常才宣布停止、太快會加劇事件或導致新事件

->>聯繫人要點  負責BC/DR活動任務的辦公室聯繫方式、涉及任何外部實體、盡可能具體
->>詳細行動、任務和活動 拆分為BC/DR策略適用的附件或附錄、可則成策略主體

BC/DR工具包 至少是另一地點有個副本、有個鏡像工具包
->>完全相同工具在現場不同位置降低無法獲得和毀壞的可能性、緊急通信設備只是用組織目的、位置和性質
->>所有適當的網路和基礎架構圖的副本、必須軟件副本用於關鍵系統創建乾淨版本和有比要包含適當更新補丁用於當前版本控制
->>緊急聯絡人信息保括一個完整通知列表、文件記錄工具和設備、少量緊急必需品
->>足以使工具包所有店員設備運行至少24小時的新電池、

重新安置BC/DR 可使用熱、撚、冷站在應急行動和恢復期間指派關鍵人員組成骨幹團隊前往恢復地點
>>>雲備份變得無所不在、只要這些地點足夠的設施來容納涉及人員及達成目標所需的足夠帶寬
->>活動應抱括人力資源和財務代表可安排付款所有參與重新安置人員都是必須
->>關鍵人員家屬成員提供足夠支持這樣避免降低當前任務的關注度、最好承擔此選項的額外費用
->>安置地點不受任何導致標準營運中斷的事件影響也不能太遠、導致延誤和出差費用效用不再具有吸引力
->>只影響到園區或局部、可使用聯合運營協議和兩解備忘錄、在本地區屬於其他組織的設施上建議優惠安置地

-->MAD maxAllowDownTime 最大允許停機時間 以時間衡量服務中斷多久導致組織倒閉
-->RTO 服務中斷後恢復營運能力BC/DR目標、這位包括完整營運能力恢復、僅限應急事件期間關鍵能力
->>>> RTO<MAD
-->RPO 恢復點目標 限制由於計畫外世間丟失數據BC/DR的目標、根據上次完全備份


供電
->>UPS不斷電源系統、給特定單個設備或機架輸電、從公用電力轉換到UPS不會對任何供電設備產生不利影響
->>>>>UPS線路調解功能作用正常操作附加組建、可自動抑制公用電力的電湧和功率驟降
->>>>>UPS應持續足夠長時間從而可以平穩關閉受影響系統、更長時間電源中斷應由其他系統供電
->>基礎架構包括HVAC、UPS、應急照明和滅火系統都需要充足發電機功率、
->>冗余電源是必須、雙路供電確保關鍵操作不間斷所需最小功率、發電機自動切換開關與UPS聯合使用
->>BC/DR 所有數據中心必須提供發電機12hrs的燃料、為所有關鍵功能供電
->>BC/DR 計畫其他替代方案可用之前、應預計發電機至少運作72hrs

```
測試
```
-->桌面測試 重要或實際參與者BC/DR在預定時間、如何在給定場景執行任務、對生產的影響最小
-->排練  在測試期間響應並執行最小限度操作、但不會執行所有實際任務、比桌面測試影響大
-->全面測試 未安排、未通知場景執行完整BC/DR活動、包括系統故障轉移和設施撤離、可能真正的中斷
```
