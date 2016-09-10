# Etiquedas `label` ausentes em formulários (Missing form label)



## Comentários em repositórios de terceiros

### ThoughtWorksInc/transervicos
- https://github.com/ThoughtWorksInc/transervicos/issues/111

> Isto é um problema de **acessibilidade** para leitores de tela, em parte, de usabilidade, porque ter tags label bem referenciadas, ao serem clicadas, clica no respectivo input.
>
> Documentação para referência: https://www.w3.org/TR/html5/forms.html#the-label-element
>
> Eu até dei fork pra alterar isso e enviar PR, mas desisti ao ver que vocês usam  [Ansible](https://www.ansible.com/). Não é FOSS o suficiente pra mim, quando exige cadastro apenas pra fazer download.
>
> De qualquer forma, aqui tem o pedaço de código com sugestão explicita para resolver problema
> ```html
> <div class="panel panel-search">
>         <div class="row">
>           <div class="col-md-12 form-group">
>             <!--
>                 Errado, for aponta para nenhum lugar
>                <label class="control-label" for="search">Nome ou Descrição</label>
>            -->
>            <label class="control-label" for="search-description">Nome ou Descrição</label>
>             <input type="text" name="search" id="search-description" placeholder="Nome ou Descrição" class="form-control">
>           </div>
>           <div class="col-md-6 form-group">
>             <!--  errado <label class="control-label" for="state">Estado</label>-->
>             <label class="control-label" for="state-selector">Estado</label>
>             <select id="state-selector" class="form-control" name="state[state_id]"><option value="">Selecione um estado</option>
>             <option value="1">Acre</option>
>             <option value="27">Tocantins</option></select>
>           </div>
>           <div class="col-md-6 form-group">
>             <!-- errado <label class="control-label" for="city">Cidade</label>-->
>             <label class="control-label" for="city-selector">Cidade</label>
>             <select id="city-selector" disabled="disabled" class="form-control" name="city[city_id]"><option value="">Selecione uma cidade</option>
> </select>
>           </div>
>         </div>
>         <div class="row search-actions">
>           <div class="col-md-offset-4 col-md-8">
>             <button name="button" type="reset" id="reset_button" class="btn font1-2x btn-search">Limpar Campos</button>
>             <input type="submit" name="commit" value="Buscar" class="btn font1-2x btn-search">
>           </div>
>         </div>
>       </div>
> ```