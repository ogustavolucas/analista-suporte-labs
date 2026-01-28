# Troubleshooting – Falha em API de Desbloqueio de Usuário no AD (Namespace)

## Contexto
Durante a utilização de uma API responsável pelo desbloqueio de usuários no Active Directory (AD), a operação falhava devido a um erro retornado pelo serviço de eventos durante a execução da requisição.

## Sintomas
- Falha ao tentar desbloquear usuário via API
- Erro retornado pelo serviço de eventos
- Requisição não processada corretamente

## Mensagem de erro
Server did not recognize the value of HTTP Header SOAPAction

## Causa raiz
O erro ocorreu devido à configuração incorreta do *namespace* utilizado na chamada da API, o que impedia o reconhecimento correto da ação SOAP pelo serviço.

## Solução aplicada
Foi realizada a correção do namespace utilizado na requisição da API, substituindo o valor configurado anteriormente por um namespace compatível com o serviço esperado.

### Exemplo de ajuste
- Namespace anterior: valor incompatível
- Namespace atualizado: padrão compatível com o serviço SOAP

## Resultado
Após a correção do namespace, a API passou a processar corretamente as requisições, permitindo o desbloqueio dos usuários no Active Directory sem erros.

## Aprendizado
A importância de validar corretamente configurações de namespace e headers em integrações SOAP, especialmente em serviços críticos como autenticação e gerenciamento de usuários.
