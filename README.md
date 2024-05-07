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
restart your terminal session
then test: 
`cln set[tab tab]` should offer you `setchannel      setconfig       setleaserates   setpsbtversion` and few others
