# Sistema de Riego Automatizado por Gravedad e Interpolación Espacial
## 1 Contexto del problema
### Contexto social 
El riego por gravedad es uno de los sistemas con menor eficiencia hídrica debido a que gran parte del agua suministrada no es aprovechada de manera efectiva. Las pérdidas ocasionadas por infiltración, evaporación y escurrimiento superficial generan desperdicios superiores al 50 % del caudal total, alcanzando valores de hasta 65 % de pérdida y eficiencias de apenas 35 % a 42 %. Además, la disminución progresiva del caudal a lo largo de los canales evidencia una distribución ineficiente del recurso hídrico, reduciendo considerablemente el volumen de agua que realmente llega a las zonas de riego. Esta situación refleja la problemática existente en los sistemas tradicionales de riego, donde el uso ineficiente del agua representa una limitación importante para el aprovechamiento sostenible del recurso hídrico.

![image alt](https://github.com/LeoNuntonUPCH/PI_Grupo3/blob/bebe215c94144d297e803f2107a4513c4dc07b5a/Proyectos_Ingenieria_1/Proyecto/img/imagenes_unidas-1.png)
---
***Figura 1. Distribución porcentual de pérdidas de agua en el sistema de riego gravitacional.***

## Contexto económico

El riego por gravedad representa un elevado impacto económico debido al gran volumen de agua utilizado en las actividades agrícolas. Estudios comparativos indican que este sistema puede consumir aproximadamente 33 000 m³ de agua por hectárea, generando costos operativos cercanos a 13 372 183 por hectárea, valores considerablemente superiores a otros sistemas de riego tecnificado. Esta situación evidencia que el uso ineficiente del recurso hídrico incrementa significativamente los gastos relacionados con la distribución y aprovechamiento del agua en el sector agrícola.
![image alt](https://github.com/LeoNuntonUPCH/PI_Grupo3/blob/b9468ccdbb9c268f3d6b8da0bb0344cdacb35bcc/Proyectos_Ingenieria_1/Proyecto/img/Screenshot_20260519-000322-display-2.png)
***Figura 2. Costo de aplicar un m³ neto de agua por método de riego.***
## 2 Definición del problema

El sistema de riego por gravedad presenta una baja eficiencia hídrica debido a la falta de control y monitoreo de la humedad del suelo durante el proceso de riego. Esta situación provoca el uso excesivo de agua, distribución no uniforme y pérdidas significativas del recurso hídrico, generando desperdicio y elevados costos operativos en las actividades agrícolas. Además, la ausencia de un control preciso de humedad dificulta el aprovechamiento eficiente del agua y limita la optimización del riego en los cultivos.
## Justificación

La presente investigación surge debido a la baja eficiencia hídrica existente en los sistemas de riego por gravedad, donde gran parte del agua utilizada no es aprovechada de manera eficiente debido a la falta de control y monitoreo de la humedad del suelo. Esta situación genera un uso excesivo del recurso hídrico y dificulta la aplicación adecuada del riego en las zonas agrícolas. Diversos estudios indican que el monitoreo de la humedad del suelo mediante sensores permite conocer el estado hídrico del terreno, facilitando un mejor control del riego y una aplicación más adecuada del agua según las necesidades del suelo. En ese sentido, el desarrollo de sistemas de monitoreo basados en sensores de humedad representa una alternativa importante para optimizar el uso del agua y contribuir a una mejor gestión hídrica en la agricultura.
![image alt](https://github.com/LeoNuntonUPCH/PI_Grupo3/blob/2ef37c7fd21f24d7bd066d48ac9e891b8c79e02c/Proyectos_Ingenieria_1/Proyecto/img/Screenshot_20260519-010247-display-2.png)
***Figura 3. Relación entre el agua disponible para la planta y el potencial hídrico en suelos arenosos, francos y arcillosos.***
# Alineación con los Objetivos de Desarrollo Sostenible (ODS)

| ODS | Meta | Contribución del Proyecto |
| :--- | :--- | :--- |
| **ODS 6: Agua Limpia y Saneamiento** | **6.4** Aumentar considerablemente el uso eficiente de los recursos hídricos. | El proyecto está enfocado en reducir el consumo de agua en la agricultura mediante el monitoreo del suelo y el cálculo de la cantidad exacta de agua que necesita el cultivo. |
| **ODS 9: Industria, Innovación e Infraestructura** | **9.5** Aumentar la investigación científica y mejorar la capacidad tecnológica. | Utiliza sensores de bajo costo para obtener información del suelo y mejorar la eficiencia del riego agrícola mediante tecnología accesible. |
| **ODS 15: Vida de Ecosistemas Terrestres** | **15.3** Luchar contra la desertificación y rehabilitar tierras degradadas. | Ayuda a evitar el exceso de riego, contribuyendo a la conservación del suelo y a la reducción de su degradación. |
---

---
# Objetivos

1. Implementar un sistema inteligente de riego por gravedad basado en sensores de humedad y temperatura del suelo.  

2. Utilizar interpolación espacial para reducir la cantidad de sensores sin perder cobertura de información.  

3. Automatizar el riego según las condiciones del suelo para optimizar el uso del agua.  

4. Diseñar un sistema de bajo consumo energético para zonas agrícolas con acceso limitado a electricidad.

# Diagrama de Ishikawa
![image alt](https://github.com/LeoNuntonUPCH/PI_Grupo3/blob/c00fc5a518111adc6395e819f831b75012a1cb14/Proyectos_Ingenieria_1/Proyecto/img/file_000000000a84720e9d35de65e5012697.png)
# Mapa de cliente 
![image alt](https://github.com/LeoNuntonUPCH/PI_Grupo3/blob/536d94d071e5d6e1ada80b57bc21f2387e6a299f/Proyectos_Ingenieria_1/Proyecto/img/file_00000000df3071fb8d985ba211363eac.png)
## Referencias Bibliográficas (Vancouver)

1. Allen RG, Pereira LS, Raes D, Smith M. Crop evapotranspiration—Guidelines for computing crop water requirements. Rome: FAO; 1998.
2. FAO. The state of the world’s land and water resources for food and agriculture (SOLAW): Managing systems at risk. Rome: FAO; 2011.
3. Jones HG. Irrigation scheduling: Advantages and pitfalls of plant-based methods. J Exp Bot. 2004;55(407):2427‑36.
4. Kim Y, Evans RG, Iversen WM. Remote sensing and control of an irrigation system using a distributed wireless sensor network. IEEE Trans Instrum Meas. 2008;57(7):1379‑87.
5. O’Shaughnessy SA, Evett SR. Canopy temperature‑based system for regulating irrigation. Agric Water Manag. 2010;98(2):347‑56.
6. Zhu X, Li M, Wang X. Smart irrigation system based on IoT and machine learning. Comput Electron Agric. 2019;162:1‑10.
7. World Bank. Water in Agriculture: An Overview. Washington D.C.: World Bank Group; 2023.
8. IPCC. Climate Change and Land: an IPCC special report. Geneva: IPCC; 2019.
9. Burney J, Woltering L, Burke M, Naylor R. Solar‑powered drip irrigation enhances food security in the Sudano‑Sahel. PNAS. 2010;107(5):1848‑53.
10. Huang J, Huang Q, Sippel SJ. The economic impact of smart irrigation technology adoption. Agric Econ. 2022;53(4):567‑82.
11. Perry C. Efficient irrigation; Inefficient communication; Flawed recommendations. Irrig Drain. 2007;56(4):367‑78.
12. Perú. Ley N.° 29338, Ley de Recursos Hídricos. Diario Oficial El Peruano, 31 de marzo de 2009.
13. Hamdy A. Water‑energy nexus in agriculture. Options Méditerranéennes. 2013;(101):101‑15.
14. Goovaerts P. Geostatistics for Natural Resources Evaluation. New York: Oxford University Press; 1997.
15. Gavidia Pucllas L. Sistemas de riego tecnificado en el Perú. RPubs; 2015.
16. Cortés F. Problema de eficiencia de riego en el Perú. Lima: Editorial Técnica; 1991.
17. López Ramírez LA. Evaluación de la eficiencia de aplicación en el cultivo de palto (Persea americana Mill) variedad Hass, bajo riego por gravedad en el centro de investigación y experimentación Cañasbamba – Yungay [Tesis de grado]. Huaraz: Universidad Nacional Santiago Antúnez de Mayolo; 2021.
18. Valdivieso A, Carrasco A. Eficiencia del riego por goteo en el crecimiento y producción orgánica de hortalizas. Pueblo Cont [Internet]. 2017 [citado 6 mayo 2026];28(1):125‑34. Disponible en: http://journal.upao.edu.pe/PuebloContinente/article/view/812
19. EOS Data Analytics. Sensores de humedad del suelo para usos agrícolas: tipos y beneficios [Internet]. California: EOSDA; 2022 [citado 6 mayo 2026]. Disponible en: https://eos.com/es/blog/sensores-de-humedad-del-suelo/
