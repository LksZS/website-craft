# Playbook de engenharia — FlexTech WebCraft

Leia este arquivo quando o projeto exigir back-end, banco de dados, autenticação, pagamentos, SEO, performance, acessibilidade ou tratamento de dados pessoais. Ele complementa as instruções centrais em `../SKILL.md`.

## 8. Engenharia back-end e dados

### 8.1 Só crie backend quando existir necessidade

Um formulário de contato pode exigir apenas endpoint serverless e envio de e-mail. Uma aplicação com login, catálogo privado, pedidos e perfis exige banco, autorização, políticas e observabilidade.

Antes de criar backend, defina:

- Dados que serão armazenados e sua finalidade.
- Entidades, relacionamentos e regras de negócio.
- Quem pode ler, criar, alterar e excluir cada registro.
- Retenção e exclusão de dados.
- Fluxo de autenticação, recuperação de senha e sessões.
- Integrações, webhooks, arquivos e limites de uso.

### 8.2 Banco de dados

- Modele entidades com nomes claros, chaves, índices, constraints e timestamps coerentes.
- Use migrations versionadas e revisáveis; não altere schema de produção manualmente sem controle.
- Use transações em operações que precisam ser atômicas.
- Valide integridade no banco, não apenas na interface.
- Planeje paginação e limites; nunca carregue tabelas inteiras sem necessidade.
- Evite armazenar dados pessoais ou sensíveis sem finalidade e base adequada.
- Crie seed de desenvolvimento com dados claramente fictícios.

### 8.3 API, formulários e validação

- Valide entradas no servidor mesmo quando houver validação no front-end.
- Use schemas de validação compartilháveis quando apropriado.
- Normalize e limite texto, arquivos, listas, paginação e parâmetros.
- Trate erros de forma explícita e sem revelar stack traces ou informações internas.
- Use rate limiting para endpoints públicos sujeitos a abuso.
- Proteja contra spam e automação indevida; captcha só quando necessário e com alternativa acessível.
- Nunca confie em campos enviados pelo cliente para preço, permissão, identidade, status de pagamento ou propriedade do recurso.
- Adote idempotência em operações sensíveis, especialmente pedidos e pagamentos.

### 8.4 Autenticação e autorização

- Diferencie autenticação (quem é o usuário) de autorização (o que ele pode fazer).
- Verifique permissão no servidor para cada recurso e operação.
- Aplique least privilege e papéis explícitos.
- Se usar Supabase, configure Row Level Security em tabelas expostas e teste as policies com usuários de papéis diferentes.
- Não exponha `service_role`, chaves privadas, tokens de administração ou segredos no bundle do navegador.
- Cookies de sessão devem ter atributos seguros apropriados; não armazene tokens sensíveis em `localStorage` sem justificativa e análise de risco.
- Inclua fluxo de recuperação de conta, logout e expiração de sessão quando houver login.

### 8.5 Pagamentos e webhooks

- Não armazene dados de cartão diretamente. Use checkout e componentes/tokenização do provedor adequado.
- Confirme o status do pagamento no servidor e por evento assinado do provedor; não confie na tela de sucesso do navegador.
- Valide assinatura de webhooks, origem, tipo e payload.
- Torne o processamento idempotente e mantenha logs de evento sem registrar segredos/dados sensíveis desnecessários.
- Trate estados pendente, aprovado, recusado, expirado, estornado e reembolsado.
- Nunca invente taxas, disponibilidade de meios de pagamento ou requisitos legais; consulte documentação vigente do provedor.

### 8.6 Upload e armazenamento

- Valide MIME type, extensão, tamanho e permissões no servidor.
- Gere nomes não previsíveis; não confie no nome original.
- Restrinja tipos de arquivo e tamanho máximo.
- Separe arquivos públicos e privados; use URLs assinadas para conteúdo privado.
- Não permita execução de arquivos enviados.

### 8.7 Segredos e ambientes

- Utilize `.env.local` ou secret manager; nunca comite credenciais.
- Inclua `.env.example` com nomes de variáveis e valores ilustrativos, sem segredos.
- Separe desenvolvimento, preview/staging e produção.
- Verifique quais variáveis são públicas e quais são exclusivamente server-side.
- Não publique um deploy com integração crítica simulada ou credenciais de teste sem deixar isso explícito.

## 9. SEO, conteúdo local e presença digital

Para cada página, cuide de:

- Title único, conciso e específico.
- Meta description útil, sem promessas não comprovadas.
- Um H1 principal claro e hierarquia H2/H3 coerente.
- URLs legíveis e estáveis.
- Canonical quando aplicável.
- Open Graph/Twitter metadata e imagem de compartilhamento.
- Sitemap XML e robots.txt coerentes.
- Links internos com âncoras descritivas.
- Imagens otimizadas e textos alternativos.
- Dados estruturados somente quando correspondam ao conteúdo real (por exemplo, Organization, LocalBusiness, Product, Article). Nunca marque avaliações ou dados que não existam.
- Página 404 útil e tratamento de rotas inexistentes.

Para negócios locais, use nome, endereço, telefone, área atendida e horários fornecidos e consistentes. Não invente endereço ou horário. Considere links para rotas, mapa, redes sociais e perfil comercial quando o cliente fornecer os dados.

SEO não é garantia de posição ou tráfego. Não prometa ranking.

## 10. Performance e acessibilidade

### 10.1 Metas de Core Web Vitals

Use como referência de boa experiência, no percentil 75 dos usuários reais:

- **LCP:** até 2,5 s.
- **INP:** até 200 ms.
- **CLS:** até 0,1.

São metas de referência, não uma garantia. Meça com ferramentas de laboratório e, quando disponível, dados de campo.

### 10.2 Performance

- Evite hidratação/client JavaScript sem necessidade.
- Carregue scripts e integrações de terceiros apenas quando necessários.
- Faça code splitting por rota e carregamento sob demanda para recursos pesados.
- Otimize imagens, fontes, vídeos, animações e bibliotecas.
- Não importe uma biblioteca inteira se apenas uma função é necessária.
- Evite layout shift reservando espaço para imagens, embeds, fontes e conteúdo assíncrono.
- Use cache apropriado, headers e estratégias de renderização com cuidado.
- Inspecione bundle e console; não ignore erros ou warnings importantes.

### 10.3 Acessibilidade

Busque WCAG 2.2 nível AA como referência de projeto, conforme aplicável.

- Use HTML semântico e landmarks.
- Garanta operação por teclado, foco visível e ordem de tabulação lógica.
- Associe labels e instruções a todos os campos.
- Informe erros de formulário de forma clara e acessível.
- Mantenha contraste suficiente e não dependa apenas de cor.
- Use nomes acessíveis para botões e ícones.
- Adicione `aria-*` somente quando necessário; não substitua semântica HTML correta por ARIA improvisado.
- Controle foco em dialogs/modais e devolva foco ao elemento que abriu o modal.
- Use heading levels de forma lógica.
- Ofereça legendas/transcrições para mídia relevante quando disponíveis.
- Respeite redução de movimento e ampliação de texto.

## 11. Privacidade e conformidade no Brasil

Quando o projeto coletar ou tratar dados pessoais, considere LGPD desde o desenho:

- Colete somente o necessário para uma finalidade clara.
- Explique de forma compreensível o que é coletado e para quê.
- Defina quem recebe os dados, onde ficam armazenados e por quanto tempo.
- Não adicione pixels, analytics, gravação de sessão ou cookies não essenciais sem avaliar necessidade, transparência e requisitos de consentimento aplicáveis.
- Disponibilize política de privacidade adequada ao projeto e informações de contato do controlador, mediante dados fornecidos pelo cliente.
- Implemente consentimento granular e mecanismo de retirada quando forem necessários.
- Não interprete a lei nem dê parecer jurídico. Sinalize pontos que dependem de orientação jurídica/privacidade do cliente.

Não transforme um aviso de cookies genérico em falsa garantia de conformidade. A adequação legal depende do tratamento real e do contexto.

