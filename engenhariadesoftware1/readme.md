# 📖 Livro *Software Engineering at Google* (O’Reilly)
**`Engenharia de software`**


<h2>🖥Comentário - Primeiro trecho do livro </h2>
<p> O primeiro trecho inicia diferenciando a programação, ciência da computação e engenharia de software. Enquanto universitários geralmente estudam ciência da computação e depois atuam como programadores, o termo “engenharia de software” sugere algo mais sério, remetendo à aplicação de conhecimento teórico para construir algo real e preciso, assim como em outras engenharias (civil, mecânica, aeronáutica). Porém, diferentemente dessas áreas, a engenharia de software ainda não possui práticas e teorias tão rigorosas. Tradicionalmente, a programação não exigia padrões tão estritos, mas, à medida que o software se torna cada vez mais central na vida cotidiana, cresce a necessidade de métodos mais confiáveis e sistemáticos.Uma vez que os softwares são intangíveis. Portanto <strong> O objetivo do livro é justamente indicar caminhos para práticas de software mais robustas.</strong> </p>



<h2>🖥Comentário - Segundo trecho do livro </h2>
<p> O trecho dois apresenta algumas perguntas comuns na área de engenharia de software, as quais não possuem respostas fundamentais.
Mas que podem ser estipulados possíveis caminhos para encontrar essas respostas. Além disso, o livro considera a engenharia de software uma 
programação integrada ao longo do tempo e questiona como um código pode se tornar sustentável ao longo do tempo.Ele conclui apresentando três principais fundamentos para projetar, arquitetar e escrever o seu código, os quais são: 
  <ul>
  <li>Tempo e mudança
     <p>Esse princípio reconhece que todo software está sujeito a mudanças com o passar do tempo. Isso pode acontecer por diversos motivos: mudanças nos requisitos do cliente, novas tecnologias, correções de erros, ou 
  evolução do mercado. Por isso, o código precisa ser projetado com flexibilidade e manutenibilidade em mente.</p>
    
  <li>Escala e crescimento 
      <p>Este fundamento trata da capacidade do software de crescer, tanto em termos de quantidade de usuários, quanto em funcionalidades e complexidade técnica.</p>

  <li>Compensações e custos  
      <p>Na engenharia de software, não existem soluções perfeitas — tudo envolve compromissos (trade-offs).Ou seja, o engenheiro de software precisa avaliar custos de curto e longo prazo ao tomar decisões técnicas.</p>

  </ul>
  </p>
 
<h2>📌Trade offs </h2>
<p> Trade-off é termo muito utilizado na economia e que exige a escolha entre duas ou mais opções, sabendo que
ao escolher uma, abrimos mão das outras.</p>
<p><b>3 exemplos</b> de Trade offs:
  <ul>
  <li>Tempo vs dinheiro
    <p>Escolher entre tempo e dinheiro depende das prioridades — se o prazo é apertado, o dinheiro pode ser o recurso a ser sacrificado; se há mais tempo disponível, pode-se reduzir os custos.</p>
    
  <li>Qualidade vs preço
    <p>Nem sempre o mais caro é o melhor, mas buscar sempre o "mais barato" pode sair caro no longo prazo. O ideal é encontrar o equilíbrio entre o custo e o valor entregue.</p>
  <li>Consumo Presente vs poupança futura
    <p>Viver o presente é importante, mas um planejamento financeiro saudável envolve equilíbrio — poupar hoje pode garantir tranquilidade amanhã, enquanto o consumo excessivo pode levar a problemas futuros.</p>
  </ul>
  </p>
 
<h2>📝Diagrama de Classes UML</h2>
<h3>📌Primeiro</h3>
<img align="right" src="../engenhariadesoftware/Aeroporto.drawio.png" alt="Diagrama" width="1000" height="600" />

<h3>📌Segundo</h3>
<img align="right" src="../engenhariadesoftware/Diagrama 2.png" alt="Diagrama" width="1000" height="600" />


<h2>Códigos em Java</h2>

<h2>✈️Aeroporto</h2>

<h3>Classe Aeroporto</h3>
<pre><code> 
import java.util.List;
import java.util.ArrayList;

class Aeroporto {

    private List<Passageiro> passageiros;

    public Aeroporto() {
        passageiros = new ArrayList<>();
    }

   
    public void addPassageiro(Passageiro passageiro) {
        passageiros.add(passageiro);
    }

    
    public List<Passageiro> buscarPassageiroNome(String nome) {
        List<Passageiro> resultado = new ArrayList<>();
        for (Passageiro p : passageiros) {
            if (p.getNome().equals(nome)) {
                resultado.add(p);
            }
        }
        return resultado;
    }

   
    public List<Passageiro> buscarPassageiroIdade(int idade) {
        List<Passageiro> resultado = new ArrayList<>();
        for (Passageiro p : passageiros) {
            if (p.getIdade() == idade) {
                resultado.add(p);
            }
        }
        return resultado;
    }
}
</code></pre>


<h3>Classe Passageiro</h3>
<pre><code> 
class Passageiro {

    private String nome;
    private int idade;

    
    public Passageiro(String nome, int idade) {
        this.nome = nome;
        this.idade = idade;
    }

   
    public String getNome() {
        return nome;
    }

  

    public int getIdade() {
        return idade;
    }
}
</code></pre>

<h2>🖥️Loja de eletrônicos</h2>

<h3>Classe Computadores</h3>
<pre><code> 
import java.util.ArrayList;
import java.util.List;

class Computadores {
    private String marca;
    private String CPU;
    private String memoria;

    public Computadores(String marca, String CPU, String memoria) {
        this.marca = marca;
        this.CPU = CPU;
        this.memoria = memoria;
    }

    public String getMarca() {
        return marca;
    }

    public String getCPU() {
        return CPU;
    }

    public String getMemoria() {
        return memoria;
    }

    @Override
    public String toString() {
        return "Computador [Marca=" + marca + ", CPU=" + CPU + ", Memória=" + memoria + "]";
    }
}

</code></pre>

<h3>Classe Celulares</h3>
<code><pre>
class Celulares {
    private String marca;
    private float tamanho;
    private String cor;

    public Celulares(String marca, float tamanho, String cor) {
        this.marca = marca;
        this.tamanho = tamanho;
        this.cor = cor;
    }

    public String getMarca() {
        return marca;
    }

    public float getTamanho() {
        return tamanho;
    }

    public String getCor() {
        return cor;
    }

    @Override
    public String toString() {
        return "Celular [Marca=" + marca + ", Tamanho=" + tamanho + "\", Cor=" + cor + "]";
    }
}
</code></pre>


<h3>Classe Loja de Eletrônicos</h3>
<code><pre>
class LojaDeEletronicos {
    private List<Computadores> computadores;
    private List<Celulares> celulares;

    public LojaDeEletronicos() {
        computadores = new ArrayList<>();
        celulares = new ArrayList<>();
    }

    // Métodos de adicionar
    public void addComputadores(Computadores c) {
        computadores.add(c);
    }

    public void addCelulares(Celulares c) {
        celulares.add(c);
    }
</code></pre>


<h3>Métodos de busca - Computadores</h3>
<code><pre>
    public List<Computadores> buscarComputadoresMarca(String marca) {
        List<Computadores> resultado = new ArrayList<>();
        for (Computadores c : computadores) {
            if (c.getMarca().equalsIgnoreCase(marca)) {
                resultado.add(c);
            }
        }
        return resultado;
    }

    public List<Computadores> buscarComputadoresCPU(String CPU) {
        List<Computadores> resultado = new ArrayList<>();
        for (Computadores c : computadores) {
            if (c.getCPU().equalsIgnoreCase(CPU)) {
                resultado.add(c);
            }
        }
        return resultado;
    }

    public List<Computadores> buscarComputadoresMemoria(String memoria) {
        List<Computadores> resultado = new ArrayList<>();
        for (Computadores c : computadores) {
            if (c.getMemoria().equalsIgnoreCase(memoria)) {
                resultado.add(c);
            }
        }
        return resultado;
    }
</code></pre>

<h3> Métodos de busca - Celulares</h3>
<code><pre>
    public List<Celulares> buscarCelularesMarca(String marca) {
        List<Celulares> resultado = new ArrayList<>();
        for (Celulares c : celulares) {
            if (c.getMarca().equalsIgnoreCase(marca)) {
                resultado.add(c);
            }
        }
        return resultado;
    }

    public List<Celulares> buscarCelularesTamanho(float tamanho) {
        List<Celulares> resultado = new ArrayList<>();
        for (Celulares c : celulares) {
            if (c.getTamanho() == tamanho) {
                resultado.add(c);
            }
        }
        return resultado;
    }

    public List<Celulares> buscarCelularesCor(String cor) {
        List<Celulares> resultado = new ArrayList<>();
        for (Celulares c : celulares) {
            if (c.getCor().equalsIgnoreCase(cor)) {
                resultado.add(c);
            }
        }
        return resultado;
    }
}
</code></pre>

<h2>🛠️Testes dos códigos em Java</h2>

<h3>✈️Aeroporto - teste</h3>
<code><pre>
import java.util.List;

public class Main {
    public static void main(String[] args) {

        Aeroporto aeroporto = new Aeroporto();

        
        aeroporto.addPassageiro(new Passageiro("Fernanda", 25));
        aeroporto.addPassageiro(new Passageiro("Carlos", 30));
        aeroporto.addPassageiro(new Passageiro("Ana", 25));
        aeroporto.addPassageiro(new Passageiro("Fernanda", 40));

      
        System.out.println("=== Passageiros com nome Fernanda ===");
        List<Passageiro> listaNome = aeroporto.buscarPassageiroNome("Fernanda");
        for (Passageiro p : listaNome) {
            System.out.println("Nome: " + p.getNome() + ", Idade: " + p.getIdade());
        }

        System.out.println("\n=== Passageiros com idade 25 ===");
        List<Passageiro> listaIdade = aeroporto.buscarPassageiroIdade(25);
        for (Passageiro p : listaIdade) {
            System.out.println("Nome: " + p.getNome() + ", Idade: " + p.getIdade());
        }
    }
}
</code></pre>

<h3>🖥️Loja de eletrônicos - teste</h3>
<code><pre>
  public class Main {
    public static void main(String[] args) {
        LojaDeEletronicos loja = new LojaDeEletronicos();

        loja.addComputadores(new Computadores("Dell", "i7", "16GB"));
        loja.addComputadores(new Computadores("HP", "i5", "8GB"));
        loja.addComputadores(new Computadores("Apple", "M1", "16GB"));

     
        loja.addCelulares(new Celulares("Samsung", 6.5f, "Preto"));
        loja.addCelulares(new Celulares("Apple", 6.1f, "Branco"));
        loja.addCelulares(new Celulares("Xiaomi", 6.7f, "Azul"));


        System.out.println("=== Computadores Dell ===");
        System.out.println(loja.buscarComputadoresMarca("Dell"));

        System.out.println("\n=== Computadores com 16GB de memória ===");
        System.out.println(loja.buscarComputadoresMemoria("16GB"));

        System.out.println("\n=== Celulares cor Azul ===");
        System.out.println(loja.buscarCelularesCor("Azul"));

        System.out.println("\n=== Celulares com tamanho 6.1 ===");
        System.out.println(loja.buscarCelularesTamanho(6.1f));
    }
}
</code></pre>
