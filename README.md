### 📊 Análise Epidemiológica — Município de Araranguá/SC

Este projeto consiste num framework prático de engenharia de dados desenvolvido em Python para recolha, limpeza, tradução e análise visual dos microdados do Sistema de Informações sobre Mortalidade (SIM), disponibilizados pela API de Dados Abertos do Ministério da Saúde. O principal objetivo é reduzir a complexidade das bases de dados epidemiológicas brutas do DATASUS. O fluxo converte os registos técnicos originais em informações acessíveis e de fácil compreensão para gestores públicos e cidadãos, mitigando a exclusão cognitiva sem comprometer a integridade dos dados.  

## 🔍 Fontes e Tecnologias

- Base de dados: Dados abertos de mortalidade do SIM/DATASUS filtrados dinamicamente para o recorte geográfico de Araranguá/SC através do código IBGE 420140.
- Tecnologias utilizadas: Desenvolvido no ecossistema cloud do Google Colab , utilizando Python 3 com as bibliotecas requests para o consumo automatizado da API , pandas e numpy para o tratamento de dados , e matplotlib combinado com seaborn para a geração de gráficos estatísticos.  

## 📂 Pipeline e Arquivos Gerados

- *sim_ararangua_historico.csv:*  Cópia de segurança com os 285 registos brutos extraídos diretamente da API governamental.
- *sim_ararangua_limpo_traduzido.csv (ou dados_mortalidade_ararangua_tratado.csv):* Base final higienizada, livre de colunas redundantes ou vazias e com todas as variáveis sociodemográficas traduzidas. Os códigos da CID-10 e as codificações de idade são convertidos de forma automática em descrições por extenso de linguagem cidadã.
- *maiores_causas_morte_ararangua.png:* Gráfico de barras horizontais ordenadas exportado em alta resolução (300 DPI). A visualização mapeia o perfil epidemiológico local, evidenciando as doenças do sistema circulatório (80 óbitos) e as neoplasias (59 óbitos) como as principais causas de mortalidade no município.  

## 🚀 Como Executar
- Instale todas as dependências necessárias através do terminal utilizando o comando:pip install pandas numpy requests matplotlib seaborn
- Abra o caderno estruturado Framework.ipynb no ambiente do Google Colab.
- Certifique-se de configurar a sua credencial oculta API_KEY utilizando o módulo nativo de segurança google.colab.userdata.
- Execute as células sequencialmente para processar os dados em tempo real. O notebook está programado para disparar automaticamente o download dos ficheiros finais e da imagem para o seu dispositivo local assim que o processamento terminar.  
