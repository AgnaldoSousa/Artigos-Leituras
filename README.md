# Artigos-Leituras

# Metodos em C#

O que são Métodos?



Um método em C# é como uma receita em um livro de culinária. Ele é um conjunto de instruções que realizam uma tarefa específica quando são chamadas. Em outras palavras, é um bloco de código que faz algo útil.



- Como Definir um Método?



Para definir um método em C#, você precisa seguir algumas regras simples:



Escolha um nome para o método.
Decida se o método será público (pode ser acessado de fora da classe) ou privado (só pode ser acessado de dentro da classe).
Especifique o que o método retorna (se ele retorna algum valor ou não).
Liste os parâmetros que o método precisa (se houver).


Como Chamar um Método?



Depois de definir um método, você pode chamá-lo sempre que precisar realizar a tarefa que ele executa. Existem dois tipos de métodos que você pode chamar:



Métodos de Instância: Estes métodos precisam que você crie um objeto da classe em que estão definidos e, em seguida, você pode chamá-los usando esse objeto.



Métodos Estáticos: Estes métodos pertencem à classe em si, não a objetos específicos. Você pode chamá-los diretamente usando o nome da classe.



Exemplo:



using System;

class Program
{
  // Método simples que soma dois números
  static int Soma(int num1, int num2)
  {
    return num1 + num2;
  }

  static void Main()
  {
    // Chamando o método e armazenando o resultado em uma variável
    int resultado = Soma(5, 3);
     
    // Imprimindo o resultado
    Console.WriteLine("A soma de 5 e 3 é: " + resultado);
  }
Definimos um método chamado Soma que recebe dois números como parâmetros e retorna a soma deles. Em seguida, chamamos esse método dentro do método Main e imprimimos o resultado.

﻿

https://learn.microsoft.com/en-us/dotnet/csharp/methods


# Interfaces em C#

Interfaces em C# são como contratos que definem um conjunto de funcionalidades relacionadas que uma classe ou uma estrutura (struct) podem implementar. Elas permitem que você defina um conjunto de métodos, propriedades, eventos ou indexadores que uma classe deve fornecer.



Por que usar interfaces?



Em C#, não é possível herdar de várias classes, mas é possível implementar várias interfaces. Isso é útil para compartilhar comportamentos entre diferentes tipos de classes.
Interfaces permitem simular herança para estruturas (structs), que não podem herdar de outras estruturas ou classes.


Como definir uma interface:



Você define uma interface usando a palavra-chave interface.
O nome da interface deve começar com uma letra maiúscula (por convenção, começamos com "I").
Uma interface pode conter métodos, propriedades, eventos ou indexadores.
A partir do C# 8.0, interfaces podem fornecer implementações padrão para alguns ou todos os seus membros.


Implementando uma interface:



Uma classe ou uma estrutura que implementa uma interface deve fornecer uma implementação para todos os membros declarados na interface.
Para implementar um membro de interface, a classe deve ter um membro público, não estático, com o mesmo nome e assinatura do membro de interface.


Exemplo:



interface IVeiculo

{

  void Acelerar();

  void Parar();

}



class Carro : IVeiculo

{

  public void Acelerar()

  {

    Console.WriteLine("Carro acelerando...");

  }



  public void Parar()

  {

    Console.WriteLine("Carro parando...");

  }

}



Então as Interfaces em C# são como contratos que definem um conjunto de funcionalidades, Permitem compartilhar comportamentos entre diferentes tipos de classes.
Uma classe pode implementar várias interfaces.
São úteis para simular herança em estruturas e para contornar a limitação de herança múltipla em C#.
﻿https://learn.microsoft.com/pt-br/dotnet/csharp/fundamentals/types/interfaces

# Tratamento de Exceções no C#

Exceções no C# serve para que o fluxo do código não seja interrompido por algum erro ou situação que possa vir no nosso código, que é algo comum de acontecer e para lidar com esses erros ou falhas, podemos usar exceções e manipulação de exceções em C#.



O que são Exceções?



Uma exceção em C# é uma ocorrência anormal que interrompe o fluxo normal do programa. Isso pode acontecer devido a erros de lógica, problemas de entrada de dados, falhas de hardware ou outras condições inesperadas. As exceções são representadas por objetos que derivam, em última instância, da classe System.Exception.



Como Lidar com Exceções em C#



A manipulação de exceções em C# é feita usando os blocos try, catch e finally. Aqui está uma visão geral de como esses blocos funcionam:



try: O código que pode gerar uma exceção é colocado dentro de um bloco try.

catch: Se uma exceção ocorrer dentro do bloco try, o controle é transferido para um bloco catch correspondente que lida com essa exceção.

finally: O código dentro de um bloco finally é sempre executado, independentemente de uma exceção ter sido lançada ou não. Isso é útil para realizar ações de limpeza, como fechar arquivos ou liberar recursos.



Um Exemplo:

try

{

  // Código que pode gerar uma exceção

  int resultado = 10 / 0; // Isso lançará uma exceção DividirOZeroException

}

catch (DividirOZeroException ex)

{

  // Manipulando a exceção

  Console.WriteLine("Erro: Tentativa de divisão por zero.");

}

finally

{

  // Ações de limpeza

  Console.WriteLine("Finalizando operação.");

}



Dicas para Lidar com Exceções:



Se você capturar a exceção System.Exception, é recomendável relançá-la usando a palavra-chave throw no final do bloco catch.

Utilize o bloco finally para realizar ações de limpeza e liberação de recursos, garantindo que essas ações sejam executadas independentemente de ocorrerem exceções ou não.



A manipulação de exceções em C# é uma técnica importante para lidar com situações excepcionais durante a execução de um programa. Com os blocos try, catch e finally, podemos controlar o fluxo do programa e garantir um comportamento adequado em caso de erros.

# Concatenação em C#

O que quer dizer a palavra concatenar?



Significa Ligar, unir de modo lógico e homogêneo; manter ligação ou conexão.

Ou seja na programação concatenação significa designar a operação de unir o conteúdo de duas strings.

Onde você pode combina ou junta várias cadeias de caracteres para formar uma única cadeia de caracteres maior.



Por que Concatenar Cadeias de Caracteres?



Às vezes, precisamos combinar informações ou mensagens diferentes em um único texto.



Por exemplo, se quisermos criar uma saudação personalizada como "Olá, [Nome]!", onde [Nome] é o nome de alguém que inserimos no programa, precisamos concatenar a palavra "Olá," com o nome que recebemos.



Como Concatenar Cadeias de Caracteres em C#?



Em C#, você pode usar o operador + para concatenar cadeias de caracteres. Por exemplo:



string saudacao = "Olá, ";

string nome = "João";

string mensagem = saudacao + nome + "!";

Console.WriteLine(mensagem); // Isso imprimirá "Olá, João!"



Você também pode usar o operador += para adicionar uma cadeia de caracteres a outra:



string saudacao = "Olá, ";

string nome = "Maria";

saudacao += nome + "!";

Console.WriteLine(saudacao); // Isso imprimirá "Olá, Maria!"





Certifique-se de adicionar espaços ou outros caracteres de separação conforme necessário entre as cadeias de caracteres para evitar que elas sejam unidas sem espaço.

Lembre-se de que a ordem em que você concatena as cadeias de caracteres afeta o resultado final.



A concatenação de cadeias de caracteres é uma habilidade fundamental em programação que permite criar textos personalizados e combinar informações de várias fontes em uma única mensagem. Com o operador + e += em C#, é fácil juntar cadeias de caracteres para formar mensagens significativas em seus programas.



https://learn.microsoft.com/pt-br/dotnet/csharp/how-to/concatenate-multiple-strings

# Como Resolver o Erro MSB1011 no .NET

" Erro = MSBUILD : error MSB1011: Especifique o arquivo de solução ou de projeto a usar porque esta pasta contém mais de um arquivo de solução ou de projeto."



Esse erro ocorre quando o MSBuild, a ferramenta de compilação da Microsoft, não consegue determinar qual arquivo de solução ou projeto deve ser usado, pois existem múltiplos arquivos no diretório onde o comando está sendo executado!



Verifique os Arquivos no Diretório


Primeiro, verifique os arquivos presentes no diretório onde você está executando o comando MSBuild. Certifique-se de que não há arquivos de projeto ou solução desnecessários no diretório.



Especifique o Arquivo de Projeto


Ao executar o comando MSBuild, especifique o arquivo de projeto que deseja usar. Isso pode ser feito usando a opção --project ou -p, seguida do caminho para o arquivo de projeto. Por exemplo:



dotnet build --project MeuProjeto.csproj

Substitua MeuProjeto.csproj pelo nome do seu arquivo de projeto real.



"Tive esse erro é no meu caso Descobri que meu arquivo sln ele estava gerando automaticamente um nome de arquivo diferente do meu arquivo csproj. Alterar o nome do arquivo sln para o mesmo do csproj resolveu esse erro MSB1011 e consegui executar o dotnet watch run perfeitamente."

# Solucionando um Erro de Conexão ao Banco de Dados .NET e SQL Server

Olá pessoal um erro comum que pode acontecer ao tentar criar tabelas de banco de dados usando o comando " dotnet ef database update ".



A connection was successfully established with the server, but then an error occurred during the login process. (provider: SSL Provider, error: 0 - A cadeia de certificação foi emitida por uma autoridade que não é de confiança.)



Este erro geralmente é causado pelo fato de que o servidor SQL está usando um certificado SSL auto assinado ou de uma autoridade não reconhecida pela sua máquina. 



Felizmente, há uma solução simples para contornar esse problema:

Ao configurar a string de conexão com o SQL Server, você pode adicionar o parâmetro TrustServerCertificate=True. Aqui está um exemplo de como sua string de conexão pode parecer:



Server=localhost\\sqlexpress; Initial Catalog=Agenda; Integrated Security=True; TrustServerCertificate=True



A adição de TrustServerCertificate=True permite que a sua aplicação confie no certificado SSL do servidor, mesmo que ele seja auto assinado ou provenha de uma autoridade não reconhecida.



É importante notar que esta solução é adequada para ambientes de desenvolvimento e testes. Em um ambiente de produção, é altamente recomendável obter e configurar um certificado SSL adequado de uma autoridade certificadora confiável.

Espero que esta solução simplificada ajude você a superar esse obstáculo ao trabalhar com .NET e SQL Server.



Tive esse mesmo erro no começo e achei a solução nesse artigo pela DIO.

Créditos: https://www.dio.me/articles/erro-ao-criar-a-conexao-do-banco-de-dados-no-mvc

# Regras e Convenções de Nomenclatura em C#

Quando estamos escrevendo um código em C#, é importante seguir algumas regras e convenções para nomear nossos identificadores de forma consistente e compreensível. Identificadores são os nomes que atribuímos a tipos, membros, variáveis e namespaces em nosso código.



Regras de Nomenclatura:

Comece com letra ou sublinhado (_): Todos os identificadores devem começar com uma letra do alfabeto ou um sublinhado.
Caracteres Permitidos: Os identificadores podem conter letras Unicode, dígitos decimais, caracteres de conexão, caracteres de combinação e caracteres de formatação Unicode.
Palavras-chave: Identificadores podem ser declarados usando o prefixo '@', seguido pelo nome, para corresponder a palavras-chave reservadas do C#.


Convenções de Nomenclatura:

PascalCase: Usado para nomes de tipo (classes, interfaces, structs, delegados), namespaces e membros públicos. Por exemplo: " Minha Classe ", " Meu Método ".
CamelCase: Usado para campos privados, variáveis locais e parâmetros de métodos. Por exemplo: " Minha Variável ", " Meu Parametro ".
Prefixos e Sufixos Específicos: Alguns identificadores têm prefixos ou sufixos específicos para indicar seu tipo ou finalidade. Por exemplo: interfaces começam com " i " , tipos de atributo terminam com Attribute.
Evitar Abreviações: Evite usar abreviações ou acrônimos em nomes, a menos que sejam amplamente conhecidos e aceitos.
Clareza sobre Brevidade: Prefira nomes significativos e descritivos em vez de nomes curtos.
Nomes de Assemblies e Namespaces: Devem ser significativos e seguir a notação de nome de domínio inverso.


Exemplo:
// Exemplo usando PascalCase
public class MinhaClasse {
    public int MinhaPropriedade { get; set; }


    public void MeuMetodo() {
        // Implementação
    }
}


// Exemplo usando CamelCase
public class OutraClasse {
    private int minhaVariavel;


    public void MeuMetodo(int meuParametro) {
        // Implementação
    }
}


Seguindo essas regras e convenções, nosso código se torna mais legível e fácil de entender, tanto para nós mesmos quanto para outros desenvolvedores que possam trabalhar nele.



Saiba mais em:

https://learn.microsoft.com/pt-br/dotnet/csharp/fundamentals/coding-style/identifier-names

# Como definir constantes em C#

As constantes são campos cujos valores são definidos em tempo de compilação e nunca podem ser alterados. Use constantes para fornecer nomes significativos em vez de literais numéricos ("números mágicos") a valores especiais.



Observação



No C#, a diretiva de pré-processador #define não pode ser utilizada para definir constantes da mesma maneira que é normalmente usada no C e no C++.

Para definir valores de constantes de tipos integrais (int, byte e assim por diante), use um tipo enumerado, (seria útil usar as boas práticas de nomenclatura para constantes, como usar letras maiúsculas e palavras separadas por underline)(ex: MAX_SIZE).



Para definir constantes não integrais, uma abordagem é agrupá-las em uma única classe estática de nome Constants. Isso exigirá que todas as referências às constantes sejam precedidas com o nome de classe, conforme mostrado no exemplo a seguir.



Exemplo


static class Constantes
{
    public const double Pi = 3.14159;
    public const int VelocidadeDaLuz = 300000; // km por segundo
}


class Programa
{
    static void Principal()
    {
        double raio = 5.3;
        double area = Constantes.Pi * (raio * raio);
        int segundosDoSol = 149476000 / Constantes.VelocidadeDaLuz; // em km
        Console.WriteLine(segundosDoSol);
    }
}



O uso do qualificador de nome de classe ajuda a garantir que você e outras pessoas que usam a constante entendam que ele é (constante) e não pode ser modificado.
