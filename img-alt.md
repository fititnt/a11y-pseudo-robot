# Atributo `alt` em imagem `img` inexistente, errado ou excessivamente descritivo

## Comentários em repositórios de terceiros

### ThoughtWorksInc/transervicos

- [https://github.com/ThoughtWorksInc/transervicos/issues/110](https://github.com/ThoughtWorksInc/transervicos/issues/110)

> Tanto usuários de leitores de tela, como mecanismos de busca, ao acessar o principal link do site perdem muito tempo lendo uma string que não faz sentido. `Transervicos logo 220d3f4cbb475253462b66ccdd8493c6ba4848ceda22c1a71faefbbd3229c502`. Isso é um problema de **acessibilidade**.
>
> ```html
> <h1 class="text-center">
>   <img src="http://transervicos.herokuapp.com/assets/transervicos-logo-220d3f4cbb475253462b66ccdd8493c6ba4848ceda22c1a71faefbbd3229c502.svg" alt="Transervicos logo 220d3f4cbb475253462b66ccdd8493c6ba4848ceda22c1a71faefbbd3229c502">
> </h1>
> ```
> ---
>
> O ideal é remover a string "220d3f4cbb475253462b66ccdd8493c6ba4848ceda22c1a71faefbbd3229c502". Eu pessoalmente deixaria **Transerviços**, nem mesmo deixaria **Transervicos logo** porque faz parte da estrutura de documento da página