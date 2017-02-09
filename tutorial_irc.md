#Tutorial IRC
O Weechat é um cliente IRC em CLI, que aceita diversos plugins e tem uma ampla comunidade.

Bem, vamos parar de enrolação e vamos direto ao ponto.

Instale o Tor, siga as instruções do site oficial de acordo com a sua distribuição:

https://www.torproject.org/download/download-unix.html.en

Ou em distribuições RHEL/Fedora:
```
sudo dnf install tor
```

Depois de instalado é necessário configurar o Tor:
```
# vim /etc/tor/torrc
```

Descomente a linha 44 para conseguir verificar se houve algum erro ao se conectar e salve.
```
# systemctl restart tor 
# cat /var/log/tor/notices.log
```

Caso tenha sucesso, basta iniciar o weechat, para isto, basta digitar no terminal o comando:
```
$ weechat
```
Depois de iniciado, o weechat irá aparecer. Em seguida, vamos adicionar o proxy do tor.
```
> /proxy add tor socks5 127.0.0.1 9050
```

OBS: Executar este comando no weechat. Onde estiver o ">", significa que é para executar no weechat.

Agora, o proxy do tor está adicionado ao teu weechat. Agora, vamos adicionar o servidor do Telecomix.
```
> /server add telecomix bffahylnohsp7o3b.onion
```
Adicionar o nick.
```
> /set irc.server.telecomix.nicks "Teu_Nick"
```
Desativar SSL 
```
> /set irc.server.telecomix.ssl off
> /set irc.server.telecomix.ssl_verify off
```
Adicionar o proxy tor ao servidor.
```
> /set irc.server.telecomix.proxy tor
```
Autojoin ao canal do Telecomix Brasil
```
> /set irc.server.telecomix.autojoin #TelecomixBrasil
```
Pronto, agora, é só conectar ao servidor do Telecomix.
```
> /connect telecomix
```
Agora, você está pronto para interagir com todos do canal. E seja bem vindo ao Telecomix Brasil. :)

Qualquer dúvida ou erro, por favor, comunicar, estarei tentando resolver o mais rápido possivel.

