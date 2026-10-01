---
layout: post
title:  "Configurando claves SSH en Github"
date:   2026-09-30 10:55:14 +0200
categories: github
---
Primero, si no la tienen, han de generar la clave ssh empleando ssh-keygen, con ed25519, basado en curvas elipticas, si no tienen ya las claves privada y públicas generadas en el directorio `~/.ssh/` .

```bash
ssh-keygen -t ed25519 -C "[your_mail]"
```
![alt text]({{ "/assets/images/image-1.png" | relative_url }})

```bash
cat ~/.ssh/id_ed25519.pub
```
Ahora, han de poner en su github, en el apartado de claves ssh, por el que pueden acceder pulsando la imagen del perfil de su usuario/ settings o configuración/ ssh o pgp (criptografía de clave pública, que sobretodo se usa para cifrar y descifrar mails, pero en este caso lo podemos configurar en github el PGP [Pretty Good Privacy] como firma, para proporcionar integridad en la autoría de los commits)

![alt text]({{ "/assets/images/image.png" | relative_url }})
```bash
git remote set-url origin git@github.com:[user]/[repo].github.io.git
```