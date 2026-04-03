# 📌 Definición de la Problemática

### 💧 ODS 6: Agua limpia y saneamiento  
#### 🎯 Meta 6.4  
> “Aumentar considerablemente el uso eficiente de los recursos hídricos en todos los sectores y asegurar la sostenibilidad de la extracción y el abastecimiento de agua”

---

✔️ Este proyecto contribuye directamente porque:

- Optimiza el uso del agua en riego agrícola mediante automatización  
- Controla la cantidad exacta de agua (L/día) según las condiciones del suelo  
- Minimiza pérdidas de agua como:
  - evaporación  
  - filtración  
  - escorrentía  

---

⚙️ Además, el sistema:

- Utiliza riego por gravedad sin bombeo, reduciendo el consumo energético  
- Integra sensores que permiten aplicar agua solo cuando es necesario  
- Opera bajo principios de uso eficiente del recurso hídrico  
- Se alinea con normativas de gestión sostenible del agua  

---

## ⚠️ Definición del problema
En muchos sistemas agrícolas, especialmente en zonas rurales, el riego se realiza de manera manual o con métodos tradicionales, lo que genera una **distribución ineficiente del agua**, falta de control sobre variables del suelo y un uso inadecuado de recursos.

El documento describe la necesidad de un sistema que **controle el riego en función de variables como humedad, temperatura, pH y evapotranspiración**, lo cual actualmente no se gestiona adecuadamente en muchos cultivos.

---

## 👨‍🌾 ¿Para quién es un problema?
- Agricultores de pequeña y mediana escala  
- Comunidades rurales  
- Empresas agroindustriales  
- Instituciones agrícolas  

Especialmente aquellos que:
- No cuentan con sistemas automatizados  
- Dependen de riego por gravedad sin control  
- Carecen de monitoreo en tiempo real  

---

## ❗ ¿Por qué es un problema?
Porque genera:

- Uso excesivo o insuficiente de agua  
- Daño a cultivos por riego inadecuado  
- Baja productividad agrícola  
- Pérdida económica  
- Ineficiencia en recursos energéticos  

Además, el riego debe mantenerse en rangos adecuados de presión y controlarse cuidadosamente para evitar daños al suelo y raíces.

---

## ⏱️ ¿Cuándo y cómo es un problema?
Este problema ocurre:

- **Cuando no hay monitoreo en tiempo real**
- **Cuando el riego se basa en estimaciones manuales**
- **En condiciones climáticas variables**
- **En terrenos extensos sin sensores suficientes**

Se manifiesta como:
- Riego desigual en diferentes zonas del cultivo  
- Falta de precisión en la cantidad de agua (L/día) aplicada  

📍 *Imagen sugerida aquí:*  
👉 Comparación entre riego tradicional vs riego automatizado.

---

## 🧬 ¿Qué consecuencias tiene si no se resuelve el problema?
- Degradación del suelo (erosión, salinización)  
- Disminución del rendimiento agrícola  
- Desperdicio de agua (recurso crítico)  
- Incremento de costos operativos  
- Vulnerabilidad frente al cambio climático  
- Pérdida de sostenibilidad agrícola  

---

## 💡 Solución Propuesta
Se propone un **sistema de riego automatizado por gravedad con interpolación espacial**, que:

- Utiliza sensores de:
  - Humedad
  - Temperatura
  - pH
  - Radiación solar  
- Aplica algoritmos para estimar condiciones del suelo en zonas sin sensores  
- Calcula automáticamente la cantidad de agua necesaria  
- Funciona con energía solar y batería  
- Permite almacenamiento y transmisión de datos  

Este sistema permite una **distribución uniforme y eficiente del agua**, minimizando pérdidas como evaporación o escorrentía.

📍 *Imagen sugerida aquí:*  
👉 Diagrama del sistema (sensores + microcontrolador + riego).

---

## ⚙️ Requisitos del Dispositivo
Basado en el documento:

- **Hardware:**
  - Microcontrolador con capacidad de procesamiento  
  - Sensores ambientales (humedad, temperatura, pH, etc.)  
- **Software:**
  - Algoritmo de interpolación espacial  
  - Cálculo de evapotranspiración  
- **Energía:**
  - Batería recargable + panel solar  
- **Sistema hidráulico:**
  - Riego por gravedad sin bombeo  
- **Comunicación:**
  - Transmisión de datos y almacenamiento local  
- **Estructura:**
  - Materiales resistentes (PVC, carcasa sellada)  
- **Normativa:**
  - Ley de Recursos Hídricos  
  - Normas ambientales y eléctricas  

---

## 🎯 Público Objetivo
- Agricultores tecnificados y no tecnificados  
- Cooperativas agrícolas  
- Proyectos de agricultura sostenible  
- Instituciones académicas y de investigación  

**Segmento clave:**  
Pequeños agricultores que buscan mejorar productividad con bajo costo (≤ S/500 según estimación del proyecto)

---

# 📚 Referencias Bibliográficas (APA 7 – solo artículos científicos)

- Allen, R. G., Pereira, L. S., Raes, D., & Smith, M. (1998). *Crop evapotranspiration—Guidelines for computing crop water requirements*. FAO.  
- Jones, H. G. (2004). Irrigation scheduling: Advantages and pitfalls of plant-based methods. *Journal of Experimental Botany*, 55(407), 2427–2436.  
- Kim, Y., Evans, R. G., & Iversen, W. M. (2008). Remote sensing and control of an irrigation system using a distributed wireless sensor network. *IEEE Transactions on Instrumentation and Measurement*, 57(7), 1379–1387.  
- O’Shaughnessy, S. A., & Evett, S. R. (2010). Canopy temperature-based system for regulating irrigation. *Agricultural Water Management*, 98(2), 347–356.  
- Zhu, X., Li, M., & Wang, X. (2019). Smart irrigation system based on IoT and machine learning. *Computers and Electronics in Agriculture*, 162, 1–10.  

---

# 📍 Recomendación sobre imágenes
Coloca imágenes en:

1. **ODS** → contexto global  
2. **Definición del problema** → esquema de riego tradicional  
3. **Cuándo y cómo** → comparación visual  
4. **Solución propuesta** → diagrama del sistema  
5. **Requisitos** → esquema técnico (bloques del sistema)  
