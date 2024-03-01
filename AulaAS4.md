Aula As Design Patterns

O que é Design Patterns ou Padroes de projetos?
São tecnica de resolução de problemas feito de um modo padronizado. construção do software, resumindo codar da forma "correta".


GOF- Gang Of Four livro de Design Pattens 

MVC- Modelo que seria as classes cliente e clienteDAO, Visao seria o html o static e o Controler seria a interligação entre tudo.

padrao arquitetural - é modelo definido como o projeto vai ser feito antes, como se fosse uma planta de um edificio, onde iremos ver a melhor solução e melhor caminho para o software e é diferente de design patter

Nomes de alguns padroes de projeto

Padrao de criação de Objeto: Singleton (unico) - Garante que em uma determinada classe haja  1 instancia apenas.
exemplo de uma conta por pessoa fisica em um banco a onde precisa de 1 instancia, exemplo de 1 cenario de jogo


Implementação dele

Construtor Padrão
Variavel de classe (global)
Metodo de classe (acesso a instancia)

Metodo sem static é um metodo de objeto, com o static e o metodo da classe

Lazy Singleton para atrasar a instancia e so instancia quando chama o get

´´´
public class Singleton { //Lazy Singleton
    private static Singleton singlexarope;

   
    
    private Singleton() {
    }

   
    
    public static Singleton getSinglexarope() {
        if(singlexarope == null) {
            singlexarope = new Singleton();
    }
        return singlexarope;
        }
    


Com Thread

´´´
public class SingletonCli extends Thread {

    @Override
    public void run() {

        Singleton s = Singleton.getSinglexarope();

        System.out.println(s);
    }

    public static void main(String[] args) {

        SingletonCli t1 = new SingletonCli();
        SingletonCli t2 = new SingletonCli();
        SingletonCli t3 = new SingletonCli();
        SingletonCli t4 = new SingletonCli();
        
        t1.start();
        t2.start();
        t3.start();
        t4.start();

    }

}


recomendação de site /*
Refactoring Guru para Design Patterns

 *\

#Exercícios

Defina padrões de projeto.

R- São tecnica para resoluções de problemas feito de um modo padronizado, também para a construção do software, resumindo codar da forma "correta".
Explique de forma objetiva e adequada a relação entre padrões arquiteturais e design patterns. Dê um exemplo teórico.
Padroes de arquitetura sao feito antes do projeto como a planta de alguma casa, predio e etc, ja o design patterns e um modelo para otimizar a forma correta de realizar o codigo.
Leia o trecho de uma possível conversa entre dois programadores que desenvolvem um projeto. Considere que o processo utilizado é o método ágil, portanto, as equipes trabalham em pares para incrementar a comunicação. Dado este contexto, identifique os designs patterns contidos no trecho de conversa. Para auxiliá-lo, use o catálogo GoF.
Programador 1:
“Nesta sprint vou refatorar aquele trecho utilizando um método fábrica. O que você acha?”
Programador 2:
“Boa ideia! Falando nisso...
 Podemos utilizar a composição para implementar aquela estrutura hierárquica, aproveitando a sua natureza recursiva!”
 Também será necessário uma fachada para esta unidade do software porque a interação na classe cliente está ficando muito complexa.

Quais são as características que o padrão singleton deve ter?
Ser unico e garantir que vai instanciar apenas 1 classe

Para o código a seguir:
public class Cenario {
  private static Cenario cenario=null;
  
  private Cenario(){}

  public static Cenario getCenario(){
      if(cenario==null)
        cenario=new Cenario();
      
      return cenario;
  }  
}

Escreva um método configuracoes que deve exibir uma mensagem. Esse método deve ser invocado pela instância dentro da classe Cenario. 
Utilizando o padrão Lazy Singleton, escreva uma classe que controle a quantidade de instâncias. Considere ter, no máximo, três instâncias.






