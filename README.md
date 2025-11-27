# PROJETO DE IA UNI9 

> Turma: 41 | Curso: Ciência da computação | Período: Noturno | Ano: 2025

## Equipe e Papéis
| Integrante | RA | Papel principal | Principais entregas (commits/arquivos) |
|------------|----|------------------|----------------------------------------|
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
- **Esquema**: liste as colunas (nome, tipo, significado).
- **Cuidados éticos/privacidade**: se houver.
- **Tamanho aproximado**: n linhas × m colunas.

> **Importante**: arquivos grandes **não** devem ser versionados; explique em `data/README_DATA.md` como baixar ou gerar.

---

## 4. Estrutura do Projeto
PROJ_IA_2025_TurmaX_GrupoYY/
├─ README.md
├─ requirements.txt
├─ src/ (config.py, data_prep.py, model.py, train.py, evaluate.py, main.py)
├─ notebooks/ (exploratory e experiments)
├─ data/ (raw, processed, README_DATA.md)
├─ models/ (artefatos e metadata)
├─ reports/ (figures, tables)
├─ tests/ (teste de fumaça)
└─ docs/ (ARCHITECTURE.md, ROADMAP.md)
---

## 5. Como Reproduzir

### 5.1 Ambiente
```bash
python -m venv .venv
# Windows: .venv\Scripts\activate
# Linux/Mac: source .venv/bin/activate
pip install -r requirements.txt

## 6. Resultados

Métricas (tabela curta): cole aqui ou aponte para reports/tables/.

Gráficos (imagens): inclua 3–5 principais (matriz de confusão, ROC/PR, curva de aprendizado, resíduos etc.).

Interpretação: 2–5 linhas por gráfico explicando “o que significa”.

Exemplo de figuras:


## 7. Decisões Técnicas

Pré-processamento (nulos, outliers, normalização, features).

Arquitetura/hiperparâmetros (se DL, detalhe camadas; se IA clássica, heurística/regras).

Limitações conhecidas e possíveis melhorias.

## 8. Execução do Vídeo (YouTube — não listado)

Link: (colar aqui)

Roteiro seguido: problema → dados → IA → execução ao vivo → resultados → conclusão.

## 9. Créditos e Licença

Fontes de dados/código de terceiros com links.

Licença escolhida (ex.: MIT).

Autores (nomes e RAs).

## 10. Changelog (opcional)

v1.0 — Entrega final.

v0.9 — Ajustes de avaliação e gráficos.
