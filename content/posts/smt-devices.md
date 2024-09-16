---
title: 'SMT-Devices 認識半導體元件'
date: 2024-09-15T00:36:24+08:00
draft: false
tags: ["半導體製程技術", "MOSFET", "CMOS"]
summary: ""
categories: ["半導體製程技術"]
showtoc: true  # 顯示目錄
tocopen: true  # 預設展開目錄
mathjax: true
---


## 類比與數位設備、被動與主動元件與寄生結構
### 類比與數位設備

- **類比設備（Analog Devices）**:
    - 處理連續信號，應用於無線電接收器、音頻系統和汽車點火系統。
    - **特點**: 類比設備能夠放大或處理自然界中的連續信號，通常將物理現象轉換為電子信號。
  
- **數位設備（Digital Devices）**:
    - 處理離散信號，信號形式為二進制「高」或「低」，常見於計算機、計算器等數位邏輯電路。
    - **特點**: 數位設備處理開/關的二進制狀態，主要用於邏輯運算和數據處理，具有精確性和可編程性。

### 被動與主動元件

- **被動元件（Passive Components）**:
    - 不需外部電源來工作，無法放大信號，常見被動元件有：
        - **電阻（Resistor）**: 控制電流並分配電壓。
        - **電容（Capacitor）**: 儲存和釋放電能，常用於濾波與能量存儲。
        - **電感（Inductor）**: 儲存磁能，通常用於電源線路中的濾波。
    - **寄生效應**:
        - **寄生結構（Parasitic Structures）**: 被動元件內部不可避免的效應，如寄生電容和寄生電阻，這些效應會降低電路性能。例如，寄生電容會引起信號耦合，影響高頻響應。

- **主動元件（Active Components）**:
    - 需要外部電源來工作，能夠放大信號或控制電流，常見主動元件有：
        - **二極體（Diode）**: 允許電流單向流動，控制電流方向。
        - **雙極性晶體管（BJT）**: 用於放大信號或作為開關。
        - **場效應晶體管（FET）**: 利用電場控制電流，提供更高的輸入阻抗與更低功耗。
    - **寄生效應**:
        - **寄生結構**: 主動元件內部的寄生結構，如寄生雙極性晶體管與寄生電容，可能會形成非預期的電流路徑，導致漏電、電路不穩定或性能降低。

### 寄生結構的影響

- **寄生電阻（Parasitic Resistance）**:
    - 元件內部材料和接觸點因製程缺陷產生的非理想寄生電阻，增加電路總電阻，導致功耗增加和運行速度下降。
  
- **寄生電容（Parasitic Capacitance）**:
    - 電晶體內部不同層間的寄生電容在高頻信號下會導致不必要的耦合或漏電，影響信號的穩定性與性能。

- **寄生雙極性晶體管（Parasitic Bipolar Transistor）**:
    - 在 MOSFET 中，P 型和 N 型區域可能形成意外的寄生雙極性晶體管，這些寄生晶體管會引發鎖定效應（Latch-up），導致電路短路或失效。

### 小結
- **類比與數位設備**: 類比設備處理連續信號，數位設備處理二進制信號。類比設備多用於自然信號的轉換，數位設備則主要應用於邏輯運算和數據處理。
  
- **被動與主動元件**: 被動元件無法放大信號，而主動元件可以放大信號或控制電流。兩者在電路中相輔相成，但寄生結構會影響其性能，尤其是在高頻應用中。

- **寄生結構的影響**: 寄生電阻、寄生電容和寄生晶體管會降低元件性能，導致功耗增加、信號損耗或電路不穩定，甚至可能引發鎖定效應。



## PN Junction、正向與反向偏壓

### PN Junction 的基本概念
PN 結是由 P 型半導體和 N 型半導體材料相接而形成的界面。P 型材料中多數載子是電洞，而 N 型材料中的多數載子是電子。這些載子在接面附近相互擴散，電子與電洞在接面區域再結合，形成了空乏區（Depletion Region），即一個幾乎沒有自由載子的區域。這個區域的電荷不再能自由移動，導致兩側形成內建電場，並進一步阻止多數載子穿過接面。

### 空乏區的形成與內建電場
當 P 型和 N 型材料相接後，多數載子會跨越接面，電子從 N 型區擴散到 P 型區，而電洞從 P 型區擴散到 N 型區。這些多數載子會在接面附近再結合，留下帶電的施體離子（N 型區）和受體離子（P 型區），從而在接面形成空乏區。在空乏區內，沒有可自由移動的載子，並產生了內建電場，這個電場會形成位能障壁（Barrier Potential），阻止進一步的擴散。

### PN Junction 的重要性
PN 結是所有半導體元件（如二極體、電晶體）的核心，它具有單向導電性，允許電流在一個方向流動而在另一個方向被阻止。這種特性使其在整流、開關和信號放大等應用中至關重要。此外，PN 結還是形成雙極性電晶體（BJT）和場效應電晶體（FET）的基本結構。

### PN Junction 的操作原理
- **正向偏壓（Forward Bias）**: 當 P 型區的電位高於 N 型區時，稱為正向偏壓。在這種情況下，PN 結的內建電場減弱，空乏區縮小，多數載子可以克服位能障壁，電子從 N 型區流向 P 型區，而電洞從 P 型區流向 N 型區。當正向電壓超過內建電位障壁時（矽為 0.7V，鍺為 0.3V），大電流會通過 PN 結，這是一個低阻抗狀態。
  
- **反向偏壓（Reverse Bias）** : 當 N 型區的電位高於 P 型區時，稱為反向偏壓。在這種情況下，空乏區擴大，位能障壁增加，多數載子無法越過 PN 結，因而幾乎沒有電流通過。反向偏壓下僅有少數載子貢獻極小的反向飽和電流，這些少數載子會在反向電場作用下被掃過接面。當反向偏壓過大時，可能會進入崩潰區，導致電流急劇增大。

### PN Junction 的電流-電壓特性
- **正向偏壓下的電流**: 當施加正向電壓時，PN 結導通，電流隨電壓指數上升。
- **反向偏壓下的電流**: 當施加反向偏壓時，反向電流幾乎保持不變，僅由少數載子貢獻極小的漏電流。當反向電壓達到一定臨界值時，會發生崩潰現象，電流急劇增大。

### PN Junction 的實際應用
PN 結是許多常見半導體元件的基礎，如：
- **二極體**: 利用 PN 結的單向導電性實現整流功能。
- **光電二極體**: 將光能轉換為電能，應用於光檢測。
- **雙極性電晶體（BJT）**: 基於兩個 PN 結，應用於信號放大和開關電路中。

### 小結
PN Junction 在現代半導體技術中的重要性主要體現在其控制電子與電洞流動的能力。PDF 中強調了正向與反向偏壓下的不同電流特性以及內建電場的作用，這些基礎知識對理解半導體元件如二極體、電晶體和場效應電晶體至關重要。

## 雙極技術及雙極結型晶體管（BJT）的功能、偏壓、結構與應用
### 雙極技術（Bipolar Technology）概述

雙極技術基於雙極結型晶體管（BJT）的運作機制，利用電子和電洞兩種載子來控制電流。BJT 是半導體元件的核心，特別適用於高速、高電流應用，因其增益特性非常適合放大和開關應用。

### 雙極結型晶體管（BJT）結構

- **發射極（Emitter）**: 發射載子的區域，摻雜濃度最高，釋放多數載子（電子或電洞）。
- **基極（Base）**: 摻雜濃度低，厚度很薄，負責控制來自發射極的載子。
- **集極（Collector）**: 收集來自發射極的載子。

BJT 有兩種類型：
- **NPN 型晶體管**: 發射極為 N 型，基極為 P 型，集極為 N 型。
- **PNP 型晶體管**: 發射極為 P 型，基極為 N 型，集極為 P 型。

### BJT 的運作機制與偏壓

BJT 是一種電流控制元件，基極電流大小控制發射極到集極的電流。

- **正向偏壓（Active Mode）**: 對 NPN 晶體管，當基極-發射極間施加正向電壓，集極-發射極間施加反向電壓時，晶體管進入放大模式，基極的少量電流控制集極-發射極的較大電流。
  
- **截止模式（Cut-off Mode）**: 基極-發射極間無正向偏壓，BJT 處於截止狀態，幾乎沒有電流流過集極。
  
- **飽和模式（Saturation Mode）**: 當基極-發射極和集極-發射極都施加正向偏壓時，BJT 進入飽和狀態，集極-發射極電流達到最大值，常用於開關電路。
  
- **反向有源模式（Reverse Active Mode）**: 基極-集極間施加正向偏壓，發射極-集極間施加反向偏壓，該模式極少使用。

### BJT 的特徵

- **電流增益**: BJT 能放大基極的電流，增益通常以 β（beta）表示，β = IC / IB，即集極電流與基極電流的比值。
- **雙極性導電**: BJT 利用電子和電洞兩種載子來控制電流，這與場效應晶體管（FET）的單載子導電不同。
- **高速開關能力**: BJT 的切換速度快，適用於高頻和高速電路。

### BJT 的應用

- **放大電路**: BJT 廣泛應用於音頻和無線電放大器中，具有高增益和良好的頻率響應。
- **開關電路**: 在數位邏輯電路中，BJT 用於開關，通過在截止模式與飽和模式間切換來控制開關狀態。
- **功率電子元件**: 在高電流、高功率應用，如電源調節器和電機控制，BJT 因其高增益與電流處理能力被廣泛使用。

### BJT 的優勢與劣勢

- **優勢**:
    - **高增益**: 能實現較大的電流放大。
    - **高速操作**: 適合高頻操作與開關應用。
    - **雙極性載子運作**: 同時利用電子與電洞，增強電流控制能力。

- **劣勢**:
    - **高功耗**: 需要連續基極電流來保持導通，功耗較高。
    - **熱效應敏感**: 易受溫度變化影響，尤其在大電流下工作時可能發生熱失控現象。

### BJT 與 MOSFET 的比較

- **BJT**: 電流控制型元件，透過基極電流控制集極和發射極間的電流流動。
- **MOSFET**: 電壓控制型元件，透過閘極電壓控制源極和汲極間的電流。
- **比較**:
    - BJT 優勢在於高增益與高速開關，適用於高頻和高電流應用。
    - MOSFET 功耗低，輸入阻抗高，更適合低功率與高密度應用。

### 結論

BJT 是一種強大的電流控制元件，廣泛應用於放大與開關電路中。由於其高增益和快速響應能力，BJT 在高頻和高功率應用中表現出色。雖然 MOSFET 在低功耗應用中已部分取代了 BJT，但 BJT 在需要高增益與高速性能的電路中仍不可替代。


## CMOS 技術概述

**CMOS**（Complementary Metal-Oxide-Semiconductor，互補式金屬氧化物半導體）是一種廣泛應用於現代數位電路設計的半導體技術，特別是在微處理器、記憶體和其他邏輯電路中。CMOS 技術以低功耗和高效能著稱，其核心在於互補使用 N 型和 P 型場效電晶體（MOSFET）來實現高效運行。

### MOSFET 的基本結構

**MOSFET**（Metal-Oxide-Semiconductor Field-Effect Transistor，金屬氧化物半導體場效電晶體）是 CMOS 技術的核心元件。它由四個主要部分組成：

- **閘極（Gate）**：控制電流的開關。閘極與半導體層之間有一層絕緣層（通常是二氧化矽），使得電場可以控制電流，而無需直接電流流過閘極。
- **源極（Source）**：電流的進入端，電子或電洞的來源。
- **汲極（Drain）**：電流的流出端，電子或電洞的出口。
- **基板（Body）**：通常與源極連接，作為元件的參考電位。

### MOSFET 的工作原理
MOSFET 的工作區域根據 $V_{GS}$ 和 $V_{DS}$ 的不同而變化，這影響了電流 $I_{DS}$ 的流動狀態，進而決定 MOSFET 的功能與應用。

- **$V_{GS}$**：決定 MOSFET 是否導通，當 $V_{GS} > V_{th}$，MOSFET 開啟，形成導電通道。
- **$V_{DS}$**：決定 MOSFET 的工作區域，影響 $I_{DS}$ 的大小。當 $V_{DS}$ 增加到一定程度，MOSFET 進入飽和區，電流達到最大值並保持穩定。
- **$I_{DS}$**：受 $V_{GS}$ 和 $V_{DS}$ 控制。$I_{DS}$ 在截止區幾乎為零，在線性區隨 $V_{DS}$ 增加而增加，在飽和區則由 $V_{GS}$ 決定，趨於飽和。


> | 參數       | 定義與解釋                                                                                                                                           |
> |------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
> | **$V_{DD}$** | 電源電壓，連接在汲極（Drain），源極（Source）通常接地，決定了最大 $V_{DS}$（汲極-源極電壓）。                                                             |
> | **$V_{GG}$** | 閘極電壓，施加於閘極（Gate），決定了 $V_{GS}$（閘極-源極電壓）的大小，進而控制 MOSFET 的開啟或關閉。                                                      |
> | **$V_{DS}$** | 汲極與源極之間的電壓差，控制汲極和源極之間的電流流動，影響 $I_{DS}$。                                                                                  |
> | **$V_{GS}$** | 閘極與源極之間的電壓，決定 MOSFET 是否導通。當 $V_{GS} > V_{th}$ 時，MOSFET 導通並形成導電通道。                                                         |
> | **$I_{DS}$** | 汲極和源極之間的電流，當 MOSFET 開啟時，電流從源極流向汲極，由 $V_{GS}$ 控制並受到 $V_{DS}$ 影響。                                                      |


**MOSFET 的三個工作區域**

| 區域             | 條件                                               | 解釋                                                                                                        | 狀態                                                 |
|------------------|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| **截止區**       | $V_{GS} < V_{th}$                                  | $V_{GS}$ 小於門檻電壓，無導電通道形成，$I_{DS}$ 幾乎為零。                                                   | MOSFET 關閉，無電流流動。                           |
| **線性區**       | $V_{GS} > V_{th}$ 且 $V_{DS} < V_{GS} - V_{th}$    | $V_{GS}$ 超過 $V_{th}$，但 $V_{DS}$ 未達飽和點，MOSFET 充當可變電阻，$I_{DS}$ 隨 $V_{DS}$ 線性增加。             | MOSFET 開啟，電流隨 $V_{DS}$ 增加。                |
| **飽和區**       | $V_{GS} > V_{th}$ 且 $V_{DS} \geq V_{GS} - V_{th}$ | MOSFET 進入飽和區，$I_{DS}$ 主要由 $V_{GS}$ 決定，$I_{DS}$ 趨於穩定，隨 $V_{DS}$ 增加不再顯著增長。                | MOSFET 開啟，但電流達飽和值，主要受 $V_{GS}$ 控制。 |


>-  當 $V_D > V_S$ 時，NMOS 為何仍能導通
>    - 只要 $V_{GS} > V_{th}$，NMOS 就能導通。即使汲極電壓 $V_D$ 大於源極電壓 $V_S$，只要閘極電壓足夠高，通道仍會形成，電子可從源極流向汲極。
>-  NMOS 中靠近汲極的通道變窄原因
>    - $V_{DS}$ 增加時，靠近汲極的通道區域電位升高，導致通道電荷減少，通道變窄，這被稱為夾斷效應（Pinch-Off Effect）。這是 MOSFET 進入飽和區的主要原因。

---


### CMOS 技術的核心元件

CMOS 技術基於兩種主要的 MOSFET：

| **MOSFET 類型**            | **主要載子** | **導通條件**                                     |
|----------------------------|--------------|-------------------------------------------------|
| **nMOSFET**  | 電子         | 正向閘極電壓 $V_{GS} > V_{th}$，電子從源極流向汲極     |
| **pMOSFET**  | 電洞         | 負向閘極電壓 $V_{GS} < V_{th}$，電洞從源極流向汲極     |

CMOS 技術通過互補使用 nMOSFET 和 pMOSFET，在任何時間點，總有一個 MOSFET 處於關閉狀態，這使得 CMOS 電路具有極低的功耗。

### 增強型與耗盡型 MOSFET 的區別
- **耗盡型 MOSFET（Depletion Mode MOSFET）**：廣泛用於數位邏輯電路和開關電路。
- **耗盡型 MOSFET（Depletion Mode MOSFET）**：常用於類比電路或特定的控制系統。


| **MOSFET 類型**                     | **狀態**                | **導通條件**                                          |
|-------------------------------------|------------------------------------------|------------------------------------------------------|
| **增強型 MOSFET** (Enhancement Mode)|  $V_{GS} = 0 V$ 關閉                                      | nMOSFET：$V_{GS} > V_{th}$ 施加正閘極電壓導通         |
|                                     |                                          | pMOSFET：$V_{GS} < V_{th}$ 施加負閘極電壓導通         |
| **耗盡型 MOSFET** (Depletion Mode)  |  $V_{GS} = 0 V$ 導通                                      | nMOSFET：$V_{GS} < V_{th}$ 施加負閘極電壓關閉通道     |
|                                     |                                          | pMOSFET：$V_{GS} > V_{th}$ 施加正閘極電壓關閉通道     |



### CMOS 反相器（CMOS Inverter）

**CMOS 反相器**是 CMOS 技術中最基本且最重要的電路，實現邏輯反轉功能：

- **結構**：由一個 nMOSFET 和一個 pMOSFET 組成，兩者共用同一個輸入（閘極）和輸出。
- **運作原理**：
    - 輸入低電平：pMOSFET 導通，nMOSFET 關閉，輸出高電平。
    - 輸入高電平：nMOSFET 導通，pMOSFET 關閉，輸出低電平。

這種設計使得在穩定狀態下，只有一個 MOSFET 導通，另一個關閉，極大地降低了功耗。

### MOSFET 與 CMOS 的關係

MOSFET 是 CMOS 技術的基石。CMOS 電路通過將 nMOSFET 和 pMOSFET 互補組合，實現低功耗和高效能。當一個 MOSFET 導通時，另一個 MOSFET 關閉，確保在穩態時幾乎沒有電流流過，降低能量消耗。

### CMOS 技術的優點

- **低功耗**：在穩態下無直流電流流動，只有在狀態切換時才有短暫電流，靜態功耗極低。
- **高密度**：支持高密度集成，適合大規模集成電路。
- **高速**：開關速度快，適合高速數位邏輯操作。

### 雙極性接面電晶體（BJT）與 MOSFET 的比較

- **電流驅動 vs 電壓驅動**：
    - **BJT**：電流控制元件，需要基極電流來維持導通，靜態功耗較高。
    - **MOSFET**：電壓控制元件，閘極電壓控制通道的開關，靜態功耗極低。

- **能量消耗**：
    - **BJT**：持續的基極電流導致較高的能量消耗，且開關速度較慢。
    - **MOSFET**：僅在閘極充放電時消耗能量，開關速度快，適合高頻應用。

### BiCMOS 技術

**BiCMOS 技術**結合了 CMOS 技術和**雙極性接面電晶體BJT**的優點：

- **BJT**：提供高增益和強大的電流驅動能力。
- **CMOS**：提供低功耗和高密度集成。

這種技術適用於需要高速和高驅動能力的應用，如高速運算和模擬/數位混合電路。

### 寄生晶體管對 CMOS 鎖定效應的影響

在 CMOS 結構中，P 型和 N 型區域的佈局可能形成寄生雙極性電晶體（BJT），導致鎖定效應（Latch-up）。這會產生不可控的電流迴路，可能損壞電路。

- **預防措施**：透過優化佈局設計、增加護環結構和改善製程來防止鎖定效應。

### 總結

MOSFET 是現代 CMOS 技術的核心元件，透過閘極電壓控制電流的開關功能。增強型和耗盡型 MOSFET 的區別在於是否需要施加閘極電壓來導通。理解 MOSFET 的結構與工作原理，以及它們在 CMOS 電路中的應用，有助於深入掌握現代電子電路的設計與運作。
