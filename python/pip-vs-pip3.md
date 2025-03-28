# The Curious Case of pip vs pip3

When running
```
source .venv/bin/activate
```

Your shell’s PATH is updated so that:

- python points to .venv/bin/python (in your case, Python 3.12.3),

- pip points to .venv/bin/pip, which is tied to that same Python version.

So, within the virtual environment, *pip and pip3 are effectively the same* __but they look like different files at first sight__! 
Confusing the audience!!

You can verify this by running:

```
which pip
which pip3
```

You should see:

```
> which pip
/home/w1ldrabb1t/code/openai-whisper/.venv/bin/pip

 ~/code/openai-whisper                                                                                                      openai-whisper py | 11:58:21 
> which pip3
/home/w1ldrabb1t/code/openai-whisper/.venv/bin/pip3
```

They are different files, but in practice __they are symlinks or scripts that invoke the same underlying pip module__, tied to the same Python interpreter inside your virtual environment.

You can also check this by running:
```
pip --version
pip3 --version
```

You should see something like:
```
> pip --version        
pip 24.0 from /home/w1ldrabb1t/code/openai-whisper/.venv/lib/python3.12/site-packages/pip (python 3.12)

 ~/code/openai-whisper                                                                                                      openai-whisper py | 11:59:41 
> pip3 --version
pip 24.0 from /home/w1ldrabb1t/code/openai-whisper/.venv/lib/python3.12/site-packages/pip (python 3.12)
```
# Why is there 2 different pip versions?
It's all about compatibility and clarity across systems that may have multiple Python versions installed.

You might have:

Python 2.x -> python, pip

Python 3.x -> python3, pip3

So *pip3 is there to make it explicit you're using pip for Python 3, not 2.*
