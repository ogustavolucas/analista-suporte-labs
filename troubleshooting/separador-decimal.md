# Troubleshooting – Separador Decimal Incorreto

## Contexto
Usuários relataram erro na digitação e interpretação de valores decimais em um campo numérico da aplicação, devido à utilização de separador decimal diferente do padrão esperado.

## Sintomas
- Valores decimais interpretados incorretamente
- Erro ao salvar dados
- Divergência nos valores exibidos

## Causa raiz
Configuração do campo numérico utilizando separador decimal por ponto, enquanto o ambiente exigia outro padrão de separação decimal.

## Solução aplicada
Ajuste da configuração do campo numérico para padronizar o uso correto do separador decimal.

```xml
<?xml version="1.0" encoding="utf-8"?>
<control>
  <properties>
    <subtype>decimal</subtype>
    <style width="200" />
    <numberfield thousandseparator="false" decimalseparator="true" decimaldigits="1" />
  </properties>
</control>
