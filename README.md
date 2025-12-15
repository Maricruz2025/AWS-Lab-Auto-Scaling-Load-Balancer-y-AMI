# 🚀 Laboratorio AWS: Auto Scaling + Load Balancer + AMI 

Este proyecto implementa una arquitectura **escalable, altamente disponible y automatizada** en AWS utilizando EC2, AMI personalizada, Launch Template, Auto Scaling Group, Application Load Balancer y monitoreo con CloudWatch.  
Forma parte del programa **AWS re/Start**, demostrando habilidades prácticas en Cloud Computing y DevOps.

---

## 📌 Arquitectura Final

![Arquitectura](Screenshots/Arquitectura.png)

---

## 🛠️ Tecnologías Utilizadas

| Servicio | Función |
|---------|---------|
| 🖥️ **EC2** | Instancias virtuales para la aplicación |
| 📦 **AMI** | Imagen personalizada para escalar instancias |
| 📝 **Launch Template** | Configuración base del Auto Scaling Group |
| 📈 **Auto Scaling Group** | Escalado automático según demanda |
| 🌐 **Application Load Balancer** | Distribución de tráfico entre instancias |
| 📊 **CloudWatch** | Métricas, alarmas y monitoreo |

---

## 🧩 Tareas del Laboratorio

### **1️⃣ Crear instancia base (Web Server)**  
- Instancia EC2 en subred pública  
- Instalación de Apache  
- Verificación desde navegador  

📷 *Puedes agregar aquí una captura de la instancia funcionando.*

---

### **2️⃣ Crear AMI personalizada**  
- Crear imagen desde la instancia base  
- Esperar estado **available**  

📷 *Captura sugerida: AMI creada.*

---

### **3️⃣ Crear Launch Template**  
- Seleccionar AMI personalizada  
- Configurar tipo de instancia, red y seguridad  
- Sin IP pública (subred privada)

📷 *Captura sugerida: Launch Template.*

---

### **4️⃣ Crear Auto Scaling Group (ASG)**  
- Subredes privadas  
- Capacidad: min 2, max 4  
- Política de escalado: CPU > 50%  
- Asociar al Target Group  

📷 *Captura sugerida: ASG con instancias activas.*

---

### **5️⃣ Crear Application Load Balancer (ALB)**  
- Subredes públicas  
- Security Group con HTTP 80  
- Crear Target Group  
- Asociar instancias del ASG  

📷 *Captura sugerida: ALB y Target Group.*

---

### **6️⃣ Probar acceso desde Load Balancer**  
- Abrir DNS del ALB  
- Ver página con InstanceId, zona y CPU  

📷 *Captura sugerida: Página web funcionando.*

---

### **7️⃣ Probar escalado automático**  
- Generar tráfico  
- Ver CPU en CloudWatch  
- ASG lanza nuevas instancias  
- Luego reduce cuando baja la carga  

📷 *Captura sugerida: Instancias escalando.*

---

## 📊 CloudWatch en acción

CloudWatch se activó automáticamente para:

- Métrica: **CPUUtilization**  
- Alarma: CPU > 50%  
- Acción: escalar instancias  

📷 *Captura sugerida: Alarmas en CloudWatch.*

---

## ✅ Conclusiones

✔ AMI personalizada creada  
✔ Auto Scaling Group funcionando  
✔ Load Balancer distribuyendo tráfico  
✔ Escalado automático probado  
✔ CloudWatch monitoreando métricas  
✔ Infraestructura lista para producción  

---

## 🧠 Aprendizajes Clave

- Arquitectura escalable y tolerante a fallos  
- Uso de subredes públicas y privadas  
- Seguridad en AWS  
- Integración de servicios  
- Diagnóstico y solución de problemas  
- Documentación profesional para portafolio  

---

## 📁 Estructura del repositorio



