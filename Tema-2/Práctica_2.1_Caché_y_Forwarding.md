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

![image](https://github.com/user-attachments/assets/817cbe40-86f7-4878-bc8e-64b3b4208c31)


Entramos al fichero de configuración:

```
cd /etc/bind
```

```
sudo nano named.conf.options
```

![image](https://github.com/user-attachments/assets/7dfbc10f-1106-4943-8831-3ed0f3d276e8)

Añadimos contenido al fichero:

```
acl goodclients {
    192.0.2.0/24;
    localhost;
    localnets;
};
```

```
options {
    directory "/var/cache/bind";

    recursion yes;
    allow-query { goodclients; };
    . . .
```

![image](https://github.com/user-attachments/assets/47396d74-02cf-4937-8b04-e308729d453e)








