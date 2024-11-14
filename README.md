# fila de prioridade

Este desafio de código envolve a implementação de uma fila de prioridade em Java para gerenciar eventos relacionados a estudantes em uma escola. Aqui está a explicação detalhada:

## Descrição do Problema

Uma fila de prioridade é uma estrutura de dados em que cada elemento possui uma "prioridade", e elementos com maior prioridade são atendidos antes dos de menor prioridade. No desafio, dois tipos de eventos devem ser processados:

- ENTER: Um novo estudante entra na fila.
- SERVED: O estudante com maior prioridade é atendido e removido da fila.

## Critérios de Priorização

A fila de prioridade serve os estudantes com base nos seguintes critérios:

1. CGPA (Cumulative Grade Point Average): O estudante com a maior CGPA é atendido primeiro.
2. Nome: Se dois ou mais estudantes tiverem o mesmo CGPA, o desempate é feito pelo nome em ordem alfabética (sensível a maiúsculas e minúsculas).
3. ID: Se o CGPA e o nome forem iguais, o estudante com o menor ID é atendido primeiro.

## Classes Requeridas
1. Classe Student:
   - Construtor: Student(int id, String name, double cgpa)
   - Métodos:
     * int getID(): Retorna o ID do estudante.
     * String getName(): Retorna o nome do estudante.
     * double getCGPA(): Retorna o CGPA do estudante.
2. Classe Priorities:
   - Método: List<Student> getStudents(List<String> events), que processa os eventos e retorna a lista de estudantes que ainda não foram atendidos, na ordem de prioridade.
  
## Formato de Entrada
- A primeira linha contém um número inteiro 𝑁, representando o número de eventos.
- As próximas 𝑁 linhas descrevem os eventos:
  * ENTER nome CGPA id: Adiciona um estudante à fila.
  * SERVED: Remove o estudante com a maior prioridade.
 
## Formato de Saída
- Os nomes dos estudantes que ainda não foram atendidos são impressos na ordem de prioridade. Se não houver nenhum estudante, deve ser impresso EMPTY.

