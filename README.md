# ⏰ Relógio Digital

Este é um projeto de estudo que apresenta um site simples para exibir a hora atual com minutos e segundos. 
O projeto foi desenvolvido utilizando **HTML**, **CSS** e **JavaScript**.

## Visão Geral

O site mostra a hora atual em tempo real, com os valores atualizados a cada segundo. 
O código é organizado em três partes principais:

1. **HTML:** Responsável pela estrutura do site.
2. **CSS:** Estilização do layout.
3. **JavaScript:** Manipulação da lógica e atualização dinâmica do relógio.

## Funcionalidades

- Mostra a hora atual em formato digital.
- Atualiza os valores automaticamente a cada segundo.
- Interface simples e responsiva.
  
## 🔗 Demonstração
Acesse o projeto [aqui]([https://lucasferreiraprogramador.github.io/relogio-digital/](https://lucasferreiraprogramador.github.io/Rel-gio-Digital-Interface-em-Tempo-Real-com-JavaScript/).

## 📂 Estrutura do Projeto

### HTML
O arquivo HTML define a estrutura da página, incluindo os elementos do relógio (`<span>` para horas, minutos e segundos):

```html
<div class="clock">
    <span id="hours">00</span>
    <span id="minutes">00</span>
    <span id="seconds">00</span>
</div>
```

### CSS
O CSS foi utilizado para definir as cores, espaçamentos, tipografia e tornar o layout responsivo.

### JavaScript
O JavaScript é responsável por atualizar os valores do relógio em tempo real. 
A função `newTime` utiliza o objeto `Date` para obter as horas, minutos e segundos atuais:

```javascript
function newTime() {
    const date = new Date();

    const hours = date.getHours();
    const minutes = date.getMinutes();
    const seconds = date.getSeconds();

    hoursElement.textContent = fixTime(hours);
    minutesElement.textContent = fixTime(minutes);
    secondsElement.textContent = fixTime(seconds);
}

function fixTime(time) {
    return time < 10 ? '0' + time : time;
}

newTime();
setInterval(newTime, 1000);
```
- **`fixTime`**: Adiciona um zero à esquerda para garantir que os valores tenham sempre dois dígitos.
- **`setInterval`**: Atualiza o relógio a cada segundo.


## 👤 Autor
- [Lucas Ferreira](https://lucas.ferreiradev.com/)
- [GitHub](https://github.com/LucasFerreiraProgramador)
- [LinkedIn](https://www.linkedin.com/in/lucasferreira-dev-front-end/)

## 📄 Licença
Este projeto foi desenvolvido para fins de estudo e prática de desenvolvimento Front-End.
