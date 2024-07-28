# Gemini Ai Chat para Gnome (4+)

Esta extensão usa o modelo Gemini 1.0 para bater papo.

## Usando a chave de API Gemini

1. Vá para [Google Ai](https://ai.google.dev/) e clique em Obter chave de API no Google AI Studio`
2. Na [página da chave API](https://aistudio.google.com/app/apikey) você pode criar uma nova chave de API para gemini
   1. **Nota:** se você está planejando usar a API vertex, escolha `criar novo projeto`
3. Copie a chave da API para as configurações da extensão
4. E pronto!

## Using API da Vertex API

**Observe que:** API Vertex é um SaaS (serviço pago) do Google, então você pagará suas próprias consultas e deverá saber o seguinte:

* Conhecimento básico sobre o Google Developer Console
* Conhecimento básico sobre instalação de pacotes via terminal
* Conhecimento básico sobre faturamento do Google

### Instalando

1. create billing information
2. knowledge to gcloud-cli. ref: [Install the gcloud CLI](https://cloud.google.com/sdk/docs/install)
3. Shortcut for Auth: If you test the vertex api from you account it will generate Auth credential. ref:
   * https://console.developers.google.com/apis/api/aiplatform.googleapis.com/overview?project=`PROJECT_ID`
   * if you create new project on Google Ai site you can learn your `PROJECT_ID` from [Google Dev Console](https://console.cloud.google.com/cloud-resource-manager)
4. After the installization of `gcloud-cli` you need to login via: `gcloud auth login`
5. Once you login via cli you need to follow theese steps (1-3) on your local: [Vertex AI Gemini API Beginner Guide](https://cloud.google.com/vertex-ai/generative-ai/docs/start/quickstarts/quickstart-multimodal?cloudshell=true#gemini-beginner-samples-drest)
6. Finally you can create JWT key by: `gcloud auth application-default print-access-token` on terminal
   * **Note:** You need to create manually JWT, Once you set the key to `Gemini API key` on addon settings, the addon will automaticly create new JWT's when token was expired

## Additional infos

### Diffrence between Gemini API and Vertex API

Vertex has internet access and it can be search on internet but Gemini API has no internet accsess and model update date is **(06-2023)** so it can not react to recent events. Basicly Gemini is free but outdated, Vertex is paid, outated but it can search  on internet when info isn't in the model.

### Prices for Vertex API (03-2024)

`GCP > Cloud AI and Industry Solutions > Vertex AI Model Garden > Language > Gemini > Gemini Pro`

Per Unit 1K output: **0.00036$**

Per Unit 1K input: **0.00012$**

* According the google Per unit means:
  > * The SKU's pricing tier unit quantity. For example, if the tier price is \$1 per 1000000 Bytes, then this column will show 1000000.

**For reference:** When I developed this addon, I sent 248 requests (it means 248 inputs and 248 outputs) and the cost was **0.019$.**

