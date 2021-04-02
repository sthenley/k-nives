<P style="text-align: center;">

# ⚙️ *🇰-nives* 🔪 kubectl swiss army knife

![License](https://shields.io/github/license/sthenley/k-nives)
![Issues](https://shields.io/github/issues/sthenley/k-nives)
![Last commit](https://shields.io/github/last-commit/sthenley/k-nives)
![Bash](https://img.shields.io/badge/linux-bash-blue)
![Version](https://img.shields.io/github/v/k-nives/sthenley/k-nives)
</P>

## About    

🇰-nives are Bash functions to increase your productivity with kubernetes kubectl:   
| <!-- --> | <!-- --> | 
--------------- |  ---------------
✔️ **k-nives** | List 🇰-nives tools
✔️ **kn**      | Shows avaiable or set cluster namespace - A default '--namespace NAMESPACE' for kubectl (context)    
✔️ **kp**      | List cluster pods   
✔️ **kl**      | Shows pod containers log   
FIRST LAUNCH:   | **2021-04-02**    
LAST REVISION:  | **2021-04-02**    
VERSION:        | **1.0**

This project is maintained by [Sthenley Macedo ](https://linkedin.com/in/sthenley "LinkedIN profile") under [GNU GPL v3](/LICENSE "Read LICENSE file") license.     
    
### Features:    
    
Some are native kubectl features - But in a quick/easy mode 😉

* Color output (ccze and kubecolor must be installed)    
* You can still use all kubectl flags
* Always shows the final command - You don't need to 'unlearn' nothing
* Shows kubectl flags hints
* Set current cluster namespace (allways shows current namespace@context)
* 🇰-nives kn can use namespaces aliases
* 🇰-nives kp can use pod name filtering - All ocurrences of a string
* 🇰-nives kl can use pod name filtering - First ocurrence of a string
* 🇰-nives kl 't' flag shows only 'n' last lines of log
* 🇰-nives kl allways show output timestamps
* 🇰-nives kl can allways show all containers logs
* Return error code for 'pod not found' - kubectl don't have it
* Less typing, more productivity
    
## Installation    
    
### Requisites:    
    
1. [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/ "kubectl setup instructions") - Required
2. [awk](http://awk.freeshell.org)) - Required - Also for your CLI life
2. [kubecolor](https://github.com/dty1er/kubecolor "kubecolor tool") - Recommended, for color output
3. [CCZE colorizer](https://github.com/cornet/ccze "CCZE colorizer tool") - Recommended, for color output
4. [curl](https://curl.se "curl tool") - Recommended - Also for your CLI life
> **HINT!**
> InstALL them!    
    
Quickly for recommended:    
```bash
sudo apt-get -y install curl ccze golang $(command -v awk &> /dev/null || echo awk)    
sudo apt-get -y install kubecolor || go install github.com/dty1er/kubecolor/cmd/kubecolor@latest    
```
    

### Linux CLI install or update    
    
```bash
curl -sLJ https://raw.githubusercontent.com/sthenley/k-nives/main/.bash_k-nives -o ~/.bash_k-nives
grep -q '. ~/.bash_k-nives' ~/.bashrc || echo -e '\nif [ -f ~/.bash_k-nives ]; then\n    . ~/.bash_k-nives\nfi' >> ~/.bashrc && . ~/.bash_k-nives
```
    

## Usage    
    
Try `--help` or `-h` flags to instructions at command line    
🇰-nives was made for UTF-8 environments. You`ll need to change some characters at functions source, if you are getting some “strange characters”


### Setup    

You can edit `kn` function to reflect your own namespace aliases    
If you need, edit this variables at top of `.bash_k-nives`:    

Variable  |  Description
----------------------------- |  -----------------------------
`K_NIVES_LIGHT=false`         | Change it to `true` if you have a “light backgrounded” environment. Works only if you have kubecolor
`K_NIVES_DEPLOYMENT=true`     | Enable/Disable app deployment name at 🇰-nives kp output     
`K_NIVES_TAIL=10`             | Number of lines for 🇰-nives kl 't' flag
`K_NIVES_ALL_CONTAINERS=true` | kl with a '--all-containers=true' flag
`K_NIVES_NAMESPACE1_ALIASES`  | Optional - Populate it with a list of aliases for a namespace.    Default: `c|ca|converse` for `caip`
`K_NIVES_NAMESPACE2_ALIASES`  | Optional - Populate it with a list of aliases for a namespace.    Default: `m|mo|mon|monitor` for `monitoring`

### Exit codes    

| <!-- --> | <!-- --> |
:-:  |  ---
0 | Ok (or help flag)
1 | Invalid argument (help ouput)
2 | kubectl not installed
3 | Pod not found
    

## Share 🇰-nives    

+ [Share on LinkedIn](http://www.linkedin.com/shareArticle?mini=true&url=https://github.com/sthenley/k-nives&title=k-nives%20-%20kubectl%20swiss%20army%20knife&summary=&source=)    
+ [Share on WhatsApp](https://web.whatsapp.com/send?text=https://github.com/sthenley/k-nives)
+ [Share on Telegram](https://t.me/share/url?url=https://github.com/sthenley/k-nives)
+ [Share on Twitter](http://twitter.com/intent/tweet?text=https://github.com/sthenley/k-nives&title=k-nives%20-%20kubectl%20swiss%20army%20knife)
   
## To do

* Dinamic aliases and any number of namespaces

## Contributions    
    
Always welcome. Just [open an issue](https://github.com/sthenley/k-nives/issues)
    

## References    
  * <https://kubernetes.io/docs/reference/kubectl/overview>
