![zigi](https://user-images.githubusercontent.com/117615/69496216-051d1580-0ed0-11ea-9ea5-cf0d9153482c.png)
[![anaconda downloads](https://anaconda.org/zdevops/zigi/badges/downloads.svg)](https://anaconda.org/zdevops/zigi)

## Installing zigi

Make sure you have git installed on your Mainframe.
In order to install git, head on over to https://www.rocketsoftware.com/ and create an account.
Then download git, bash, gzip and perl and bring all those files to one directory in USS.

Then head on over to https://gist.github.com/wizardofzos/897b243d4cbe9fbc471ec1396fbbe174 and stick that installer in the
same directory as the things you downloaded from rocket.

Run that script.

You should now have git installed on you Mainframe.

Clone this repository and run the installer via:

    git clone git@github.com:wizardofzos/zigi.git
    cd zigi
    ./zginstall.rex

or

[![anaconda/dl](https://anaconda.org/zdevops/zigi/badges/installer/conda.svg)](https://anaconda.org/zdevops/zigi)


### Make sure you are authorizes to allocate the target datasets


## Contributing to zigi?

Yes please!


# Known Issues (maybe solutions...)

### Git not found (even though you installed it)
Zigi needs to find the git executable in the 'PATH'. To determine the 'PATH' zigi sources /etc/proifile and ˜.profile.
Make sure one of these files contains the correct EXPORT statements.

### Weird Certificate Errors
When faced with a "SSL Certificate problem: unable to get local issuer" this might 'fix' it. Please note that this will
disable encryption for all uses of git and this is strongly discouraged in non-sandbox environments.

    git config --global http.sslVerify false

