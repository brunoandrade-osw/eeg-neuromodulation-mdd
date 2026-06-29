# eeg-neuromodulation-mdd
Análise de sinais de EEG (16 canais) para investigação de assinaturas neurofisiológicas em pacientes com Transtorno Depressivo Maior (TDM) submetidos a protocolos de neuromodulação (ETCC e tsDCS).

# EEG Neuromodulation in Major Depressive Disorder (MDD)

Este repositório contém os scripts e a estrutura de análise de dados eletroencefalográficos (EEG) de um ensaio clínico controlado, cujo foco é a investigação de assinaturas neurofisiológicas e diagnósticos clínicos no Transtorno Depressivo Maior (TDM). 

O projeto avalia os impactos de intervenções de neuromodulação cerebral e medular na sintomatologia de pacientes com TDM, buscando correlacionar as alterações fisiológicas do sinal de EEG com desfechos clínicos (ex: redução de irritabilidade e melhora do humor).

## Desenho Experimental
O estudo é um ensaio clínico randomizado, duplo-cego e controlado por placebo, envolvendo 30 participantes divididos em 3 grupos:
- **G1 (ETCC):** Estimulação Transcraniana por Corrente Contínua (2.0 mA, ânodo em F3, cátodo em F4).
- **G2 (tsDCS):** Estimulação Medular Transcutânea por Corrente Contínua (2.5 mA, ânodo em T10, cátodo em C3).
- **G3 (Placebo):** Estimulação simulada.

**Protocolo de Aquisição:**
- **Equipamento:** V-amp (BrainProducts)
- **Canais:** 16 eletrodos
- **Sistema:** Internacional 10-20
- **Momentos de Coleta:** Pré-intervenção e Pós-intervenção (15 minutos de gravação, vigília, olhos abertos).

## Estrutura do Repositório
A organização dos diretórios segue as melhores práticas de ciência de dados para garantir a reprodutibilidade da pesquisa:

* `data/raw/`: Arquivos CSV originais do EEG. **(Somente leitura)**
* `data/processed/`: Sinais filtrados e limpos após remoção de artefatos.
* `docs/`: Documentação de apoio, diário de coletas e tabelas de metadados.
* `notebooks/`: Análises exploratórias, processamento de sinal interativo e geração de Topomaps.
* `src/`: Scripts Python definitivos e funções utilitárias (ex: pipeline com MNE-Python).

## Ferramentas Utilizadas
O processamento dos sinais e a extração de características utilizam a linguagem Python, com forte dependência da biblioteca `mne-python` para manipulação dos dados neurofisiológicos, além de bibliotecas científicas padrão (NumPy, SciPy, Matplotlib).
