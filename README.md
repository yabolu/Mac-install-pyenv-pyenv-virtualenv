### Mac 上安装pyenv, pyenv-virtualenv
1. 安装

    ```
    brew update
    brew install pyenv
    brew install pyenv-virtualenv
    ```
    
2. 更改配置文件

    ```
    vi ~/.zshrc
    ###添加
    #pyenv
    export  PYENV_ROOT="$HOME/.pyenv"
    export PATH="$PYENV_ROOT/bin:$PATH"

    if which pyenv > /dev/null;
        then eval "$(pyenv init -)";
    fi
    
    # pyenv-virtualenv
    if which pyenv-virtualenv-init > /dev/null;
      then eval "$(pyenv virtualenv-init -)";
    fi
    
    ###生效
    source ~/.zshrc
    
    ```
    
3. 使用

    ```
    ###当前正在使用的python版本
    pyenv version 
    
    ###pyenv 下所有的python版本
    pyenv versions
    
    ###查看可以安装的python版本
    pyenv install --list
    
    ###安装
    pyenv install 版本号
    
    ###卸载
    pyenv uninstall 版本号
    
    ###创建虚拟环境
    pyenv virtualenv 3.7.0 venv370
    
    ###激活虚拟环境
    pyenv activate venv370
    
    ###退出虚拟环境
    pyenv deactivate
    
    ###删除虚拟环境
    pyenv uninstall venv370
    
    
    ```





