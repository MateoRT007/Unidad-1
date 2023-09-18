# Unidad-1
Trabajo
package com.mycompany.tecnicasdeprogramacionylaboratorio;

/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 */

//import java.util.*;
//import java.time.LocalDate;
//import java.time.format.DateTimeFormatter;
//import java.time.temporal.ChronoUnit;
import java.util.ArrayList;
import java.util.List;

public class Main {
    record DatosMunicipios (String codigo, 
                        String nombres,
                        float deforestacion){}
    public static void main(String[] args) {
        List<DatosMunicipios> municipio = new ArrayList<>();
            municipio.add ( new DatosMunicipios ("05604", "Remedios", 243.59f));
            municipio.add ( new DatosMunicipios ("05736", "Segovia", 150.82f));
            municipio.add ( new DatosMunicipios ("05495", "Nechí  ", 50.74f));
            municipio.add ( new DatosMunicipios ("05890", "Yolombó", 14.1f));
            municipio.add ( new DatosMunicipios ("05858", "Vegachí", 13.28f));
            municipio.add ( new DatosMunicipios ("05585", "Puerto Nare", 12.15f));
            municipio.add ( new DatosMunicipios ("05893", "Yondó  ", 11.68f));
            municipio.add ( new DatosMunicipios ("05040", "Anorí  ", 10.36f));
            municipio.add ( new DatosMunicipios ("05579", "Puerto Berrío", 10.34f));
            municipio.add ( new DatosMunicipios ("05031", "Amalfi ", 10.19f));
            municipio.add ( new DatosMunicipios ("05306", "Giraldo", 9.56f));
            municipio.add ( new DatosMunicipios ("05411", "Liborina", 8.83f));
            municipio.add ( new DatosMunicipios ("05044", "Anza   ", 7.75f));
            municipio.add ( new DatosMunicipios ("05628", "Sabanalarga", 7.46f));
            municipio.add ( new DatosMunicipios ("05004", "Abriaquí", 7.05f));
            municipio.add ( new DatosMunicipios ("05837", "Turbo  ", 6.91f));
            municipio.add ( new DatosMunicipios ("05172", "Chigorodó", 6.29f));
            municipio.add ( new DatosMunicipios ("05234", "Dabeiba", 5.71f));
            municipio.add ( new DatosMunicipios ("05138", "Cañasgordas", 4.67f));
            municipio.add ( new DatosMunicipios ("05842", "Uramita", 4.58f));
            
        //Suma y promedio de deforestacion
            System.out.println("Las hectareas deforestadas de los municipios es: ");
            float i=0f, j=0f;
            for ( DatosMunicipios deforestacionmunicipios : municipio ) {
                System.out.println(deforestacionmunicipios.codigo + "\t" + deforestacionmunicipios.nombres +
                " \t " + deforestacionmunicipios.deforestacion + " " +"Hectareas");
                i = i + deforestacionmunicipios.deforestacion;
            }
            j=(i/20);
            System.out.println();
            System.out.println("la cantidad total de hectareas deforestadas es: " + i + "  Hectareas");
            System.out.println();
            System.out.println("El promedio de la deforestacion en los 20 municipios de Antioaquia es: " + j + "  Hectareas") ;
            System.out.println();
        
        //Reforestacion del 25% de cada municipio
            System.out.println("Cada municipio debe realizar una reforestacion de: ");
            System.out.println();
            float porcentaje = 0.0f, k =0.0f;
            for ( DatosMunicipios reforestacion : municipio ) {
                porcentaje = (reforestacion.deforestacion * 25) / 100;
                System.out.println( porcentaje + " Hectareas de bosques para reforestar en " + reforestacion.nombres);
                k = k + reforestacion.deforestacion;
            }
            System.out.println();
            System.out.println("la cantidad de areas reforestadas es " + k + "  Hectareas");
            
        //Dinero para cada municipio
            System.out.println("A cada municipio le toca la cantidad dinero de: ");
            System.out.println();
            float dinero = 10000.0f, dineroPorHecta = 0.0f, total = 0.0f;
            dineroPorHecta = (dinero/i);
            for ( DatosMunicipios incentivos : municipio ) {
                total = dineroPorHecta * incentivos.deforestacion;
                System.out.println( total + "$ millones de incentivo para  " + incentivos.nombres );
                System.out.println();
            }
   }
}
