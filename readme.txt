=========================IKDD-HW10 第八組=========================
原始資料來源:http://data.gov.tw/
資料內容:臺灣102年各縣市年底人口統計資料
使用的套件:
1. d3.js
2. d3-tip.js
3. d3.js的topojson套件
頁面右上方設有多個按鈕, 可作各類visualization頁面的切換

實做三個data visualization
1. Bar chart
2. Donut chart
3. Map

Transition應用有:
1. sorted bar chart
2. animated donut chart

Bar chart:
以長條圖呈現資料, 在進入網頁3秒後會自動以人口為根據, 將資料由大到小作排序.
右上角的"sort values"也會自動打勾, 若點選之會變成以ascending方式排序的圖表(可重複操作) 
游標移到bar上會變色, 並顯示單筆的人口資料.

Donut chart:
以圓環圖呈現資料, 以順時針方向.動態的方式載入並在尾端做彈跳(詳細可見頁面)
由於有些縣市所占人口比例過小, 會造成後段部分縣市的名稱在圖表上不甚完整與重疊.
為彌補之, 游標移到各arc上時會顯示縣市名稱&單筆的人口資料&其所占百分比例.

Map:
使用g0v提供的twgeojson(https://github.com/g0v/twgeojson), 轉換成topo.json格式後繪出台灣地圖.(但缺少連江縣的位置)
在此基礎上附上人口資料,越深色的區域代表人口數越多.
同樣, 移到該區域會變色, 並顯示縣市名稱與人口數.

[進階實作部分]
1. Different levels to view the data:
	-Elementary: 游標移到區域上顯示單筆資料
        -Intermediate: 以台灣地圖.bar chart等方式可看出
	-Overall: 從Donut chart,地圖能明顯看出整體的資料分布.
2. Different aspects to show the meaning of the data:
	-以地圖的方式, 讓資料多了地理的概念, 以更直觀的方法呈現.