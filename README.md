# WSO2RCE

A [CVE-2022-29464](https://docs.wso2.com/display/Security/Security+Advisory+WSO2-2021-1738) afeta alguns produtos *WSO2* como *WSO2 API Manager* e *WSO2 Open Banking*, permitindo upload arbitrário de arquivos e execução remota de código.

**Produtos afetados:**

 - WSO2 API Manager 2.2.0, up to 4.0.0  
 - WSO2 Identity Server 5.2.0, up to 5.11.0  
 - WSO2 Identity Server Analytics 5.4.0, 5.4.1, 5.5.0, 5.6.0  
 - WSO2 Identity Server as Key Manager 5.3.0, up to 5.11.0  
 - WSO2 Enterprise Integrator 6.2.0, up to 6.6.0  
 - WSO2 Open Banking AM 1.4.0, up to 2.0.0  
 - WSO2 Open Banking KM 1.4.0, up to 2.0.0

# PoC

*Aviso: Apenas para fins educativos.*

## Baixe o exploit
Clone este repositório:


    git clone https://github.com/Pasch0/WSO2RCE.git
    cd WSO2RCE
    pip install rich



## Executando o exploit
Para iniciar o ataque utilize o comando -u para indicar uma única URL como alvo ou -f para um arquivo com múltiplos alvos:

    python run.py -u https://alvo.com/

![python3 run.py -f alvos.txt](imagens/run.png?raw=true "python3 run.py -f alvos.txt")

## Acessando a backdoor
Ao acessar a backdoor pela URL gerada na execução do script é possível interagir com o campo de texto inserindo comandos do sistema e recebendo a resposta na página.

![shell](/imagens/passwd.png?raw=true "Pwned")

## SOLUÇÃO

O WSO2 forneceu mitigações temporárias aos clientes em janeiro de 2022 e forneceu as correções para todas as versões de produtos com suporte listadas na [Matriz de Suporte do WSO2](https://wso2.com/products/support-matrix/) (status "disponível" e "obsoleto") em fevereiro. Se você for um cliente WSO2 com uma Assinatura de Suporte, use as [Atualizações WSO2](https://wso2.com/updates/) para aplicar a correção.

Para mais detalhes acesse: https://docs.wso2.com/display/Security/Security+Advisory+WSO2-2021-1738

