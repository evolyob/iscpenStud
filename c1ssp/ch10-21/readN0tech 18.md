ch.18 災難復原計畫
```
BCP評估優先級彈性流程維持業務營運繼續::DRP是BCP補充，中斷後阻止中斷和恢復的技術控制
一但IT無法支持關鍵任務進誠就需要透過DRP還原或恢復，盡可能自動運行、人員培訓

-自然災害  地震、洪水、暴風雨、火災、海嘯、火山、流行病、其他自然事件

-人為災害 火災、恐怖行為、爆炸、電力中斷(UPS)、網路、公共設施和基礎設施故障、軟硬件故障(HA)、罷工示威、偷竊蓄意破壞
>>定期檢查UPS  自動測試報告、每個UPS支持設備數量/類型
>>備用站足夠遠、一但通知能立即使用、備品庫存

系統韌性高可用性和容錯
-**單點故障SPOF造成服務不可用
>>系統韌性  遇到不利可保持可接受水平能力，並恢復到先前狀態能力將確保系統、切換集群到另一台服務器等修復好後恢復原先狀態
>>容錯性  故障後仍可繼續運行能力，能經歷短暫中斷後快速復原(HA)，冗餘組件、RAID、集群切換的額外服務器
保護硬盤驅動  容錯和系統恢復組件用RAID陣列
>>RAID-0 又稱條帶 使用兩到多個磁盤、性能提升但不能容錯,  RAID-1鏡像 使用兩個保存相同數據(可自動或手動切換)
>>RAID-5 帶奇偶校驗的磁條，使用3個或更多、萬一單個丟失就會奇偶校驗允許數學計算重建數據其他接手工作,
>>RAID-6 另種奇偶校驗進行磁盤條帶化、但是要在兩個磁盤做奇偶校驗信息所以至少要四個以上,

-->增加以偶數增加、只要一個鏡像是好的就能繼續工作
>>RAID-10 RAID1+0或是鏡像磁條帶或鏡像帶，配置兩個或多個鏡像(RAID-1)、每個鏡像配置RAID-0::至少要四個磁盤
>>條帶化技術就是一種自動的將 I/O 的負載均衡到多個物理磁盤上的技術，
--->條帶化技術就是將一塊連續的數據分成很多小部分並把他們分別存儲到不同磁盤上去

>>>基於軟件是系統管理陣列磁盤會降低效能但便宜::基於硬件 通常有效可靠，當使用這種陣列增加到關鍵組件的可用性
>>>RAID-5 三個在工作、兩個是備用也可支持熱插拔
```
||熱備|最小數|可用容量||
|:--:|:--:|:--:|:--:|:--:|
|RAID-0|N|2|n*pcs|!=16|
|RAID-1|y|2|(n/2)*pcs|!=16|
|RAID-3|y|3|(n-1)*pcs|!=16|
|RAID-5|y|3|(n-1)*pcs|!=16|
|RAID-0+1|y|4|(n/2)*pcs|!=16|
```
保護服務器  可切換兩台以上集群的容錯添加到關鍵服務器、配置負載均衡集群用來增家係桶可擴展性、
-雲IaaS的自動縮放資源和檢查健康或自動重啟、放在不同區域、兼具可擴展和韌性

保護電源  可用UPS完成系統邏輯關機或直到發電機通電提供穩定電源

可信恢復  故障後注重安全性還是可用性、
>>失敗準備：準備備份、系統恢復及容錯方法
：：系統恢復過程  系統應該重啟到正常用戶能夠登入、恢復受影響丟失受損的文件、更正變更標籤、檢查重要安全設置

>>手動恢復 執行必要操作已實施安全或可性恢復：：自動恢復可信但不能恢復整個服務器故障就需要手動
>>無不當損失的自動恢復  能指特定對象免於受損失的機制、對數據及其他對象恢復重建日誌數據及驗證密鑰系統和安全組件的完整性
>>功能恢復 功能恢復系統能自動恢復某些功能、確保系統能成功完成功能恢復

服務質量QoS  能夠保護負載下數據網路可用性、滿足商業需求環境：：帶寬、延遲、抖動、數據包丟失、干擾、特定流量加密
```
```
恢復策略  能立即展開恢復工作、設計有效恢復計劃涉及關鍵子任務、買足夠保險、實際重製成本、折舊補償：：但不包括紙質
-業務單元  識別和優化重要業務功能順序BIA(不需要完成所有業務功能),
＊＊ 風險管理？
-功能優先級  拆分具體業務過程、按優先級別排序表、MTTR(平均恢復),MTD(最大允許),RTO(恢復時間),RPO(恢復點)、需要干預和額外控制情況
-危機管理    全面恢復流程培訓、正確通知流程和立即響應機制、正確方法處理緊急狀況
-應急溝通    內外部溝通轉給公共關西團隊
-工作組恢復  恢復到正常狀態重新開始日常工作地點和活動、應為不同工作組開發單獨恢復設施

-備用處理站點
>>冷站點  只有備用設施、足夠大能解決組織銀運負荷、可是倉庫、空大樓、
--->沒有預先安裝好計算設施和網路、可使用最低限度通知設備、冗余切換恢復站點、便宜
--->存在巨大時間滯延跟費用很難得到測試、買設備安裝配置、備份還原建立通信鏈路

>>熱站點   隨時接管主站點、定期或持續複製熱站點的服務器、兩點使用帶寬實施同步
--->關閉前充足時間強制進行數據複製、事物日誌備份磁到搬到熱點手動恢復上次發生的事物、都無法的話只能允許丟失部分數據在RPO範圍內
--->與主站點相同級別的紀錄和物理安全機制、也可選擇第三方共享熱點設施再有合同簽署、也可把熱站點當作開發測試環境提供有用的服務

>>溫站點
--->數據連接、對設備預先配置但沒有可用數據和信息、不包含客戶端數據副本、將是和備份介質送到溫站恢復重要數據
--->可通過共享基礎設施、要確保合同有無鎖定政策及實在高需求時期仍有適合設施

>>移動站點  非主流小型工作組、設備齊全的拖車或容易安置單位組成、隨時準備海陸空運去任何地點部署或是有供應商提供
--->可配置冷站或溫站點模式、硬件替換儲備內部額外或重覆設備存在不同但很近位置、可立即取出適和的設備
--->簽署SLA 4,12,24,48小時替換硬件合同當作第二選項唯一恢復、有太多不可控因素

>>雲計算  首選災害復原選項IaaS的服務架構、成本較低按需求提供服務作為備用服務
--->但須考慮如何處理雲環境中問題、設計和配置雲服務、利用冗余選項、地理分佈類似因素
--->雲平台可能內置冗余功能應考慮調查這些選項簡化計畫及特定服務的局限性

>>相互援助協議MAA  現實很少被採用、通過共享設計設施和技術資源、
--->兩方不需要維護昂貴備用處理站點、只維護工作設施一些開方空間、在熱站點情況下可通過完全冗余服務器為彼此提供服務
--->履行協議風險、地理位置太近就沒任何意義、保密性考慮法規要求或商業考慮

數據庫恢復  最適合並在PRO範圍內方案、若超出PRO範圍就有丟失數據風險或成本
>>電子連接  適當備份數據透過批量傳輸轉移到遠處專用(熱)恢復站或是承包商(要求儲存容量、通信帶寬)、定期測試的設置和還原的可用性
--->不是完整數據副本、而是事務紀錄和遠程日誌紀錄選項

>>遠程日誌  更快方式傳輸也可以批量進行、通常每小時或更短更頻繁、傳輸數據庫事務日誌副本包括上次批量傳輸以來發生的事物
--->不會應用實時數據庫服務器而是被存入備份設備、發生災難時找出適合事務日誌將其應用正式數據庫達到當前生產狀態
>>遠程鏡像  最先進備份方案、同時也收到副本一通知就接管適合實施熱站點、但所支援基礎設施和人員成本

```
```
復原計畫開發  文檔類型 by ISO27001, NIST SP800-34
＊＊
--->執行概要：對計畫高度概要、具體部門計畫、負責現實維護關鍵備份系統技術指南、人員檢查、重要成員完整計畫副本
##管理层(包括公关人员)看的概览式文件;
##适用于某个部门的计划;
##针对IT技术人员的技术性指南;
##DR团队人员要使用的检查清单(checklist)
--->檢查表能指導他們行為、技術指南幫助建制啟用備用站點、公關人員有份簡單文檔了解當前復原工作如何協調

-應急響應  立即遵守簡單清晰指令針對DR性質、對事件做出人員種類、需撤離設備和關機可用時間的優先級

-職員和通信  災難時連絡表包含重要成員執行關鍵恢復人員
-評估  簡單評估、分類活動並啟動DR響應::更詳細評估有效性資源分配的優先級

-備份和離站儲存  磁帶、磁盤、雲、其他介質的備分恢復、RPO決定無法容忍最低丟失數據
>>完整  :複製系統所有文件、每個文件歸檔味都會重設或關閉設為0
>>增量  :只複製歸檔位(或時戳)被打開、開啟或設為1，增量備分完歸檔位都會備重置或關閉設為0
:: 復原  完整+時間順序逐次復原
>>差異  :只複製歸檔位(或時戳)被打開、開啟或設為1、但是不會改變歸檔位
:: 復原  完整+最近的一份
->> 增量(長)和差異(短)的不同再發生事件還原所需時間、備份介質保存在主運營中心或附近、檢索信息基於不同地理要滿足監管需求
->> 差異備份是只需要兩個容器(最新完成+差異)，特定時間定期更新。 正式區增量+開發區做差異備份
-1>>現在單位用TB(磁帶和CD已無法應付需求)、目前DRP D2D磁盤到磁盤備份方式或虛擬磁帶庫VTL使用軟體容量配置可變化、異地保存(雲)
-2>>最佳備份::空閒足夠時間備份、避免備份成功的下一次前崩潰應部屬實時連續備份(RAID、集群、鏡像)、消除冗餘文件備份降低儲存成本
-3>>磁帶輪換GFS,漢洛塔,六帶輪換,::分層儲存管理HSM系統是自動化機械備份換帶機 32,64光學或磁帶備份設備組成(單個驅動器陣列)
-軟件託管協議  太依賴訂製開發軟件或小公司開發軟件，在託管協議下將源代碼副本給獨立第三方，用安全方式更新源代碼副本，
--->萬一無法履行SLA第三方會向最終用戶提供源代碼副本，來解決問題或升級軟件

-公用設施  電力水天然氣管道服務，在DRP應包含聯絡信息和措施、
-物流供應  提供食物水避難所適當設施。
-恢復和還原比較  恢復工作花費很長時間將業務營運和流程還原到工作狀態::還原業務設施和環境還原到可工作狀態
-迅速應用DRP和還原IT能力在MTD/RTO內完成，確認原站是安全還原至最初能力狀態或原始位置、找到可靠性高的基礎設施
-重構網路進行壓力測試，關鍵任務進程返回原有站點過程存在嚴重脆弱性時 回到原有站點會災難
```
```
培訓、意識和文檔紀錄
-新員工入職培訓、第一次擔任DR腳色初始培訓、詳細在培訓、其他進行簡要意識培訓
-關鍵人員和高級管理人知曉整個計畫和理解高級實施細節，但不必每個參與者需了解全部內容

測試維護
-通讀測試  最簡單最重要的測試、只需分發計畫的副本要求審查、完全書面演練
--->職責意識定期複習知識、根據變化更新修改內容、利用崗位描述納入恢復職責

-結構化演練  桌面演練、情境只有主持人知道、透過討論特定災難得出適當響應方法、項目組會議
--->不同情境範圍、物理動作演練、要求所有人離開大樓回家參加演練

-模擬測試  與結構化類似呈現情境並要求做適當響應、某些響應措施後就被測試
--->可能中斷""非關鍵的業務活並使用某些運營人員

-並行測試 下一層級測試、**實際人員重新部署到備用站恢復並實施站點啟用、
--->以實際發生履行他們恢復職責、不會中斷主要設施運營但這個站點仍處理日常業務

-完全中斷測試  與並行測試類似但關閉實際主站點移轉到恢復站點、風險很大
--->測試完畢、主站點執行恢復營運

-經驗教訓  時間是經驗總結的關鍵、指導未來的反饋 NIST SP800-61
>>到底發生什麼、何時、處理事件表現、是否遵循文件程序、程序是否足夠、是否採取可能阻礙恢復的行動
>>下次發生類似事件會採取哪些不同措施、改進和其他組織共享、糾正錯是可以防止哪些會發生的事件
>>未來應注意哪些前兆或指標來檢測類似事件、需要哪些工具或資源分析或抑制未來風險事件、紀錄報告和建議

-維護  定期消防訓練和演練確保所有元素正確使用、所有職員培訓、重覆這些過程和演練、了解所有設施位置
```
