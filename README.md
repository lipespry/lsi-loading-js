# LSILoading

Ilustração de carregamento animada para páginas HTML - manipulado via JavaScript.

## Sintaxe:
```javascript
LSILoading(seletor)
```
**Cria** os elementos do loading e retorna a instância de `LSILoadingObject`;

#### Parâmetro do construtor:
- `seletor`: *query selector* do elemento onde o loading será renderizado;

#### Métodos (protótipos):
- `LSILoadingObject.prototype.mostra()`
**Exibe** o loading se oculto e retorna a instância;

- `LSILoadingObject.prototype.esconde()`
**Oculta** o loading se exposto e retorna a instância;

- `LSILoadingObject.prototype.toggle()`
**Exibe ou oculta** o loading conforme estado atual e retorna a instância;

## Exemplo de uso padrão:

1) Carregue os arquivos no HTML:

```html
<script src="lsi-loading/script.js"></script>
<link rel="stylesheet" type="text/css" href="lsi-loading/estilo.css">
```

2) Instancie o LSILoading:

```javascript
// <script>
var meuLoading = LSILoading('#alvo');
// </script>
```

3) Adicione a(s) ação(ões) onde quiser:

    - Via método `.addEventListener()`:

    ```javascript
    document.getElementById('botaoMostrar').addEventListener(
        'click',
        function(){
            meuLoading.mostra();
        },
        false
    );
    ```

   - Via propriedade `onclick` no HTML:

    ```html
    <button type="button" onclick="meuLoading.toggle();">Toggle</button>
    ```

   - Via propriedade `onclick` no JavaScript:

    ```javascript
    document.getElementById('botaoEsconder').onclick = function(){
        meuLoading.esconde();
    }
    ```

## Licença: [MIT](LICENSE)

## Autor

Felipe "LipESprY" Moraes
<[felipemdeoliveira@live.com](mailto:felipemdeoliveira@live.com)>
