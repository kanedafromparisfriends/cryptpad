# CryptPad

Unity is Strength - Collaboration is Key

## hold on, it's still a prototype...

![and_so_it_begins.png](https://github.com/cjdelisle/cryptpad/raw/master/and_so_it_begins.png "We are the 99%")

CryptPad is the **zero knowledge** realtime collaborative editor.
Encryption carried out in your web browser protects the data from the server, the cloud
and the NSA. This project uses the [CKEditor] Visual Editor and the [ChainPad] realtime
engine. The secret key is stored in the URL [fragment identifier] which is never sent to
the server but is available to javascript so by sharing the URL, you give authorization
to others who want to participate.

To install:

    git clone <this repo>
    npm install
    npm install -g bower ## if necessary
    bower install
    ## copy config.js.dist to config.js and modify configuration (use your own mongodb instance)
    node ./server.js


## Security

CryptPad is *private* not *anonymous*. Privacy protects your data, anonymity protects you.
As such, it is possible for a collaborator on the pad to include some silly/ugly/nasty things
in a CryptPad such as an image which reveals your IP address when your browser automatically
loads it or a script which plays Rick Asleys's greatest hits. It is acceptable for anyone
who does not have the key to be able to change anything in the pad or add anything, even the
server.

The server does have a certain power, it can send you evil javascript which does the wrong
thing (leaks the key or the data back to the server or to someone else). This is however an
[active attack] which makes it detectable. The NSA really hates doing these because they might
get caught and laughed at and humiliated in front of the whole world (again). If you're making
the NSA mad enough for them to use an active attack against you, Great Success Highfive, now take
the battery out of your computer before it spawns Agent Smith.

Still there are other low-lives in the world so using CryptPad over HTTPS is probably a good idea.




[ChainPad]: https://github.com/xwiki-contrib/chainpad
[CKEditor]: http://ckeditor.com/
[fragment identifier]: https://en.wikipedia.org/wiki/Fragment_identifier
[active attack]: https://en.wikipedia.org/wiki/Attack_(computing)#Types_of_attacks
