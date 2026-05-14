2-
public class Aluno {

    // Atributos
    String nome;
    String matricula;
    double nota1;
    double nota2;

    // Método para calcular média
    double calcularMedia() {
        return (nota1 + nota2) / 2;
    }

    // Método para verificar aprovação
    boolean aprovado() {
        return calcularMedia() >= 6.0;
    }

    // Método para exibir boletim
    void exibirBoletim() {

        System.out.println("Aluno: " + nome + " | Matrícula: " + matricula);
        System.out.println("Nota 1: " + nota1 + " | Nota 2: " + nota2);
        System.out.println("Média: " + calcularMedia());

        if (aprovado()) {
            System.out.println("Situação: APROVADO");
        } else {
            System.out.println("Situação: REPROVADO");
        }
    }

    // Método principal
    public static void main(String[] args) {

        Aluno aluno = new Aluno();

        aluno.nome = "Maria Clara";
        aluno.matricula = "2024001";
        aluno.nota1 = 7.5;
        aluno.nota2 = 8.0;

        aluno.exibirBoletim();
    }
}
