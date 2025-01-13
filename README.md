# Televisor
public class Televisor {
    // Propiedades públicas
    public String marca;
    public String modelo;
    public int tamañoPulgadas;
    public boolean esSmartTV;
    public float precio;

    // Campos privados
    private String resolucion;
    private String tipoPantalla;
    private int puertosHDMI;
    private boolean tieneUSB;
    private String sistemaOperativo;

    // Getters y Setters para los atributos privados
    public String getResolucion() {
        return resolucion;
    }

    public void setResolucion(String resolucion) {
        this.resolucion = resolucion;
    }

    public String getTipoPantalla() {
        return tipoPantalla;
    }

    public void setTipoPantalla(String tipoPantalla) {
        this.tipoPantalla = tipoPantalla;
    }

    public int getPuertosHDMI() {
        return puertosHDMI;
    }

    public void setPuertosHDMI(int puertosHDMI) {
        this.puertosHDMI = puertosHDMI;
    }

    public boolean isTieneUSB() {
        return tieneUSB;
    }

    public void setTieneUSB(boolean tieneUSB) {
        this.tieneUSB = tieneUSB;
    }

    public String getSistemaOperativo() {
        return sistemaOperativo;
    }

    public void setSistemaOperativo(String sistemaOperativo) {
        this.sistemaOperativo = sistemaOperativo;
    }

    // Constructor sin parámetros
    public Televisor() {
        this.marca = "";
        this.modelo = "";
        this.tamañoPulgadas = 0;
        this.esSmartTV = false;
        this.precio = 0.0f;

        this.resolucion = "";
        this.tipoPantalla = "";
        this.puertosHDMI = 0;
        this.tieneUSB = false;
        this.sistemaOperativo = "";
    }

    // Constructor con parámetros públicos
    public Televisor(String marca, String modelo, int tamañoPulgadas, boolean esSmartTV, float precio) {
        this.marca = marca;
        this.modelo = modelo;
        this.tamañoPulgadas = tamañoPulgadas;
        this.esSmartTV = esSmartTV;
        this.precio = precio;

        this.resolucion = "";
        this.tipoPantalla = "";
        this.puertosHDMI = 0;
        this.tieneUSB = false;
        this.sistemaOperativo = "";
    }

    // Constructor con todos los parámetros
    public Televisor(String marca, String modelo, int tamañoPulgadas, boolean esSmartTV, float precio,
                     String resolucion, String tipoPantalla, int puertosHDMI, boolean tieneUSB, String sistemaOperativo) {
        this.marca = marca;
        this.modelo = modelo;
        this.tamañoPulgadas = tamañoPulgadas;
        this.esSmartTV = esSmartTV;
        this.precio = precio;

        this.resolucion = resolucion;
        this.tipoPantalla = tipoPantalla;
        this.puertosHDMI = puertosHDMI;
        this.tieneUSB = tieneUSB;
        this.sistemaOperativo = sistemaOperativo;
    }

}

class Main {
    public static void main(String[] args) {
        Televisor televisor1 = new Televisor();
        televisor1.mostrarInformacion();

        Televisor televisor2 = new Televisor("Samsung", "QLED Q80A", 55, true, 999.99f);
        televisor2.mostrarInformacion();

        Televisor televisor3 = new Televisor(
            "LG", "OLED C1", 65, true, 1499.99f,
            "4K UHD", "OLED", 4, true, "webOS"
        );
        televisor3.mostrarInformacion();
    }
}
