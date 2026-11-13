<h1 align="center">Lucas Muniz</h1>

<p align="center">
  <strong>Desenvolvedor backend</strong> — PHP · Laravel · Go · PostgreSQL · Docker
</p>

<p align="center">
  Backend-first, TDD e domínio determinístico.<br/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/PHP-8.3-777BB4?style=flat-square&logo=php&logoColor=white" alt="PHP 8.3"/>
  <img src="https://img.shields.io/badge/Laravel-12-FF2D20?style=flat-square&logo=laravel&logoColor=white" alt="Laravel 12"/>
  <img src="https://img.shields.io/badge/PostgreSQL-16-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL 16"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker"/>
  <img src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white" alt="Go"/>
  <img src="https://img.shields.io/badge/Pest-TDD-6C5CE7?style=flat-square" alt="Pest / TDD"/>
  <img src="https://img.shields.io/badge/GitHub%20Actions-CI%2FCD-2088FF?style=flat-square&logo=githubactions&logoColor=white" alt="GitHub Actions"/>
</p>

---

## 🔭 Projeto em destaque

### 📡 server-stream · 🔒 código privado

**Um ingest. Todas as plataformas.** Relay de multistreaming: você publica **um** sinal do OBS
e o servidor espelha para Twitch, YouTube e Kick — sem re-encode, com telas de fallback quando
o sinal cai.

- **Zero re-encode.** Só MediaMTX e `ffmpeg -c copy` repassando byte a byte para cada destino.
Sem GPU, sem custo de CPU por destino — a decisão que organiza o produto inteiro.
- **A live não morre.** Caiu o sinal, o fan-out troca a fonte para um MP4 pré-renderizado
(STARTING / BRB / ENDED) sem derrubar a conexão RTMP com a plataforma.
- **Máquina de estados em Go.** Um orchestrator dirigido pelos eventos `ready`/`notready` do
MediaMTX + polling de 1 s decide o que cada destino recebe.
- **Ingest robusto.** SRT na `8890/udp`, RTMPS como fallback, com enforcement de bitrate e
resolução por plano.
- **Segredo nunca em env var.** Sempre em arquivo montado, desde o dev. A chave de stream nunca
é logada.
- **Tudo em contêiner.** Um único `./x setup` deixa a árvore pronta; o host só precisa de Docker.

<sub>Stack: Laravel 12 · Vue 3 · Go · PostgreSQL 16 · MediaMTX · ffmpeg · Docker · k3s</sub>

---

## 🧭 Como eu trabalho


| Princípio                  | Na prática                                                          |
| -------------------------- | ------------------------------------------------------------------- |
| **Test-first**             | O teste que falha vem antes da implementação. Sem exceção.          |
| **Domínio determinístico** | Regra de negócio não mora no controller nem no prompt.              |
| **Dinheiro é inteiro**     | Centavos em `BIGINT`. Formatação só na borda.                       |
| **Backend antes da tela**  | Domínio, testes e contrato primeiro; apresentação é etapa separada. |
| **Tudo em contêiner**      | O único pré-requisito no host é Docker + `make`.                    |
| **README que não mente**   | Todo número publicado tem um comando que o reproduz.                |


---

## 📫 Contato

<p align="left">
  <a href="https://www.linkedin.com/in/lucasmunizb/">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
  </a>
  <a href="mailto:lucasmunizbraga@gmail.com">
    <img src="https://img.shields.io/badge/E--mail-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="E-mail"/>
  </a>
</p>

