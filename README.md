# Televisor
using System;

public class Televisor
{
    // Propiedades públicas
    public string Marca 
    public string Modelo 
    public int TamañoPulgadas 
    public bool EsSmartTV 
    public float Precio 

    // Campos privados
    private string resolucion;
    private string tipoPantalla;
    private int puertosHDMI;
    private bool tieneUSB;
    private string sistemaOperativo;

    // Getters y Setters para los atributos privados
    public string Resolucion
    {
        get { return resolucion; }
        set { resolucion = value; }
    }

    public string TipoPantalla
    {
        get { return tipoPantalla; }
        set { tipoPantalla = value; }
    }

    public int PuertosHDMI
    {
        get { return puertosHDMI; }
        set { puertosHDMI = value; }
    }

    public bool TieneUSB
    {
        get { return tieneUSB; }
        set { tieneUSB = value; }
    }

    public string SistemaOperativo
    {
        get { return sistemaOperativo; }
        set { sistemaOperativo = value; }
    }

    // Constructor sin parámetros
    public Televisor()
    {
        Marca = "";
        Modelo = "";
        TamañoPulgadas = 0;
        EsSmartTV = false;
        Precio = 0.0m;

        resolucion = "";
        tipoPantalla = "";
        puertosHDMI = 0;
        tieneUSB = false;
        sistemaOperativo = "";
    }

    // Constructor con parámetros públicos
    public Televisor(string marca, string modelo, int tamañoPulgadas, bool esSmartTV, decimal precio)
    {
        Marca = marca;
        Modelo = modelo;
        TamañoPulgadas = tamañoPulgadas;
        EsSmartTV = esSmartTV;
        Precio = precio;

        resolucion = "";
        tipoPantalla = "";
        puertosHDMI = 0;
        tieneUSB = false;
        sistemaOperativo = "";
    }

    // Constructor con todos los parámetros
    public Televisor(string marca, string modelo, int tamañoPulgadas, bool esSmartTV, decimal precio,
                     string resolucion, string tipoPantalla, int puertosHDMI, bool tieneUSB, string sistemaOperativo)
    {
        Marca = marca;
        Modelo = modelo;
        TamañoPulgadas = tamañoPulgadas;
        EsSmartTV = esSmartTV;
        Precio = precio;

        resolucion = resolucion;
        tipoPantalla = tipoPantalla;
        puertosHDMI = puertosHDMI;
        tieneUSB = tieneUSB;
        sistemaOperativo = sistemaOperativo;
    }

}


class Program
{
    static void Main()
    {
   
        Televisor televisor1 = new Televisor();
        televisor1.MostrarInformacion();

        Televisor televisor2 = new Televisor("Samsung", "QLED Q80A", 55, true, 999.99m);
        televisor2.MostrarInformacion();

        Televisor televisor3 = new Televisor(
            "LG", "OLED C1", 65, true, 1499.99m,
            "4K UHD", "OLED", 4, true, "webOS"
        );
        televisor3.MostrarInformacion();
    }
}
