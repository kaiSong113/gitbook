## 使用chain_of_thought處理複雜的問題
如果你想詢問的問題較為複雜，可以將它拆解成一連串的小問題並使用chain_of_thought詢問。


### example

```python!=
import akasha
import os


os.environ["OPENAI_API_KEY"] = "your openAI key"

dir_path = "mic/"
queries2 = ["西門子自有工廠如何朝工業4.0 發展","詳細解釋「工業4.0 成熟度指數」發展路徑的六個成熟度","根據西門子自有工廠朝工業4.0發展，探討其各項工業4.0的成熟度指標"]
ak = akasha.Doc_QA()
response = ak.chain_of_thought(dir_path, queries2, search_type='svm')
print(response)
```

```shell!=
response 1:
西門子自有工廠朝工業4.0發展的方式包括以下幾個方面：

1. 數位化戰略：西門子提出數位化戰略，從工業4.0策略擬定到落地執行，為客戶提供一條龍服務。他們設計數位工廠原型
，搭配OT、IT方案，並使用西門子的MindSphere工業物聯網平台，發展數據可視化和數據分析相關應用。

2. 跨領域合作：西門子近年積極與雲服務商、系統商等跨領域合作，推動智慧製造解決方案。此外，他們也與SAP進行ERP整合，專注於物聯網領域。

3. 虛實整合：西門子在中國大陸成都生產研發基地的案例中，從研發、生產、訂單管理、供應商管理到物流作業
，實現了整條價值鏈的虛實整合。他們不斷提高配料、傳輸、檢測等流程的自動化程度。

總體而言，西門子通過數位化戰略、跨領域合作和虛實整合等方式，推動自有工廠朝工業4.0發 
展。他們致力於提升生產效率和效能，並利用先進的技術和解決方案實現智慧工廠的建設。






response 2:
「工業4.0成熟度指數」的發展路徑劃分為六個成熟度，分別是電腦化、可連結、可視化、可分析、可預測和自適應。

1. 電腦化：這是工業4.0發展的起點，指企業開始使用計算機技
術，人員不再手動操作機械。然而，機械仍未聯網，各個IT系統仍各自獨立，資料尚未串聯。例如，企業的ERP系統與生產相關的系統獨立運作，訂單與產品品檢紀錄分散於兩套系統，導致 
訂單無法回溯出現品質問題的環節。

2. 可連結：在這個成熟度階段，企業開始將各個IT系統進行連接，實現資料的串聯。這使得不同系統之間可以共享資料，提高資訊的流通效率。例 
如，企業的ERP系統與生產相關的系統進行連接，訂單與產品品檢紀錄可以實現資料的回溯。

3. 可視化：在這個成熟度階段，企業開始實現資料的可視化，將資料以圖形化或圖表化的方
式呈現，使得管理者可以直觀地了解企業的運營狀況。例如，企業可以使用數據儀表板或報表來呈現生產線的運行情況和產品的品質指標。

4. 可分析：在這個成熟度階段，企業開始進 
行資料的分析，利用數據分析工具和算法來挖掘資料中的價值和洞察。這使得企業可以更深入地了解生產過程中的問題和潛在的改進空間。例如，企業可以使用數據分析工具來分析生產線的
效率和品質問題，並提出改進措施。

5. 可預測：在這個成熟度階段，企業開始利用資料分析的結果來進行預測和預測模型的建立。這使得企業可以預測生產過程中可能出現的問題，並 
提前採取相應的措施。例如，企業可以利用預測模型來預測生產線的故障和產品的品質問題，並提前進行維護和調整。

6. 自適應：在這個成熟度階段，企業開始實現自動化和自適應能 
力，使得生產過程可以根據實時的數據和環境變化進行調整和優化。這使得企業可以更靈活地應對市場需求和生產變化。例如，企業可以實現生產線的自動調整和產品的自動優化，以適應市
場需求的變化。

這六個成熟度階段代表了企業在工業4.0發展過程中的不同階段和能力水平，企業可以根據自身的情況和目標，逐步提升成熟度，實現工業4.0的目標。






response 3:
根據西門子自有工廠朝工業4.0發展的方式，可以探討其在工業4.0成熟度指標中的幾個方面：

 

1. 數位化戰略：西門子提出數位化戰略，從工業4.0策略擬定到落地執行提供一條龍服務
。這代表企業在工業4.0成熟度指標中已經達到了可連結和可視化的階段，並開始將數據應用於生產優化和資源利用。

 

2. 整合系統：西門子在廠內進行軟體間整合，包括PLM、ERP、MOM 
、WMS和Automation五大系統的整合，使數據互聯互通。這代表企業在工業4.0成熟度指標中已經達到了可分析和可預測的階段，並能夠利用數據分析技術進行深入分析和預測。

 

3. 數據 應用：西門子利用自有的數位雙生軟體Tecnomatix，打造虛擬工廠，模擬生產狀況或監控實際生產狀況。這代表企業在工業4.0成熟度指標中已經達到了可分析和可預測的階段，並能夠利用 
數據應用提供的資訊，優化生產設備和工序。

 

總的來說，根據西門子自有工廠朝工業4.0發展的方式，可以看出他們在工業4.0成熟度指標中已經達到了可連結、可視化、可分析和可預測，優化生產設備和工序。
```





</br>
</br>
</br>
</br>


```python!=
### Arguments of Doc_QA class ###
"""
Args:
            **embeddings (str, optional)**: the embeddings used in query and vector storage. Defaults to "text-embedding-ada-002".\n
            **chunk_size (int, optional)**: chunk size of texts from documents. Defaults to 1000.\n
            **model (str, optional)**: llm model to use. Defaults to "gpt-3.5-turbo".\n
            **verbose (bool, optional)**: show log texts or not. Defaults to False.\n
            **topK (int, optional)**: search top k number of similar documents. Defaults to 2.\n
            **threshold (float, optional)**: the similarity threshold of searching. Defaults to 0.2.\n
            **language (str, optional)**: the language of documents and prompt, use to make sure docs won't exceed
                max token size of llm input.\n
            **search_type (str, optional)**: search type to find similar documents from db, default 'merge'.
                includes 'merge', 'mmr', 'svm', 'tfidf', also, you can custom your own search_type function, as long as your
                function input is (query_embeds:np.array, docs_embeds:list[np.array], k:int, relevancy_threshold:float, log:dict) 
                and output is a list [index of selected documents].\n
            **record_exp (str, optional)**: use aiido to save running params and metrics to the remote mlflow or not if record_exp not empty, and set record_exp as experiment name.  default "".\n
            **system_prompt (str, optional)**: the system prompt that you assign special instruction to llm model, so will not be used
                in searching relevant documents. Defaults to "".\n
            **max_doc_len (int, optional)**: max document size of llm input. Defaults to 1500.\n
            **temperature (float, optional)**: temperature of llm model from 0.0 to 1.0 . Defaults to 0.0.\n

"""
```