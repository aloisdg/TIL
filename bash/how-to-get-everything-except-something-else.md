## How to get everything except something else

The `extglob` shell option gives you more powerful pattern matching in the command line. Enable the `extglob` option, like this:

    ~/foobar> shopt extglob # display the value of extglob
    extglob         off
    ~/foobar> ls
    abar  afoo  bbar  bfoo
    ~/foobar> ls !(b*)
    -bash: !: event not found
    ~/foobar> shopt -s extglob  # enable extglob
    ~/foobar> ls !(b*)
    abar  afoo
    ~/foobar> ls !(a*)
    bbar  bfoo
    ~/foobar> ls !(*foo)
    abar  bbar

You can later disable extglob with

    shopt -u extglob


[source](http://stackoverflow.com/a/217017/1248177)

[more](http://stackoverflow.com/a/217208/1248177)
