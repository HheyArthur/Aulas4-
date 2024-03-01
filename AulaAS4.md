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
