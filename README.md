# currency1-converter.js
var conversionRate = 10.50;

document.addEventListener('DOMContentLoaded', function() {
    var prices = document.getElementsByClassName('amount');
    for (var i = 0; i < prices.length; i++) {
        var usdAmount = parseFloat(prices[i].innerText);
        if (!isNaN(usdAmount)) {
            var madAmount = usdAmount * conversionRate;
            prices[i].innerText = madAmount.toFixed(2);
        }
    }

    var currencySymbols = document.getElementsByClassName('price');
    for (var i = 0; i < currencySymbols.length; i++) {
        currencySymbols[i].innerHTML = currencySymbols[i].innerHTML.replace('$', 'DH ');
    }
});
