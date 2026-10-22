# Bloco de Ancoragem com Dente

Aplicativo web para verificação de estabilidade e dimensionamento em concreto simples ou armado de **bloco de ancoragem em L com dente de cisalhamento**, para curvas horizontais com junta elástica em redes de água. Gera a memória de cálculo em Word (.docx, A4).

**Acesse:** https://engrafaeljralves.github.io/Bloco-de-Ancoragem-a-flex-o/

Funciona direto no navegador, no computador ou no celular. Não precisa instalar nada nem criar conta.

## O que o aplicativo verifica

**Estabilidade, nos casos de serviço e de teste**
- Tombamento e deslizamento, com os fatores de segurança mínimos informados.
- Tensões na base e posição da resultante (critério ACI quando há tração na base).
- Empuxos de Rankine: ativo e passivo acompanham o dente até o seu fundo.

**Flexão e cortante nas peças (NBR 6118)**

No painel **Concreto**, escolha o tipo de dimensionamento:

- **Concreto armado:** dimensiona as armaduras N1 a N5 da tabela abaixo.
- **Concreto simples:** verifica as mesmas peças sem armadura (NBR 6118, seção 24, γc = 1,68), com Mrd = fctd·W e Vrd = 2/3·τwRd·bw·h. Os esforços são os mesmos nos dois casos, e a estabilidade não muda.


| Posição | Peça | Esforço principal |
|---|---|---|
| N1 | Degrau, face superior | Peso do tubo, água, solo sobre o degrau e peso próprio |
| N5 | Degrau, face inferior | Reação do solo sob o degrau |
| N3 | Parede de apoio do tubo | Força hidráulica e empuxo ativo |
| N2 | Dente, face do passivo | Empuxo passivo |
| N4 | Dente, face do ativo | Empuxo ativo |

No concreto armado, para cada posição: armadura calculada e mínima, bitola e espaçamento adotados, armadura de distribuição, cortante sem estribos (VRd1) e abertura de fissuras (ELS-W, item 17.3.3) com o momento de serviço, contra o limite wk,lim escolhido (0,3 mm por padrão).

A formulação completa está no próprio aplicativo, na seção **Memória de cálculo**, no fim da página.

## Como usar

1. Preencha os dados da tubulação, cotas, solo, bloco, dente e concreto, e escolha concreto simples ou armado. Os resultados atualizam a cada alteração.
2. No topo, confira a estabilidade (tombamento, deslizamento e tensões na base). No corte A-A, a aba **Geometria e cargas** mostra os esforços de serviço e de teste, e a aba **Armaduras e esforços** mostra a disposição das armaduras e os diagramas de momento fletor e cortante de cada peça. Mais abaixo, o **Quadro de armaduras** traz o resultado das peças e as verificações de flexão e cortante.
3. Clique em **Gerar memorial** para baixar a memória de cálculo em Word.

### Unidades salvas

- Dê um nome à unidade e clique em **Salvar unidade**. Use **Abrir** na lista para retomar, **Salvar como nova** para partir de um bloco parecido e **Nova unidade** para começar outro.
- As unidades ficam salvas **no seu navegador**, neste computador. Elas não são enviadas para nenhum servidor e não aparecem para outras pessoas.
- Use **Exportar unidades (.json)** para guardar uma cópia ou levar as unidades para outro computador, e **Importar unidades** para trazê-las de volta.
- Em janela anônima, ou com os dados do site apagados, as unidades se perdem. Exporte antes.

## Arquivos

- `index.html`: o aplicativo completo, em um único arquivo. Também pode ser baixado e aberto localmente no navegador (precisa de internet para carregar as fontes e a biblioteca que gera o .docx).

## Aviso

Ferramenta de apoio ao projeto. Os resultados devem ser conferidos pelo engenheiro responsável, com parâmetros geotécnicos obtidos em ensaio. A flexão da parede no plano horizontal sob a carga localizada do tubo, a ancoragem e o detalhamento das barras não são verificados.

Versão V1.8 · outubro de 2026 · Eng. Rafael J. R. Alves
