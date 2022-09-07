

#### conda ####
```brew install miniconda```

as per brew caveats when I installed ("$(basename "${SHELL}")" will resolve to current shel)
```conda init "$(basename "${SHELL}")"```

the above `init` command will make conda as default python for new shell, overwriting other python installations, like `pyenv`
which I dont want to, so based on [this page (jump to the last solution section)](https://www.linuxfixes.com/2022/07/solved-installing-anaconda-with-pyenv.html),
we should deactivate conda base for new shells, so we will have the conda command, but it will not manage the shell, unless we need it
```conda config --set auto_activate_base false```
