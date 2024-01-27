https://qiita.com/nanasess/items/de9f5450717cc8ede51a

1/ Install Symfony command line
wget https://get.symfony.com/cli/installer -O - | bash
export PATH=$HOME/.symfony/bin:$PATH

2/ Install Eccube
git clone git@github.com:EC-CUBE/ec-cube.gitgit@github.com:EC-CUBE/ec-cube.git
symfony composer install
symfony console eccube:install -n

3/ Run Eccube
symfony server:start

*** If you use complex MySQL password included special characters, please use URI encode for it. Example user root with password Jsfa6205!@*$

DATABASE_URL=mysql://root:Jsfa6205%21%40%2A%24@localhost:3306/eccube
