## ask_whole_file
如果你想詢問單個檔案的內容，且該文件檔不長，在語言模型的窗口大小內，你可以使用ask_whole_file將整個文件的內容給語言模型做為參考。


### example

```python!=
ak = akasha.Doc_QA(
    search_type="merge",
    verbose=True,
    max_doc_len=15000,
    model="openai:gpt-4-32k",
)

response = ak.ask_whole_file(system_prompt="用列舉的方式描述"
    file_path="docs/mic/20230726_工業4_0發展重點與案例分析，以西門子、鴻海為例.pdf",
    prompt="工業4.0有什麼可以參考的標準或是架構嗎?")

```

```shell!=
工業4.0的參考標準或架構主要有以下幾種：

1. 「工業 4.0成熟度指數」：由德國國家工程院（Acatech）提出，將發展階段劃分為電腦化、可連結、可視化、可分析、可預測、自適應共六個成熟度，前項為後項發展基礎。

2. 「新加坡工業智慧指數」（Singapore Smart Industry Readiness Index, SIRI）：由新加坡政府提出，用於評估企業在工業4.0的發展程度。

3. 「工業 4.0實施步驟方法論」：這是一種實施工業4.0的具體步驟，包括盤點公司內部待改善問題，分析現況與預期目標差異，以及規劃具體要改善的業務流程路線圖。
```