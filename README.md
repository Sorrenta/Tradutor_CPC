📘 Logic Processor — Tradução entre Português e Lógica Proposicional (CPC)

Este repositório contém um módulo em Python que implementa dois modos principais de conversão entre linguagem natural em português e fórmulas de Lógica Proposicional Clássica (CPC).
A aplicação usa SymPy, Streamlit e o modelo Gemini (Google Generative AI) para conduzir traduções precisas e estruturadas.

✨ Funcionalidades
🔹 Modo 1 — Tradução NL → CPC

Converte uma sentença em português para uma fórmula lógica usando:

Conectivos: &, |, ~, ->, <->
Proposições atômicas: P, Q, R...
Retorno estruturado em JSON com:
formula: expressão lógica em CPC
propositions: mapeamento entre símbolos e significados textuais

🔹 Modo 2 — Tradução CPC → NL
Transforma uma fórmula lógica proposicional em uma frase natural em português.
Pode:
Usar definições fornecidas pelo usuário
Gerar automaticamente proposições coerentes
Retornar JSON contendo:
sentence: frase montada
propositions: significados das proposições

🔹 Extração de proposições de fórmulas
O módulo identifica automaticamente símbolos proposicionais em expressões lógicas, aceitando tanto ASCII quanto Unicode.

🧩 Tecnologias utilizadas
SymPy — parsing e manipulação de fórmulas lógicas
Streamlit — cacheamento eficiente das chamadas
Google Generative AI (Gemini) — geração e interpretação semântica
Regex — extração de variáveis e limpeza de respostas
JSON — interface consistente entre partes da aplicação

▶️ Exemplo de uso (resumido)
Tradução Português → Lógica:
translate_nl_to_cpc("Se chover, então levo o guarda-chuva.", api_key)

Tradução Lógica → Português:
translate_cpc_to_nl_AI("P -> Q", api_key, {"P": "está chovendo", "Q": "levo o guarda-chuva"})

⚠️ Observações
O módulo depende de chamadas à API da Google; certifique-se de ter créditos suficientes.
A entrada deve seguir estritamente os tipos esperados.
Em caso de erros da API, retorna um JSON com a chave "error".
