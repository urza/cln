# core lightning bits

* These code snippets assume running on ubuntu server native (not docker or umbrell and such).
* CLN has [great documentation](https://docs.corelightning.org/docs/home)

## ✨ create alias "cln" for "lightning-cli" 
* if lightning-cli is in PATH:
  
`echo "alias cln='lightning-cli'" >> ~/.bash_aliases && source ~/.bash_aliases`

* or absolute path:

`echo "alias cln='/path/to/lightning-cli'" >> ~/.bash_aliases && source ~/.bash_aliases`

## ✨ bash auto completion for cln
```
curl https://raw.githubusercontent.com/urza/cln/main/cln.bash-completion > cln.bash-completion
sudo cp cln.bash-completion /etc/bash_completion.d/cln.bash-completion
```
restart your terminal session<br>
then test: <br>
`cln set[tab tab]` <br>
should offer you <br>
`setchannel setconfig setleaserates setpsbtversion`

<img alt="Example of completion with FZF" src="https://github.com/urza/cln/assets/189804/b52c006e-e67b-4c72-9039-3615cd1cfd52" width=200/>

## ✨ ppm to % table
(understand your fees)
`cln setchannel short_chan_id base_fee ppm_fee`

| PPM  | % |
| ------: | ------: |
| 10 ppm  | 0.001%  |
| 100 ppm  | 0.01%  |
| 500 ppm  | 0.05%  |
| 1000 ppm  | 0.1%  |
| 10_000 ppm  | 1%  |

## ✨ amount in sats
Millisatoshis are annoying. Luckily in most places when working with lightning-cli you can provide amount as sats or even btc using "sat" or "btc" suffix. <br/> 
For example:<br/>
`cln invoice 50000sat label_test_77 description_test`


