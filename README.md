/ Classe base Veiculo
class Veiculo {
    protected String marca, modelo;
    protected int ano;

    public Veiculo(String marca, String modelo, int ano) {
        this.marca = marca;
        this.modelo = modelo;
        this.ano = ano;
    }

    public String exibirInfo() {
        return marca + " " + modelo + " (" + ano + ")";
    }
}

// Carro{
class Carro extends Veiculo {
    public Carro(String marca, String modelo, int ano) {
        super(marca, modelo, ano);
    }
}



// Moto
class Moto extends Veiculo {
    public Moto(String marca, String modelo, int ano) {
        super(marca, modelo, ano);
    }
}
}



public class Main {
    public static void main(String[] args) {
        Veiculo carro = new Carro("Toyota", "Corolla", 2022);
        Veiculo moto = new Moto("Honda", "CB 500", 2021);

        

        System.out.println(carro.exibirInfo());
        System.out.println(moto.exibirInfo());
    }
}
