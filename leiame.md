## create a new repository on the command line

echo "# MoodleAPI" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M master
git remote add origin https://github.com/adilsonfuta/MoodleAPI.git
git push -u origin master


## push an existing repository from the command line

git remote add origin https://github.com/adilsonfuta/MoodleAPI.git
git branch -M master
git push -u origin master


Configure proxy settings for Git
Posted on 18 Mar 19by mike632t
If you are using git from behind a proxy then you will need to tell it what your proxy settings are.

The following commands configure the proxy settings for http and https, if you don’t need to specify a username and password then you can leave them (and the @ sign) out, and just substitute the correct URL for your proxy server.

$ git config --global http.proxy http://username:password@proxy.server:port
$ git config --global https.proxy https://username:password@proxy.server:port
If you need to undo you changes then you can unset the proxy settings using the following commands.

$ git config --global --unset http.proxy
$ git config --global --unset https.proxy