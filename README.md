# Estattistica-exp-cliente-codigo-em-Java

Ir para o conteúdo principal
 
Moodle - IFRS

Programação Básica com Java III - Turma 2022B
Painel Meus cursos  PBJIII2022B 1. Integrando Estruturas de Controle  1.4. Estatísticas no Cinema 2: a missão!
1.4. Estatísticas no Cinema 2: a missão!
Resolvemos o problema de calcular estatísticas do cinema considerando um número fixo de 100 expectadores. Porém agora, temos uma pequena mudança no problema original: devemos considerar uma quantidade qualquer de espectadores e não um número fixo! Nosso programa deve terminar quando uma nota F (de fim) for informada pelo usuário.

Isso é uma repetição controlada por flag, abordada no curso Programação Básica com Java II. Assim, devemos substituir a estrutura para...faça do algoritmo anterior por uma estrutura enquanto ou repita. Vamos utilizar uma estrutura repita. A figura abaixo mostra o algoritmo modificado. 



Algoritmo “Estatísticas do cinema 2”

var

idade, cont, resOtimo, resRuim, somaIdades, resPessimo : inteiro

maioridade, numPessoas: inteiro

nota: caractere

mediaIdades, percPessimo: real

início

       resOtimo ← 0

       resRuim ← 0

       somaIdades ← 0

       resPessimo ← 0

       maioridade ← -1

       numPessoas ← 0

 

repita

leia idade, nota 

se nota != ‘F’ então

numPessoas ← numPessoas + 1

se nota = ‘A’ então

             resOtimo ← resOtimo + 1

senão

             se nota = ‘D’ então

                    resRuim ← resRuim + 1

                    somaIdades ← somaIdades + idade

             senão

                    se nota = ‘E’ então

                    resPessimo ← resPessimo + 1

                           se idade > maiorIdade então

                           maiorIdade ← idade

                           fim se

                    fim se

             fim se

fim se

fim se
até que nota = ‘F’

mediaIdades ← somaIdades / resRuim

percPessimo ← resPessimo * 100 / numPessoas

 

escreva resOtimo, mediaIdades, percPessimo, maiorIdade

fim



Foi necessário incluir um teste após ler a nota e idade , pois se a nota informada for ‘F’, não deve ser processada (ela indica apenas o fim da leitura de dados). Também foi necessário incluir uma nova variável, numPessoas, que foi utilizada para contar o número de entrevistados. Precisamos dessa informação para calcular o percentual de respostas “Péssimo”. O cálculo do percentual de respostas “Péssimo” foi realizado multiplicando-se o número de respostas “Péssimo” por 100 e dividindo o resultado pelo número total de entrevistados (armazenado na variável numPessoas). O programa em Java é mostrado abaixo.



public class EstatisticasCinema2 {

public static void main(String[] args) {

int idade, somaIdades = 0, maioridade = -1;

int resOtimo = 0, resRuim = 0, resPessimo = 0, numPessoas = 0;

char nota;

double mediaIdades, percPessimo;

 

       do {

System.out.printf(“--- ESPECTADOR %03d ---”, cont);

System.out.printf(“Idade: ”);

idade = Double.parseDouble(System.console().readLine());

System.out.printf(“Nota: ”);

nota = System.console().readLine().charAt(0);

 

if(nota != ‘F’) {

       numPessoas++;

              if(nota == ‘A’)

                    resOtimo++;

else if(nota == ‘D’) {

                    resRuim++;

                           somaIdades += idade;

                      } else if(nota == ‘E’) {

                    resPessimo++;

                           if(idade > maiorIdade)

                           maiorIdade = idade;

                      }

              }

       } while(nota != ‘F’);

       mediaIdades = somaIdades / resRuim;

       percPessimo = resPessimo * 100 / numPessoas;

 

       System.out.printf(“Notas Ótimo = %d\n”, resOtimo);

       System.out.printf(“Média Idades = %.1f\n”, mediaIdades);

       System.out.printf(“Percentual notas “Péssimo” = %d\n”, percPessimo);

       System.out.printf(“Maior idade a responder “Péssimo” = %d\n”, maiorIdade);

}



}


Última atualização: domingo, 1 nov 2020, 17:22
Seguir para...
Academi
Dúvidas? 
Perguntas frequentes

Fale conosco | Suporte | Contato

Informação
Termos e Condições de Uso
Aviso de Privacidade e Proteção de Dados Pessoais
Contato
Rua Gen. Osório, 348, Bento Gonçalves/RS
Siga-nos
Copyright © 2017 - Desenvolvido por LMSACE.com. Distribuído por Moodle

Português - Brasil ‎(pt_br)‎
English ‎(en)‎
Español - Internacional ‎(es)‎
Français ‎(fr)‎
Italiano ‎(it)‎
Português - Brasil ‎(pt_br)‎
Mudar para o tema padrão
