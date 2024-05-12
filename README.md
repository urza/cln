# core lightning bits

These code snippets assume running on ubuntu server native (not docker or umbrell and such).

## create alias "cln" for "lightning-cli" 
* if lightning-cli is in PATH:
  
`echo "alias cln='lightning-cli'" >> ~/.bash_aliases && source ~/.bash_aliases`

* or absolute path:

`echo "alias cln='/path/to/lightning-cli'" >> ~/.bash_aliases && source ~/.bash_aliases`

## bash auto completion for cln
```
curl https://raw.githubusercontent.com/urza/cln/main/cln.bash-completion > cln.bash-completion
sudo cp cln.bash-completion /etc/bash_completion.d/cln.bash-completion
```
restart your terminal session<br>
then test: <br>
`cln set[tab tab]` <br>
should offer you <br>
`setchannel setconfig setleaserates setpsbtversion`

![Example of completion with FZF](https://github.com/urza/cln/assets/189804/b52c006e-e67b-4c72-9039-3615cd1cfd52)

