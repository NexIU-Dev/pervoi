# Plano de implementação — PerVoí

## Briefing e direção atual

- PerVoí: beleza, estética, noiva e spa em São José dos Campos.
- Prioridade definida pelo usuário: **loiros e mega hair de alto padrão**, como na bio atual do Instagram.
- Objetivo: levar visitantes à conversa com a equipe pelo WhatsApp `https://wa.me/5512996118050`.
- O bio.site serve apenas para confirmar destinos de links. A linguagem visual nasce das fotos do Instagram e de uma composição própria.
- Após revisão da primeira versão, o usuário pediu uma linha visual inovadora e diferente de templates comuns. A referência escolhida foi [Hair Styling Studio | Website design](https://www.behance.net/gallery/252269205/Hair-Styling-Studio-Website-design): fotografia dominante na capa, assinatura em serif de grande escala, alternância de áreas creme e chocolate, respiro amplo e imagens de cabelo como eixo da narrativa. A PerVoí usa essa gramática visual com conteúdo, fotografia e composição próprios.
- Entrega estática local. Publicação, agenda online, formulário, preços e analytics fora do escopo. Horários aproximados não serão publicados como oficiais.

## Fontes e imagens

- [Instagram oficial](https://www.instagram.com/pervoibeleza/): bio, avatar e publicações públicas. Para a capa e a fachada, foram obtidos os arquivos maiores servidos nas páginas dos posts. A galeria ainda usa miniaturas de até 640 px. Os arquivos são locais, sem depender de URLs temporárias.
- [Bio.site](https://bio.site/pervoi): somente WhatsApp e Instagram.
- Endereço, telefone e serviços complementares: briefing fornecido pelo usuário.

| Arquivo | Publicação de origem | Uso | Limite |
| --- | --- | --- | --- |
| `logo-instagram.jpg` | [Perfil](https://www.instagram.com/pervoibeleza/) | Favicon | 150 × 150 px. |
| `loiro-portrait-hq.jpg` | [Foto de 10/08/2026](https://www.instagram.com/pervoibeleza/p/Db3pyM6xZnJ/) | Capa fotográfica | 1537 × 1791 px. |
| `mega-portrait.jpg` | [Carrossel de 04/08/2026](https://www.instagram.com/pervoibeleza/p/DbnvVgAkRX-/) | Aba Mega Hair e galeria | 480 × 640 px. |
| `tons-quentes.jpg` | [Foto de 19/08/2026](https://www.instagram.com/pervoibeleza/p/DcPjh2ERVcN/) | Sequência de trabalhos | 640 × 640 px. |
| `loiro-movimento.jpg` | [Foto de 18/09/2026](https://www.instagram.com/pervoibeleza/p/Ddcet04Rbtb/) | Foto em largura total e galeria | 561 × 640 px. |
| `loiro-longo.jpg` | [Publicação oficial](https://www.instagram.com/pervoibeleza/p/DcZabvdq2Cm/) | Aba Loiros e galeria | 600 × 640 px. |
| `fachada-pervoi-hq.jpg` | [Foto oficial](https://www.instagram.com/pervoibeleza/p/B6E9odkDEn2/) | Espaço e endereço | 1241 × 894 px; fotografia antiga. |

Não há foto pública de noiva ou spa adequada na parte acessível do perfil; essas áreas serão textuais. Nada de banco de imagens, simulação de resultado, métricas ou depoimentos inventados.

## Estrutura e experiência

1. **Capa fotográfica:** retrato real do salão com assinatura PerVoí em serif ampla e CTA direto para WhatsApp.
2. **Abertura editorial:** posicionamento breve e imagem de cabelo em largura total.
3. **Especialidades:** seletor acessível entre Loiros e Mega Hair, com imagem, texto e CTA específicos para cada escolha. Sem JavaScript, o painel inicial permanece legível.
4. **Trabalhos reais:** galeria de fotos oficiais com links às publicações. No telefone, desliza com o dedo.
5. **Casa PerVoí:** serviços complementares em índice textual, fachada, endereço e mapa.
6. **Contato final:** WhatsApp, telefone e Instagram.

**Desktop:** capa em largura total com nome sobreposto, seções com muita margem e tipografia serif, fotografia de cabelo em largura total, seletor em duas abas e galeria escalonada.

**Telefone:** capa vertical com título e CTA na base, abas de especialidades e painel de serviço empilhado, galeria rolável por toque, endereço e contato em sequência curta.

## Sistema e stack

- Cores: chocolate `#2B190F`, creme `#F5EFE6`, areia `#E8DED1` e cobre `#A87C5D`; sem copiar o bio.site.
- Tipos: Italiana para assinatura e títulos de grande escala; DM Sans para navegação e informação.
- Astro estático, CSS próprio e pequeno script para a escolha entre as duas especialidades. Sem backend.
- `src/pages/index.astro`: conteúdo, semântica e interação; `src/styles/global.css`: sistema visual e responsividade; `public/images`: imagens oficiais locais.
- Hospedagem não indicada; não definir canonical nem OG image absoluto sem domínio.

## Execução e aceite

1. Atualizar capa, imagens e textos; conferir origem e resolução.
2. Implementar escolha acessível entre Loiros e Mega Hair e links de WhatsApp reais.
3. Revisar semântica, foco visível, teclado, redução de movimento e navegação por âncoras.
4. Rodar `astro check` e `astro build`.
5. Abrir build no navegador em 320, 360, 390, 430 px, tablet e desktop. Confirmar ausência de rolagem lateral, legibilidade da capa, troca de caminhos, rolagem da galeria e carregamento de imagens.

As miniaturas restantes do Instagram não devem ser ampliadas em telas grandes. Os links de WhatsApp identificam o site como origem da conversa. O site só será publicado mediante definição de hospedagem/domínio.
