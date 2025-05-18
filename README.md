# 🛠️ Mão na Roda - Seu Assistente Digital para Reparos Domésticos (Notebook Executável)

![Banner do Projeto - Opcional: Crie uma imagem legal para colocar aqui!]

Um notebook executável que demonstra um assistente de IA conversacional construído com Google Gemini para ajudar usuários leigos em pequenos reparos e projetos de faça-você-mesmo em casa. Este projeto foi desenvolvido como parte da Imersão Alura + Google Gemini.

## 📝 Sobre o Projeto

O "Mão na Roda" nasceu da necessidade de democratizar o conhecimento técnico em reparos domésticos. Muitas pessoas se sentem inseguras ao lidar com problemas simples em casa, resultando em frustração, gastos desnecessários ou o descarte prematuro de itens que poderiam ser consertados.

Este notebook apresenta um protótipo de assistente de IA que busca oferecer uma solução acessível e amigável, atuando como um "Faz-Tudo Digital" que guia o usuário passo a passo no diagnóstico e na resolução de problemas comuns, sempre com foco na segurança e na capacitação.

## ✨ Diferenciais e Inovação

* **Diagnóstico Conversacional:** Interage com o usuário, fazendo perguntas de acompanhamento (uma por vez!) para entender o problema em detalhe.
* **Instruções Adaptativas:** As orientações são geradas dinamicamente pelo Google Gemini, personalizadas para a situação do usuário, com linguagem simples e avisos de segurança claros.
* **Suporte Visual (Via Imagens):** Capacidade de processar (dentro do ambiente do notebook) imagens enviadas pelo usuário para auxiliar no diagnóstico.
* **Empoderamento DIY:** O foco principal é capacitar o usuário a resolver o problema por conta própria.

## 🧠 Como o Google Gemini Atua

O Google Gemini é a inteligência central por trás do "Mão na Roda". Ele é responsável por:

* Compreender a descrição do problema do usuário (NLU).
* Gerar as perguntas de follow-up para refinar o diagnóstico.
* Criar as instruções de reparo passo a passo e seguras.
* Sugerir materiais e ferramentas necessários.
* Saber quando o problema excede o escopo do DIY e recomendar um profissional.
* Manter o contexto da conversa.

## 🚀 Como Executar o Notebook

O notebook `Mao_na_Roda.ipynb` é projetado para rodar no Google Colab.

### Pré-requisitos

* Uma conta Google para acessar o Google Colab.
* Uma chave de API do Google Gemini. Você pode obtê-la gratuitamente no [Google AI Studio](https://aistudio.google.com/).

### Passos para Execução

1.  **Abrir no Google Colab:** Clique no botão "Open in Colab" abaixo ou faça o upload do arquivo `Mao_na_Roda.ipynb` para o seu Google Drive e abra-o com o Google Colab.

    [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/SEU_USUARIO/mao-na-roda/blob/main/Mao_na_Roda.ipynb)
    *(**Nota:** Você precisará ajustar o link acima após criar seu repositório no GitHub, substituindo `SEU_USUARIO` e `mao-na-roda` pelos seus dados.)*

2.  **Configurar a API Key:**
    * No Google Colab, no menu lateral esquerdo, clique no ícone de chave (Segredos).
    * Clique em "+ Novo segredo do Notebook".
    * No campo "Nome", digite `GOOGLE_API_KEY`.
    * No campo "Valor", cole a sua chave de API do Google Gemini.
    * Certifique-se de que a opção "Acessar no notebook" esteja marcada.

3.  **Executar as Células:** Execute as células do notebook sequencialmente (Shift + Enter em cada célula ou use o menu "Runtime" -> "Run all"). As células irão instalar as bibliotecas necessárias, configurar a API Key e iniciar a interação com o agente.

4.  **Interagir com o Agente:** Após executar a última célula, você poderá interagir com o "Mão na Roda" diretamente na saída do notebook. Siga as instruções e responda às perguntas do agente.

    * Para enviar uma imagem, digite `/enviarimagem` quando o agente solicitar ou se você desejar enviar uma, e depois forneça o caminho do arquivo na próxima linha.

## 🤝 Contribuições

Este notebook é um ponto de partida. Sinta-se à vontade para "Forkar" este repositório, fazer melhorias e compartilhar!

## 📄 Licença

Este projeto está licenciado sob a Licença MIT. Veja o arquivo `LICENSE` para mais detalhes.

## 📞 Contato

Seu Nome/Seu GitHub/Seu LinkedIn (Opcional)

---

**Lembre-se de:**

1.  **Criar o Repositório no GitHub:** Crie um novo repositório público chamado `mao-na-roda`.
2.  **Adicionar os Arquivos:** Faça o upload do `Mao_na_Roda.ipynb` e do `README.md` (com o conteúdo acima ajustado) para o repositório. Adicione também um arquivo `.gitignore` (pode ser gerado pelo próprio GitHub ao criar o repositório, escolhendo template para Python) e um arquivo `LICENSE`.
3.  **Ajustar o link "Open in Colab":** Edite o `README.md` no GitHub e ajuste o link do badge para apontar para o seu repositório.
4.  **Adicionar um Banner:** (Opcional) Crie uma imagem legal para o projeto e adicione-a na pasta raiz, ajustando o link no README.

Com esta estrutura simplificada e README, qualquer pessoa poderá facilmente entender seu projeto e executá-lo no Google Colab! Boa sorte!
