# PROJETO DE IA UNI9 

> Turma: 41 | Curso: Ciência da computação | Período: Noturno | Ano: 2025

## Equipe e Papéis
| Integrante | RA | Papel principal | 
|------------|----|------------------|
| Ayrton Senna Cabani Bastos | 2225109182 | Consultoria e programação
| Giovanne Furtado Fischer | 2225106324 | Gerência e programação 
| Luan Benedito Alves | 2225202024 | Documentação e README.md
| Malcolm Agostinho Mendes | 2225107711 | Edição de video


Perfeito!
Aqui está a **versão completa com links de navegação**, no formato clássico usado em READMEs do GitHub.

Você pode colar **no início do README**, logo abaixo do título.

---

#  **Índice de Navegação**

Use os links abaixo para navegar entre as seções:

2. [Abordagem de IA](#2-abordagem-de-ia)
3. [Dados](#3-dados)
4. [Estrutura do Projeto](#4-estrutura-do-projeto)
5. [Resultados](#5-resultados)
6. [Decisões Técnicas](#6-decisões-técnicas)
7. [Execução do Vídeo](#7-execução-do-vídeo)
8. [Como Rodar o Projeto](#8-como-rodar-o-projeto)
9. [Chave de API](#9-sobre-a-chave-de-api-openrouter)

---

# Solução para pesquisa rápida de receitas

A IA oferece uma solução rápida e fácil para o usuário encontrar receitas com velocidade e praticidade. O
principal problema que ela se propõe a resolver são aquelas situações em que o usuário precisa descobrir
uma receita de forma imediata, mas não dispõe de tempo para realizar uma pesquisa mais aprofundada.
Assim, nossa IA, conectada a diversas fontes de informações externas, consegue realizar uma busca ágil e
selecionar a melhor receita que se encaixa na descrição fornecida.

Além disso, quando dizemos que nossa IA “funciona”, estamos nos referindo à sua capacidade de processar
a solicitação, interpretar corretamente os ingredientes ou preferências do usuário e, em poucos segundos,
retornar uma recomendação precisa e útil. Isso envolve entender o contexto, filtrar informações irrelevantes
e apresentar uma opção clara e prática. Em outras palavras, a IA funciona quando entrega exatamente o que
o usuário precisa, no menor tempo possível e com o máximo de eficiência.

**Métrica(s) alvo:** Taxa de Respostas Válidas e Taxa de Defeitos

---

## 2. Abordagem de IA
- **Tipo de IA/ML**: Mistral AI NeMo, um LLM pré-treinado.
- **Justificativa técnica**: O NeMo é um modelo leve e rápido porém com treinamento para responder grande parte das perguntas culinárias, principalmente com o uso da biblioteca DDGS.

---

## 3. Dados
- **Origem**: https://openrouter.ai/mistralai/mistral-nemo:free

 | Coluna                | Tipo           | Significado                                               |
| --------------------- | -------------- | --------------------------------------------------------- |
| `mensagem_usuario`    | String         | Pergunta digitada pelo usuário                            |
| `pesquisa_necessaria` | Boolean/String | Indica se foi preciso pesquisar e qual pesquisa foi feita |
| `resultado_pesquisa`  | String         | Texto retornado pelo DuckDuckGo (se houver)               |
| `resposta_modelo`     | String         | Resposta da IA                                            |
| `tempo_resposta`      | Float          | Tempo gasto para gerar a resposta                         |
| `timestamp`           | String         | Data/hora da interação                                    |


---

## 4. Estrutura do Projeto
```
PROJ_IA_2025_Turma41_
├── .gitignore
├── Codigo.ipynb
├── README.md
└── requirements.txt
```

---

# 5. Resultados

![IMG-20251126-WA0004](https://github.com/user-attachments/assets/08fbc48f-933b-4d76-95de-b691807241f1)

![IMG-20251126-WA0000](https://github.com/user-attachments/assets/6c696018-c21f-4fb2-b512-8835da115f76)

![IMG-20251126-WA0001](https://github.com/user-attachments/assets/747b6502-8e69-4603-ae72-32eb2e231ef7)

![IMG-20251126-WA0002](https://github.com/user-attachments/assets/9df84ca2-00d8-425f-a890-4c9ba961b410)

![IMG-20251126-WA0003](https://github.com/user-attachments/assets/80816f62-353b-4adc-912d-5a451071d5f5)



## 6. Decisões Técnicas

Pré-processamento
- Limpeza e Padronização básicas

Arquitetura/hiperparâmetros
- Interface (aplicativo ou API que recebe a pergunta do usuário).

- Módulo de decisão (verifica se deve usar resposta interna ou realizar busca na web).

- Chamadas ao LLM Mistral NeMo para geração da resposta.

- Pós-processamento do texto gerado (formatar, corrigir pequenos erros).

Limitações conhecidas e possíveis melhorias
- As instruções para o modelo poderiam ser mais claras, impedindo erros;
- Uma possível limpeza do histórico poderia tornar possível e prático conversas longas e mais complexas;
- Uma forma do modelo se lembrar das pesquisas poderia evitar pesquisas repetidas.

## 7. Execução do Vídeo

- Link: https://youtu.be/xsYj-2MXh6I

- Linha do tempo:
- 00:00 - Apresentação e Introdução
- 1:55 - Explicação da Função perguntar_openrouter
- 5:25 - Explicação das Funções de Pesquisa
- 6:49 - Loop Final e Encerramento

---

# 8. Como Rodar o Projeto

Siga os passos abaixo para executar o projeto localmente:

### **1. Clone o repositório**

```bash
git clone https://github.com/luanbalves-40/PROJ_IA_2025_Turma41_.git
cd PROJ_IA_2025_Turma41_
```

### **2. Crie um ambiente virtual (opcional, mas recomendado)**

```bash
python -m venv venv
```

Ative:

* **Windows**

  ```bash
  venv\Scripts\activate
  ```
* **Linux/Mac**

  ```bash
  source venv/bin/activate
  ```

### **3. Instale as dependências**

```bash
pip install -r requirements.txt
```

>  O arquivo `requirements.txt` contém muitas bibliotecas porque foi gerado automaticamente no ambiente do Google Colab. Para rodar localmente, normalmente apenas **requests**, **ddgs**, **matplotlib** e dependências básicas são necessárias.

---

### **4. Configure sua chave da OpenRouter**

O projeto utiliza a variável:

```python
OPENROUTER_API_KEY = "sua-chave-aqui"
```

Crie um arquivo `.env` (opcional) ou coloque diretamente no código.

---

### **5. Execute o notebook**

Abra o arquivo:

```
projeto_ia.ipynb
```

Pode ser executado em:

* Jupyter Notebook
* VSCode (extensão Jupyter)
* Google Colab

---

### **6. Rode a célula principal**

No final do notebook, há o loop de execução:

```python
pergunta = input("Pergunte ou digite '1' para sair: ")
resposta = perguntar_openrouter(...)
print(f'Resposta: {resposta}')
```

Basta rodar para conversar com o modelo.

---

#  9. Sobre a Chave de API (OpenRouter)

Por motivos de **segurança**, a chave da API **NÃO está incluída** no código-fonte do repositório.

Isso é fundamental para evitar:

* vazamento da chave,
* uso indevido por terceiros,
* consumo indevido de créditos.

### Como obter uma chave válida?

Você tem duas opções:

###  **1. Gerar sua própria chave**

Acesse:

[https://openrouter.ai/](https://openrouter.ai/)

Depois, crie uma conta e gere sua própria API KEY.

###  **2. Solicitar a chave usada no projeto**

Se você estiver participando oficialmente do projeto (ex.: aluno ou professor da UNI9), pode solicitar a chave ao **time de desenvolvimento**.

A chave original foi fornecida no **documento PDF oficial do projeto**.

> Recomendação:
> **Nunca compartilhe sua chave publicamente**, nem faça o commit dela dentro do repositório Git.

---

## 10. Créditos e Licença

Fontes de dados/código de terceiros com links
- Modelo de Linguagem:
- https://openrouter.ai/mistralai/mistral-nemo

Bibliotecas:
- MatPlotLib: https://matplotlib.org/
- Requests: HTTP for Humans™: https://requests.readthedocs.io/en/latest/
- DDGS: https://pypi.org/project/ddgs/

## Licença escolhida: MIT

## Autores
- Ayrton Senna Cabani Bastos; RA: 2225109182

- Giovanne Furtado Fischer; RA: 2225106324

- Luan Benedito Alves; RA: 2225202024

- Malcolm Agostinho Mendes; RA: 2225107711
