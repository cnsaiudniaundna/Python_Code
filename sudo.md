### In this file we are looking to how use Sudo in IPython 

This is like `root` access in `Terminal`!
There are differnt methods to do that, I will share here, if you found something more please fork it! 👨‍💻👩‍💻

Sources: [Link_1](https://docs.python.org/3.1/library/getpass.html)

#### So lets do it!😎

1️⃣ First method!


```python
# Import and install packages

import getpass
import os
```


```python
# Create a variable with name "password"
sudo_password_1 = getpass.getpass()
# This is work fancy like command line in terminal 
# Why do we need -S ? It enables input from stdin
command_line = "sudo -S apt-get update" 
os.system('echo %s | %s' % (sudo_password_1, command_line))
```

    ········





    256



👆256 is bad sign that it means this code work really great! 🤓

2️⃣ Second method!


```python
# Import packages
import getpass
import os
```


```python
sudo_password_2 = getpass.getpass()
command = "sudo -S apt-get update"
os.popen(command, 'w').write(sudo_password_2+'\n') 
# It will act as popup (vscode), or input box in local webpage
```

👆256 is good sign that it means this code work really great! 🤓

3️⃣ Third Method!

It will work in command line (`terminal`).

> $ sudo jupyter-notebook --allow-root


```python

```
