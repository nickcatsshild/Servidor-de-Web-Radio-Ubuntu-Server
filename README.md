# Servidor de Web Radio - Ubuntu Server

 ## Tutorial de Instalação do AzuraCast no Ubuntu 22.04

O AzuraCast é um software de gerenciamento de rádio online que facilita a criação, gerenciamento e transmissão de sua própria estação de rádio. Este tutorial irá guiá-lo através do processo de instalação do AzuraCast no Ubuntu 22.04 usando o Docker.

**Pré-requisitos:**

* Um servidor Ubuntu 22.04 com acesso root ou sudo.
* Pelo menos 2GB de RAM.
* 20GB ou mais de espaço em disco.
* Docker instalado.

**Passo 1: Instalar o Docker**

Se você ainda não tem o Docker instalado, siga estas etapas:

1. Atualize a lista de pacotes:

```
sudo apt update
```

2. Instale o Docker:

```
sudo apt install docker.io
```

3. Adicione seu usuário ao grupo `docker` para executar comandos Docker sem `sudo`:

```
sudo usermod -aG docker $USER
```

4. Faça logout e login novamente para que as alterações do grupo entrem em vigor.

**Passo 2: Instalar o AzuraCast**

1. Crie um diretório para armazenar os arquivos do AzuraCast:

```
mkdir -p /var/azuracast
```

2. Navegue até o diretório:

```
cd /var/azuracast
```

3. Baixe o script de instalação do AzuraCast:

```
curl -fsSL https://raw.githubusercontent.com/AzuraCast/AzuraCast/main/docker.sh > docker.sh
```

4. Dê permissão de execução ao script:

```
chmod +x docker.sh
```

5. Execute o script de instalação, respondendo às perguntas na tela:

```
./docker.sh install
```

O script irá instalar o AzuraCast e configurar o Docker para executá-lo automaticamente na inicialização do sistema.

**Passo 3: Acessar o AzuraCast**

1. Abra um navegador da web e navegue até o endereço IP do seu servidor seguido da porta 80:

```
http://<seu_endereço_ip>:80
```

2. Siga as instruções na tela para criar sua conta de administrador e concluir a configuração inicial do AzuraCast.

**Dicas:**

* Você pode encontrar mais informações sobre a instalação e configuração do AzuraCast na documentação oficial: [https://www.azuracast.com/docs/getting-started/installation/](https://www.azuracast.com/docs/getting-started/installation/)
* Se você tiver problemas durante a instalação, consulte o fórum da comunidade AzuraCast: [https://github.com/AzuraCast/AzuraCast/discussions](https://github.com/AzuraCast/AzuraCast/discussions)

**Observações:**

* Este tutorial assume que você está instalando o AzuraCast em um novo servidor Ubuntu 22.04. Se você estiver instalando em um servidor existente, poderá ser necessário fazer algumas modificações nas etapas.
* Certifique-se de ler a documentação oficial do AzuraCast para obter mais informações sobre como usar o software.
