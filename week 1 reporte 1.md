# 🛡️ Bitácora de Ciberseguridad - Semana 01

## 📋 Información General
- **Fecha:** 06 de Abril al 12 de Abril, 2026
- **Objetivo:** Dominio de la terminal Linux y configuración del entorno de ataque.
- **Horas dedicadas:** 12 horas.

---

## 🛠️ Entorno de Laboratorio
* **Hipervisor:** VirtualBox v7.0
* **S.O. Atacante:** Kali Linux 2024.1
* **Conectividad:** OpenVPN (TryHackMe)

---

## 📚 Aprendizaje Teórico
He visualizado el video de **VulnHunters** sobre Linux. Conceptos clave aprendidos:
- **Gestión de Permisos:** Uso de `chmod` (representación octal 755, 644).
- **Filtros:** Uso de `grep` para buscar cadenas de texto y `awk` para columnas.
- **Redirecciones:** Diferencia entre `>` (sobrescribir) y `>>` (añadir).

---

## 🧪 Laboratorios Prácticos (TryHackMe)
### Sala: [Linux Fundamentals Part 1](https://tryhackme.com/room/linuxfundamentalspart1)
- **Habilidad Ganada:** Navegación por el sistema de archivos (`cd`, `ls`, `pwd`).
- **Comando Favorito:** `find / -name flag.txt 2>/dev/null` 
    - *Nota: Aprendí que `2>/dev/null` sirve para ocultar los errores de "Permiso denegado".*

---

## 🚩 Retos y Soluciones
**Reto:** No lograba conectar la VPN de TryHackMe desde VirtualBox.
**Solución:** Cambié el adaptador de red de la máquina virtual de "NAT" a "Bridged" (Puente) para que tuviera su propia IP en mi red local y reinicié el servicio de OpenVPN.

---

## ✅ Checklist de Progreso
- [x] Instalación de Kali Linux en VirtualBox.
- [x] Conexión exitosa a la VPN de THM.
- [x] Uso fluido de comandos de lectura (`cat`, `less`, `head`, `tail`).
- [x] Documentación subida a GitHub.

---
*Próxima semana: Redes e Intercepción de tráfico (Wireshark).*

***********************

