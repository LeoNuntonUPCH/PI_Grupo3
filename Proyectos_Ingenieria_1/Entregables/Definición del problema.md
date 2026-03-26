# 🌱 Sistema de Riego Inteligente

---

## 🌍 ODS Relacionados

### 💧 ODS 6: Agua limpia y saneamiento
#### 🎯 Meta 6.4
> “Aumentar el uso eficiente de los recursos hídricos y asegurar la sostenibilidad del agua”

✔️ Este proyecto contribuye directamente porque:

- Reduce el desperdicio de agua mediante riego solo cuando es necesario  
- Evita riegos innecesarios usando predicción de lluvia  
- Optimiza el consumo en pequeños cultivos y hogares  

---

### ♻️ ODS 12: Producción y consumo responsables
#### 🎯 Meta 12.2
> “Lograr la gestión sostenible y el uso eficiente de los recursos naturales”

✔️ Aporta mediante:

- Uso eficiente del agua (recurso natural clave)  
- Decisiones basadas en datos (sensor + clima)  
- Automatización inteligente para evitar desperdicio  

---

## ❗ Problema

El riego de plantas en entornos domésticos y pequeños sistemas agrícolas se realiza generalmente de manera manual o mediante temporizadores fijos, lo cual no considera ni el estado real del suelo ni las condiciones climáticas futuras.

Esto provoca un uso ineficiente del agua, generando tanto exceso como déficit de riego.

Además, los sistemas tradicionales no integran información externa como la probabilidad de lluvia, lo que impide una toma de decisiones optimizada basada en datos reales y predictivos.

---

## 👥 ¿Para quién es un problema?

### 🎯 Afecta directamente a:
- Personas con jardines domésticos  
- Pequeños agricultores  
- Encargados de viveros  
- Instituciones educativas con áreas verdes  

### 🌱 Impacta indirectamente a:
- Entidades ambientales  
- Organismos que promueven el uso sostenible del agua  

---

## 🌐 ¿Por qué es un problema?

El agua es un recurso limitado y su uso ineficiente contribuye a su desperdicio.

En sistemas tradicionales:

- ❌ No se considera la humedad real del suelo  
- ❌ No se toma en cuenta la probabilidad de lluvia  
- ❌ Se generan pérdidas por sobre-riego  
- ❌ Se afecta el desarrollo de las plantas  

📌 Además, la falta de integración entre sensores y datos climáticos limita la automatización inteligente.

---

## ⏱️ ¿Cuándo ocurre?

Este problema aparece cuando:

- Se riega antes de una lluvia  
- El suelo ya tiene suficiente humedad  
- No hay monitoreo en tiempo real  
- No se consideran variables ambientales externas  

➡️ Ocurre en sistemas manuales o con lógica fija.

---

## ⚠️ Consecuencias

### 🌱 Ambientales
- Desperdicio de agua potable  
- Uso ineficiente de recursos  
- Aumento de la huella hídrica  

### 🌿 Agrícolas
- Estrés hídrico  
- Crecimiento deficiente  
- Pérdida de cultivos  

### 💰 Económicas
- Mayor costo de agua  
- Baja eficiencia productiva  

### 🔬 Tecnológicas
- Limitación en sistemas inteligentes  
- Baja adopción de automatización  

---

## 🧪 Parámetros del sistema

- **Humedad del suelo (%)** → Indica necesidad de riego  
- **Probabilidad de lluvia (%)** → Permite anticipación  
- **Condiciones ambientales** (opcional) → Temperatura, humedad  

---

## 💡 Solución Propuesta

Desarrollo de un sistema de riego inteligente automatizado con:

- Sensor de humedad del suelo  
- Conectividad a internet  
- API climática  
- Algoritmo de decisión  

### 🔄 Lógica de funcionamiento

```text
Si humedad < 40% y lluvia < 80% → Regar
Si humedad < 40% y lluvia ≥ 80% → No regar

## ✔️ Resultado

- Ahorro de agua  
- Mayor eficiencia  
- Mejor salud de las plantas  

---

## 🧰 Requisitos del dispositivo

- Sensor de humedad del suelo  
- Microcontrolador (Arduino / ESP32)  
- Módulo WiFi  
- Bomba de agua  
- Fuente de alimentación  
- Interfaz (LED o pantalla)  
- API climática  

---

## 🎯 Público objetivo

- Jardines domésticos  
- Pequeños agricultores  
- Viveros  
- Instituciones educativas  
- Proyectos ambientales  

---

## 📚 Referencias (APA 7)

- Allen, R. G., et al. (1998). *Crop evapotranspiration*. FAO.  
- Jones, H. G. (2004). *Journal of Experimental Botany*.  
- Kim, Y., et al. (2008). *IEEE Transactions*.  
- O’Shaughnessy, S. A., & Evett, S. R. (2010). *Agricultural Water Management*.  
- Zotarelli, L., et al. (2010). *University of Florida IFAS Extension*.  
