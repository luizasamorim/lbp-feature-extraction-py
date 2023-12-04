# Uso do LBP para a classificação de raios-X (covid e normal)

Este projeto utiliza o descritor de textura Local Binary Pattern para a classificação de imagens de raio-X divididas em duas classes: covid e normal.

## Equipe

- Luiza Schons Amorim
- Willian Gomes Zentil

## Descritor implementado

O método de extração de características Local Binary Patterns (LBP) examina cada pixel em uma imagem e o compara com seus vizinhos diretos. Ele cria um número binário (sequência de 0s e 1s) com base na comparação dos valores de intensidade dos pixels vizinhos com o valor do pixel central.

O processo básico do LBP envolve os seguintes passos para cada pixel na imagem:

1. Selecione um pixel central na imagem.
2. Compare o valor de intensidade deste pixel central com os valores de intensidade dos pixels vizinhos ao redor dele.
3. Para cada vizinho, atribua um bit '1' se o valor de intensidade do vizinho for maior ou igual ao valor do pixel central, caso contrário, atribua '0'.
4. Combine os bits resultantes em uma sequência binária para representar o padrão local ao redor do pixel central.
5. Repita esses passos para todos os pixels na imagem, gerando uma representação LBP da textura da imagem.

## Repositório do projeto

[Acesse aqui.](https://github.com/luizasamorim/lbp-feature-extraction-py)

## Classificadores e acurácia

- MLP: 94.64%
- RF: 96.43%
- SVM: 89.29%

## Instruções de uso

### Dataset

As imagens podem ser obtidas [aqui](https://www.kaggle.com/datasets/tarandeep97/covid19-normal-posteroanteriorpa-xrays).

Orienta-se que sejam inseridas na pasta "images_full", separadas em duas pastas: "covid" e "normal".

### Bibliotecas utilizadas

- progress
- split folders
- numpy
- matplotlib
- open cv
- scikit learn
- scikit image

### Execução do projeto

Após extrair/baixar as imagens na pasta "images_full", executa-se, no VScode, o arquivo "main.py"

Os resutados serão salvos na pasta "results".