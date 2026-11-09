# Índice de referências — FlexTech WebCraft

Este arquivo reúne galerias, bibliotecas, repositórios e documentação que a skill deve consultar conforme a necessidade. **Não instale tudo.** Escolha recursos adequados ao projeto, confirme as versões e leia os termos atuais de cada licença.

## 1. Inspiração e pesquisa de web design

| Fonte | Melhor uso | URL |
|---|---|---|
| Awwwards | Sites premiados, experiências interativas, motion e direção de arte ousada | https://www.awwwards.com/ |
| SiteInspire | Galeria curada de sites reais; composição, tipografia e estilos | https://www.siteinspire.com/ |
| Land-book | Landing pages e sites comerciais completos | https://land-book.com/ |
| Lapa Ninja | Landing pages por setor, estrutura, seções e padrões de conversão | https://www.lapa.ninja/ |
| One Page Love | Sites one-page, portfolios e organização de seções | https://onepagelove.com/ |
| Recent Design | Websites contemporâneos, motion e direção visual experimental | https://recent.design/ |
| Mobbin | Padrões de produto, apps, telas e jornadas reais | https://mobbin.com/ |
| Refero | Referências de UI e padrões de produtos digitais | https://refero.design/ |
| SaaSFrame | Sites SaaS, páginas de produto e padrões de marketing | https://www.saasframe.io/ |
| Ecomm.design | Experiências e padrões de e-commerce | https://ecomm.design/ |
| Typewolf | Tipografia em uso, combinações de fontes e referências editoriais | https://www.typewolf.com/ |
| Google Fonts | Fontes e famílias tipográficas; conferir licença e performance | https://fonts.google.com/ |
| Coolors | Exploração inicial de paletas; validar contraste e coerência | https://coolors.co/ |

**Método:** use uma galeria para entender o mercado, outra para estudar composição e uma referência de UX quando existir fluxo transacional. Registre o princípio aprendido. Não copie a página.

## 2. Bibliotecas de UI e componentes

| Recurso | Uso principal | Código / docs |
|---|---|---|
| shadcn/ui | Componentes acessíveis, customizáveis e copiados para o projeto | https://github.com/shadcn-ui/ui · https://ui.shadcn.com/docs |
| Magic UI | Componentes animados, seções e efeitos para React/Tailwind | https://github.com/magicuidesign/magicui · https://magicui.design/ |
| React Bits | Componentes interativos, efeitos, texto, backgrounds e microinterações | https://github.com/DavidHDev/react-bits · https://reactbits.dev/ |
| Aceternity UI | Componentes de marketing e efeitos animados | https://ui.aceternity.com/ |
| 21st.dev | Registry e descoberta de componentes da comunidade | https://21st.dev/ |
| Radix UI | Primitivos de interface acessíveis e sem estilo opinativo | https://www.radix-ui.com/ |
| React Aria | Primitivos e hooks com foco em acessibilidade | https://react-spectrum.adobe.com/react-aria/ |
| Lucide | Ícones consistentes e open source | https://lucide.dev/ |
| Tremor | Componentes de dashboard, gráficos e analytics | https://www.tremor.so/ |

**Cuidados:** shadcn/ui, Magic UI e outros registries podem inserir código-fonte no repositório. Revise o componente, dependências, licença e acessibilidade. Magic UI tem repositório MIT; React Bits declara MIT + Commons Clause: leia os termos antes de usar ou redistribuir em produtos comerciais. Em Aceternity, 21st.dev e componentes comunitários, confira a licença específica e os termos atuais de cada item.

## 3. Motion, animação e experiências imersivas

| Recurso | Uso principal | Código / docs |
|---|---|---|
| Motion for React | Microinterações, transições, layout, gestos e scroll em React | https://motion.dev/docs/react · https://github.com/motiondivision/motion |
| GSAP | Timelines, sequências, ScrollTrigger, SVG e animação avançada | https://gsap.com/docs/ · https://github.com/greensock/GSAP |
| Lenis | Smooth scroll e sincronização com animações/cenas | https://lenis.dev/ · https://github.com/darkroomengineering/lenis |
| React Three Fiber | Integração de Three.js com React | https://docs.pmnd.rs/react-three-fiber/getting-started/introduction |
| Three.js | 3D, WebGL e visualização interativa | https://threejs.org/docs/ · https://github.com/mrdoob/three.js |
| Rive | Ilustrações interativas, estados e motion vetorial | https://rive.app/use-cases/websites · https://github.com/rive-app |
| Lottie | Reprodução de animações vetoriais exportadas | https://airbnb.io/lottie/ · https://github.com/airbnb/lottie-web |
| Theatre.js | Ferramentas de animação e direção de cenas 3D/DOM | https://www.theatrejs.com/ · https://github.com/theatre-js/theatre |

**Escolha recomendada:** CSS para detalhes; Motion para UI React; GSAP para sequências complexas; Rive/Lottie para assets animados; Three.js/R3F quando o 3D fizer parte do valor da experiência. Evite combinar vários motores para resolver o mesmo problema.

## 4. Frameworks e fundamentos de front-end

| Recurso | Uso principal | URL |
|---|---|---|
| Next.js | React full-stack, App Router, rendering e endpoints | https://nextjs.org/docs · https://github.com/vercel/next.js |
| Astro | Sites orientados a conteúdo, marketing, blogs e páginas rápidas | https://docs.astro.build/ · https://github.com/withastro/astro |
| React | Componentes e UI | https://react.dev/ |
| TypeScript | Tipagem estática | https://www.typescriptlang.org/docs/ |
| Tailwind CSS | Sistema de utilitários e responsividade | https://tailwindcss.com/docs |
| Vite | Ferramentas de desenvolvimento e build | https://vite.dev/guide/ |
| web.dev | Performance, acessibilidade e boas práticas web | https://web.dev/ |

## 5. Back-end, banco de dados e serviços

| Recurso | Uso principal | URL |
|---|---|---|
| Supabase | Postgres, Auth, Storage, Realtime e Edge Functions | https://supabase.com/docs · https://github.com/supabase/supabase |
| PostgreSQL | Banco relacional | https://www.postgresql.org/docs/ |
| Drizzle ORM | ORM TypeScript leve e SQL-like; schema e migrations | https://orm.drizzle.team/docs · https://github.com/drizzle-team/drizzle-orm |
| Prisma ORM | ORM tipado e migrations; confira a versão estável e suporte atual | https://www.prisma.io/docs/orm · https://github.com/prisma/prisma |
| Zod | Validação e inferência de tipos TypeScript | https://zod.dev/ |
| Better Auth | Autenticação para aplicações TypeScript | https://www.better-auth.com/docs · https://github.com/better-auth/better-auth |
| Payload CMS | CMS/headless e aplicações com conteúdo | https://payloadcms.com/docs · https://github.com/payloadcms/payload |
| Resend | E-mail transacional | https://resend.com/docs |
| UploadThing | Fluxos de upload para aplicações | https://docs.uploadthing.com/ |
| Vercel AI SDK | Recursos de IA em aplicações, quando solicitados | https://ai-sdk.dev/docs · https://github.com/vercel/ai |

**Alternativa de arquitetura:** para sites pequenos, não implemente um backend inteiro apenas para receber uma mensagem. Para aplicações, não use um formulário estático como substituto de uma operação real.

## 6. Testes, qualidade e segurança

| Recurso | Uso principal | URL |
|---|---|---|
| Playwright | Testes end-to-end em Chromium, Firefox e WebKit | https://playwright.dev/docs/ · https://github.com/microsoft/playwright |
| axe-core | Verificações automatizadas de acessibilidade | https://github.com/dequelabs/axe-core |
| Lighthouse | Auditoria de performance, acessibilidade, SEO e boas práticas | https://developer.chrome.com/docs/lighthouse/overview/ |
| Core Web Vitals | Métricas e orientação de experiência real | https://developers.google.com/search/docs/appearance/core-web-vitals |
| WCAG 2.2 | Critérios de acessibilidade | https://www.w3.org/TR/WCAG22/ |
| OWASP Top 10:2025 | Riscos comuns de segurança em aplicações web | https://owasp.org/Top10/2025/ |
| OWASP ASVS | Requisitos verificáveis para segurança de aplicações | https://asvs.owasp.org/ |

## 7. SEO, dados estruturados e presença local

| Recurso | Uso principal | URL |
|---|---|---|
| Google Search Central | SEO técnico e requisitos de busca | https://developers.google.com/search/docs |
| Next.js Metadata | Metadata, Open Graph, robots, sitemap e ícones | https://nextjs.org/docs/app/getting-started/metadata-and-og-images |
| Schema.org | Vocabulário de dados estruturados | https://schema.org/ |
| Google Business Profile | Presença local do negócio (gerido pelo cliente) | https://www.google.com/business/ |

## 8. Privacidade e Brasil

- LGPD — texto atualizado: https://www2.camara.leg.br/legin/fed/lei/2018/lei-13709-14-agosto-2018-787077-normaatualizada-pl.html
- Portal Gov.br sobre LGPD: https://www.gov.br/mcti/pt-br/acesso-a-informacao/lei-geral-de-protecao-de-dados-pessoais-lgpd
- ANPD: https://www.gov.br/anpd/pt-br

A skill deve tratar privacidade como requisito de produto, não como um banner decorativo. Questões de base legal, controlador/operador e obrigações específicas podem exigir análise jurídica do cliente.

## 9. Repositórios de partida e estudo

Use como referências de arquitetura, padrões de implementação ou componentes pontuais. Não os clone integralmente sem avaliar necessidade:

- **shadcn/ui:** https://github.com/shadcn-ui/ui
- **Magic UI:** https://github.com/magicuidesign/magicui
- **React Bits:** https://github.com/DavidHDev/react-bits
- **Next.js:** https://github.com/vercel/next.js
- **Astro:** https://github.com/withastro/astro
- **Supabase:** https://github.com/supabase/supabase
- **Drizzle ORM:** https://github.com/drizzle-team/drizzle-orm
- **Prisma:** https://github.com/prisma/prisma
- **GSAP:** https://github.com/greensock/GSAP
- **Lenis:** https://github.com/darkroomengineering/lenis
- **Three.js:** https://github.com/mrdoob/three.js
- **React Three Fiber:** https://github.com/pmndrs/react-three-fiber
- **Playwright:** https://github.com/microsoft/playwright
- **Next.js SaaS Starter:** https://github.com/nextjs/saas-starter — estudar arquitetura com autenticação, Postgres, billing e dashboard; não assumir que todos os recursos fazem sentido para todo cliente.

## 10. Protocolo para manter este índice atualizado

Antes de adotar uma ferramenta:

1. Abra a documentação oficial e o repositório original.
2. Confira release estável, data de manutenção, compatibilidade com framework/runtime e requisitos de instalação.
3. Leia licença e termos de uso comercial, incluindo licenças de assets e exemplos.
4. Leia issues/avisos relevantes e verifique se o projeto está ativo.
5. Compare o custo total: bundle, manutenção, serviços externos, limites de plano e risco de lock-in.
6. Registre no projeto a ferramenta escolhida e por que ela foi necessária.

Última curadoria inicial: 9 de novembro de 2026. Links, versões, preços, políticas e licenças podem mudar; sempre revalidar antes de uso.
