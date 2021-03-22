# bash

Hey :D
This repo is from my collection of useful commandlines, these scripts can be invoked following the cmd below. Have fun.
http://stackoverflow.com/questions/5735666/execute-bash-script-from-url
```
bash <(curl -s https://bash.kenyos.me/dokidokiupdate.txt)
```

http://stackoverflow.com/questions/4642915/passing-parameters-to-bash-when-executing-a-script-fetched-by-curl
```
curl http://foo.com/script.sh | bash -s arg1 arg2
```

Function for zsh/bash config for easily call in the terminal
```
sv() {
    bash <(curl -s https://bash.kenyos.me/$1.txt)
)
```
https://stackoverflow.com/questions/7131670/make-a-bash-alias-that-takes-a-parameter

Then.. hide sensitivy information in your command line by using cat with xargs
cat will take all the information from varsecret.txt and then send to xargs, xargs will store in this variable '%' (it can be anything) and you replace in the right location
```
cat ~/scripts/bash/flyctl/varsecret.txt | xargs -I % flyctl --app % restart

```

https://unix.stackexchange.com/questions/3593/using-xargs-with-input-from-a-file

finally, you can call your code simple as that for each mycode.txt.
```
sv mycode

```
