# Eventex

Sistema de eventos encomendado pela Morena.

## Como desenvolver?

1. Clone o respositório
2. Crie um virtualenv
3. Ative o virtualenv
4. Instale as dependências
5. Configure a instância com o .env
6. Execute os testes

```console
git clone git@github.com:vellinha/eventex.git wttd
cd wttd
python -m venv .wttd
call .wttd\scripts\activate.bat
cp contrib/env-sample .env
python manage.py test
```

## Como fazer deploy?

1. Crie uma instancia no heroku
2. Envie as configurações para o heroku
3. Defina uma secret key segura para a instância
4. Defina debug=False
5. Configure o serviço de email
6. Envie o código para o heroku

```console
# steps for UNIX systems. for windows it maybe different
heroku create minhainstancia
heroku config:push
heroku config:set SECRET_KEY=*chave*
heroku config:set DEBUG=False
# configura o email
git push heroku master --force 
```