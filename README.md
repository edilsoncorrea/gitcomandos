# Tutorial com diversas sequências de comandos úteis

## Sincronizar dados de um projeto fork com os dados do projeto original

Tutorial do canal Data School [Syncing Your GitHub Fork](https://www.youtube.com/watch?v=-zvHQXnBO6c)

### Estrutura logo após o Fork
![Diagrama](/github1.png "Diagrama")

### Estrutura após o Upstream
![Diagrama2](/github2.png "Diagrama 2")

Lista os branches atuais
````
git remote -v
````

Traz para o repositório local os branches antigos e novos do repositório original

Adiona a url do repositório original, nesse exemplo: 'https://github.com/MarlinFirmware' ao repositório local do repositório Fork 'https://github.com/edilsoncorrea/Marlin'
````
git remote add upstream https://github.com/MarlinFirmware/Marlin.git
````

Traz para o repositório local os branches do repositório original.
Eles vêem com o prefixo upstream
````
git fetch upstream
````

Certifica que está no branche para o qual se quer fazer o merge
````
git checkout 2.1.x
````

Realiza o merge do branch do repositório original para o repositório local do repositório Fork
````
git merge upstream/2.1.x
````

Sobe as alterações para o repositório Fork no Github
````
git push origin 2.1.x
````
