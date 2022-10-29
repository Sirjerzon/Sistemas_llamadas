using System;
using System.Diagnostics.Contracts;


namespace proyecto
{

    class Program
    {
        static void Main(String[] args)
        {


            int opcion;
            Console.ForegroundColor = ConsoleColor.Green;
            Console.Clear();
            Console.WriteLine("----------------------------------------------Empresa de Telefonia Telecorp---------------------------------------------");
            Console.WriteLine("");
            Console.WriteLine("Ingrese el tipo de llamada que desea realizar");
            Console.WriteLine("");
            Console.WriteLine("Marque 1 para realizar una llamada Internacional. Q7.59 por minuto los primeros 3 minutos y Q3.03 por minuto adicional");
            Console.WriteLine(" ");
            Console.WriteLine("Marque 2 para realizar una llamada Llamada Nacional. Q1.20 Por minuto los primeros 3 minutos y Q.0.48 por minuto adicional");
            Console.WriteLine(" ");
            Console.WriteLine("Marque 3 para realizar una llamada Llamada Local. SIN COSTO EXTRA LAS PRIMERAS 50 LLAMADAS luego 0.60 por cada llamada adicional");
            Console.WriteLine(" ");
            opcion = int.Parse(Console.ReadLine());
            switch (opcion)
            {
                case 1:
                    internacional();
                    break;

                case 2:
                    nacional();
                    break;

                case 3:
                    local();
                    break;

                default:
                    Console.WriteLine("Valor ingresado Invalido");
                    break;
            }



        }

        static void internacional()
        {
            int minutos;
            int minutos_reales;
            double a;
            double b;
            double c;
            string nombre;
            string titular;
            string contacto;
            string area;
            Console.Clear();
            Console.WriteLine("Llamada Internacional");
            Console.WriteLine("---------------------");
            Console.WriteLine("Ingrese Su nombre");
            nombre = Console.ReadLine();
            Console.WriteLine(" ");
            Console.WriteLine("Ingrese el su numero telefonico");
            titular = Console.ReadLine();
            Console.WriteLine(" ");
            Console.WriteLine("Ingrese el area del numero telefonico al que desea llamar");
            area = Console.ReadLine();
            Console.WriteLine(" ");
            Console.WriteLine("Ingrese el numero telefonico al que desea llamar");
            contacto = Console.ReadLine();
            Console.WriteLine(" ");
            Console.WriteLine("Ingrese la cantidad de minutos que desea hablar (Con fines de simulación)");

            minutos = int.Parse(Console.ReadLine());
            if (minutos <= 3)
            {
                a = minutos * 7.59;

                Console.Clear();
                Console.WriteLine("---------------- Empresa de Telefonia Telecorp ----------------");
                Console.WriteLine("---------------------------------------------------------------");
                Console.WriteLine("15-75 15 Avenida Ruta 2 Zona 9");
                Console.WriteLine("Guatemala, Guatemala, 01009");
                Console.WriteLine("PBX: 2335-4539");
                Console.WriteLine("---------------------------------------------------------------");
                Console.WriteLine("Factura a nombre de:");
                Console.WriteLine(" ");
                Console.WriteLine("Nombre: " + nombre);
                Console.WriteLine(" ");
                Console.WriteLine("Numero del usuario: +502 " + titular);
                Console.WriteLine(" ");
                Console.WriteLine("Numero de su contacto: " + area + " " + contacto);
                Console.WriteLine(" ");
                Console.WriteLine("El Costo total de su llamada es: Q" + a);
                Console.WriteLine("---------------------------------------------------------------");
                Console.ReadKey();
            }
            if (minutos >= 4)
            {
                minutos_reales = minutos - 3;
                a = 3 * 7.59;
                b = minutos_reales * 3.03;
                c = a + b;
                Console.Clear();
                Console.WriteLine("---------------- Empresa de Telefonia Telecorp ----------------");
                Console.WriteLine("---------------------------------------------------------------");
                Console.WriteLine("15-75 15 Avenida Ruta 2 Zona 9");
                Console.WriteLine("Guatemala, Guatemala, 01009");
                Console.WriteLine("PBX: 2335-4539");
                Console.WriteLine("---------------------------------------------------------------");
                Console.WriteLine("Factura a nombre de:");
                Console.WriteLine(" ");
                Console.WriteLine("Nombre: " + nombre);
                Console.WriteLine(" ");
                Console.WriteLine("Numero del usuario: 502 " + titular);
                Console.WriteLine(" ");
                Console.WriteLine("Numero de su contacto: " + area + " " + contacto);
                Console.WriteLine(" ");
                Console.WriteLine("El Costo total de su llamada es: Q" + c);
                Console.WriteLine("---------------------------------------------------------------");
                Console.ReadKey();
            }
            else
            {
                Console.WriteLine("Error");
                Console.ReadKey();
            }
        }
        static void nacional()
        {
            int minutos;
            int minutos_reales;
            double a;
            double b;
            double c;
            string nombre;
            string titular;
            string contacto;
            Console.Clear();
            Console.WriteLine("Llamada Nacinal");
            Console.WriteLine(" ");
            Console.WriteLine("Ingrese Su nombre");
            nombre = Console.ReadLine();
            Console.WriteLine(" ");
            Console.WriteLine("Ingrese el su numero telefonico");
            titular = Console.ReadLine();
            Console.WriteLine(" ");
            Console.WriteLine("Ingrese el numero telefonico al que desea llamar");
            contacto = Console.ReadLine();
            Console.WriteLine(" ");
            Console.WriteLine("Ingrese la cantidad de minutos que desea hablar (Con fines de simulación)");
            minutos = int.Parse(Console.ReadLine());
            if (minutos <= 3)
            {
                a = minutos * 1.20;
                Console.Clear();
                Console.WriteLine("---------------- Empresa de Telefonia Telecorp ----------------");
                Console.WriteLine("---------------------------------------------------------------");
                Console.WriteLine("15-75 15 Avenida Ruta 2 Zona 9");
                Console.WriteLine("Guatemala, Guatemala, 01009");
                Console.WriteLine("PBX: 2335-4539");
                Console.WriteLine("---------------------------------------------------------------");
                Console.WriteLine("Factura a nombre de:");
                Console.WriteLine(" ");
                Console.WriteLine("Nombre: " + nombre);
                Console.WriteLine(" ");
                Console.WriteLine("Numero del usuario: 502 " + titular);
                Console.WriteLine(" ");
                Console.WriteLine("Numero de su contacto: 502 " + contacto);
                Console.WriteLine(" ");
                Console.WriteLine("El Costo total de su llamada es: Q" + a);
                Console.WriteLine("---------------------------------------------------------------");
                Console.ReadKey();
            }
            if (minutos >= 4)
            {
                minutos_reales = minutos - 3;
                a = 3 * 1.20;
                b = minutos_reales * 0.48;
                c = a + b;
                Console.Clear();
                Console.WriteLine("---------------- Empresa de Telefonia Telecorp ----------------");
                Console.WriteLine("---------------------------------------------------------------");
                Console.WriteLine("15-75 15 Avenida Ruta 2 Zona 9");
                Console.WriteLine("Guatemala, Guatemala, 01009");
                Console.WriteLine("PBX: 2335-4539");
                Console.WriteLine("---------------------------------------------------------------");
                Console.WriteLine("Factura a nombre de:");
                Console.WriteLine(" ");
                Console.WriteLine("Nombre: " + nombre);
                Console.WriteLine(" ");
                Console.WriteLine("Numero del usuario: 502 " + titular);
                Console.WriteLine(" ");
                Console.WriteLine("Numero de su contacto: 502 " + contacto);
                Console.WriteLine(" ");
                Console.WriteLine("El Costo total de su llamada es: Q" + c);
                Console.WriteLine("---------------------------------------------------------------");
                Console.ReadKey();
            }

        }
        static void local()
        {
            int minutos;
            int minutos_reales;
            double a;
            double b;
            double c;
            string nombre;
            string titular;
            string contacto;
            Console.Clear();
            Console.WriteLine("Llamada Local");
            Console.WriteLine(" ");
            Console.WriteLine("Ingrese Su nombre");
            nombre = Console.ReadLine();
            Console.WriteLine(" ");
            Console.WriteLine("Ingrese el su numero telefonico");
            titular = Console.ReadLine();
            Console.WriteLine(" ");
            Console.WriteLine("Ingrese el numero telefonico al que desea llamar");
            contacto = Console.ReadLine();
            Console.WriteLine(" ");
            Console.WriteLine("Ingrese la cantidad de Llamadas realizadas (Con fines de simulación)");
            minutos = int.Parse(Console.ReadLine());
            if (minutos <= 50)
            {
                Console.Clear();
                Console.WriteLine("---------------- Empresa de Telefonia Telecorp ----------------");
                Console.WriteLine("---------------------------------------------------------------");
                Console.WriteLine("15-75 15 Avenida Ruta 2 Zona 9");
                Console.WriteLine("Guatemala, Guatemala, 01009");
                Console.WriteLine("PBX: 2335-4539");
                Console.WriteLine("---------------------------------------------------------------");
                Console.WriteLine("Factura a nombre de:");
                Console.WriteLine(" ");
                Console.WriteLine("Nombre: " + nombre);
                Console.WriteLine(" ");
                Console.WriteLine("Numero del usuario: 502 " + titular);
                Console.WriteLine(" ");
                Console.WriteLine("Numero de su contacto: 502 " + contacto);
                Console.WriteLine(" ");
                Console.WriteLine("Su total a pagar es Q0.00");
                Console.WriteLine("---------------------------------------------------------------");
            }
            if (minutos > 50)
            {
                minutos_reales = minutos - 50;
                a = minutos_reales * 0.60;
                Console.Clear();
                Console.WriteLine("---------------- Empresa de Telefonia Telecorp ----------------");
                Console.WriteLine("---------------------------------------------------------------");
                Console.WriteLine("15-75 15 Avenida Ruta 2 Zona 9");
                Console.WriteLine("Guatemala, Guatemala, 01009");
                Console.WriteLine("PBX: 2335-4539");
                Console.WriteLine("---------------------------------------------------------------");
                Console.WriteLine("Factura a nombre de:");
                Console.WriteLine(" ");
                Console.WriteLine("Nombre: " + nombre);
                Console.WriteLine(" ");
                Console.WriteLine("Numero del usuario: 502 " + titular);
                Console.WriteLine(" ");
                Console.WriteLine("El Costo total de sus llamadas es: Q" + a);
                Console.WriteLine("---------------------------------------------------------------");
            }

        }

    }
}
