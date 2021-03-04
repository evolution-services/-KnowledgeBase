## Jquery - Bootstrap

### Passando dados para modal bootstrap usando jquery

##### Example

```js
$('#my-modal').on('show.bs.modal', function (event) {
  var myVal = $(event.relatedTarget).data('val');
  $(this).find(".modal-body").text(myVal);
});
```


### Local Storage Increment With setTimeout

##### Example

```js
setTimeout(function() {
  atualizaLabel(true);
}, 1000);

function atualizaLabel(initiate) {
  if (initiate !== true) {
  
    var valorAgora = 0;
    valorAgora = ($("#valorParcela").val() != "") ? $("#valorParcela").val() : 0;
    
    // set the item in localStorage
    localStorage.setItem('Nome', "Ederson Jr");
    localStorage.setItem('Valor', parseFloat(valorAgora) + 5.23);


    var nome = localStorage.getItem('Nome');
    var valor = parseFloat(localStorage.getItem('Valor'));

    $('#resultado').text(`${nome} ganhou R$${valor.toFixed(2).replace(".", ",")}`);    
    $("#valorParcela").val(valor);
    
    //localStorage.clear();

  }
  setTimeout(atualizaLabel, 2000);
}
```
