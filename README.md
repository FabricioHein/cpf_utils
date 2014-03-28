# CpfUtils
[![Gem Version](https://badge.fury.io/rb/cpf_utils.png)](http://badge.fury.io/rb/cpf_utils)
[![Build status](https://secure.travis-ci.org/jacksonpires/cpf_utils.png)](https://secure.travis-ci.org/jacksonpires/cpf_utils)
[![Code Climate](https://codeclimate.com/github/jacksonpires/cpf_utils.png)](https://codeclimate.com/github/jacksonpires/cpf_utils)
[![Coverage](https://codeclimate.com/github/jacksonpires/cpf_utils/coverage.png)](https://codeclimate.com/github/jacksonpires/cpf_utils/coverage.png)

CpfUtils é uma suíte de funcionalidades para CPF.
O CpfUtils é capaz de gerar CPF para testes no formado tradicional ou apenas numérico, testa se determinado número de CPF é válido, gera dígitos verificadores para determinado número candidato a CPF, dentre outras coisas.

## Instalação

Adicione essa linha na Gemfile da sua aplicação:

    gem 'cpf_utils'

E então execute:

    $ bundle

Ou instale você mesmo, conforme abaixo:

    $ gem install cpf_utils

## Uso

O CpfUtils é muito fácil de usar, por exempo:

    # Para gerar um número de CPF:
    CpfUtils.cpf => # "45698394823"

    # Para gerar um CPF formatado:
    CpfUtils.cpf_formatted => # "456.983.948-23"

    # Para verificar se um CPF é válido:
    CpfUtils.valid_cpf?("47238051923") => # true
    CpfUtils.valid_cpf?(47238051923) => # true
    CpfUtils.valid_cpf?("472.380.519-23") => # true

    # Outra forma de verificar se um CPF é válido:
    "45698394823".valid_cpf? => # true
    "456.983.948-23".valid_cpf? => # true

    # Para verificar se uma máscara de CPF é válida:
    "456.983.948-23".valid_cpf_mask? => # true
    "456.983..948-23".valid_cpf_mask? => # false

    # Para formatar um número válido de CPF:
    "45698394823".to_cpf_format => # "456.983.948-23"

    # Para gerar um número de CPF a partir de um número candidato  de 9 dígitos:
    "456983948".generate_cpf => # "45698394823"

    # Para gerar um número de CPF formatado a partir de um número candidato de 9 dígitos:
    "456983948".generate_cpf_formatted => # "456.983.948-23"

Também é possível usar métodos em português:

    # Para gerar um número de CPF:
    CpfUtils.cpf => # "45698394823"

    # Para gerar um CPF formatado:
    CpfUtils.cpf_formatado => # "456.983.948-23"

    # Para verificar se um CPF é válido:
    CpfUtils.cpf_valido?("47238051923") => # true
    CpfUtils.cpf_valido?(47238051923) => # true
    CpfUtils.cpf_valido?("472.380.519-23") => # true

    # Outra forma de verificar se um CPF é válido:
    "45698394823".cpf_valido? => # true
    "456.983.948-23".cpf_valido? => # true

    # Para verificar se uma máscara de CPF é válida:
    "456.983.948-23".mascara_de_cpf_valida? => # true
    "456.983..948-23".mascara_de_cpf_valida? => # false

    # Para formatar um número válido de CPF:
    "45698394823".para_formato_cpf => # "456.983.948-23"

    # Para gerar um número de CPF a partir de um número candidato de 9 dígitos:
    "456983948".gerar_cpf => # "45698394823"

    # Para gerar um número de CPF formatado a partir de um número candidato de 9 dígitos:
    "456983948".gerar_cpf_formatado => # "456.983.948-23"

## Recomende

Gostou dessa gem? Recomende-me no [Working With Rails](http://www.workingwithrails.com/people/148426)!

## Contribuindo

1. Faça um Fork
2. Crie um branch para a nova funcionalidade (`git checkout -b minha-nova-funcionalidade`)
3. Faça o commit de suas alterações  (`git commit -am 'Adicionada nova funcionalidade'`)
4. Faça um push da sua nova funconalidade (`git push origin minha-nova-funcionalidade`)
5. Submeta uma nova Pull Request
