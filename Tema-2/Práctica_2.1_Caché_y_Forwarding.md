<p align="center">
  <img src="https://github.com/user-attachments/assets/92b13dd5-01d7-4f83-8bb6-e218dfb11235" alt="Descripción de la imagen"/>
</p>

# 🖥️ Práctica Caché y Forwarding

---

## 🎯 Objetivo

Instalar y configurar bin9 en primer lugar como servidor caché y por último como forwarding. 

En ambos casos debes:

- Comprobar la sintaxis del archivo de configuración (named-checkconf)
- Visualizar el archivo log y comprueba que responde adecuadamente (/var/log/syslog)

---

### 1. Bind9 como servidor caché 

Instalamos Bind9:

```
sudo apt install bind9 bind9utils bind9-doc
```

Entramos al fichero de configuración:

```
cd /etc/bind
```

```
sudo nano named.conf.options
```


