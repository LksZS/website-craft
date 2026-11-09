# Checklist de release — FlexTech WebCraft

## Conteúdo e conversão
- [ ] A primeira dobra explica o que é oferecido, para quem e qual o próximo passo.
- [ ] Textos são específicos, revisados e sem promessas/depoimentos inventados.
- [ ] CTA principal funciona e leva ao destino correto.
- [ ] Telefone, WhatsApp, e-mail, endereço e horários foram confirmados.
- [ ] Formulários explicam o que acontecerá após o envio.

## Visual e responsividade
- [ ] Desktop, tablet e mobile foram revisados.
- [ ] Sem overflow horizontal ou conteúdo cortado.
- [ ] Tipografia, contraste, espaçamento e hierarquia estão consistentes.
- [ ] Imagens carregam, têm proporção definida e texto alternativo adequado.
- [ ] Menu, botões, modais, filtros e interações funcionam por toque e teclado.
- [ ] `prefers-reduced-motion` é respeitado.
- [ ] Efeitos não bloqueiam leitura nem prejudicam performance.

## Funcionalidade e dados
- [ ] Links internos e externos foram verificados.
- [ ] Formulários validam no cliente e servidor (quando aplicável).
- [ ] Estados de loading, sucesso, vazio e erro existem.
- [ ] Login, logout, recuperação e permissões foram testados (se aplicável).
- [ ] Uploads, pagamentos e webhooks foram testados em ambiente seguro (se aplicável).
- [ ] Não há dados ou credenciais secretas expostas.

## SEO e privacidade
- [ ] Titles, descriptions e H1 estão configurados.
- [ ] Metadata social/Open Graph configurada.
- [ ] Sitemap, robots, canonical e dados estruturados revisados quando aplicáveis.
- [ ] Páginas 404 e redirects tratados.
- [ ] Coleta de dados está limitada à finalidade informada.
- [ ] Cookies, pixels e analytics foram avaliados; política/aviso não é genérico.

## Engenharia e release
- [ ] Dependências e licenças foram verificadas.
- [ ] Lint e typecheck executados, se disponíveis.
- [ ] Build de produção concluído.
- [ ] Testes automatizados e smoke tests executados, se disponíveis.
- [ ] Console sem erros críticos.
- [ ] Core Web Vitals/performance revisados quando possível.
- [ ] Variáveis de produção configuradas sem expor segredos.
- [ ] Deploy validado no domínio publicado.
- [ ] README e `.env.example` atualizados.
- [ ] Pendências e limitações comunicadas ao cliente.
