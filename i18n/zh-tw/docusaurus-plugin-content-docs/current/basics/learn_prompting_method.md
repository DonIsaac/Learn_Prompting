---
sidebar_position: 1000
---

# 🟢 學習提示的方法

:::takeaways
- 了解學習 Gen AI 與提示工程
- 將其應用到案例研究中
:::

使用生成式人工智慧解決問題的學習提示方法是生成式人工智慧領域解決問題的框架。它可以幫助您確定 Gen AI 是否是正確的解決方案、如何應用提示工程、選擇哪些工具等等。
我們將逐步完成這五個步驟，然後提供使用此方法的案例研究。

## 五個步驟

### 1. 說出你的問題

學習提示工程的第一步是陳述你的問題。這涉及清楚地闡明您面臨的問題，而不是跳到潛在的解決方案。


### 2. 檢查相關資訊

陳述問題後，下一步就是檢查相關資訊。這可能包括研究類似的問題及其解決方案、研究問題的背景或分析與問題相關的數據。它還包括尋找相關提示和 [Gen AI 工具](https://learnprompting.org/docs/category/-tooling)。此步驟對於理解問題的細微差別並確定解決問題的潛在方法至關重要。此時，您應該知道 Gen AI 是否適合您的問題。


### 3. 提出解決方案

檢查相關資訊後，您應該更清楚地了解如何解決您的問題。現在是時候提出解決方案了。這可以是提示、新工具或使用目前工具的新方法。解決方案應該直接連結到您所陳述的問題和您所檢查的資訊。

### 4. 調整解決方案

一旦您選擇了解決方案（可以是提示或工具），下一步就是根據回饋和測試進行調整。這可能涉及設定測試以查看用戶如何與提示互動、獲取用戶回饋或根據您自己的直覺和專業知識進行調整。這就是提示工程發揮作用的地方！

### 5. 啟動解決方案

學習提示方法的最後一步是啟動您的解決方案。這可能涉及將其整合到您的產品中，將其發佈到平台上，或只是開始在與用戶的互動中使用它。

學習提示法是一個循環，而不是線性過程。啟動解決方案後，您應該繼續監控其效能並根據需要進行調整。您可以使用縮寫 SEPAL 來記住這些步驟！

## 案例研究：使用學習提示方法創建帽子資訊機器人

讓我們來看一個案例研究，了解如何使用學習提示方法從頭開始建立聊天機器人。在本例中，我們收集了有關帽子的使用者問題。

1. **說出你的問題:** 我們有大量用戶詢問不同類型的帽子、它們的歷史以及如何佩戴它們。我們需要對此採取一些措施，因為我們正在失去潛在的業務機會。

2. **檢查相關資訊:** 我們分析收集到的用戶查詢。我們注意到，最常見的問題是關於特定類型帽子的歷史、如何正確佩戴它們以及如何保養牠們。我們還研究了現有的聊天機器人，檢查它們的上下文長度、定價和速度，以及可能幫助我們解決問題的 Gen AI 工具。

3. **提出解決方案:** 根據我們的分析，我們決定使用 ChatGPT 來創建一個可以回答這三類問題的聊天機器人。我們起草一個初步提示：

    <AIInput>
    您是一位知識淵博的帽子歷史學家，研究過各種帽子的歷史、風格和正確佩戴方法。用戶向您詢問有關帽子的問題。以有用且資訊豐富的方式回覆他們的查詢：USER_INPUT
    </AIInput>

4. **調整解決方案:** 我們與一小群用戶測試我們的初始提示並收集他們的回饋。根據他們的回饋，我們意識到我們的提示需要更具吸引力且不那麼正式。

    我們相應地調整提示:

    <AIInput>
    您是一位帽子愛好者，對各種帽子的歷史、風格和佩戴禮儀有豐富的了解。用戶對帽子感到好奇並問您一個問題。以友好且信息豐富的方式回答他們的詢問。
    </AIInput>

    我們進行了更多的用戶測試，並意識到我們需要細分市場：對帽子歷史感興趣的人更喜歡更正式的方法，而對風格和戴帽子感興趣的人則更喜歡更非正式的機器人。我們開發了一個初始路由提示，根據他們的問題來決定他們屬於哪種類型的使用者：

    <AIInput>
    "你是一個人工智慧，了解與帽子相關的查詢的細微差別。根據用戶的問題，確定他們是否對帽子的正式歷史更感興趣，還是對帽子的非正式風格和佩戴更感興趣。正式嚴謹地回答歷史類的問題，並且用輕鬆生活化的口吻來回答風格和穿著相關的相關查詢。"
    </AIInput>

    我們使用 Langchain、Voiceflow 或 Dust 之類的[工具](https://learnprompting.org/docs/category/-tooling) 來實現解決方案。

5. **啟動解決方案:** 我們在我們的網站上啟動聊天機器人。我們將繼續監控用戶與機器人的交互，並根據需要進行進一步調整。

透過遵循學習提示方法，我們能夠創建一個聊天機器人，可以有效地回答使用者有關帽子的查詢。這個過程凸顯了了解使用者需求、測試和調整解決方案以及根據使用者回饋不斷改進的重要性。