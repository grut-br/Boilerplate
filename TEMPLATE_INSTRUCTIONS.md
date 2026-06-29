# Manual do Agente - Devio Master Boilerplate

Este repositório serve como o template mestre (boilerplate) da agência para a criação de todos os futuros sites institucionais. Abaixo estão listadas as diretrizes arquiteturais, stack tecnológica e regras de desenvolvimento que devem ser estritamente seguidas por qualquer desenvolvedor ou agente de IA.

---

## 🛠 Stack Tecnológica

* **Framework:** Next.js 16 (ou superior) com App Router
* **Biblioteca Base:** React 19
* **Estilização:** Tailwind CSS v4
* **Animações:** Framer Motion
* **Ícones:** Lucide React

---

## 📂 Arquitetura de Pastas (Clean Architecture)

O projeto segue uma estrutura modular e limpa para facilitar a manutenção e escalabilidade:

* `src/app/` - Rotas, layouts globais e páginas (App Router).
* `src/components/layout/` - Componentes estruturais globais que persistem entre rotas (ex: `Header`, `Footer`, `Sidebar`).
* `src/components/ui/` - Componentes de interface reutilizáveis e atômicos (ex: `Button`, `Input`, `Card`).
* `src/components/sections/` - Seções de página completas e auto-contidas (ex: `HeroSection`, `ServicesSection`, `ContactSection`).
* `src/lib/` - Configurações, utilitários, clientes de API e mock de banco de dados.
* `.agents/skills/ui-ux-pro-max/` - Diretório reservado para instruções customizadas e melhores práticas de UI/UX para agentes.

---

## ⚠️ Regras de Ouro e Diretrizes de Desenvolvimento

### 🥇 1. Herança Global de Layout (DRY)
* **Regra:** O `<Header />` e o `<Footer />` são injetados **EXCLUSIVAMENTE** via `src/app/layout.tsx` e **NUNCA** devem ser importados ou renderizados diretamente dentro de arquivos `page.tsx`.
* **Motivo:** Evita duplicação de código, garante que os estados globais do layout se comportem de forma consistente e facilita transições de página limpas.

### 🎨 2. Padrão de Design UI/UX Consistente
* **Regra:** Sempre consulte a pasta `.agents/skills/ui-ux-pro-max/` para aplicar as diretrizes de design de alto padrão.
* **Foco:** Assegurar a implementação correta de *Color Blocking*, micro-interações táteis (efeitos hover, active, feedbacks visuais sutis) e uma tipografia refinada e hierárquica.

### 📊 3. Fontes de Dados Mockadas
* **Regra:** Consuma dados dinâmicos estruturados a partir de `src/lib/mock-data.ts`. Isso permite que o desenvolvimento da UI seja isolado e facilmente integrado com um CMS ou API no futuro.
