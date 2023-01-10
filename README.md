# padr-es-de-projeto

Pesquise sobre padrões de projeto e escolha um para apresentar e descrever o seu funcionamento. Além disso, explique quais as vantagens e desvantagens comparados a outros e mostre suas referências.

Um padrão de projeto é uma solução bem-sucedida para um problema comum de design que ocorre em um determinado contexto. Eles são usados para melhorar a estrutura, flexibilidade e manutenibilidade do código de um software.

Um dos padrões de projeto mais conhecidos é o padrão Singleton, que garante que uma classe tenha apenas uma instância e fornece um ponto de acesso global para ela. Ele é útil quando precisamos garantir que apenas uma instância de uma classe seja criada, como um gerenciador de recursos compartilhado ou um objeto de configuração.

O padrão Singleton é implementado criando uma classe com um método de fabricação que verifica se uma instância já foi criada. Se sim, ele retorna a instância existente; caso contrário, ele cria uma nova instância e a armazena em uma variável de classe para uso futuro.

class Singleton {
  // Variável para armazenar a instância única
  private static instance: Singleton;

  // Construtor privado para evitar instanciação direta
  private constructor() {}

  // Método de fabricação para criar ou recuperar a instância única
  public static getInstance(): Singleton {
    if (!Singleton.instance) {
      Singleton.instance = new Singleton();
    }
    return Singleton.instance;
  }
}

Algumas vantagens do padrão Singleton são:

    Ele garante que apenas uma instância de uma classe seja criada, o que pode ser útil para economizar recursos ou evitar conflitos.
    Ele fornece um ponto de acesso global único para a instância, o que facilita o gerenciamento e a comunicação com outras partes do sistema.

Algumas desvantagens do padrão Singleton são:

    Ele pode ser difícil de testar, pois a instância única pode ser difícil de substituir por uma "falsa" durante os testes.
    Ele pode criar dependências excessivas no código, já que muitas partes do sistema podem depender da instância única.

Referências:

    https://refactoring.guru/pt-br/design-patterns/singleton
    https://www.tutorialspoint.com/design_pattern/singleton_pattern.htm
    https://en.wikipedia.org/wiki/Singleton_pattern
