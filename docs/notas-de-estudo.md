# Estudo Técnico — Projeto Snitap

## Configuração Inicial e Otimização de Performance

- **Cache Busting para Favicon**: Solucionado o problema de persistência de cache do navegador ao mover arquivos de lugar adicionando um parâmetro de versão no link do HTML `<link rel="shortcut icon" href="assets/img/icons/favicon.png?v=2" type="image/png" />`.
- **Prevenção de FOUT (Flash of Unstyled Text)**: Organização da ordem de carregamento no `<head>`, priorizando os `preconnect` e o Google Fonts antes do arquivo CSS local para garantir que as fontes estejam prontas no momento da renderização do texto.

## Arquitetura de Design System (CSS Variables)

- **Escalabilidade Semântica**: Centralização de tokens de cores (ex: `--snitap-sun`, `--snitap-sky-mid`) e tipografia no `:root`.
- **Praticidade Técnica**: Aplicação estratégica de fontes nos seletores base (`html`, `button`, `h1`), reduzindo a necessidade de declarações repetitivas.

## Componentização e Animações de UI

- **Hero Slider**: Efeito de palavras alternadas no `h1` utilizando `overflow: hidden` e animação `translateY` com cálculos de `bounce` manuais para simular movimento orgânico.
- **Animated Gradient Banner**: Técnica de "Zoom e Deslize" utilizando `background-size: 400%` e animação da `background-position` para criar uma transição de cores fluida.

## Layout Avançado e Scroll-Linked Animations

- **Photo Gallery com CSS Grid**: Uso de `grid-template-areas` para criar um mosaico assimétrico, com cada `figure` mapeado para sua respectiva área.
- **Scroll Reveal**: Implementação de animações baseadas no scroll do usuário através de `animation-timeline: view()`, com uso de atributos `data-delay` para escalonar a entrada dos elementos.
- **Footer Interativo**: Links sociais com efeito de preenchimento circular via pseudo-elemento `::before` e navegação com underline animado usando `scaleX`.

> [!NOTE]
> Estas notas são um resumo técnico. O processo detalhado com todos os desafios resolvidos está documentado nos meus arquivos pessoais de estudo.
> [Veja as anotações de estudo deste projeto aqui](https://docs.google.com/document/d/1JAOca15x5IYKGfyDHnehhZrjZ-efLAmC4ljKqlDd1HY/edit?usp=sharing)
