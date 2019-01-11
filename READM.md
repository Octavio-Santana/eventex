# Eventex

Sistema de Eventos encomentado pela Morena.

[![Build Status](https://travis-ci.org/Octavio-Santana/eventex.svg?branch=master)](https://travis-ci.org/Octavio-Santana/eventex)
[![Maintainability](https://api.codeclimate.com/v1/badges/79f898de60d0357b1b1b/maintainability)](https://codeclimate.com/github/Octavio-Santana/eventex/maintainability)
[![Test Coverage](https://api.codeclimate.com/v1/badges/79f898de60d0357b1b1b/test_coverage)](https://codeclimate.com/github/Octavio-Santana/eventex/test_coverage)

## Como desenvolver

1. Clone o repositório
2. Crie um virtualenv com Python 3.6
3. Ative o virtualenv
4. Instale as dependências
5. Configure a instância com o .env
6. Excute os testes.

```console
git clone https://github.com/Octavio-Santana/eventex.git wttd
cd wttd
python -m venv .wttd
source .wttd/bin/activate
pip install -r requirements.txt
cp contrib/env-sample .env
python manage.py test
```

## Como fazer o deploy

1. Crie uma instância no heroku
2. Envie as instâncias para o heroku
3. Defina uma SECRET_KEY segura para o heroku
4. Defina DEBUG=False
5. Configure o serviço de email
6. Envie o código para o heroku

```console
heroku create minhainstancia
heroku config:push
heroku config:set SECRET_KEY=`python contrib/secret_gen.py`
heroku config:set DEBUG=False
#configura o email
git push heroku master --force
```