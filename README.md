# Implementação de Lista Sequencial Estática em C

## Descrição
Este projeto em C implementa uma lista sequencial estática utilizando um array fixo. A lista permite operações básicas como inclusão, exclusão, alteração e obtenção de elementos. É ideal para aplicações onde o tamanho máximo da lista é conhecido e fixo, garantindo uma gestão eficiente da memória.

## Funcionalidades
- **Inicialização da Lista**: Cria uma lista vazia, pronta para armazenar elementos.
- **Inclusão de Elemento**: Insere um novo elemento na lista em uma posição específica.
- **Alteração de Elemento**: Modifica o valor de um elemento existente na lista.
- **Exclusão de Elemento**: Remove um elemento da lista em uma posição específica.
- **Obtenção de Elemento**: Recupera o valor de um elemento em uma posição específica da lista.
- **Tamanho da Lista**: Retorna o número de elementos atualmente armazenados na lista.

## Como Usar
1. Compile o código utilizando um compilador C. Exemplo:
   ```bash
   gcc -o lista_array lista_array.c
   ```
2. Execute o programa, utilizando as funções para manipular a lista conforme necessário:
   - Inicialize a lista com `inicializa_lista(&la)`.
   - Inclua elementos com `incluir_elemento(&la, posicao, elemento)`.
   - Exclua elementos com `excluir_elemento(&la, posicao)`.
   - Altere elementos com `alterar_elemento(&la, posicao, elemento)`.
   - Obtenha elementos com `obter_elemento(la, posicao, &elemento)`.

## Estrutura de Dados
O projeto utiliza a seguinte estrutura de dados:

- **lista_array**: Representa a lista sequencial, contendo um array de elementos (`lista`) e o tamanho atual da lista (`tamanho`).

### Funções Principais
- **inicializa_lista(lista_array *la)**: Inicializa a lista como vazia.
- **tamanho(lista_array la)**: Retorna o tamanho atual da lista.
- **obter_elemento(lista_array la, int i, elemento *e)**: Obtém o elemento na posição `i` da lista.
- **incluir_elemento(lista_array *la, int i, elemento e)**: Insere um elemento na posição `i` da lista.
- **alterar_elemento(lista_array *la, int i, elemento e)**: Altera o elemento na posição `i` da lista.
- **excluir_elemento(lista_array *la, int i)**: Remove o elemento na posição `i` da lista.

## Exemplo de Uso
```c
lista_array la;
inicializa_lista(&la);

elemento e1 = 10;
incluir_elemento(&la, 1, e1);

elemento e;
obter_elemento(la, 1, &e);
printf("Elemento na posição 1: %d\n", e);  // Saída: 10

elemento e2 = 20;
alterar_elemento(&la, 1, e2);
obter_elemento(la, 1, &e);
printf("Elemento na posição 1 após alteração: %d\n", e);  // Saída: 20

excluir_elemento(&la, 1);
printf("Tamanho da lista após exclusão: %d\n", tamanho(la));  // Saída: 0
```

## Contribuições
Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests.

## Licença
Este projeto está licenciado sob a [MIT License](LICENSE).
