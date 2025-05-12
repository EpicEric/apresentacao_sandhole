---
title: Sandhole
sub_title: Uma jornada de self-host em Rust
author: Eric Pires
theme:
  name: catppuccin-macchiato
---

println!("Hello, world!");
===

<!-- column_layout: [2, 1] -->

<!-- column: 0 -->

- Eric **"Epic Eric"** Pires 
- Engenheiro de software @ **Artemis Technologies**
- Anteriormente @ **NIC.br**
- Entusiasta de open-source e Rust

<!-- column: 1 -->

![image](eric.jpg)

<!-- end_slide -->

Self-hosting
===

<!-- column_layout: [1, 2, 1] -->

<!-- column: 0 -->

![image](rpi3.jpg)

<!-- column: 1 -->

<!-- incremental_lists: true -->

- Independência virtual.
- Privacidade e controle.
- Reciclagem de hardware.
- Aprendizado sobre tecnologias.
- É divertido!
- <3 open-source.

<!-- end_slide -->

Desafios
===

Network Address Translation...

<!-- pause -->

E port forwarding...

<!-- pause -->

E IPs dinâmicos...

<!-- incremental_lists: true -->

- VPN
  - Software específico
- VPS com IP público
  - Limitado aos recursos da máquina
- Proxy reverso
  - Segurança

<!-- end_slide -->

E se eu somar tudo? Existe uma solução...?

<!-- pause -->

Sim. Sim, há.

<!-- pause -->

<!-- jump_to_middle -->

SSH
===

<!-- end_slide -->

![image](logo_sandhole.png)

Um reverse proxy baseado em SSH.
- Sem mais problemas de NAT!
- HTTPS automático para serviços expostos

```bash
ssh -R meusite.com.br:80:localhost:3000 sandhole.com.br
```

<!-- end_slide -->

E mais...!
===

- Domínios personalizados
- Load balancing
- Suporte a portas TCP, incluindo SSH
- Autenticação via chaves SSH
- Forwarding local - quase uma VPN
- UI de administração no terminal (via SSH, claro)

<!-- end_slide -->

<!-- jump_to_middle -->

![image](example_flow.png)

<!-- alignment: center -->

https://sandhole.com.br

<!-- end_slide -->

Sandhole
===

Escrito em Rust
<!-- pause -->
... por um principiante em Rust
<!-- pause -->
... sem experiência em redes ou proxies.

![image](does_not_compile.png)

<!-- end_slide -->

A linguagem certa?
===

<!-- incremental_lists: true -->

<!-- column_layout: [1, 1] -->

<!-- column: 0 -->

- Rewrite it in Rust!
- Baixo nível (HTTP, TCP, TLS, SSH...)
- async via tokio
- Ecossistema de bibliotecas

<!-- column: 1 -->

- Tipagem e erros de compilação
- Testes unitários+integração
- CI/CD, cross-compilation com Docker
- Refatoração sem medo

<!-- reset_layout -->

<!-- pause -->

<!-- new_lines: 2 -->

<!-- alignment: center -->

Aprendizagem => Síntese

<!-- end_slide -->

<!-- jump_to_middle -->

Demonstração
===

```fish +exec +acquire_terminal
~/tmp/demo/CraneGame_linux_x86_64
```

<!-- end_slide -->

Obrigado!
===

<!-- column_layout: [2, 1] -->

<!-- column: 0 -->

- https://github.com/EpicEric/sandhole
- E-mail: eric@eric.dev.br
- Mastodon: @EpicEric@mastodon.xyz
- Discord: @epiceric
- Telegram: @ericpires9

<!-- column: 1 -->

![image](epic_eric.png)
