# Detecção de Jogadores em Imagens de Futebol

## Descrição

Este projeto implementa um sistema de detecção de jogadores em imagens de partidas de futebol utilizando técnicas de Processamento Digital de Imagens.

A abordagem consiste em:

* Conversão do espaço de cores RGB para HSV
* Segmentação do campo por limiarização de cor
* Binarização dos objetos de interesse
* Operações de morfologia matemática (erosão e dilatação)
* Rotulagem de componentes conexos (Flood Fill)
* Filtragem por características geométricas
* Desenho de bounding boxes sobre os objetos detectados

---

## Estrutura do Repositório

```
.
├── notebooks/
│   └── deteccao_jogadores.ipynb
├── data/
│       └── IMG-20260209-WA0013.jpg
├── apresentacao.md
└── README.md
```

* **notebooks/**: código da solução em Jupyter Notebook
* **data/**: imagens utilizadas nos experimentos
* **apresentacao/**: link para vídeo no youtube com a apresentação da solução

---

## Como Executar

### Google Colab

Abra o notebook diretamente no Colab:

https://colab.research.google.com/drive/1zUVjrqR6fIpAiv41_-o8lnBtvBMNdTWt?usp=sharing

Após abrir, baixe uma das imagens presentes na pasta data/ deste repositório e rode as células do notebook de maneira sequencial, substituindo o caminho genérico da imagem pelo caminho da imagem baixada.

## Técnicas Utilizadas

* Operações pixel a pixel
* Binarização
* Modelo de cores HSV
* Morfologia matemática binária

  * Erosão
  * Dilatação
  * Abertura e fechamento
* Segmentação por cor
* Rotulagem de componentes conexos
* Análise geométrica de regiões

---

## Dataset

Devido às limitações de técnicas a serem utilizadas,pois é preciso ser restrito ao que foi aprendido na disciplina,foi necessário reduzir o escopo do dataset original(roboflow) para que o programa funcionasse corretamente,utilizamos os seguintes parâmetros para escolher uma imagem:

* Imagens mais focadas no centro do campo
* Imagens com jogadores não muito próximos um do outro
* Imagens com jogadores que não possuem vestimenta verde
* Imagens com jogadores estáticos(sem uma ofuscação devido à movimentação)

---

## Resultados

O sistema é capaz de:

* Remover o campo (segmentação do verde)
* Detectar jogadores e bola
* Gerar bounding boxes sobre os elementos de interesse

---

## Vídeo de Apresentação

Link do YouTube (máx. 15 min):

?

---

## Autores

Nomes: Felipe Ramos Santana e Leonardo Caricchio do Nascimento
Disciplina: Processamento de Imagens
Ano: 2026
