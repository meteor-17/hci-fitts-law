# hci-fitts-law

1.	Experiment Video Link：
    https://youtu.be/DzKO6MzmtMU
   

3.	Scatter Plot:
<img width="1600" height="1100" alt="Code_Generated_Image " src="https://github.com/user-attachments/assets/8e7614da-bb9a-4d31-b864-c2227cd47d01" />

4.	### Custom Empirical Formula & Parameter Analysis

Based on 80 empirical trials collected on the multi-tier radial interface using the Shannon formulation $ID = \log_2(A/W + 1)$, the linear regression model is:

$$MT = 534.72 + 46.32 \times ID \quad (\text{ms})$$

- **Intercept ($a = 534.72\text{ ms}$):**
  Represents non-movement overhead, including initial sensory perception, visual search across concentric sectors, and motor preparation latency. In an automotive cockpit context, this baseline latency (~535 ms) captures the critical glance-off-road duration required for a driver to identify target stimuli before executing a physical pointing gesture.

- **Slope ($b = 46.32\text{ ms/bit}$):**
  Reflects information processing delay per unit of task difficulty. The calculated throughput is $TP = 1/b \approx 21.59\text{ bits/s}$, demonstrating high motor efficiency. The radial clustering significantly suppresses long-distance linear arm movements compared to traditional stretched horizontal dashboards.

- **HCI Implications & Model Correlation ($R^2 = 0.1573, r = 0.3966$):**
  The model empirically validates the safety advantage of concentric hierarchical sizing. The enlarged innermost climate controls (+ / −, $W = 125\text{ px}$) produced the shortest acquisition times (523–532 ms, $ID \approx 1.09\text{ bits}$), while peripheral shortcut sectors ($W = 60\text{ px}$) required higher targeting precision (670–760 ms, $ID \approx 2.17\text{ bits}$). This demonstrates that frequently used primary controls should be allocated to central, high-area targets to minimize driver distraction.


4.	Scenario, Innovation, and Application：
   傳統方向盤：
  	<img width="600" height="600" alt="20241101131812mr9hf1" src="https://github.com/user-attachments/assets/6f4297bf-c158-46a8-aff0-9d5d9a3f39ce" />

   Fitts' Law-based design：
   <img width="1600" height="1333" alt="Code_Generated_Image" src="https://github.com/user-attachments/assets/786288a9-a510-49f3-9a40-6f5b4f36a46b" />

    · Scenario
        駕駛在行駛中，主要視覺注意力必須維持在車前方路面，然而，現代車輛的功能日益繁多，駕駛常需於行車過程中執行次要任務（如切換曲目、     調整音量、變更空調溫度、接聽通話等）。傳統方向盤的控制鍵通常零散分佈在盤面左右兩大區塊，按鍵排列多為平面陣列式或分散橫跨於多個幅條      上。這導致駕駛在盲操時難以快速建立空間參考座標，常因無法精確辨認按鈕位置而被迫將視線移開路面進行二次確認，大幅增加事故風險。

    · Innovation
  	    以圓心為錨點的觸覺定位，相較於傳統平面矩陣式排列，同心圓輪盤提供了一個非常明確的物理與空間參考中心，操作者的手指只要靠向中心的     大半圓，就能立刻建立起方位座標系（如：上方是除霜、右邊是 AUTO、外圍是捷徑），無需依賴視覺，僅靠觸覺就能迅速辨識按鍵層級與方位，而輪
  	盤式按鍵，也大大增強了使用者的肌肉記憶，幫助使用者快速記憶對應按鈕的位置。
  	    將原本分散於左右兩側手勢範圍的操作按鍵，改為全部置於大拇指可及的操作範圍，這讓駕駛的單一隻大拇指在固定握姿下，無需手腕大幅位移     或更換握盤姿勢，即可覆蓋全部功能按鍵。
  	    在傳統佈局中，按鍵間的距離較長，輪盤設計大幅縮短了按鈕間的相互距離，使最長的移動距離不會超過圓的直徑，且利用外擴的角度扇區與大
  	半圓補償了容錯空間，壓低了難度指數，擁有費茨法則下的多項優勢。

  	· Application（實際應用價值與解決之 HCI 問題）
    實現了盲操的可能性：
    此應用藉由「階層式尺寸策略（最常調節的溫度放核心大半圓、重要空調居中、快捷鍵居外）」與「觸覺引導」，實現了「零視覺脫離」的盲操可能。
