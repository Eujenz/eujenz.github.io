---
title: 'Deposition'
date: 2024-09-26T00:16:24+08:00
draft: false
tags: ["半導體製程技術", "CVD", "ALD", "PVD"]
summary: ""
categories: ["半導體製程技術"]
showtoc: true  # 顯示目錄
tocopen: true  # 預設展開目錄
mathjax: true
---

## SMT薄膜沉積（Deposition）課堂重點整理
薄膜沉積技術是半導體製造中不可或缺的步驟，負責在晶圓表面形成多層金屬互連和介電層，實現電氣隔離與導電連接。

### 1. 薄膜沉積（Deposition）
薄膜沉積技術是指在晶圓表面形成極薄的固體膜的過程。這些薄膜包括金屬層和介電層，負責在晶片上實現電氣隔離和導電連接。薄膜沉積是多層金屬化過程中的關鍵步驟，對確保晶片性能、可靠性和製造效率至關重要。主要挑戰包括薄膜的均勻性、步覆蓋性（step coverage）以及其電氣性能。


### 4. 晶圓製造中的製程流程
- 擴散（Diffusion）： 在晶圓中引入摻雜物，改變其電性質。
- 蝕刻（Etching）： 去除不需要的材料，形成所需的圖案。
- 光刻（Photolithography）： 使用光掩膜將圖案轉移到晶圓表面。
- 拋光（Polishing）： 通過化學機械平坦化（CMP）技術平滑晶圓表面。
- 薄膜沉積（Deposition）： 在晶圓表面沉積金屬層和介電層。
- 封裝（Packaging）： 將完成的晶圓切割成單個晶片，進行封裝以保護元件。

### 5. 薄膜層的種類

薄膜沉積種類主要分為：
- 金屬層（Metal Layers）： 用於導電連接，實現晶片內部的電氣互連。常用的金屬材料包括鋁（Al）和銅（Cu）。
- 介電層（Dielectric Layers）： 提供電氣隔離，防止不同金屬層之間的短路。常用的介電材料包括SiO₂和低介電常數材料（low-k dielectrics）。

### 6. ULSI晶片的多層金屬化結構

在ULSI（Ultra Large Scale Integration）晶片中，多層金屬化結構包括多個金屬層（如M1至M4）和介電層（如ILD1至ILD6）的交替排列。
這些金屬層負責不同層次的電氣互連，而介電層則提供絕緣，防止不同金屬層之間的電氣干擾。低k材料在這些介電層中被廣泛應用，以減少寄生電容，降低RC延遲，從而提高晶片的運行速度和性能。

### 7. 晶片中的金屬層是如何沉積的？為什麼從鋁轉向銅？

晶片中的金屬層通常通過以下步驟沉積：

    沉積阻擋層（如Ti/TiN）： 防止金屬擴散並提高附著性。
    沉積金屬籽層（如銅籽層）： 提供銅電鍍的基底。
    銅電鍍（Electroplating）： 在籽層上沉積銅，填充導通孔和金屬層。

早期使用鋁（Al）作為導電層，但隨著技術的發展，銅（Cu）逐漸取代鋁，原因包括：

    較低的電阻： 銅的電阻率低於鋁，能顯著降低電路的電阻。
    更好的電遷移抗性： 銅在高電流下較不易發生電遷移，提高導線的穩定性。
    更高的速度： 銅能夠支持更高的運行速度，滿足現代高性能晶片的需求。

然而，銅的沉積和蝕刻過程較鋁複雜，需要使用先進的技術如Damascene工藝來實現高效沉積和精確蝕刻。
### 8. 薄膜沉積的主要特性
    良好的步覆蓋性（Step Coverage）： 能夠有效覆蓋晶片表面的凹凸不平區域，確保導電層的連續性。
    填充高縱橫比的間隙能力： 能夠在高縱橫比的導通孔和溝槽中均勻填充金屬或介電材料，防止孔洞和缺陷的形成。
    均勻的厚度分佈： 確保整個晶片表面的薄膜厚度一致，避免局部過薄或過厚影響電氣性能。
    高純度： 薄膜材料需具有高純度，避免移動離子和顆粒的污染，確保薄膜的電氣性能和結構完美性。
    低薄膜應力： 控制薄膜沉積過程中的應力，防止晶片翹曲和裂紋的產生。

這些特性對於確保晶片的可靠性和高性能運行至關重

9. 固態薄膜是什麼？其在製程中的作用是什麼？

固態薄膜是指沉積在晶片表面上的極薄的固體材料層，厚度通常在納米到微米範圍內。這些薄膜能夠有效覆蓋整個基板，確保電氣性能和結構的完整性。固態薄膜在製程中的作用包括：

    提供電氣隔離和導電連接： 通過多層金屬化實現不同元件之間的電氣互連。
    保護晶片表面： 防止化學腐蝕和物理損傷。
    影響元件性能： 薄膜的厚度、均勻性和材料特性直接影響晶片的電氣性能和可靠性。

10. 薄膜在階梯結構上的覆蓋特性有何重要性？

薄膜在階梯結構上的覆蓋特性，即步覆蓋性（Step Coverage），對於確保導電層的連續性和電氣性能至關重要。良好的步覆蓋性能夠有效覆蓋晶片表面的凹凸不平區域，避免形成薄膜厚度不一致或孔洞，確保導電層的可靠連接。反之，不均勻覆蓋會導致薄膜厚度變化，影響電路的電阻和穩定性，甚至導致導線失效。
11. 薄膜沉積中的縱橫比是什麼？其對沉積工藝有何影響？

縱橫比（Aspect Ratio）指的是沉積區域的深度與寬度之比。在薄膜沉積中，高縱橫比意味著需要在狹窄且深的間隙中填充材料。高縱橫比對沉積工藝提出了更高的要求，包括：

    填充能力： 薄膜需能夠均勻填充高縱橫比的間隙，避免孔洞和缺陷。
    步覆蓋性： 薄膜需能夠有效覆蓋間隙內部的垂直和水平面。
    沉積速率和均勻性： 高縱橫比的結構需要高效且均勻的沉積技術，以確保薄膜的質量和一致性。

隨著晶片設計的不斷縮小，縱橫比的挑戰變得更加顯著，要求使用先進的沉積技術如高密度等離子體CVD（HDPCVD）和雙Damascene工藝來應對。
12. 高縱橫比間隙在半導體製程中的重要性是什麼？

高縱橫比間隙在現代半導體製程中尤為重要，因為隨著晶片集成度的提升，導通孔和溝槽的尺寸越來越小且縱橫比越來越高。這些高縱橫比間隙需要高效且均勻的材料填充，以確保金屬層和介電層的電氣性能和結構完整性。未能有效填充高縱橫比間隙可能導致導電層的電阻增加、信號延遲以及元件失效，從而影響整個晶片的性能和可靠性。
13. 薄膜生長的三個階段是什麼？每個階段的特點是什麼？

薄膜生長的三個階段包括成核（Nucleation）、聚合（Aggregation）和連續薄膜形成（Continuous Film Formation）：

    成核階段（Nucleation Phase）：
        特點： 薄膜材料開始在晶片表面形成微小的晶核。
        影響因素： 表面能量、溫度和沉積速率影響晶核的大小和分佈。
        結果： 初期薄膜中存在較多的晶核，影響後續薄膜的結晶性和均勻性。

    聚合階段（Aggregation Phase）：
        特點： 晶核逐漸增大並開始聚合，形成更大的晶粒。
        影響因素： 表面擴散性和成核速率影響晶粒的成長。
        結果： 薄膜逐漸從多晶態轉變為更有序的結構，晶粒尺寸增大。

    連續薄膜形成階段（Continuous Film Formation Phase）：
        特點： 薄膜材料覆蓋整個晶片表面，形成連續且均勻的薄膜。
        影響因素： 沉積速率和材料供應影響薄膜的完整性。
        結果： 形成高質量的薄膜，具備良好的電氣和機械性能。

14. 化學與物理沉積過程有何不同？各種沉積技術有何優缺點？

化學和物理沉積過程的主要區別在於沉積材料的轉移方式和沉積機理：

    化學沉積（如CVD）：
        機理： 通過氣相化學反應在晶片表面生成固體薄膜。
        優點： 能夠覆蓋複雜結構，沉積均勻性高，適合高縱橫比間隙填充。
        缺點： 需要較高的溫度和複雜的氣體控制，可能產生副產物。

    物理沉積（如PVD）：
        機理： 通過物理方法（如蒸發或濺射）將材料從靶材轉移到晶片表面。
        優點： 沉積速率高，設備相對簡單，適合沉積金屬薄膜。
        缺點： 步覆蓋性較差，難以覆蓋高縱橫比間隙，薄膜均勻性可能較低。

常見沉積技術的優缺點比較：
沉積技術	優點	缺點
CVD	覆蓋均勻、適合高縱橫比間隙、材料種類多	需要高溫、設備複雜、可能產生副產物
PVD	沉積速率高、設備簡單、適合金屬薄膜	步覆蓋性差、難以覆蓋高縱橫比間隙、薄膜均勻性低
蒸鍍	簡單高效、成本較低	覆蓋性差、難以控制薄膜厚度
旋塗法	適合自旋塗佈的薄膜、厚度均勻	只適用於低縱橫比結構、難以覆蓋複雜結構
15. 什麼是化學氣相沉積（CVD），其主要特點是什麼？

化學氣相沉積（CVD） 是一種通過氣體混合物的化學反應在晶片表面沉積固體薄膜的技術。其主要特點包括：

    化學反應參與過程： 薄膜的形成依賴於反應物在氣相中的化學反應。
    所有薄膜材料均由外部供應： 沉積所需的前驅物均需從外部供應，確保薄膜的純度和質量。
    反應物必須以氣態存在： 反應物以氣態形式進入反應室，與晶片表面進行反應形成薄膜。

CVD技術適用於沉積各種材料，包括氧化物、氮化物和金屬等，廣泛應用於多層金屬化和介電層的製程中。
16. 化學氣相沉積（CVD）的設備結構是什麼樣的？

CVD設備主要包括以下幾個部分：

    反應器（Reactor）： 核心部件，負責進行氣體反應和薄膜沉積。
    加熱系統（Heating System）： 提供必要的溫度，使化學反應順利進行。
    氣體供應系統（Gas Supply System）： 控制反應物氣體的流量和混合比例。
    氣體分佈系統（Gas Distribution System）： 確保氣體均勻分佈在晶片表面，實現均勻沉積。
    排氣系統（Exhaust System）： 移除反應生成的副產物和未反應的氣體，保持反應室的清潔。
    溫度控制系統（Temperature Control System）： 精確控制反應器內的溫度，確保沉積過程的穩定性和均勻性。

CVD設備根據壓力和氣體流動特性可分為多種類型，如大氣壓CVD（APCVD）、低壓CVD（LPCVD）、等離子輔助CVD（PECVD）等，每種類型適用於不同的應用場景。
17. CVD中的化學過程包括哪些類型？請舉例說明。

CVD中的化學過程主要包括以下五種類型：

    熱分解（Pyrolysis）：
        描述： 高溫下，前驅物分解生成沉積材料。
        例子： 四乙氧基矽（TEOS）在高溫下分解生成SiO₂。

    光解（Photolysis）：
        描述： 使用光源激發前驅物，使其分解生成沉積材料。
        例子： 使用紫外光分解有機硅化合物沉積SiO₂。

    還原反應（Reduction）：
        描述： 前驅物在還原性氣氛下反應生成沉積材料。
        例子： 使用氫氣還原金屬有機前驅物沉積金屬薄膜。

    氧化反應（Oxidation）：
        描述： 前驅物在氧氣或水蒸氣中反應生成氧化物薄膜。
        例子： 在氧氣環境中沉積SiO₂薄膜。

    氧化還原反應（Redox Reaction）：
        描述： 前驅物同時經歷氧化和還原過程生成複合薄膜。
        例子： 使用含氮前驅物沉積氮化矽（Si₃N₄）薄膜。

這些化學過程決定了CVD技術能夠沉積各種材料，滿足不同半導體製程的需求。
18. CVD反應的八個基本步驟是什麼？每個步驟的作用是什麼？

CVD反應的八個基本步驟包括：

    氣體傳輸到反應室： 前驅物氣體通過氣體供應系統進入反應室。
    前驅物與反應氣體的反應： 前驅物與其他反應氣體在反應室內發生化學反應。
    氣體擴散至基板表面： 反應氣體擴散至晶片表面，準備進行表面反應。
    前驅物在表面吸附： 前驅物分子在晶片表面吸附，形成吸附層。
    前驅物擴散到基板內部： 吸附的前驅物分子擴散至基板內部，準備與矽反應。
    表面反應形成薄膜： 前驅物分子在晶片表面發生化學反應，生成固體薄膜。
    副產物脫附： 化學反應生成的副產物從晶片表面脫附。
    副產物通過氣體流動移除反應室： 副產物隨氣體流動被移除，保持反應室內的清潔。

這些步驟強調了氣體流動和表面反應對薄膜形成的重要性，尤其是如何控制反應速度來確保均勻的沉積。
19. 氣體流動及CVD反應的限制因素有哪些？

CVD反應速度受以下兩個主要機制限制：

    質量傳輸限制（Mass Transport Limitation）：
        描述： 在高溫和高壓下，反應物的供應不足會限制反應速度。
        特點： 質量傳輸限制對溫度變化不敏感，主要受氣體流量和壓力影響。

    表面反應限制（Surface Reaction Limitation）：
        描述： 在低溫下，反應物分子缺乏足夠的能量進行表面反應，導致反應速率降低。
        特點： 表面反應限制對溫度變化非常敏感，溫度提高能顯著提升反應速率。

這兩種限制因素決定了CVD反應的整體速率和沉積薄膜的品質。
20. CVD沉積過程中的沉積區域有哪些？它們的特點是什麼？

CVD沉積過程中的沉積區域包括：

    強制對流區（Forced Convection Zone）：
        描述： 反應物氣體進入反應室後的區域，氣體以快速對流方式進行擴散。
        特點： 高氣流速度，反應物氣體迅速傳輸至晶片表面。

    邊界層（Boundary Layer）：
        描述： 反應物氣體接觸晶片表面時形成的緩衝區，氣體流動速度較慢。
        特點： 氣體在此區域進行化學反應，形成初始薄膜。

    沉積區域（Deposition Zone）：
        描述： 反應物氣體在基板表面進行沉積，形成薄膜。
        特點： 薄膜材料在此區域生長，確保薄膜的完整性和均勻性。

這些沉積區域的劃分有助於理解氣體在反應器內的流動和反應過程，從而優化沉積條件以提升薄膜質量。
21. 氣體動力學與表面沉積有何關係？低壓下如何提高沉積效率？

氣體動力學在CVD沉積過程中扮演著關鍵角色，決定了反應物氣體如何在晶片表面進行擴散和反應。尤其在低壓條件下，氣體分子之間的碰撞減少，氣體動力學效應增強，反應物氣體更容易到達晶片表面進行沉積反應。

在低壓下提高沉積效率的方法包括：

    減小晶片間的間隔： 降低晶片之間的距離，可以增加氣體分子到達晶片表面的機會，提升沉積速率。
    優化氣體流量和壓力： 精確控制氣體流量和反應室壓力，確保反應物氣體均勻分布，提高沉積效率。
    使用高活性前驅物： 選擇具有高反應活性的前驅物氣體，促進表面反應，提升沉積速率。

這些方法有助於在低壓條件下實現高效且均勻的薄膜沉積。
22. CVD沉積中的摻雜效應是什麼？其對薄膜特性有何影響？

在CVD沉積過程中，摻雜效應指的是在沉積氣體中加入摻雜劑，以改變沉積薄膜的電學和物理特性。摻雜劑可以在沉積過程中引入特定的雜質元素，影響薄膜的導電性、應力和結構。

摻雜效應對薄膜特性的影響包括：

    改變導電性： 通過摻雜，薄膜的導電性可以得到調整，以滿足不同電氣需求。
    調整應力： 摻雜劑的加入可以調整薄膜的內部應力，減少薄膜應力導致的晶片翹曲和裂紋。
    影響結構穩定性： 摻雜劑可以改變薄膜的晶體結構，提升薄膜的穩定性和耐久性。

具體應用：

    形成磷硅玻璃（PSG）： 通過加入磷摻雜劑，可以形成PSG，有助於去除離子污染，並降低薄膜應力。
    調整薄膜流動性和熔點： 摻雜物的濃度和種類會影響薄膜的流動性和熔點，需精確控制以達到所需的薄膜特性。

23. CVD系統的設計與配置有哪些關鍵因素？

CVD系統的設計與配置對沉積薄膜的質量和製程穩定性至關重要，主要包括以下關鍵因素：

    反應器的加熱設計： 提供均勻且可控的加熱源，確保反應器內的溫度一致性。
    氣體流量控制系統： 精確控制反應物氣體的流量和混合比例，確保沉積過程的穩定性。
    壓力控制系統： 調整反應室內的壓力，影響氣體分布和沉積速率。
    氣體分佈系統： 設計合理的氣體流道，確保反應物氣體均勻分布在晶片表面，實現均勻沉積。
    冷卻系統： 控制反應器內的溫度，防止過熱或冷卻不均，保持製程的穩定性。
    排氣系統： 高效移除反應生成的副產物和未反應氣體，保持反應室的清潔和安全。
    自動化控制系統： 實現沉積過程的自動化控制，減少人為操作誤差，提升製程穩定性和重複性。

這些設計和配置因素共同作用，確保CVD系統能夠穩定、高效地進行薄膜沉積，滿足半導體製程的高標準要求。
24. 不同類型的CVD反應器有哪些？它們各自的特點和應用場景是什麼？

不同類型的CVD反應器根據壓力和氣體流動特性可以分為以下幾種：

    大氣壓CVD（APCVD）：
        特點： 操作在大氣壓下，設備結構簡單，沉積速率高。
        應用場景： 適用於需要快速沉積的應用，如某些金屬薄膜和大批量晶圓處理。

    低壓CVD（LPCVD）：
        特點： 操作在低壓下，提供良好的薄膜均勻性和高純度。
        應用場景： 適用於沉積高質量的氧化物、氮化物和多晶矽薄膜，如閘極氧化層和介電層。

    等離子輔助CVD（PECVD）：
        特點： 使用等離子體輔助化學反應，能在較低溫度下沉積薄膜。
        應用場景： 適用於高縱橫比間隙的填充和低應力薄膜的沉積，如低k介電材料和氮化矽薄膜。

    高密度等離子CVD（HDPCVD）：
        特點： 提供更高密度的等離子體，增強薄膜沉積效率和均勻性。
        應用場景： 適用於高縱橫比間隙填充和高性能介電層的沉積，如超高密度集成電路。

    原子層沉積（ALCVD）：
        特點： 通過交替供應前驅物氣體，實現原子層級的沉積控制，薄膜厚度精確可控。
        應用場景： 適用於需要高精度和均勻性的應用，如先進閘極氧化層和高k介電材料的沉積。

25. LPCVD反應室是如何設計的？其在沉積氧化物、氮化物或多晶矽中的應用是什麼？

LPCVD反應室 的設計重點在於實現均勻的薄膜覆蓋和高純度的沉積過程。其主要特點包括：

    高效的氣體流動系統： 確保反應物氣體均勻分布在晶片表面，避免沉積不均。
    穩定的溫度控制系統： 保持反應室內的溫度穩定，確保沉積過程的可重複性和一致性。
    高真空環境： 減少氣體分子間的碰撞，提高沉積速率和薄膜純度。
    高品質材料內襯： 使用耐高溫和耐腐蝕的材料製作反應室內襯，確保長期穩定運行。

在沉積氧化物、氮化物或多晶矽中的應用：

    氧化物沉積： 如SiO₂，用於製作介電層和閘極氧化層，提供電氣隔離和表面保護。
    氮化物沉積： 如Si₃N₄，用於製作氮化層和阻擋層，提供額外的電氣隔離和結構支持。
    多晶矽沉積： 用於製作多晶矽閘極和其他導電結構，提供優良的導電性和高溫穩定性。

LPCVD反應室因其優異的薄膜均勻性和高純度，廣泛應用於先進半導體製程中，滿足高性能晶片的需求。
26. HDPCVD反應器中的晶圓冷卻是如何實現的？其作用是什麼？

HDPCVD（高密度等離子體CVD）反應器 中的晶圓冷卻通常通過背面氦冷卻技術實現。具體步驟如下：

    背面氦冷卻系統： 在晶圓的背面安裝冷卻系統，通過氦氣流過晶圓背面以快速散熱。
    控制熱負荷： 快速散熱減少晶圓在高溫下的總熱負荷，防止薄膜應力過大和晶片翹曲。
    穩定沉積條件： 保持晶圓溫度穩定，確保沉積過程中的薄膜質量和均勻性。

作用：

    減少高溫負載： 降低晶圓在沉積過程中承受的熱量，避免過熱導致的材料變形和性能下降。
    提高沉積效率： 快速冷卻有助於保持反應室內的穩定溫度，提升沉積速率和薄膜均勻性。
    保護晶圓結構： 減少晶圓因高溫引起的翹曲和裂紋，提升元件的可靠性和穩定性。

課後練習

    描述多層金屬化結構，討論薄膜的可接受特徵及薄膜生長的三個階段。

    多層金屬化結構由多個金屬層和介電層交替組成，每個金屬層負責不同層次的電氣互連，介電層提供絕緣，防止不同金屬層之間的短路。薄膜的可接受特徵包括良好的步覆蓋性、高填充能力、均勻的厚度分佈和低應力。薄膜生長的三個階段為成核、聚合和連續薄膜形成，分別涉及晶核的形成、晶粒的增大和薄膜的完整覆蓋。

    概述不同的薄膜沉積技術。

    薄膜沉積技術主要包括化學氣相沉積（CVD）、物理氣相沉積（PVD）、蒸鍍和旋塗法等。CVD通過氣體化學反應沉積薄膜，適合高縱橫比間隙填充；PVD通過物理方法轉移材料，適合快速沉積金屬薄膜；蒸鍍是PVD的一種，通過加熱蒸發材料沉積薄膜；旋塗法適合沉積均勻的有機薄膜，常用於介電材料。

    說明化學氣相沉積（CVD）反應的八個基本步驟及其反應類型。

    CVD反應的八個基本步驟包括：
        氣體傳輸到反應室。
        前驅物與反應氣體的反應。
        氣體擴散至基板表面。
        前驅物在表面吸附。
        前驅物擴散到基板內部。
        表面反應形成薄膜。
        副產物脫附。
        副產物通過氣體流動移除反應室。

    CVD反應類型包括熱分解、光解、還原反應、氧化反應和氧化還原反應，這些反應類型決定了沉積薄膜的組成和特性。

    討論CVD反應的動態及摻雜對薄膜的影響。

    CVD反應的動態受質量傳輸限制和表面反應限制的影響。高溫和高壓下，質量傳輸可能限制反應速率；低溫下，表面反應速度變慢。摻雜在CVD沉積中能改變薄膜的電學和物理特性，如改變導電性、調整應力和影響結構穩定性。精確控制摻雜劑的種類和濃度是確保薄膜性能的關鍵。

    描述不同的CVD系統及其應用。

    不同的CVD系統包括大氣壓CVD（APCVD）、低壓CVD（LPCVD）、等離子輔助CVD（PECVD）、高密度等離子CVD（HDPCVD）和原子層沉積（ALCVD）。APCVD適用於快速沉積大批量晶圓；LPCVD適合沉積高質量氧化物、氮化物和多晶矽薄膜；PECVD適合高縱橫比間隙填充和低應力薄膜；HDPCVD適合高密度集成電路；ALCVD適合需要高精度和均勻性的應用，如先進閘極氧化層。

    討論介電材料在芯片技術中的重要性及應用。

    介電材料在芯片技術中主要用於提供電氣隔離，防止不同金屬層之間的短路，並減少寄生電容，降低RC延遲。低介電常數（low-k dielectrics）材料被廣泛應用於多層金屬化中，以提升信號傳輸速度和晶片性能。高介電常數（high-k dielectrics）材料則用於存儲應用中，如製作高效能的電容器，提升存儲器的密度和效能。

    討論外延層沉積技術及三種外延層沉積方法。

    外延層沉積技術是指在晶片表面沉積與基底材料晶格匹配的薄膜，以增強晶片的電學和機械性能。三種主要的外延層沉積方法包括：
        分子束外延（MBE）： 使用高純度氣體在高真空下沉積薄膜，適合高精度和低缺陷的外延層。
        金屬有機化學氣相沉積（MOCVD）： 通過金屬有機前驅物在較低壓力下沉積外延層，適合大批量生產。
        脈衝激光沉積（PLD）： 使用脈衝激光轟擊靶材，沉積高品質的外延層，適合研究和小批量生產。

    解釋旋轉塗佈介電層的應用。

    旋轉塗佈（Spin Coating）技術用於在晶片表面沉積均勻的液態介電材料薄膜。其應用包括：
        自旋塗佈玻璃（SOG）： 用於填充和覆蓋晶片表面的微小凹凸，提供光滑的介電層。
        自旋塗佈電介質（SOD）： 用於形成均勻的介電薄膜，確保電氣隔離和信號傳輸的穩定性。

    旋轉塗佈技術能夠在晶片表面形成高均勻性的薄膜，適合用於高縱橫比結構的間隙填充，確保後續製程的順利進行。