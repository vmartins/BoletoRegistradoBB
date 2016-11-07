# BoletoRegistradoBB
Biblioteca PHP para gerar boleto registrado do Banco do Brasil

## Exemplo
```
<?php
include 'BoletoRegistradoBB.php';

$boleto = new BoletoRegistradoBB();
$boleto->setIdConv('987654')
       ->setRefTran($boleto->gerarRefTran(1, 1234567)) //12345670000000001
       ->setValor('15099') //com centavos
       ->setDtVenc('11032017')
       ->setIndicadorPessoa('1') //1=PF e 2=PJ
       ->setCpfCnpj('12345678900')
       ->setNome('Fulano da Silva')
       ->setEndereco('Rua dos Bobos, número 0')
       ->setCidade('Rio de Janeiro')
       ->setUf('RJ')
       ->setCep('20300400')
       ->gerar();
```
