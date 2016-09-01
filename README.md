<p align="center"><img src="https://github.com/coder-factory-academy/cf-guidline-css/blob/master/CFA.png"></p>

# Install Rails on Linux (Ubuntu/Mint)
Before you start: Your terminal should run in the login shell. The login shell reads the .profile file in your home directory. Open the terminal preferences Edit>Profile Preferences>Command

Then check **Run command as login shell**.

1. Open the terminal.
2. Enter the code below into your terminal. It will get some required keys.
    ```
    command curl -sSL https://rvm.io/mpapis.asc | gpg --import
    ```
3. Now install RVM (it downloads the stable version of Ruby).
    ```
    \curl -sSL https://get.rvm.io | bash -s stable --ruby
    ```
4. After rvm has installed ruby you need to add the source of the scripts that give you rvm commands in your terminal. Copy and paste the code below into your terminal.
    ```
    echo "source $HOME/.rvm/scripts/rvm" >> ~/.bash_profile
    ```
5. Install Ruby!
    ```
    rvm install 2.3.1
    ```
6. Create an area for RVM to install rails
    ```
    rvm use ruby-2.3.1@rails500 --create
    ```
7. Install Ruby On Rails!
    ```
    gem install rails --version=500 --no-ri --no-rdoc
    ```
8. Tell rvm to use this as your default (important!)
    ```
    rvm use ruby-2.3.1@rails500 --default
    ```
9. Curl &  **apt-get** will get version 6 of NodeJS (it's required for some of the packages Rails uses). It will ask for your password too and enter yes for any package install questions.
    ```
    curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash
    ```
10. Install NodeJS.
    ```
    sudo apt-get install nodejs
    ```
11. Close your terminal, open it again and test that you have everything.
    ```
    ruby -v
    ```
    ```
    rails -v
    ```
    ```
    node -v
    ```
