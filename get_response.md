## get_response
使用者輸入一個或多個文件(.pdf, .docx, .txt)資料夾，此函數可以讓語言模型根據搜尋到的文件回答問題。藉由使用者的問題和文件庫搜尋到知識片段，可以不用將整份文件輸入給模型，就讓語言模型正確回答問題。


### example

```python!=
qa = akasha.Doc_QA(verbose=False, search_type="svm", model="openai:gpt-3.5-turbo")

qa.get_response(
        doc_path="docs/mic/",
        prompt="五軸是甚麼?",
        chunk_size=500,
        max_doc_len=1500,
        system_prompt="請用中文回答",
)
```



```shell!=
五軸工具機是一種先進的加工裝置，透過2軸控制工具旋轉方向，再透過長寬高3軸移動進行切削加工。相較於工具方向不會改變的3軸工具機，五軸工具機能夠進行更加複雜形狀的加工，並且具有更高
的加工精密度和自動化能力。
```

### 參數

##### verbose: 如果設True，會顯示每個步驟產生的文字和狀態

##### search_type: 用來搜尋文件段落的方法，可選擇: ***svm***, ***tfidf***, ***merge***, ***mmr***, ***knn***.

##### model: 使用的語言模型，如 ***openai:gpt-3.5-turbo***, ***hf:meta-llama/Llama-2-13b-chat-hf***

##### doc_path: 一個或多個包含文件檔案的資料夾路徑名稱

##### prompt: 使用者的問題

##### max_doc_len: 最長可允許的文件段落總長度

##### chunk_size: 單個文件段落的長度

##### topK: 使用topK個最相似的文件段落給語言模型作回答

##### system_prompt: 指示給語言模型的output格式需求