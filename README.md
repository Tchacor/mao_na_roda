# 🛠️ Mão na Roda - Seu Assistente Digital para Reparos Domésticos

![Image](https://github.com/user-attachments/assets/0f13b41d-9731-4658-b54f-d241a5845944)

## 📝 Sobre o Projeto

O projeto **"Mão na Roda - Seu Faz-Tudo Digital"** nasceu da necessidade clara de democratizar o conhecimento técnico em reparos domésticos básicos e projetos de "faça-você-mesmo" (DIY). Em um mundo onde a conveniência muitas vezes leva ao descarte, muitas pessoas sentem-se inseguras ou despreparadas para lidar com problemas simples em suas casas – desde uma torneira pingando a uma tomada com mau contato. Essa hesitação resulta não apenas em frustração e desconforto, mas também em gastos desnecessários com serviços profissionais para tarefas que poderiam ser resolvidas de forma autônoma, e contribui para o ciclo de consumo e descarte prematuro de itens.

Desenvolvido no contexto da Imersão Alura + Google Gemini, o "Mão na Roda" propõe uma solução inovadora e acessível. Atuando como um **assistente inteligente e conversacional de IA**, o objetivo principal é empoderar indivíduos, fornecendo o conhecimento e a confiança necessários para que possam resolver problemas comuns em suas residências por conta própria, de forma segura e eficiente.

Mais do que um simples manual digital, este projeto busca ser um "Faz-Tudo Digital" amigável que guia o usuário passo a passo. Através de uma interação natural e didática, ele ajuda a diagnosticar a situação, sugere os materiais e ferramentas necessários e fornece instruções claras, sempre priorizando a segurança. Acreditamos que, ao capacitar as pessoas com esse conhecimento, podemos promover maior autossuficiência, economia doméstica e um comportamento mais sustentável, incentivando o reparo e a reutilização em vez do descarte. Este notebook serve como um protótipo funcional dessa visão, demonstrando a capacidade da IA em tornar o DIY acessível a todos.

## ✨ Diferenciais e Inovação

* **Diagnóstico Conversacional:** Interage com o usuário, fazendo perguntas de acompanhamento (uma por vez!) para entender o problema em detalhe.
* **Instruções Adaptativas:** As orientações são geradas dinamicamente pelo Google Gemini, personalizadas para a situação do usuário, com linguagem simples e avisos de segurança claros.
* **Suporte Visual (Via Imagens):** Capacidade de processar (dentro do ambiente do notebook) imagens enviadas pelo usuário para auxiliar no diagnóstico.
* **Empoderamento DIY:** O foco principal é capacitar o usuário a resolver o problema por conta própria.

## 🧠 Como o Google Gemini Atua

O Google Gemini é a inteligência central por trás do "Mão na Roda". Ele é responsável por:

* Compreender a descrição do problema do usuário.
* Gerar as perguntas de follow-up para refinar o diagnóstico.
* Criar as instruções de reparo passo a passo e seguras.
* Sugerir materiais e ferramentas necessários.
* Saber quando o problema excede o escopo do DIY e recomendar um profissional.
* Manter o contexto da conversa.

## 💻 Contexto Técnico

O "Mão na Roda" é construído sobre a poderosa plataforma de modelos de linguagem do Google, utilizando o **Google Gemini** como sua inteligência central. A implementação atual, demonstrada no notebook, utiliza as seguintes tecnologias e abordagens:

* **Google Gemini API:** Interagimos diretamente com o modelo `gemini-2.0-flash` através da **Google AI SDK para Python (`google-genai`)**. A escolha deste modelo visa um bom equilíbrio entre capacidade e velocidade para interações conversacionais.
* **Agent Logic via Prompt Engineering:** A inteligência e o comportamento do agente "Mão na Roda" (sua capacidade de fazer perguntas de diagnóstico, fornecer instruções passo a passo, priorizar segurança, etc.) são orquestrados principalmente através de uma **instrução de sistema (system instruction)** cuidadosamente elaborada no prompt enviado ao modelo Gemini.
* **Processamento de Imagens:** Utilizamos a biblioteca **Pillow** para manipulação básica de imagens, permitindo que o usuário envie fotos que são codificadas e enviadas ao modelo Gemini como parte da requisição multimodal, enriquecendo o contexto para o diagnóstico.
* **Ambiente de Execução:** O notebook foi desenvolvido e é otimizado para execução no **Google Colab**, aproveitando recursos como a gestão segura de chaves de API (`userdata`) e a facilidade de instalação de bibliotecas (`%pip`).
* **Interação Conversacional:** A lógica no notebook gerencia o histórico da conversa (`chat_history`) para manter o contexto entre as turns do diálogo, simulando uma interação contínua com o assistente.
* **Framework ADK (Mencionado/Contexto):** Embora a lógica central no notebook utilize primariamente a SDK `google-genai` com prompt engineering, o projeto está inserido no contexto do **Agent Developer Kit (ADK) do Google**, importando módulos relevantes que indicam um alinhamento com as abordagens recomendadas para a construção de agentes baseados em LLMs.

Esta estrutura inicial no notebook demonstra a capacidade do Gemini de atuar como um assistente conversacional e multimodal para casos de uso práticos como reparos domésticos.

## ⚙️ Executando o Notebook no Colab

O código principal do assistente "Mão na Roda", que demonstra a interação com o Google Gemini, está contido no arquivo `Mao_na_Roda.ipynb`. Este notebook é projetado para ser executado no ambiente online e gratuito do Google Colab.

Siga estes passos para rodar o agente:


1.  **Abra o Notebook no Google Colab:**
      Clique no botão "Open in Colab" abaixo ou faça o upload do arquivo `Mao_na_Roda.ipynb` para o seu Google Drive e abra-o com o Google Colab.
        [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Tchacor/mao_na_roda/blob/main/Mao_na_Roda.ipynb)

3.  **Obtenha uma Chave de API do Google Gemini:**
    * Você precisará de uma chave de API válida para acessar os modelos do Gemini.
    * Vá para o [Google AI Studio](https://aistudio.google.com/) e faça login com sua conta Google.
    * No Google AI Studio, você pode gerar e gerenciar suas chaves de API gratuitamente. Crie ou selecione um projeto e gere sua chave.
    * **Mantenha sua chave de API segura e nunca a exponha publicamente!**

4.  **Configure a Chave de API no Colab (Usando Segredos):**
    * Dentro do ambiente Google Colab com o notebook aberto, localize e clique no ícone de chave (geralmente no menu lateral esquerdo). Este é o gerenciador de "Segredos" (Secrets).
    * Clique em "+ Novo segredo do Notebook".
    * No campo "Nome" (Key), digite exatamente `GOOGLE_API_KEY`.
    * No campo "Valor" (Value), cole a chave de API do Google Gemini que você obteve anteriormente.
    * Certifique-se de que a opção "Acessar neste notebook" esteja marcada. Isso permite que o código do notebook acesse o valor usando `userdata.get('GOOGLE_API_KEY')`.
    * **Não cole sua chave de API diretamente no código do notebook!** Usar o gerenciador de Segredos do Colab é a forma segura de fazer isso.

5.  **Execute as Células do Notebook:**
    * Vá para o menu "Runtime" (Ambiente de execução) na parte superior e selecione "Run all" (Executar tudo).
    * O Colab executará cada célula sequencialmente.
    * As primeiras células instalarão as bibliotecas Python necessárias (`google-genai`, `Pillow`, etc.) utilizando `%pip`.
    * A célula de configuração da API lerá a chave do gerenciador de Segredos.
    * As células seguintes configurarão o cliente Gemini e o agente.
    * A última célula iniciará o loop de interação com o assistente.

6.  **Interaja com o Agente:**
    * Após a execução da última célula, você verá a mensagem de boas-vindas do "Mão na Roda" na saída do notebook.
    * Você poderá digitar sua descrição do problema de reparo no campo de entrada e pressionar Enter para enviar.
    * Siga as perguntas do agente e forneça as informações solicitadas para ajudá-lo a diagnosticar o problema.

### 📷 **Como Enviar Imagens para o Agente no Colab**

O agente "Mão na Roda" tem a capacidade de receber e analisar imagens para auxiliar no diagnóstico de problemas. Ao executar o notebook no Google Colab, você pode enviar uma imagem seguindo estes passos:

1.  **Faça o Upload da Imagem para o Ambiente do Colab:**
    * No menu lateral esquerdo do Google Colab, clique no ícone de pasta (Explorador de arquivos).
    * Clique no ícone de upload de arquivo (um papel com uma seta para cima).
    * Selecione o arquivo de imagem no seu computador e faça o upload para o ambiente temporário do Colab.
    * **Atenção:** Os arquivos uploaded para o ambiente do Colab são temporários e serão apagados quando a sessão do Colab for encerrada.

2.  **Obtenha o Caminho do Arquivo no Colab:**
    * No Explorador de arquivos do Colab, localize a imagem que você acabou de subir.
    * Clique com o botão direito do mouse sobre o nome do arquivo da imagem.
    * Selecione a opção **"Copiar caminho do arquivo"**. Este caminho será algo como `/content/sua_imagem.jpg`.

3.  **Cole o caminho da imagem na Interação com o Agente:**
    * Na área de interação do notebook (onde você digita suas mensagens para o agente), cole o caminho que você copiou no passo anterior (ex: `/content/sua_imagem.jpg`) e pressione Enter.
    * Você pode então fornecer uma descrição opcional da imagem ou fazer sua pergunta relacionada a ela na próxima linha.

## 🤝 Contribuições

Este notebook é um ponto de partida. Sinta-se à vontade para "Forkar" este repositório, fazer melhorias e compartilhar!

## 📄 Licença

Este projeto está licenciado sob a Licença MIT. Veja o arquivo `LICENSE` para mais detalhes.

## 📞 Contato

Tcharles Sousa Coutinho

Linkedin: https://www.linkedin.com/in/tcharles-coutinho-066960201/

GitHub: https://github.com/Tchacor
