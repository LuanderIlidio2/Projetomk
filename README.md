##Relatório de atualizações - Alteração do TBS 	
>Este relatório traz informações de tabelas criadas, excluídas e alterações específicas em campos pré-existentes, descrevendo detalhadamente cada uma das alterações.

[Gestão Empresarial | ERP] (http://documentacao.senior.com.br/gestaoempresarialerp/notasdaversao/)

![](http://documentacao.senior.com.br/gestaoempresarialerp/notasdaversao/resources/images/alteracoes-tbs.png)


**F440GNE_SRNF - Suprimentos / Gestão de Recebimento / Notas Fiscais de Entrada / Agrupada**



NOTAS DA VERSÃO


###5.8.8.47###
------------------------------
>**Valor cobrado em nome de terceiros na nota fiscal de entrada**


Adicionamos o campo Valor cobrado em nome de terceiros na tela Valores da Nota Fiscal de Entrada (F440VAL), acessada através do botão Valores da tela Nota Fiscal de Entrada Agrupada. O valor cobrado em nome de terceiros nas notas fiscais de entrada possui caráter informativo e não influencia no valor total da nota fiscal.

-------------------------------------------------------------------------------

>**Depósitos exportados para a loja na nota fiscal de entrada**

Alteramos a tela Nota Fiscal de Entrada Agrupada para que, ao gerar uma nota fiscal de entrada utilizando uma filial do Gestão de Lojas, seja permitido informar na coluna Depós. da guia Produtos, apenas depósitos que são exportados para O Gestão de Lojas.
O ERP considera uma filial do Gestão de Lojas quando:
* possui proprietária do Gestão de Lojas (JLCA ou JLRE);


* o campo Utiliza Módulo Varejo EM da tela Cadastro de Empresa (F070EMP) está parametrizado como Sim; e

* o campo Integração Varejo, da tela Parâmetros das Filiais para Integrações (
F070VAR), está parametrizado como Sim.

-------------------------------------------------------------------------------

>**Bloqueio de ICMS diferido com situação tributária inválida**


Com o objetivo de evitar que o ICMS diferido seja informado com uma situação tributária inválida, alteramos a tela Nota Fiscal de Entrada Agrupada para que os campos Base ICMS Diferido, % ICMS Diferido e Vlr. ICMS Diferido, das guias Produtos e Serviços, sejam habilitados apenas quando a situação tributária do ICMS 

-------------------------------------------------------------------------------

>**Cálculo de Valor Desconto Zona Franca era calculado incorretamente**


Problema: ao definir, manualmente, o campo Valor Desconto Zona Franca para filiais que possuem Benefício fiscal de zona franca ou Área de Livre Comércio, o sistema não descontava o Valor Desconto Zona Franca da Base de Cálculo do ICMS Substituído.
*Correção efetuada: ajustamos o sistema para que o cálculo do Valor Desconto Zona Franca seja realizado corretamente

-------------------------------------------------------------------------------

>**Dispositivo fiscal não era sugerido**


Problema: nas notas fiscais de entrada, não era considerada a sugestão do dispositivo fiscal cadastrado na tela Parâmetros Fiscais de produtos e serviços por filial e estado (F070PSE).


*Correção efetuada:* ajustamos a rotina para que seja considerada a busca do dispositivo fiscal.


