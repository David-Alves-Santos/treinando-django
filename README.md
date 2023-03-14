# treinando-django

Introdução ao Django

Necessário ter instalado: Python / Virtualvenv
Verifica a versão:
python  -- version 
virtualenv --version

Ativar a virtualenv:
venv/Scripts/Activate 
Obs: (Prompt pode estar bloqueado, passa para desbloqueio no whatsapp grupo programação).

Instale o Django:
pip install django

Quais são os programas e versões para o projeto?
pip freeze

pip freeze > requirements.txt ( cria arquivo com todos os programas até então instalados, sempre que for feito a instalação de um novo programa é necessário repetir esse processo)

Criando meu primeiro projeto
Vamos iniciar nosso projeto:
django-admin startproject Setup . (uma boa pratica é dar o nome do projeto de Setup .)
nesse momento é criado uma pasta com todas as configurações do projeto.

Control + Shift + P em select interpreter (vemos se estamos usando a versão que está rodando a virtualenv.

Para abrirmos algo na tela: python manage.py runserver (basra clicar no link com o Control pressionado). 

Todos as informações vem por padrão em inglês, para mudar precisamos acessar o arquivo setting.py e alterar o LINGUAGE_CODE e o TIME_ZONE.


Versionando para o Github

Por questão de segurança algumas informações não podem ser enviadas para o Github. Exemplo: SECRET_KEY.
Para colocar o texto em uma variável de ambiente instalamos o dotenv:
pip install python-dotenv
pip freeze > requirements.txt para atualizar a lista de programas no arquivo.

 Criamos um arquivo .env
E dentro dele adicionamos o texto da SECRET_KEY sem "".

Em setting.py fazemos a seguintes alterações:

E nos lugar da variável SECRETY_KEY: 

Criando o git.ignore
Criamos um arquimo .gitignore
Já existe um arquivo pronto no site "gitignore.io"

Subindo para o Github:
git init 
dit add .
git commit -m "nome do projeto" ex: alura space
Na pagina do Github copiar o endereço do "ssh".

git remote "endereço ssh".
git push origin (main ou as branche que preferir)
Nesse momento todo o codigo vai para o git hub.

Criando meu primeiro APP
python manage.py startapp "nome do app" Exemplo: Galeria
Nesse momento uma pasta com o nome dado deve ser adicionado.
Para adicionar o app vamos ao arquivo setting.py e adicionamos em INSTALLED_APPS=[]

Para tonar ele visível entramos na pasta "galeira" no arquivo "views.py"
E adicionamos os seguintes comando: 
Os nome dados são apenas exemplos. Logo devemos adicionar os nomes dos arquivos html que será usado no nosso projeto. 

Isolando Urls
Uma boa pratica seria criar um arquivo urls.py dentro da nossa pasta GALERIA.
Depois vamos a o arquivo urls.py na pasta GALERIA e adicionamos os seguintes comandos:

No SETUP urls.py 
Dessa forma direcionamos a responsabilidade para outro arquivo de dentro de galeria e devemos faze isso com todos os app criados. 
Adicionando HTML no Django

Adicionamos o seguinte comando que aparece na linha 61: 'DIRS' : [os.path.join(BASE_DIR, 'templates')],

Em seguida criamos a pasta "template" e criamos uma arquivo "index.html".
