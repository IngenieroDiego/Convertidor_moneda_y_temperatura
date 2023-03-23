import java.util.Scanner;

import java.util.Scanner;

public class Conversor {
    public static void main(String[] args) {
        try (Scanner scanner = new Scanner(System.in)) {
			int opcion = 0;
			
			do {
			    System.out.println("Seleccione una opción:");
			    System.out.println("1. Conversión de moneda");
			    System.out.println("2. Conversión de temperatura");
			    System.out.println("3. Salir");
			    
			    opcion = scanner.nextInt();
			    
			    switch (opcion) {
			        case 1:
			            System.out.println("Ingrese la cantidad de dinero a convertir:");
			            double cantidad = scanner.nextDouble();
			            System.out.println("Ingrese la moneda de origen (USD, EUR, MXN, COP):");
			            String monedaOrigen = scanner.next().toUpperCase();
			            System.out.println("Ingrese la moneda de destino (USD, EUR, MXN, COP):");
			            String monedaDestino = scanner.next().toUpperCase();
			            double resultadoMoneda = convertirMoneda(cantidad, monedaOrigen, monedaDestino);
			            System.out.println(cantidad + " " + monedaOrigen + " equivale a " + resultadoMoneda + " " + monedaDestino);
			            break;
			        case 2:
			            System.out.println("Ingrese la temperatura a convertir:");
			            double temperatura = scanner.nextDouble();
			            System.out.println("Ingrese la unidad de origen (C, F, K):");
			            String unidadOrigen = scanner.next().toUpperCase();
			            System.out.println("Ingrese la unidad de destino (C, F, K):");
			            String unidadDestino = scanner.next().toUpperCase();
			            double resultadoTemperatura = convertirTemperatura(temperatura, unidadOrigen, unidadDestino);
			            System.out.println(temperatura + " " + unidadOrigen + " equivale a " + resultadoTemperatura + " " + unidadDestino);
			            break;
			        case 3:
			            System.out.println("¡Hasta pronto!");
			            break;
			        default:
			            System.out.println("Opción inválida, intente de nuevo.");
			            break;
			    }
			} while (opcion != 3);
		}
    }
    
    public static double convertirMoneda(double cantidad, String monedaOrigen, String monedaDestino) {
        double tasaOrigen = 0;
        double tasaDestino = 0;
        
        switch (monedaOrigen) {
            case "USD":
                tasaOrigen = 1.0;
                break;
            case "EUR":
                tasaOrigen = 1.19;
                break;
            case "MXN":
                tasaOrigen = 0.05;
                break;
            case "COP":
                tasaOrigen = 0.00027;
                break;
            default:
                break;
        }
        
        switch (monedaDestino) {
            case "USD":
                tasaDestino = 1.0;
                break;
            case "EUR":
                tasaDestino = 0.84;
                break;
            case "MXN":
                tasaDestino = 20.06;
                break;
            case "COP":
                tasaDestino = 3675.66;
                break;
            default:
                break;
        }
        
        double resultado = cantidad * tasaDestino / tasaOrigen;
        return resultado;
    }
    
    public static double convertirTemperatura(double temperatura, String unidadOrigen, String unidadDestino) {
        double resultado = 0;
        
        if (unidadOrigen.equals(unidadDestino)) {
            resultado = temperatura;
        } else if (unidadOrigen.equals("C")) {
            if (unidadDestino.equals("F")) {
                resultado = (temperatura * 9 / 5) + 32;
            } else if (unidadDestino.equals("K")) {
                resultado = temperatura + 273.15;
            }
        } else if (unidadOrigen.equals("F")) {
            if (unidadDestino.equals("C")) {
                resultado = (temperatura - 32) * 5 / 9;
            } else if (unidadDestino.equals("K")) {
                resultado = (temperatura + 459.67) * 5 / 9;
            }
        } else if (unidadOrigen.equals("K")) {
            if (unidadDestino.equals("C")) {
                resultado = temperatura - 273.15;
            } else if (unidadDestino.equals("F")) {
                resultado = temperatura * 9 / 5 - 459.67;
            }
        }
        
        return resultado;
    }
}
