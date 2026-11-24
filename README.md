# desafio2_prf_maranhao_2025
**Acidentes nas Rodovias Federais do Maranhão (PRF 2025)**

## Integrante
* **Geovane de Oliveira da Costa**

---

## 1. Base de Dados Utilizada
* **Dataset:** Acidentes 2025 — Agrupados por Ocorrência (Dados Abertos da Polícia Rodoviária Federal - PRF).
* **Arquivo original:** `dados/datatran2025_original.csv` (mantido sem alterações).
* **Recorte investigado:** Ocorrências registradas no estado do **Maranhão (`UF = MA`)** entre 01/01/2025 e 31/12/2025 (**1.262 registros** e **30 colunas**).

---

## 2. Perguntas Investigadas
1. **Distribuição Espacial:** Quais rodovias federais (BRs) e municípios concentram a maior parte dos acidentes e das mortes no Maranhão em 2025?
2. **Padrão Temporal:** Em quais dias da semana, faixas horárias e meses do ano ocorre o maior volume de sinistros nas rodovias maranhenses?
3. **Causas e Tipologia:** Quais são as principais causas e tipos de acidentes no Maranhão, e quais ocorrências apresentam a maior severidade (letalidade)?
4. **Comparação de Grupos (Teste de Hipótese):** Acidentes ocorridos em **pistas simples** apresentam média de **vítimas graves ou fatais** (`mortos + feridos_graves`) estatisticamente maior do que acidentes em **pistas duplas**?

---

## 3. Principais Conclusões
* **Concentração por Rodovia e Município:** O Maranhão contabilizou **1.262 acidentes** e **281 óbitos** nas BRs em 2025. A **BR-135** lidera em número absoluto de ocorrências (**390 acidentes; 30,90%**), impulsionada por **São Luís** (**237 acidentes**), enquanto a **BR-316** (**72 mortos**) e a **BR-222** (**46 mortos**) concentram as maiores taxas de letalidade.
* **Horários e Dias Críticos:** **Domingo** (226 acidentes) e **sábado** (213) somam **34,79%** das ocorrências semanais. A faixa das **17h às 19h** concentra **22,35%** (282 sinistros) do volume diário, e **dezembro** (150 acidentes) é o mês mais crítico.
* **Descoberta de Alta Severidade:** Embora colisões transversais (238) e traseiras (213) sejam mais comuns, as **colisões frontais** (193 casos) provocaram **128 mortes — 45,55% de todos os óbitos** do estado em 2025.
* **Resultado do Teste de Hipótese (Mann-Whitney U):** Com **$p = 3,37 \times 10^{-14}$** ($p < 0,05$), rejeitamos a hipótese nula ($H_0$). Acidentes em **pista simples** possuem média de **0,689** vítimas graves ou fatais por ocorrência, mais que o dobro da média observada em **pista dupla** (**0,323**).

---

## 4. Estrutura do Repositório
```text
├── dados/datatran2025_original.csv      # base original da PRF sem alterações
    dados/datatran2025_tratada.csv       # base depois da limpeza
├── analise_acidentes_prf_ma_2025.ipynb  # notebook completo executado e comentado
└── README.md                            # resumo do projeto e conclusões
    requirements.txt                     # bibliotecas necessárias para rodar o notebook
```

**Como rodar**
**Só para ver**

#Clique em desafio2_prf_maranhao_2025.ipynb aqui no GitHub. O notebook aparece com todas as tabelas e gráficos, sem instalar nada.

#No seu computador

Você precisa do Python 3.10 ou mais novo.

    Baixe o repositório: botão Code → Download ZIP (e descompacte), ou:

    git clone https://github.com/Trilhas-Inova/exemplo_desafio2_cd.git

    Abra o terminal dentro da pasta do projeto e instale as bibliotecas:

    pip install -r requirements.txt

    Abra o Jupyter:

    python -m jupyter lab

    No navegador, clique em desafio02_exemplo_delivery.ipynb e use Run → Run All Cells.

    O notebook precisa estar na mesma pasta que a pasta dados/. Se mover o arquivo .ipynb sozinho, ele não encontra os dados.

No Google Colab (sem instalar nada)

    Clique no botão Abrir no Colab no topo desta página.
    No Colab, use Ambiente de execução → Executar tudo.

O notebook baixa os dados sozinho deste repositório, então não é preciso enviar nenhum arquivo.
