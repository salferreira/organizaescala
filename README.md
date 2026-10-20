# OrganizaEscala 📅

Plataforma SaaS web responsiva de gestão e geração inteligente de escalas de trabalho corporativas, de varejo e atendimento, com aderência estrita à legislação trabalhista brasileira (CLT).

---

## 🎯 Objetivo
Automatizar a criação e o balanceamento de escalas de trabalho complexas (5x2, 6x1, 12x36), validando em tempo real:
- **Interjornada de 11h** consecutivas de descanso.
- **DSR de 24h** consecutivas (totalizando 35h de repouso).
- Limite de até 6 dias de trabalho consecutivos.
- Regras de folga aos domingos e feriados.
- Cobertura mínima por função/cargo por turno e **diagnóstico de déficit de pessoal**.

---

## 🚀 Arquitetura & Stack Tecnológica
- **Backend:** PHP 8.2+ / Laravel 11
- **Frontend:** Blade Templates + Tailwind CSS + Alpine.js
- **Banco de Dados:** MySQL 8 (Single-Database Multi-Tenant isolado por `company_id`)
- **Infraestrutura de Produção:** Linux LiteSpeed (cPanel) em `organizaescala.com`
- **Portais:**
  - Painel do Gestor / RH (visão dupla: Colaborador x Dias e Posto/Turno x Dias)
  - Portal do Colaborador (Mobile-first para visualização, solicitação de folgas e trocas)
  - Super Admin (gestão de planos e parametrização de limites de usuários gratuitos)

---

## 📂 Documentação
- [Documento de Requisitos de Produto & Arquitetura (PRD)](docs/PRD_OrganizaEscala.md)
- [Diagnóstico de Infraestrutura](infra_hospedagem_web.pdf)

---

## 💻 Como continuar o desenvolvimento em outro computador (ex: Notebook)

1. Clone o repositório:
   ```bash
   git clone https://github.com/salferreira/organizaescala.git
   cd organizaescala
   ```
2. Para conectar no servidor via SSH no novo computador:
   - Adicione o host no seu `~/.ssh/config`:
     ```text
     Host organiza-server
       HostName ssh.organizaescala.com
       User salomaot
       IdentityFile ~/.ssh/id_ed25519
       Port 22
     ```
   - Certifique-se de que a chave privada correspondente esteja em `~/.ssh/id_ed25519`.
