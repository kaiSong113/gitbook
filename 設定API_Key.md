# openAI API Key

</br>
</br>

## openAI:
如果需要使用openAI的模型，必須先去[openai](https://platform.openai.com/account/api-keys)取得API KEY。取得KEY後，你可以選擇其中一種方法來匯入key:

##### 1.將KEY放於.env檔案中OPENAI_API_KEY=your api key
```shell!
OPENAI_API_KEY={your api key}
```
##### 2.設定成環境變數(變數名:OPENAI_API_KEY)

##### 3.在terminal中使用export設定環境變數
```shell!
export OPENAI_API_KEY={your api key}
```
##### 4.在Python中使用os.environ['OPENAI_API_KEY']=your api key

</br>
</br>

## Azure openAI
如果你想使用Azure openAI，先去[azureAI](https://oai.azure.com/portal)取得base url 和 API key。

將***OPENAI_API_KEY=your azure key***, ***OPENAI_API_BASE=your Language API base url***, ***OPENAI_API_TYPE=azure***, ***OPENAI_API_VERSION=2023-05-15*** 寫於.env檔案並放於你要執行akasha的路徑中。
```shell!=
## .env file
AZURE_API_KEY={your azure key}
AZURE_API_BASE={your Language API base url}
AZURE_API_TYPE=azure
AZURE_API_VERSION=2023-05-15
```

:::info
請記得在[Azure openAI Studio](https://oai.azure.com/portal)部署所有你需要的模型，且部署名稱與模型名稱相同。
:::



</br>
</br>


## LLAMA-2
如果你想使用原版的meta-llama model，並須先去[meta-llama](https://ai.meta.com/resources/models-and-libraries/llama-downloads/)去取得授權，並註冊[huggingface](https://huggingface.co/login?next=%2Fsettings%2Ftokens)取得access token，取得授權後才能經由huggingface下載並使用模型。
![granted](https://hackmd.io/_uploads/H1LOb2ot6.png)

:::info
the account on Hugging Face and the email you use to request access to Meta-Llama must be the same, so that you can download models from Hugging Face once your account is approved.

You should see the Gated model You have been granted access to this model once your account is approved
:::


</br>
</br>


同樣的，取得huggingface key值後，你可以選擇其中一種方法來匯入key:
##### 1.將KEY放於.env檔案中HUGGINGFACEHUB_API_TOKEN=your api key
```shell!
HUGGINGFACEHUB_API_TOKEN={your api key}
```
##### 2.設定成環境變數(變數名:HUGGINGFACEHUB_API_TOKEN)

##### 3.在terminal中使用export設定環境變數
```shell!
export HUGGINGFACEHUB_API_TOKEN={your api key}
```
##### 4.在Python中使用os.environ['HUGGINGFACEHUB_API_TOKEN']=your api key

```python!=
#PYTHON3.8
# os.environ['HUGGINGFACEHUB_API_TOKEN']=your api key
import akasha
ak = akasha.Doc_QA()
response = ak.get_response(dir_path, prompt, model="hf:meta-llama/Llama-2-7b-chat-hf")
```