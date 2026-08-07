<h1 align="center">Lucas Muniz</h1>

<p align="center">
  <strong>Desenvolvedor backend</strong> — PHP · Laravel · PostgreSQL · Docker
</p>

<p align="center">
  Backend-first, TDD e domínio determinístico.<br/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/PHP-8.3-777BB4?style=flat-square&logo=php&logoColor=white" alt="PHP 8.3"/>
  <img src="https://img.shields.io/badge/Laravel-12-FF2D20?style=flat-square&logo=laravel&logoColor=white" alt="Laravel 12"/>
  <img src="https://img.shields.io/badge/PostgreSQL-16-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL 16"/>
  <img src="https://img.shields.io/badge/Docker-Swarm-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker Swarm"/>
  <img src="https://img.shields.io/badge/Pest-TDD-6C5CE7?style=flat-square" alt="Pest / TDD"/>
  <img src="https://img.shields.io/badge/GitHub%20Actions-CI%2FCD-2088FF?style=flat-square&logo=githubactions&logoColor=white" alt="GitHub Actions"/>
</p>

---

## 🔭 Projeto em destaque

### [💸 agente-financeiro](https://github.com/lucasmunizb/agente-financeiro) · 🟢 [em produção](https://agentefinanceiro.muniztecnologia.com.br)

**Gestão financeira pessoal por linguagem natural** — no Telegram e na web.
Você registra um gasto conversando (*"paguei 35 conto de uber"*) e consulta suas finanças
por pergunta (*"quanto gastei com comida esse mês?"*).

O diferencial não é o chat: é o que existe **atrás** dele.

- **A IA nunca calcula dinheiro.** Valores, saldos, parcelas e vencimentos saem de um motor
financeiro determinístico (centavos em `BIGINT`, sem float). A IA só interpreta e redige —
e um **guard pós-geração** audita cada número e cada data do texto contra o payload
calculado antes de enviar. Divergiu, regenera; esgotou, responde sem números.
- **Test-first de verdade.** 1.321 testes · 96,7% de cobertura de linhas. O teste que falha
vem antes do código da feature, sempre.
- **CI é portão, não enfeite.** `test` (PHPStan + suíte) → `build + scan` (Trivy, HIGH/CRITICAL
reprovam) → `deploy` (Docker Swarm em fases) → `smoke` (healthcheck público).
Gate vermelho, nada é publicado.
- **Produção sem `.env`.** Docker Swarm + Docker Secrets em `/run/secrets`, atrás de
Cloudflare → Nginx. Runtime FrankenPHP.
- **Segurança levada a sério.** Nenhum id real em URL (todo identificador é criptografado com
a `APP_KEY`), CSP sem `unsafe-inline`, pentest documentado e corrigido com testes de regressão.

<sub>Stack: Laravel 12 · PHP 8.3 · PostgreSQL 16 · Docker Swarm · Pest · Laravel AI SDK · FrankenPHP</sub>

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
  <a href="https://agentefinanceiro.muniztecnologia.com.br">
    <img src="https://img.shields.io/badge/Demo%20no%20ar-2ea44f?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Demo no ar"/>
  </a>
</p>

