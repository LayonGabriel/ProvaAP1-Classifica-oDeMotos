# Classificador de Motocicletas por Objeto e Cor 🏍️🎨

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/SEU-USUARIO/SEU-REPOSITORIO/blob/main/classificador_motos.ipynb)

## 📄 Descrição do Projeto

Este projeto, desenvolvido em Google Colab, utiliza Visão Computacional para analisar um conjunto de imagens e realizar uma classificação em duas etapas:

1.  **Classificação Primária:** Identifica se a imagem contém uma motocicleta ("moto") ou não ("não moto").
2.  **Classificação Secundária:** Para as imagens identificadas como "moto", o sistema analisa a cor predominante do veículo e a organiza em uma subpasta correspondente.

O objetivo é automatizar a organização de um grande volume de imagens de forma inteligente e baseada em conteúdo.

---

## ✨ Funcionalidades

-   **Detecção de Objetos:** Utiliza o modelo pré-treinado **YOLOv8** para identificar motocicletas com alta precisão.
-   **Análise de Cor:** Aplica o algoritmo de clusterização **K-Means** para extrair a cor dominante da motocicleta detectada na imagem.
-   **Organização Automática:** Move e organiza os arquivos de imagem em uma estrutura de pastas lógica (`/nao_moto`, `/moto/vermelho`, `/moto/preto`, etc.).
-   **Ambiente em Nuvem:** Totalmente desenvolvido para ser executado no ambiente do Google Colab, facilitando o acesso e a execução sem a necessidade de configuração de hardware local.

---

## 🛠️ Tecnologias Utilizadas

-   **Python 3**
-   **Google Colab**
-   **Google Drive** (para armazenamento de arquivos)
-   **OpenCV:** Para manipulação de imagens (leitura, recorte, conversão de cores).
-   **Ultralytics (YOLOv8):** Para a tarefa de detecção de objetos.
-   **Scikit-learn:** Para a implementação do algoritmo K-Means.
-   **NumPy:** Para operações matemáticas e manipulação de arrays.

---

## 📁 Estrutura de Pastas Esperada

Para que o script funcione corretamente, a seguinte estrutura de pastas deve ser criada no seu Google Drive:

/MyDrive/
└── analise_de_imagens/
├── imagens_para_analisar/   <-- COLOQUE SUAS IMAGENS AQUI
│   ├── imagem1.jpg
│   └── imagem2.png
└── imagens_classificadas/   <-- PASTA GERADA PELO SCRIPT
├── nao_moto/
└── moto/

---

## 🚀 Como Usar

1.  **Clone o repositório ou baixe o notebook.**
2.  **Abra o notebook `classificador_motos.ipynb` no Google Colab.**
3.  **Prepare o ambiente:**
    - Crie a pasta `analise_de_imagens/imagens_para_analisar/` no seu Google Drive.
    - Faça o upload das imagens que deseja classificar para essa pasta.
4.  **Execute as células do notebook em ordem:**
    - **Célula 1:** Monta o Google Drive e instala as dependências.
    - **Célula 2:** Cria a estrutura de pastas de saída.
    - **Célula 3:** Executa a classificação primária (moto vs. não moto).
    - **Célula 4:** Executa a análise de cor e a organização final das motos.
    - **Célula 5:** Exibe a estrutura de pastas resultante.

---

## 📈 Exemplo de Saída

Após a execução do script, a pasta `imagens_classificadas` terá uma estrutura parecida com esta:

/imagens_classificadas/
├── nao_moto/
│   ├── carro.jpg
│   └── paisagem.png
└── moto/
├── azul/
│   └── moto_esportiva_azul.jpg
├── preto/
│   ├── harley_preta.jpg
│   └── scooter_preta.png
└── vermelho/
└── ducati_vermelha.jpg

---
##  _Autores_

- **Layon Gabriel**, **Elenildo Machado**, **Juan Carlos**, **Déric Lima**, **Marcos Venicius**.
