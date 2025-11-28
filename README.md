# PROJETO DE IA UNI9 

> Turma: 41 | Curso: Ciência da computação | Período: Noturno | Ano: 2025

## Equipe e Papéis
| Integrante | RA | Papel principal | 
|------------|----|------------------|
| Ayrton Senna Cabani Bastos | 2225109182 | Consultoria e programação
| Giovanne Furtado Fischer | 2225106324 | Gerência e programação 
| Luan Benedito Alves | 2225202024 | Documentação e README.md
| Malcolm Agostinho Mendes | 2225107711 | Edição de video

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
PROJ_IA_2025_Turma41_
├─ .gitignore
├─ Codígo.ipynb
├─ README.md
├─ requirements.txt

---

# 5. Resultados

![IMG-20251126-WA0004](https://github.com/user-attachments/assets/08fbc48f-933b-4d76-95de-b691807241f1)

![IMG-20251126-WA0000](https://github.com/user-attachments/assets/6c696018-c21f-4fb2-b512-8835da115f76)

![IMG-20251126-WA0001](https://github.com/user-attachments/assets/747b6502-8e69-4603-ae72-32eb2e231ef7)

![IMG-20251126-WA0002](https://github.com/user-attachments/assets/9df84ca2-00d8-425f-a890-4c9ba961b410)

![IMG-20251126-WA0003](https://github.com/user-attachments/assets/80816f62-353b-4adc-912d-5a451071d5f5)



## 6. Decisões Técnicas

Pré-processamento (nulos, outliers, normalização, features).

Arquitetura/hiperparâmetros (se DL, detalhe camadas; se IA clássica, heurística/regras).

Limitações conhecidas e possíveis melhorias.

## 7. Execução do Vídeo (YouTube — não listado)

Link: (colar aqui)

Roteiro seguido: problema → dados → IA → execução ao vivo → resultados → conclusão.

## 8. Créditos e Licença

Fontes de dados/código de terceiros com links.

Licença escolhida (ex.: MIT).

Autores (nomes e RAs).

